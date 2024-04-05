# Promise

## 手撕Promise

**思考问题&&解决方案：**

1. Promise有几种状态？
2. 如何修改resolve和reject的this指向？
3. 如何处理Promise的异常？
4. 如何处理Promise中异步代码执行问题？
5. 如何实现Promise链式调用？

```javascript
class MyPromise {
  static PENDING = '待定';
  static FULFILLED = '成功';
  static REJECTED = '失败';

  constructor(func) {
    // 当前状态
    this.status = MyPromise.PENDING;
    // 结果
    this.result = null;
    // this本来指向window即undefined，所以使用bind来手动绑定this
    this.resolveCallback = [];
    this.rejectCallback = [];

    try {
      func(this.resolve.bind(this), this.reject.bind(this))
    } catch (error) {
      this.reject(error)
    }
  }
  resolve(result) {
    if (this.status === MyPromise.PENDING) {
      this.status = MyPromise.FULFILLED;
      this.result = result;

      this.resolveCallback.forEach(callback => {
        callback(result);
      })
    }
  }
  reject(result) {
    if (this.status === MyPromise.PENDING) {
      this.status = MyPromise.REJECTED;
      this.result = result;

      this.rejectCallback.forEach(callback => {
        callback(result);
      })
    }
  }
  then(onFULFILLED, onREJECTED) {
    // then的链式调用
    return new MyPromise((resolve, reject) => {
      // 当promise中代码是异步时，会导致执行then时，状态仍然是pending，最终无法执行onFulfilled
      // 解决方案：把回调函数暂存起来，待执行resolve和reject时统一调用
      if (this.status === MyPromise.PENDING) {
        this.resolveCallback.forEach(() => {
          let x = onFULFILLED(this.result);
          this.resolvePromise(x, resolve, reject);
        })
        this.resolveCallback.push(onFULFILLED);
        this.rejectCallback.push(onREJECTED);
      }

      onFULFILLED = typeof onFULFILLED === 'function' ? onFULFILLED : () => { };
      if (this.status === MyPromise.FULFILLED) {
        setTimeout(() => {
          let x = onFULFILLED(this.result);
          this.resolvePromise(x, resolve, reject);
        });
      }

      onREJECTED = typeof onREJECTED === 'function' ? onREJECTED : () => { };
      if (this.status === MyPromise.REJECTED) {
        setTimeout(() => {
          onREJECTED(this.result);
        });
      }
    })
  }

  resolvePromise(x, resolve, reject) {
    if (x instanceof MyPromise) {
      x.then(y => {
        this.resolvePromise(y, resolve, reject);
      }, result => {
        reject(resolve);
      })
    } else {
      resolve(x);
    }
  }
}
```

