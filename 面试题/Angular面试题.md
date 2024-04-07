# Angular面试题

## 目录

| No. | Questions |
|---- | ---------|
|1 | [什么是Angular？](#什么是Angular？) |
| 2 | [Angular的特点？](#Angular的特点？) |
| 3 | [AngularJS和Angular的区别？](#AngularJS和Angular的区别？) |
| 4 | [MVC和MVVM的概念是什么？](#MVC和MVVM的概念是什么？) |
| 5 | [Angular的关键组件有哪些？](#Angular的关键组件有哪些？) |
| 6 | [Angular内置指令有哪些？](#Angular内置指令有哪些？) |
| 7 | [Component和 Directive的区别是什么？](#Component和 Directive的区别是什么？) |
| 8 | [module是什么？](#module是什么？) |
| 9 | [Angular的生命周期有哪些？](#Angular的生命周期有哪些？) |
| 10 | [Angular 中的变更检测机制是什么？](#Angular 中的变更检测机制是什么？) |
| 11 | [数据绑定是什么？](#数据绑定是什么？) |
| 12 | [metadata是什么？](#metadata是什么？) |
| 13 | [constructor和 ngOnInit 的区别？](#constructor和 ngOnInit 的区别？) |
| 14 | [什么是服务？](#什么是服务？) |
| 15 | [Angular 中的依赖注入是什么？](#Angular 中的依赖注入是什么？) |
| 16 | [依赖层次结构是如何形成的？](#依赖层次结构是如何形成的？) |
| 17 | [async pipe是什么？](#async pipe是什么？) |
| 18 | [Angular指令前面加上星号（*）是为什么？](#Angular指令前面加上星号（*）是为什么？) |
| 19 | [如果在模板中使用 script 标签会发生什么？](#如果在模板中使用 script 标签会发生什么？) |
| 20 | [你如何分类数据绑定类型？](#你如何分类数据绑定类型？) |
| 21 | [什么是管道？](#什么是管道？) |
| 22 | [什么是带参数的管道？](#什么是带参数的管道？) |
| 23 | [什么是自定义管道？](#什么是自定义管道？) |
| 24 | [什么是 Observables？](#什么是 Observables？) |
| 25 | [HttpClient 是什么？及其优势是什么？](#HttpClient 是什么？及其优势是什么？) |
| 26 | [如何读取完整的HttpClient响应？](#如何读取完整的HttpClient响应？) |
| 27 | [如何进行HttpClient的错误处理？](#如何进行HttpClient的错误处理？) |
| 28 | [RxJS 是什么？](#RxJS 是什么？) |



## 题目

1. ### 什么是Angular？

    Angular是一个基于**TypeScript**的前端框架，它简化了构建Web、移动和桌面应用程序的过程。
    
    该框架的主要特点包括**声明式模板**、**依赖注入**和**端到端工具**，这些都使应用程序开发变得更加容易。
    
    **[⬆ Back to Top](#目录)**



2. ### Angular的特点？

   - **TypeScript 支持：** Angular 是用 TypeScript 编写的，这使得代码更加健壮、可维护，并且提供了静态类型检查等优势。
   - **组件化开发：** Angular 采用了组件化的架构，将应用程序拆分为多个组件，每个组件都有自己的模板、样式和逻辑，从而使得代码更易于管理和重用。
   - **声明式模板：** Angular 使用 HTML 模板来定义用户界面，支持使用指令和数据绑定等特性，使得界面逻辑更加清晰和简单。
   - **依赖注入：** Angular 提供了强大的依赖注入系统，使得组件之间的通信和依赖关系管理更加简单和灵活。
   - **端到端工具：** Angular 提供了一整套工具和库，用于构建、测试和部署应用程序，包括 Angular CLI、测试工具和路由器等。

   **[⬆ Back to Top](#目录)**

   

3. ### AngularJS和Angular的区别？

   | AngularJS                                                    | Angular                                                      |
   | ------------------------------------------------------------ | ------------------------------------------------------------ |
   | 基于JavaScript                                               | 基于TypeScript                                               |
   | AngularJS 是一个基于 MVC（Model-View-Controller）模式的框架。 | Angular 是一个基于 MVVM 架构的前端框架，它使用了类似 MVVM 的模式，但不是纯粹的 MVVM。 |
   | AngularJS 使用控制器来实现 MVC 架构中的控制器部分，用于将模型和视图连接起来。 | Angular 采用了一种基于组件的 UI 开发方法，将应用程序拆分为独立、可重用的组件，从而提高了代码的可维护性和复用性。 |
   | 不支持移动端。                                               | 支持移动端。                                                 |
   | 由于其单页面应用程序 (SPA) 的特性，搜索引擎优化 (SEO) 方面存在一些挑战。因为 SPA 在加载时通常只会加载一个 HTML 文件，并使用 JavaScript 动态地更新内容，这样搜索引擎的爬虫可能无法正确解析页面内容，导致 SEO 效果不佳。 | Angular 框架提供了更易于构建 SEO 友好应用的解决方案。Angular 支持服务器端渲染 (SSR)，这意味着应用程序的初始 HTML 内容可以在服务器端生成，并发送到浏览器，从而使搜索引擎能够更好地索引内容。 |

   **[⬆ Back to Top](#目录)**

   

4. ### MVC和MVVM的概念是什么？

   - MVC：

     - 在 MVC 架构中，应用程序被分成三个部分：

       - 模型（Model）：表示应用程序的数据结构和业务逻辑。
       - 视图（View）：负责显示模型的内容给用户，并与用户进行交互。
       - 控制器（Controller）：充当模型和视图之间的中介，处理用户输入并更新模型或视图。

       MVC 架构有助于将应用程序的不同部分分离开来，使得代码更易于理解、维护和扩展。

       

   - 在 MVVM 架构中，同样分成三个部分：

     - 模型（Model）：表示应用程序的数据结构和业务逻辑。
     - 视图（View）：负责显示模型的内容给用户，并与用户进行交互。
     - 视图模型（ViewModel）：是一个中间层，负责将视图的状态和行为与模型分离开来。视图模型通过数据绑定技术将视图和模型连接起来，当模型改变时，视图会自动更新，反之亦然。

     MVVM 架构将视图和业务逻辑分离得更加彻底，使得代码更加模块化和可测试性更高。

     在Angular 中，组件扮演了视图和视图模型的角色，模板和组件类一起构成视图模板，而服务则提供了模型层的数据和业务逻辑。Angular 使用数据绑定来连接组件类和模板，实现了视图和模型的自动同步更新。

     **[⬆ Back to Top](#目录)**

     

5. ### Angular的关键组件有哪些？

   1. **组件（Component）：** 这些是Angular应用程序的基本构建块，用于控制HTML视图。
   2. **模块（Module）：** Angular模块是一组Angular基本构建块，如组件、指令、服务等。一个应用程序被划分为逻辑单元，每个代码单元被称为“模块”，用于执行单一任务。
   3. **模板（Template）：** 这些代表Angular应用程序的视图。
   4. **服务（Service）：** 用于创建可在整个应用程序中共享的组件。
   5. **元数据（Metadata）：** 可用于向Angular类添加更多数据。

   **[⬆ Back to Top](#目录)**

   

6. ### Angular内置指令有哪些？

   1. **ngIf：** 用于根据条件添加或移除DOM元素。
   2. **ngFor：** 用于循环遍历数组或对象，并为每个项目生成HTML元素。
   3. **ngSwitch：** 类似于JavaScript的switch语句，根据表达式的值选择一个内嵌的模板进行显示。
   4. **ngModel：** 用于双向绑定表单控件和模型数据。
   5. **ngClass：** 用于根据表达式的真假值动态添加或移除元素的CSS类。
   6. **ngStyle：** 用于根据表达式的值动态设置元素的内联样式。

   **[⬆ Back to Top](#目录)**

   

7. ### Component和 Directive的区别是什么？

   | Component                                        | Directive                              |
   | ------------------------------------------------ | -------------------------------------- |
   | 使用 `@Component` 元数据注解来注册组件           | 使用 `@Directive` 元数据注解来注册指令 |
   | 组件通常用于创建 UI 小部件                       | 指令用于向现有 DOM 元素添加行为        |
   | 组件用于将应用程序分解为更小的组件               | 指令用于设计可重用的组件               |
   | 每个 DOM 元素只能有一个组件                      | 一个 DOM 元素可以使用多个指令          |
   | `@View` 装饰器或 `templateUrl/template` 是必需的 | 指令不使用视图                         |

   **[⬆ Back to Top](#目录)**

   

8. ### module是什么？

   NgModule 是 Angular 中的一个装饰器（Decorator），用于定义模块（Module）。NgModule 提供了一种方式来将组件、指令、管道和服务组织到一个单独的功能单元中，以便更好地管理和组织 Angular 应用程序的代码。

   NgModule 装饰器有五个重要的选项：

   1. `imports` 选项用于导入其他依赖模块。`BrowserModule` 是任何基于 Web 的 Angular 应用程序默认所需的模块。
   2. `declarations` 选项用于在相应模块中定义组件。
   3. `bootstrap` 选项告诉 Angular 应用程序中要启动哪个组件。
   4. `providers` 选项用于配置一组可在此模块的注入器中使用的可注入对象。

   **[⬆ Back to Top](#目录)**

   

9. ### Angular的生命周期有哪些？

   1. **constructor():** 当组件或指令的实例被创建时，`constructor` 方法会被自动调用。通常情况下，`constructor` 方法用于依赖注入、初始化类的属性以及执行一些一次性的初始化逻辑。
   2. **ngOnChanges():** 当组件或指令的输入属性发生变化时调用。这个钩子在组件实例化之后以及输入属性的值发生变化时被调用。
   3. **ngOnInit():** 当组件或指令初始化完成时调用。通常用于执行初始化逻辑，比如从服务获取数据。
   4. **ngDoCheck():** 在 Angular 执行变更检测时调用。它允许开发人员检测和做出反应，以在 Angular 无法或不会自动检测到的变化时执行额外的操作。
   5. **ngAfterContentInit():** 在 Angular 投影内容到组件或指令的视图之后调用。这个钩子在投影内容被检查并初始化后被调用。
   6. **ngAfterContentChecked():** 在 Angular 检查投影内容后调用。它在投影内容的变更检测完成后被调用。
   7. **ngAfterViewInit():** 在 Angular 初始化组件或指令的视图及其子视图后调用。在这个阶段，组件或指令的视图已经初始化完成，但是子组件或指令的视图可能还没有。
   8. **ngAfterViewChecked():** 在 Angular 检查组件或指令的视图及其子视图后调用。它在视图的变更检测完成后被调用。
   9. **ngOnDestroy():** 在组件或指令被销毁之前调用。通常用于执行一些清理工作，比如取消订阅、关闭定时器等。

   **[⬆ Back to Top](#目录)**

   

10. ### Angular 中的变更检测机制是什么？

    在 Angular 中，变更检测是指框架用于检测数据模型中的变化并将这些变化更新到视图的过程。

    Angular 应用程序中的变更检测是一个核心概念，它是实现**数据绑定**和**响应式 UI** 的基础。

    当应用程序中的数据发生变化时，Angular 的变更检测机制会检测到这些变化，并且会自动更新受影响的视图以反映这些变化。这种自动更新使得开发人员无需手动操作 DOM 元素来更新视图，而是可以专注于操作数据模型。

    Angular 中的变更检测机制主要依赖于 **Zone.js 和 Zone.js 所提供的异步任务检测能力**。当应用程序的状态发生变化时（比如用户输入、HTTP 请求返回、定时器触发等），Zone.js 会捕获这些事件并通知 Angular 执行变更检测。然后 **Angular 会遍历组件树**，检查每个组件的**数据绑定表达式**是否有变化，如果有变化，就更新相关的视图。

    **[⬆ Back to Top](#目录)**

    

11. ### 数据绑定是什么？

    数据绑定是 Angular 中的核心概念，允许定义组件与 DOM 之间的通信，使得定义交互式应用程序变得非常简单，而不必担心数据的推送和拉取。数据绑定有四种形式（分为3个类别），其数据流动方式不同。

    1. **从组件到 DOM：**

        **插值表达式（Interpolation）:** {{ value }}：将组件中属性的值添加到 DOM 中
        ```html
        <li>姓名：{{ user.name }}</li>
        <li>地址：{{ user.address }}</li>
        ```
        **属性绑定（Property binding）:** [property]=”value”：将值从组件传递到指定的属性或简单的 HTML 属性
        ```html
        <input type="email" [value]="user.email">
        ```

    2. **从 DOM 到组件：**

        **事件绑定（Event binding）: (event)=”function”:** 当特定的 DOM 事件发生时（例如：点击、改变、键盘按键），调用组件中指定的方法
        ```html
        <button (click)="logout()"></button>
        ```

    3. **双向绑定：**

        **双向数据绑定（Two-way data binding）:** [(ngModel)]=”value”：双向数据绑定允许数据双向流动。例如，在下面的代码片段中，DOM 输入的电子邮件和组件中的电子邮件属性是同步的
        ```html
        <input type="email" [(ngModel)]="user.email">
        ```

    **[⬆ Back to Top](#目录)**

    

12. ### metadata是什么？

    metadata用于装饰一个类，以配置类的预期行为。元数据由装饰器表示。
    1. **类装饰器**，例如 @Component 和 @NgModule

    2. **属性装饰器** 用于类内的属性，例如 @Input 和 @Output

    3. **方法装饰器** 用于类内的方法，例如 @HostListener

        ```typescript
        import { Component, HostListener } from '@angular/core';
        
        @Component({
            selector: 'my-component',
            template: '<div>方法装饰器</div>'
        })
        export class MyComponent {
            @HostListener('click', ['$event'])
            onHostClick(event: Event) {
                // 点击事件触发后，`event` 可用
            }
        }
        ```

    4. **参数装饰器** 用于类构造函数内的参数，例如 @Inject,  @Optional

        ```typescript
        import { Component, Inject } from '@angular/core';
        import { MyService } from './my-service';
        
        @Component({
            selector: 'my-component',
            template: '<div>参数装饰器</div>'
        })
        export class MyComponent {
            constructor(@Inject(MyService) myService) {
                console.log(myService); // MyService
            }
        }
        ```

    **[⬆ Back to Top](#目录)**

    

13. ### constructor和 ngOnInit 的区别？

    构造函数是类的默认方法，在实例化类时执行，确保类及其子类中的字段得到正确的初始化。

    Angular（或更好地说是依赖注入器（DI））分析构造函数参数，当通过调用 new Class() 创建新实例时，它会尝试找到与构造函数参数类型匹配的提供者，解析它们并将它们传递给构造函数。 

    ngOnInit 是 Angular 调用的一个生命周期钩子，表示 Angular 已经完成创建组件。 

    **总结：**通常，我们使用 ngOnInit 来进行所有的初始化/声明，并避免在构造函数中执行过多的操作。构造函数应该只用于初始化类成员，而不应该执行实际的“工作”。 因此，你应该使用 constructor() 来设置依赖注入，而不要做太多其他的事情。ngOnInit() 更适合“启动” - 这是组件绑定解析的地方/时机。

    **[⬆ Back to Top](#目录)**

    

14. ### 什么是服务？

    服务用于在各种模块之间提供通用功能。通过服务，可以更好地分离应用程序的关注点，将通用功能提取出来实现更好的模块化。

    **[⬆ Back to Top](#目录)**

    

15. ### Angular 中的依赖注入是什么？

    依赖注入（DI）是一种重要的应用程序设计模式，其中类从外部来源请求依赖项，而不是自己创建它们。Angular 自带了自己的依赖注入框架，用于解析依赖关系（类需要执行其功能所需的服务或对象）。因此，您可以在整个应用程序中使您的服务依赖于其他服务。

    以下是一个简单的示意图，说明了依赖注入的概念：

    ```
    +-----------------+                  +---------------------+
    |    Component    |       DI         |       Service       |
    +-----------------+    Injection     +---------------------+
    |    Dependency   | <-------------- |      Dependency     |
    |    Injection    |                  |      Injection      |
    +-----------------+                  +---------------------+
    ```

    在这个示意图中：

    - **Component（组件）**：表示使用依赖注入的组件。它需要一些依赖项来完成其功能。
    - **Service（服务）**：表示提供这些依赖项的服务。服务可能有自己的依赖项。
    - **Dependency Injection（依赖注入）**：表示将服务注入到组件中，以满足其依赖项的过程。组件不需要自己创建服务，而是通过依赖注入机制获得所需的服务实例。

    **[⬆ Back to Top](#目录)**

    

16. ### 依赖层次结构是如何形成的？

    在 Angular 中，依赖层次结构是通过注入器（injector）来实现的。Angular 的注入器是负责创建、管理和解析依赖项的机制。当 Angular 应用启动时，会创建一个根注入器，然后根据应用的结构和组件树形成一种层次结构。

    下面是 Angular 中依赖层次结构的形成方式：

    1. **根注入器（Root Injector）：** Angular 应用启动时会创建一个根注入器。根注入器是整个应用的顶层注入器，负责管理应用中的所有服务。根注入器中注册的服务对整个应用可见，即在整个应用的任何地方都可以访问这些服务。

       ```typescript
       import { Injectable } from '@angular/core';
       
       @Injectable({
         providedIn: 'root'
       })
       export class LoggerService {
         log(message: string) {
           console.log(message);
         }
       }
       ```

    2. **模块注入器（Module Injector）：** 每个 NgModule（Angular 模块）都有自己的注入器。当一个模块被加载时，Angular 会为该模块创建一个新的注入器。模块注入器负责管理模块内部的服务和提供者。模块注入器可以访问根注入器中注册的服务，因此模块中的组件和服务可以共享根注入器中的服务。

       ```typescript
       import { NgModule } from '@angular/core';
       import { DataService } from './data.service';
       
       @NgModule({
         providers: [DataService]
       })
       export class DataModule { }
       ```

    3. **组件注入器（Component Injector）：** 每个组件都有自己的注入器。当组件被实例化时，Angular 会为该组件创建一个新的注入器。组件注入器负责管理组件内部的服务和依赖项。组件注入器可以访问模块注入器和根注入器中注册的服务，因此组件中可以使用模块和根注入器中提供的服务。

       ```typescript
       import { Component } from '@angular/core';
       import { DataService } from './data.service';
       
       @Component({
         selector: 'app-example',
         template: '<p>Example Component</p>',
         providers: [DataService] // 在组件级别提供 DataService
       })
       export class ExampleComponent { }
       ```

    4. **元素注入器（Element Injector）：** 每个 DOM 元素都可以有一个元素注入器。元素注入器用于管理与该 DOM 元素关联的 Angular 指令或组件的依赖项。元素注入器负责解析元素级别的依赖项，并可以访问组件注入器、模块注入器和根注入器中注册的服务。

       ```typescript
       import { Directive, ElementRef } from '@angular/core';
       import { LoggerService } from './logger.service';
       
       @Directive({
         selector: '[appExampleDirective]',
         providers: [LoggerService] // 在指令级别提供 LoggerService
       })
       export class ExampleDirective {
         constructor(private elementRef: ElementRef, private logger: LoggerService) {
           logger.log('ExampleDirective instantiated.');
         }
       }
       ```

    总之，Angular 中的依赖层次结构是通过不同级别的注入器来实现的，每个注入器负责管理一定范围内的依赖关系，并且可以访问更高级别的注入器中注册的服务。这种层次结构确保了依赖项的正确解析和管理，同时提供了灵活性和可维护性。

    **[⬆ Back to Top](#目录)**

    

17. ### async pipe是什么？

    async pipe 是 Angular 中的一个内置管道，用于处理 Observable 或 Promise 类型的异步数据流。它订阅了 Observable 或 Promise，并在数据流中有新值时自动更新视图。async 管道使得在模板中处理异步数据变得更加简单和方便。

    以下是一个示例，演示了如何在 Angular 组件中使用 async 管道：

    ```typescript
    import { Component } from '@angular/core';
    import { Observable } from 'rxjs';
    
    @Component({
      selector: 'app-example',
      template: `
        <div>
          <p>Data: {{ asyncData | async }}</p>
          <button (click)="fetchData()">Fetch Data</button>
        </div>
      `
    })
    export class ExampleComponent {
      asyncData: Observable<any>;
    
      constructor(private dataService: DataService) {}
    
      fetchData() {
        this.asyncData = this.dataService.getData(); // Assume this returns an Observable
      }
    }
    ```

    在上面的示例中，当用户点击按钮时，会调用 `fetchData()` 方法，该方法从数据服务中获取数据并将返回的 Observable 赋值给 `asyncData` 属性。然后，模板中的 async 管道会自动订阅 `asyncData`，并在数据流中有新值时自动更新视图。

    这样，我们就可以轻松地在 Angular 模板中处理异步数据，而不必担心手动管理订阅和取消订阅。

    **[⬆ Back to Top](#目录)**

    

18. ### Angular指令前面加上星号（*）是为什么？

    在 Angular 中，将指令前面加上星号（*）是为了使用 Angular 的结构指令（structural directive）。结构指令会修改 DOM 的结构，根据指令的逻辑添加、删除或替换 DOM 元素。

    **[⬆ Back to Top](#目录)**

    

19. ### 如果在模板中使用 script 标签会发生什么？

    Angular 会将这个值识别为不安全的，并自动对其进行消毒处理，即移除 `script` 标签，但保留 `script` 标签的安全内容，比如文本内容。这样可以消除脚本注入攻击的风险。如果你仍然使用了 `script` 标签，它将被忽略，并且浏览器控制台会出现警告信息。

    让我们看一个使用 innerHtml 属性绑定导致 XSS 漏洞的例子：
    ```typescript
    export class InnerHtmlBindingComponent {
      // 例如，来自 URL 的用户/攻击者可控的值。
      htmlSnippet = 'Template <script>alert("0wned")</script> <b>Syntax</b>';
    }
    ```

    **[⬆ Back to Top](#目录)**

    

20. ### 你如何分类数据绑定类型？

    "源"是指组件类中的属性，而"视图"是指用户界面中的可见元素。

    数据绑定类型可以分为三类，根据数据流的方向进行区分。它们如下所示：

    1. 从源到视图
    2. 从视图到源
    3. 视图到源到视图

    可能的绑定语法可以如下表格化：

    | 数据方向               | 语法                                                         | 类型                                   |
    | ---------------------- | ------------------------------------------------------------ | -------------------------------------- |
    | 从源到视图（单向）     | 1. {{expression}} 2. [target]="expression" 3. bind-target="expression" | 插值、属性、属性绑定、类绑定、样式绑定 |
    | 从视图到源（单向）     | 1. (target)="statement" 2. on-target="statement"             | 事件绑定                               |
    | 视图到源到视图（双向） | 1. [(target)]="expression" 2. bindon-target="expression"     | 双向绑定                               |

    **[⬆ Back to Top](#目录)**

    

21. ### 什么是管道？

    管道是简单的函数，使用模板表达式作为输入，并将其转换为所需的输出。例如，让我们使用 **date** 管道来将组件的生日属性转换为易读的日期格式。

    ```javascript
    import { Component } from '@angular/core';
    
    @Component({
      selector: 'app-birthday',
      template: `<p>Birthday is {{ birthday | date }}</p>`
    })
    export class BirthdayComponent {
      birthday = new Date(1987, 6, 18); // 1987年6月18日
    }
    ```

    **[⬆ 返回顶部](#目录)**

    

22. ### 什么是带参数的管道？

    管道可以接受任意数量的可选参数来微调其输出。带参数的管道可以通过在管道名称后面加上冒号（:）然后是参数值来创建。如果管道接受多个参数，请使用冒号分隔值。让我们以一个具有特定格式（dd/MM/yyyy）的生日示例为例：

    ```javascript
    import { Component } from '@angular/core';
    
    @Component({
      selector: 'app-birthday',
      template: `<p>Birthday is {{ birthday | date:'dd/MM/yyyy'}}</p>` // 18/06/1987
    })
    export class BirthdayComponent {
      birthday = new Date(1987, 6, 18);
    }
    ```

    **注意：** 参数值可以是任何有效的模板表达式，例如字符串字面量或组件属性。

    **[⬆ 返回顶部](#目录)**

    

23. ### 什么是自定义管道？

    除了内置管道外，您还可以编写自己的自定义管道。

    您可以创建用于转换现有值的自定义可重用管道。例如，让我们创建一个用于根据文件扩展名查找文件大小的自定义管道：

    ```typescript
    import { Pipe, PipeTransform } from '@angular/core';
    
    @Pipe({name: 'customFileSizePipe'})
    export class FileSizePipe implements PipeTransform {
      transform(size: number, extension: string = 'MB'): string {
        return (size / (1024 * 1024)).toFixed(2) + extension;
      }
    }
    ```

    **[⬆ 返回顶部](#目录)**

    

24. ###  什么是 Observables？

    Observables 是声明性的，它们提供了在应用程序中发布者和订阅者之间传递消息的支持。它们主要用于事件处理、异步编程和处理多个值。在这种情况下，你定义了一个用于发布值的函数，但直到有一个消费者订阅它时才会执行。订阅的消费者然后接收通知，直到函数完成或者直到它们取消订阅。

    **[⬆ 返回顶部](#目录)**

    

25. ### HttpClient 是什么？及其优势是什么？

    大多数前端应用程序通过 `HTTP` 协议与后端服务进行通信，使用的是 `XMLHttpRequest` 接口或 `fetch()` API。Angular 提供了一个简化的客户端 HTTP API，称为 `HttpClient`，它是基于 `XMLHttpRequest` 接口构建的。这个客户端可以从 `@angular/common/http` 包中获得。 你可以在根模块中导入它，如下所示：

    ```typescript
    import { HttpClientModule } from '@angular/common/http';
    ```

    `HttpClient` 的主要优势可以列举如下：

    1. 包含可测试性功能
    2. 提供了类型化的请求和响应对象
    3. 拦截请求和响应
    4. 支持 Observable API
    5. 支持简化的错误处理

    **[⬆ 返回顶部](#目录)**

    

26. ### 如何读取完整的HttpClient响应？

    响应体可能不会返回完整的响应数据，因为有时服务器还会返回特殊的标头或状态码，这些对应用程序的工作流程很重要。为了获取完整的响应，你应该使用 `HttpClient` 中的 `observe` 选项：

    ```typescript
    getUserResponse(): Observable<HttpResponse<User>> {
      return this.http.get<User>(
        this.userUrl, { observe: 'response' });
    }
    ```

    现在，`HttpClient.get()` 方法返回的是一个类型为 `HttpResponse` 的 Observable，而不仅仅是 JSON 数据。

    **[⬆ 返回顶部](#目录)**

    

27. ### 如何进行HttpClient的错误处理？

    如果请求在服务器端失败或由于网络问题无法到达服务器，则 `HttpClient` 将返回一个错误对象，而不是成功的响应。在这种情况下，你需要在组件中处理错误，通过将 `error` 对象作为 `subscribe()` 方法的第二个回调函数来处理。

    让我们看看如何在组件中处理错误，举个例子：

    ```typescript
    fetchUser() {
      this.userService.getProfile()
        .subscribe(
          (data: User) => this.userProfile = { ...data }, // 成功路径
          error => this.error = error // 错误路径
        );
    }
    ```

    最好给用户一些有意义的反馈，而不是显示从 `HttpClient` 返回的原始错误对象。

    **[⬆ 返回顶部](#目录)**

    

28. ### RxJS 是什么？

    RxJS 是一个库，用于以函数式、响应式风格组合异步和基于回调的代码，使用 Observables。许多 API，如 HttpClient，会产生和消费 RxJS Observables，并使用操作符来处理 Observables。

    例如，你可以导入观察者和操作符来使用 HttpClient，如下所示：

    ```javascript
    import { Observable, throwError } from 'rxjs';
    import { catchError, retry } from 'rxjs/operators';
    ```

    **[⬆ 返回顶部](#目录)**
