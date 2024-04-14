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
| 7 | [complete和unsubscribe对repeat()操作符而言区别是什么？](#complete和unsubscribe对repeat()操作符而言区别是什么？) |
| 8 | [创建异步数据流的操作符有哪些？](#创建异步数据流的操作符有哪些？) |
| 9 | [timer(1000, 1000)的写法相当于什么？](#timer(1000, 1000)的写法相当于什么？) |
| 10 | [defer操作符的作用是什么？](#defer操作符的作用是什么？) |
| 11 | [合并操作符有哪些？](#合并操作符有哪些？) |
| 12 | [concat()要注意什么？](#concat()要注意什么？) |
| 13 | [merge()为什么有时会出现和concat()相同的效果？](#merge()为什么有时会出现和concat()相同的效果？) |
| 14 | [zip()什么情况下会占用很多内存？](#zip()什么情况下会占用很多内存？) |
| 15 | [如果combineLatest()三个of()产生的数据流结果会是什么？](#如果combineLatest()三个of()产生的数据流结果会是什么？) |
| 16 | [combineLatest最后一个参数是函数会出现什么情况？](#combineLatest最后一个参数是函数会出现什么情况？) |
| 17 | [combineLatest和withLatestFrom的区别是什么？](#combineLatest和withLatestFrom的区别是什么？) |
| 18 | [concat()可以实现startWith吗？](#concat()可以实现startWith吗？) |
| 19 | [为什么有startWith()但没有endWith()呢？](#为什么有startWith()但没有endWith()呢？) |
| 20 | [操作observable的高阶合并类操作符有哪些？](#操作observable的高阶合并类操作符有哪些？) |
| 21 | [切换输入Observable用哪个操作符？](#切换输入Observable用哪个操作符？) |
| 22 | [辅助类操作符有哪些？](#辅助类操作符有哪些？) |
| 23 | |
| 24 | |
| 25 | |
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

   

10. ### defer操作符的作用是什么？

    `defer` 操作符用于延迟创建 Observable，直到有观察者订阅它时才创建。它可以确保 Observable 的创建是惰性的。

    **[⬆ Back to Top](#目录)**

    

11. ### 合并操作符有哪些？

    - `merge`: 将多个Observables的输出合并成一个Observable，不论哪个Observable发出值，它们都会被发射到输出Observable中。它们的发出是并行的。
    - `concat`: 按照给定的顺序连接多个Observables的输出。一个Observable的所有输出都完成后，才会订阅下一个Observable。
    - `combineLatest`: 当任何一个输入Observable发出值时，它会从每个输入Observable中收集最新的值并将它们作为数组发射。
    - `zip`: 当所有输入的Observables都发出一个新的项时，`zip`会将所有Observables的当前值作为数组发射。它按顺序等待每个Observable发出值。
    - `forkJoin`: 当所有的输入Observables完成时，`forkJoin`会收集每个Observable的最后一个值，并将这些值作为数组发射。如果任何一个Observable在发出值之前完成，则不会发出任何东西。
    - `withLatestFrom`: 当源Observable发出值时，它会将该值与其他输入Observables的最新值合并，并将它们作为数组发射。
    - `startWith`: 在Observable开始发射之前，用一个特定的值或一系列值开始发射数据序列。
    - `switchMap`: 对源Observable发出的每个值，都会将其映射到一个新的Observable，并发出这个新的Observable的所有值，同时自动取消之前的内部订阅。

    **[⬆ Back to Top](#目录)**

    

12. ### concat()要注意什么？

    上游的流是可完结的，不然永远轮不到后面的流登场。

    **[⬆ Back to Top](#目录)**

    

13. ### merge()为什么有时会出现和concat()相同的效果？

    ```typescript
    const source$1 = Observable.of(1, 2, 3);
    const source$2 = Observable.of(4, 5, 6);
    
    const merge$ = Observable.merge(source$1, source$2);
    ```

    以上代码输出的就是：

    1

    2

    3

    4

    5

    6

    还没来得及subscribe，同步数据流就已经被吐出来了。

    **[⬆ Back to Top](#目录)**

    

14. ### zip()什么情况下会占用很多内存？

    zip()的一个流如果迟迟不吐出数据，而另一个流的数据越吐越多，就会造成数据堆积。

    **[⬆ Back to Top](#目录)**

    

15. ### 如果combineLatest()三个of()产生的数据流结果会是什么？

    参考merge()操作符产生concat()的效果，前两个of()都是最后一个数据然后再跟着最后一个of()产生的数据流走。

    **[⬆ Back to Top](#目录)**

    

16. ### combineLatest最后一个参数是函数会出现什么情况？

    `combineLatest` 将调用这个函数，并将所有输入 Observable 的最新值作为参数传递给它。然后，`combineLatest` 会将这个函数的**返回值作为它自己发出的值**（所以这里不一定再是数组了）。

    **[⬆ Back to Top](#目录)**

    

17. ### combineLatest和withLatestFrom的区别是什么？

    `combineLatest` 和 `withLatestFrom` 都是用于将多个 Observable 的最新值进行组合的操作符，但它们的行为有所不同，适用于不同的使用场景。

    1. **combineLatest**：
       - **行为**：当任何一个输入 Observable 发出新值时，`combineLatest` 将组合所有输入 Observable 的最新值，并发出一个新值。这意味着每当任何一个输入 Observable 发出值时，都会触发组合和发出新值。
       - **使用场景**：适用于需要同时考虑多个输入 Observable 的最新值，并将它们组合为一个值的情况。常见的应用场景包括多个输入参数的计算或者 UI 组件的状态更新。

    2. **withLatestFrom**：
       - **行为**：`withLatestFrom` 只关注主 Observable，只有当主 Observable 发出值时，才会获取其他输入 Observable 的最新值，并将它们组合为一个值，并发出。这意味着主 Observable 的值驱动了组合的发生。
       - **使用场景**：适用于主要 Observable 驱动的场景，其中主 Observable 的值是触发其他 Observable 最新值的关键因素。常见的应用场景包括用户交互事件（如按钮点击、鼠标移动等）触发的操作。

    举个例子来说明两者之间的区别和使用场景对比：

    假设我们有两个 Observable：`buttonClick$` 和 `inputValue$`，分别表示按钮点击事件和输入框的值。我们想要在每次按钮点击时，将输入框的最新值与点击次数进行组合，并发出组合后的值。

    使用 `combineLatest`：
    ```javascript
    import { combineLatest } from 'rxjs';
    
    const buttonClick$ = ...; // 按钮点击事件的 Observable
    const inputValue$ = ...; // 输入框值的 Observable
    
    const combined$ = combineLatest(buttonClick$, inputValue$);
    
    combined$.subscribe(([clickEvent, inputValue]) => {
      console.log('Button clicked:', clickEvent);
      console.log('Input value:', inputValue);
    });
    ```

    使用 `withLatestFrom`：
    ```javascript
    import { withLatestFrom } from 'rxjs/operators';
    
    const buttonClick$ = ...; // 按钮点击事件的 Observable
    const inputValue$ = ...; // 输入框值的 Observable
    
    const combined$ = buttonClick$.pipe(
      withLatestFrom(inputValue$)
    );
    
    combined$.subscribe(([clickEvent, inputValue]) => {
      console.log('Button clicked:', clickEvent);
      console.log('Input value:', inputValue);
    });
    ```

    在这个例子中，如果我们使用 `combineLatest`，那么每次按钮点击或输入框值的变化都会触发组合和发出值，而使用 `withLatestFrom`，只有按钮点击事件触发时，才会获取输入框的最新值进行组合。因此，根据主 Observable 的驱动情况来选择合适的合并操作符。

    **[⬆ Back to Top](#目录)**

    

18. ### concat()可以实现startWith吗？

    可以，但是如果实现startWith()也没办法形成连续的链式调用。

    **[⬆ Back to Top](#目录)**

    

19. ### 为什么有startWith()但没有endWith()呢？

    因为concat(Observable.of('end'))就可以实现endWith()要做到的目的，而且能形成链式调用。

    **[⬆ Back to Top](#目录)**

    

20. ### 操作observable的高阶合并类操作符有哪些？

    高阶Observable是指其元素本身也是Observable的Observable。在RxJS中，处理高阶Observable的合并类操作符主要有以下几种：

    1. `concatAll`: 将高阶Observable中的内部Observables串行地订阅，只有当一个内部Observable完成后，才会订阅下一个内部Observable。
    2. `mergeAll`: 将高阶Observable中的所有内部Observables同时订阅，并将它们的值合并到单个Observable中。这是一个并发的合并操作。
    3. `switchAll`: 每当高阶Observable发出一个新的内部Observable时，`switchAll`会停止订阅当前的内部Observable，并开始订阅最新的内部Observable。只有最新的内部Observable会被订阅和发出值。
    4. `exhaustAll` (也称为 `exhaust`): 当高阶Observable发出内部Observable时，`exhaustAll`会订阅并发出第一个内部Observable的值，忽略同时发出的其他内部Observables，直到当前订阅的内部Observable完成。该操作符不会同时处理多个内部Observables。
    5. `zipAll` 是一个高阶Observable操作符，它需要与类似 `map` 的操作符结合使用来将值映射到内部Observables。`zipAll`操作符等待外部Observable发出内部Observables，然后它将这些内部Observables中相同索引的值配对并一起发出。当最短的内部Observable完成时，输出Observable也完成。

    这些高阶合并操作符有时与映射操作符结合使用（如`concatMap`, `mergeMap`, `switchMap`, `exhaustMap`），这些映射操作符将值映射到Observable，并使用相应的合并策略处理结果。

    下面是使用`mergeAll`的简单示例：

    ```javascript
    import { fromEvent, map, mergeAll } from 'rxjs';
    
    // 假设我们有多个按钮，当点击按钮时，会发出按钮的id
    const button1 = document.getElementById('button1');
    const button2 = document.getElementById('button2');
    
    const higherOrderObservable$ = fromEvent([button1, button2], 'click').pipe(
      map(event => {
        // 假设我们有一个返回Observable的函数，比如fetchData
        return fetchData(event.target.id);
      })
    );
    
    higherOrderObservable$.pipe(
      mergeAll()  // 合并内部Observable发出的值
    ).subscribe(console.log);
    ```

    在这个示例中，每次按钮点击会创建一个新的Observable（`fetchData`的返回值），`mergeAll`操作符将这些内部Observables发出的值合并到一个Observable中进行处理。

    **[⬆ Back to Top](#目录)**

    

21. ### 切换输入Observable用哪个操作符？

    switch()

    **[⬆ Back to Top](#目录)**

    

22. ### 辅助类操作符有哪些？

    RxJS 中的数学类操作符主要用于对 Observable 发出的值进行数学运算或操作。以下是一些常见的数学类操作符：

    1. **reduce**: 对 Observable 发出的值进行累加、累乘或者进行自定义的累积操作。

    2. **scan**: 类似于 `reduce`，但是会发出每个累积值，而不是只发出最终的累积结果。

    3. **min**: 发出 Observable 中最小的值。

    4. **max**: 发出 Observable 中最大的值。

    5. **sum**: 计算 Observable 中所有值的总和。

    6. **average**: 计算 Observable 中所有值的平均值。

    7. **count**: 计算 Observable 发出值的总数。

    8. **every**: 判断 Observable 中所有值是否都满足某个条件。

    9. **some**: 判断 Observable 中是否有任意一个值满足某个条件。

    10. **find**: 查找 Observable 中第一个满足条件的值。

    11. **findIndex**: 查找 Observable 中第一个满足条件的值的索引。

    12. **isEmpty**: 判断 Observable 是否为空。

    这些数学类操作符可以用于对 Observable 发出的值进行各种数学运算或操作，从而进行数据处理、筛选或分析。

    **[⬆ Back to Top](#目录)**

    

23. ### 过滤数据流的操作符有哪些？

    RxJS中用于过滤数据流的操作符有很多，以下是一些常用的过滤操作符：

    1. `filter`: 仅通过那些满足指定谓词函数条件的项。

       ```javascript
       observable$.pipe(
           filter(value => value % 2 === 0) // 只通过偶数
       );
       ```

    2. `take`: 只取Observable开始发出的前N个值，然后完成。

       ```javascript
       observable$.pipe(
           take(5) // 只取前5个值
       );
       ```

    3. `takeUntil`: 取值直到另一个Observable发出值或完成。

       ```javascript
       observable$.pipe(
           takeUntil(notifier$) // 直到notifier$发出值
       );
       ```

    4. `takeWhile`: 取值直到源Observable发出的值不满足提供的条件。

       ```javascript
       observable$.pipe(
           takeWhile(value => value < 10) // 只取值小于10的项
       );
       ```

    5. `skip`: 跳过源Observable最初发出的前N个值。

       ```javascript
       observable$.pipe(
           skip(3) // 跳过前3个值
       );
       ```

    6. `skipUntil`: 跳过项直到另一个Observable发出值。

       ```javascript
       observable$.pipe(
           skipUntil(notifier$) // 直到notifier$发出值
       );
       ```

    7. `skipWhile`: 跳过源Observable发出的每个值，直到提供的条件第一次返回false。

       ```javascript
       observable$.pipe(
           skipWhile(value => value < 4) // 跳过小于4的值
       );
       ```

    8. `distinct`: 只允许还未曾发出过的值通过。

       ```javascript
       observable$.pipe(
           distinct() // 不允许重复的值通过
       );
       ```

    9. `distinctUntilChanged`: 如果当前值与最后一个发出的值相同，则忽略它。

       ```javascript
       observable$.pipe(
           distinctUntilChanged() // 只有值变化了才通过
       );
       ```

    10. `distinctUntilKeyChanged`: 这是`distinctUntilChanged`的一个变体，它根据提供的键来检查对象的变化。

        ```javascript
        observable$.pipe(
            distinctUntilKeyChanged('id') // 根据对象的id属性判断变化
        );
        ```

        这些操作符可以组合使用，以提供强大的数据流筛选和处理能力。使用它们可以帮助你根据特定条件控制数据流，以及管理Observable的生命周期。

    **[⬆ Back to Top](#目录)**

    

24. 
