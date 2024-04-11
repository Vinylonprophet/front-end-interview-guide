# RxJS面试题

## 目录

| No. | Questions |
|---- | ---------|
|1 | [RxJS有哪些方式导入方式？](#RxJS有哪些方式导入方式？) |
| 2 | [Tree-shaking是什么？](#Tree-shaking是什么？) |
| 3 | [通过Script语句导入依赖的优缺点是什么？](#通过Script语句导入依赖的优缺点是什么？) |
| 4 | [Observable和Observer是什么？Observable遵循了哪些设计模式？](#Observable和Observer是什么？Observable遵循了哪些设计模式？) |
| 5 | [Observable使用的两种形式？](#Observable使用的两种形式？) |
| 6 | [创建同步数据流的操作符有哪些？](#创建同步数据流的操作符有哪些？) |
| 7 | |
| 8 | |
|  | |
|  | |
|  | |
|  | |
|  | |



## 题目

1. ### RxJS有哪些方式导入方式？

   - **Require 方法**：你可以使用 `require()` 方法来导入 RxJS。

     ```javascript
     const Rx = require('rxjs');
     ```

   - **Import方法：**你可以使用`import()`方法来导入RxJS。

     ```javascript
     import { Observable } from 'rxjs/Observable';
     ```

   我们更应该使用`import`语句导入RxJS，因为**Tree-shaking**对`import`语句产生作用。

   **注意：**上面的话虽如此，但是RxJS**大部分功能**围绕Observable类创建，函数大多在RxJS内部都已经被这个类引用了，所以Tree-shaking也不会完全按你需要的生效。

   **[⬆ Back to Top](#目录)**

   

2. ### Tree-shaking是什么？

   Tree-shaking 是一种优化技术，用于删除 JavaScript 代码中未使用的部分，以减少最终打包后的文件大小。它的原理主要基于两个关键概念：静态分析和模块依赖关系。

   - `import`只能出现在代码的第一层，不能出现在if分支中，被导入的模块以字符串常量出现，所以import完全可以满足静态分析的需要。
   - `require`可以出现在if分支中，参数也可以是动态产生的字符串，所以只有在动态执行时才知道require函数如何执行，Tree-shaking爱莫能助。

   Tree-shaking 的工作流程大致如下：

   - 构建工具通过静态分析源代码，找出被引用的模块和变量。
   - 识别出哪些模块和变量没有被引用。
   - 删除未被引用的模块和变量。
   - 最终生成一个优化过的、仅包含被使用部分的代码包。

   **[⬆ Back to Top](#目录)**

   

3. ### 通过Script语句导入依赖的优缺点是什么？

   - 优点：
     1. 如果在其他网站也访问过该CDN(Content Delivery Network)，那么可以直接从浏览器的缓存中获取，省去下载时间。
   - 缺点：
     1. 要下载就要全部下载。

   **[⬆ Back to Top](#目录)**

   

4. ### Observable和Observer是什么？Observable遵循了哪些设计模式？

   Observable是可被观察的对象，即可观察对象。RxJS中的数据流全是Observable。

   Observer是观察者。

   subscribe是连接两者的桥梁。

   **设计模式：**

   1. 观察者模式
   2. 迭代器模式（可说可不说，因为subscribe之后自然能接收到消息的推送，根本不用关注消息是如何被吐出来的）

   **[⬆ Back to Top](#目录)**

   

5. ### Observable使用的两种形式？

   - 创建Observer对象：

     ```typescript
     import { Observable } from 'rxjs';
     
     const observerVL = {
       next: (item: any) => console.log(item),
       complete: () => console.log('complete'),
       error: (err: any) => console.log('Error: ', err),
     };
     
     const onSubscribe = (observer: any) => {
       observer.next(1), observer.next(2), observer.next(3), observer.complete();
     };
     
     const source$ = new Observable(onSubscribe);
     
     source$.subscribe(observerVL);
     ```

   - 简单形式：

     ```typescript
     import { Observable } from 'rxjs';
     
     const onSubscribe = (observer) => {
       observer.next(1);
       observer.next(2);
       observer.next(3);
       observer.complete();
     };
     
     const source$ = new Observable(onSubscribe);
     
     source$.subscribe(
       (item) => console.log(item), // next 函数
       () => console.log('complete'), // complete 函数
       (err) => console.log('Error: ', err) // error 函数
     );
     ```

   **[⬆ Back to Top](#目录)**

   

6. ### 创建同步数据流的操作符有哪些？

   - `of()`: 将一系列的值同步转换为Observable序列。

     ```typescript
     import { of } from 'rxjs';
     
     // 创建一个发出三个值的 Observable
     const source$ = of(1, 2, 3);
     // 订阅这个 Observable
     source$.subscribe({
       next: value => console.log(value), // 输出：1 2 3
       complete: () => console.log('Complete') // 输出：Complete
     });
     ```

   - `from()`: 将数组、类数组对象、Promise、迭代器或类似Observable的对象转换为Observable。如果输入是数组，则会同步发出数组中的每个元素。

     ```typescript
     import { from } from 'rxjs';
     
     // 创建一个发出数组中所有元素的 Observable
     const source$ = from([1, 2, 3]);
     // 订阅这个 Observable
     source$.subscribe({
       next: value => console.log(value), // 输出：1 2 3
       complete: () => console.log('Complete') // 输出：Complete
     });
     ```

   - `range()`: 同步发出一个范围内的数字序列。

     ```typescript
     import { range } from 'rxjs';
     
     // 创建一个发出从 1 到 5 的数字序列的 Observable
     const source$ = range(1, 5);
     // 订阅这个 Observable
     source$.subscribe({
       next: value => console.log(value), // 输出：1 2 3 4 5
       complete: () => console.log('Complete') // 输出：Complete
     });
     ```

   - `generate()`: 使用同步循环生成Observable序列，它接受一个初始状态，一个条件函数，一个迭代函数和一个结果选择器函数。

     ```typescript
     import { generate } from 'rxjs';
     
     // 创建一个发出从 1 到 5 的数字序列的 Observable
     const source$ = generate(
       1, // 初始状态
       x => x <= 5, // 条件函数
       x => x + 1, // 迭代函数
       x => x // 结果选择器函数
     );
     // 订阅这个 Observable
     source$.subscribe({
       next: value => console.log(value), // 输出：1 2 3 4 5
       complete: () => console.log('Complete') // 输出：Complete
     });
     ```

   - `throwError()`: 同步发出错误通知。

     ```typescript
     import { throwError } from 'rxjs';
     
     // 创建一个发出错误通知的 Observable
     const source$ = throwError(new Error('Something went wrong'));
     // 订阅这个 Observable
     source$.subscribe({
       error: err => console.error(err) // 输出：Error: Something went wrong
     });
     ```

   **[⬆ Back to Top](#目录)**

   

7. ### complete和unsubscribe对repeat()操作符而言区别是什么？

   `complete` 通知是 Observable 完成的信号，而 `repeat()` 操作符会忽略完成信号并重新启动 Observable。`unsubscribe` 是手动取消订阅 Observable 的行为，而 `repeat()` 不会影响取消订阅行为。

   **[⬆ Back to Top](#目录)**

   

8. ### 创建异步数据流的操作符有哪些？

   - `interval()`: 创建一个Observable，该Observable按照指定的时间间隔周期性发出一个递增的整数。
   - `timer()`: 创建一个Observable，该Observable在一个指定的延迟之后发出它的第一个值，然后可选地按照指定的时间间隔周期性发出递增的整数。
   - `fromEvent()`: 创建一个Observable，该Observable将指定DOM事件转换为Observable流。
   - `fromEventPattern()`: 创建一个Observable，该Observable对于那些不是标准DOM事件的事件，如Node.js的EventEmitter事件或者RxJS的Subject，可以把它们转换为Observable流。
   - `ajax()`: 创建一个Observable以发出AJAX请求的结果，适用于处理HTTP请求。
   - `fromPromise()`: 创建一个Observable，它会将Promise转换为Observable。当Promise被解析时，发出Promise的解析结果。
   - `bindCallback()`: 将回调API转换为返回Observable的函数。
   - `bindNodeCallback()`: 专门用于将Node.js风格的回调API转换为返回Observable的函数。

   **[⬆ Back to Top](#目录)**

   

9. ### timer(1000, 1000)的写法相当于什么？

   相当于interval(1000)。

   **[⬆ Back to Top](#目录)**

   

10. 
