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
| 29 | [订阅是什么？](#订阅是什么？) |
| 30 | [什么是 Observable？](#什么是 Observable？) |
| 31 | [什么是 Observer？](#什么是 Observer？) |
| 32 | [Promise 和 Observable 之间的区别是什么？](#Promise 和 Observable 之间的区别是什么？) |
| 33 | [subscribe 方法的简写是什么？](#subscribe 方法的简写是什么？) |
| 34 | [如何在非 Angular 应用程序中使用 Angular 组件？](#如何在非 Angular 应用程序中使用 Angular 组件？) |
| 35 | [指令有哪些种类？](#指令有哪些种类？) |
| 36 | [base href 标签的目的是什么？](#base href 标签的目的是什么？) |
| 37 | [什么是RouterLinkActive？](#什么是RouterLinkActive？) |
| 38 | [router events是什么？](#router events是什么？) |
| 39 | [Angular中两种不同的编译模式是什么？性能差异是什么？](#Angular中两种不同的编译模式是什么？性能差异是什么？) |
| 40 | [如何控制AOT编译的方式？](#如何控制AOT编译的方式？) |
| 41 | [AOT有哪三个阶段？](#AOT有哪三个阶段？) |
| 42 | [Angular中元数据 JSON 文件是什么？目的是什么？](#Angular中元数据 JSON 文件是什么？目的是什么？) |
| 43 | [如何提供配置继承？](#如何提供配置继承？) |
| 44 | [什么是非空断言操作符？](#什么是非空断言操作符？) |
| 45 | [什么是 Zone（区域）？](#什么是 Zone（区域）？) |
| 46 | [什么是 Codelyzer？](#什么是 Codelyzer？) |
| 47 | [什么是 Angular 动画？](#什么是 Angular 动画？) |
| 48 | [如何在 Angular 中注入动态脚本？](#如何在 Angular 中注入动态脚本？) |
| 49 | [什么是 Angular Ivy？](#什么是 Angular Ivy？) |
| 50 | [Angular 中有哪些命名规则类型？](#Angular 中有哪些命名规则类型？) |
| 51 | [Angular的DSL是什么？](#Angular的DSL是什么？) |
| 52 | [什么是 Angular 中的 RxJS 的 Subject？](#什么是 Angular 中的 RxJS 的 Subject？) |
| 53 | [单播和多播的区别是什么？](#单播和多播的区别是什么？) |
| 54 | [什么是 Bazel 工具？](#什么是 Bazel 工具？) |
| 55 | [如何在 Angular 中检测路由变化？](#如何在 Angular 中检测路由变化？) |
| 56 | [如何为 HTTP 客户端传递标头？](#如何为 HTTP 客户端传递标头？) |
| 57 | [Angular 支持动态导入吗？](#Angular 支持动态导入吗？) |
| 58 | [什么是懒加载？](#什么是懒加载？) |
| 59 | [什么是workspace APIs？](#什么是workspace APIs？) |
| 60 | [Angular怎么升级版本？](#Angular怎么升级版本？) |
| 61 | [如何使用 CLI 测试 Angular 应用程序？](#如何使用 CLI 测试 Angular 应用程序？) |
| 62 | [如何在 Angular 应用程序中使用 polyfills？](#如何在 Angular 应用程序中使用 polyfills？) |
| 63 | [触发 Angular 中变更检测的方式有哪些？](#触发 Angular 中变更检测的方式有哪些？) |
| 64 | [Angular 的各个版本有什么区别？](#Angular 的各个版本有什么区别？)**（仅了解即可）** |
| 65 | [Angular 中的安全原则是什么？](#Angular 中的安全原则是什么？) |
| 66 | [Angular 针对预防 XSS 攻击的安全模型是什么？](#Angular 针对预防 XSS 攻击的安全模型是什么？) |
| 67 | [模板编译器(AOT)在预防 XSS 攻击中的作用是什么？](#模板编译器(AOT)在预防 XSS 攻击中的作用是什么？) |
| 68 | [什么是Sanitization（消毒）？Angular是否支持它？](#什么是Sanitization（消毒）？Angular是否支持它？) |
| 69 | [插值内容和innerHTML之间有什么区别？](#插值内容和innerHTML之间有什么区别？) |
| 70 | [如何防止自动消毒？](#如何防止自动消毒？) |
| 71 | [Angular是否能防止HTTP级别的漏洞？](#Angular是否能防止HTTP级别的漏洞？) |
| 72 | [什么是HTTP拦截器？](#什么是HTTP拦截器？) |
| 73 | [HTTP拦截器的应用有哪些？](#HTTP拦截器的应用有哪些？) |
| 74 | [Angular是否支持多个拦截器？](#Angular是否支持多个拦截器？) |
| 75 | [Angular如何简化国际化？](#Angular如何简化国际化？) |
| 76 | [如何手动注册区域数据？](#如何手动注册区域数据？)**（仅了解即可）** |
| 77 | [ngIf和hidden属性之间的区别是什么？](#ngIf和hidden属性之间的区别是什么？) |
| 78 | [ngFor 的 trackBy 属性的目的是什么？](#ngFor 的 trackBy 属性的目的是什么？) |
| 79 | [ngSwitch指令的目的是什么？](#ngSwitch指令的目的是什么？) |
| 80 | [什么是安全导航运算符？](#什么是安全导航运算符？) |
| 81 | [什么是入口组件？](#什么是入口组件？) |
| 82 | [什么是引导组件？](#什么是引导组件？) |
| 83 | [什么是路由入口组件？](#什么是路由入口组件？) |
| 84 | [什么是 Angular 编译器？](#什么是 Angular 编译器？) |
| 85 | [ngModule 元数据在编译过程中的作用是什么？](#ngModule 元数据在编译过程中的作用是什么？) |
| 86 | [什么是特性模块？](#什么是特性模块？) |
| 87 | [如果在特性模块中使用 BrowserModule 会发生什么？](#如果在特性模块中使用 BrowserModule 会发生什么？) |
| 88 | [特性模块的类型有哪些？](#特性模块的类型有哪些？) |
| 89 | [什么是提供者（Provider）？](#什么是提供者（Provider）？) |
| 90 | [对提供者的作用域有何推荐？](#对提供者的作用域有何推荐？) |
| 91 | [如何将提供者作用域限制在一个模块内？](#如何将提供者作用域限制在一个模块内？) |
| 92 | [如何提供一个单例服务？](#如何提供一个单例服务？) |
| 93 | [有哪些消除重复Service注册的不同方法？](#有哪些消除重复Service注册的不同方法？) |
| 94 | [forRoot方法如何帮助避免重复的路由实例？](#forRoot方法如何帮助避免重复的路由实例？) |
| 95 | [什么是shared共享模块？](#什么是shared共享模块？) |
| 96 | [可以使用模块共享服务吗？](#可以使用模块共享服务吗？) |
| 97 | [什么是 ngcc？](#什么是 ngcc？) |
| 98 | [什么是 NgZone？](#什么是 NgZone？) |
| 99 | [什么是 NoopZone？](#什么是 NoopZone？) |
| 100 | [变更检测的可能数据更新场景有哪些？](#变更检测的可能数据更新场景有哪些？) |
| 101 | [什么是zone context（区域上下文）？](#什么是zone context（区域上下文）？) |
| 102 | [zone的生命周期钩子是什么？](#zone的生命周期钩子是什么？) |
| 103 | [NgZone 的哪些方法用于控制变更检测？](#NgZone 的哪些方法用于控制变更检测？) |
| 104 | [如何更改 zonejs 的设置？](#如何更改 zonejs 的设置？) |
| 105 | [什么是可选依赖项？](#什么是可选依赖项？) |
| 106 | [注入器层次结构有哪些类型？](#注入器层次结构有哪些类型？) |
| 107 | [什么是响应式表单？](#什么是响应式表单？) |
| 108 | [什么是模板驱动表单？](#什么是模板驱动表单？) |
| 109 | [响应式表单和模板驱动表单之间有哪些区别？](#响应式表单和模板驱动表单之间有哪些区别？) |
| 110 | [表单控件分组有哪些不同的方法？](#表单控件分组有哪些不同的方法？) |
| 111 | [如何更新表单模型的特定属性？](#如何更新表单模型的特定属性？) |
| 112 | [FormBuilder 的目的是什么？](#FormBuilder 的目的是什么？) |
| 113 | [如何验证表单中模型的更改？](#如何验证表单中模型的更改？) |
| 114 | [ngModel 提供的状态 CSS 类是什么？](#ngModel 提供的状态 CSS 类是什么？) |
| 115 | [验证器函数有哪些类型？](#验证器函数有哪些类型？) |
| 116 | [能举一个内置验证器的例子吗？](#能举一个内置验证器的例子吗？) |
| 117 | [如何优化异步验证器的性能？](#如何优化异步验证器的性能？) |
| 118 | [如何在同一个元素上设置 ngFor 和 ngIf？](#如何在同一个元素上设置 ngFor 和 ngIf？) |
| 119 | [CSS 中的 host 属性是什么？](#CSS 中的 host 属性是什么？) |
| 120 | [什么是内容投影（Content Projection）？](#什么是内容投影（Content Projection）？) |
| 121 | [什么是ng-template？](#什么是ng-template？) |
| 122 | [ng-content、ng-template和ng-container三者的用途？](#ng-content、ng-template和ng-container三者的用途？) |
| 123 | [什么是路由守卫？](#什么是路由守卫？) |
| 124 | [路由守卫可以用来做什么？](#路由守卫可以用来做什么？) |
| 125 | [路由守卫怎么优化angular性能的？](#路由守卫怎么优化angular性能的？) |



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

    

29. ### 订阅是什么？

    只有当有人订阅 Observable 实例时，它才开始发布值。因此，你需要通过调用实例的 `subscribe()` 方法进行订阅，并传递一个观察者对象来接收通知。

    让我们以创建和订阅一个简单的 observable 为例，使用一个观察者将接收到的消息记录到控制台上。

    ```javascript
    // 创建一个包含 5 个整数的 observable 序列，从 1 开始
    const source = range(1, 5);
    
    // 创建观察者对象
    const myObserver = {
      next: x => console.log('Observer got a next value: ' + x),
      error: err => console.error('Observer got an error: ' + err),
      complete: () => console.log('Observer got a complete notification'),
    };
    
    // 使用观察者对象执行并打印每个项
    source.subscribe(myObserver);
    // => Observer got a next value: 1
    // => Observer got a next value: 2
    // => Observer got a next value: 3
    // => Observer got a next value: 4
    // => Observer got a next value: 5
    // => Observer got a complete notification
    ```

    **[⬆ 返回顶部](#目录)**

    

30. ### 什么是 Observable？

    Observable 是一种类似于 Promise 的独特对象，可以帮助管理异步代码。Observables 不是 JavaScript 语言的一部分，因此我们需要依赖一个流行的 Observable 库，称为 RxJS。
    Observables 是使用 `new` 关键字创建的。

    让我们看一个简单的 Observable 示例：

    ```javascript
    import { Observable } from 'rxjs';
    
    const observable = new Observable(observer => {
      setTimeout(() => {
        observer.next('Hello from a Observable!');
      }, 2000);
    });
    ```

    **[⬆ 返回顶部](#目录)**

    

31. ### 什么是 Observer？

    在 RxJS 中，观察者（Observer）是一种消费者接口，用于接收 Observable 发出的通知。观察者通常由三个回调函数组成：

    1. `next(value)`：用于处理 Observable 发出的每个值。
    2. `error(err)`：用于处理 Observable 发出的任何错误。
    3. `complete()`：用于处理 Observable 完成的通知。

    观察者可以通过调用 `subscribe()` 方法订阅 Observable 来接收通知。当 Observable 发出值、错误或完成通知时，观察者的相应回调函数将被调用。

    以下是一个简单的观察者示例：

    ```javascript
    const observer = {
      next: (value) => console.log('Received value:', value),
      error: (err) => console.error('Received error:', err),
      complete: () => console.log('Received complete notification')
    };
    
    observable.subscribe(observer);
    ```

    在这个示例中，当 Observable 发出值时，`next` 回调将被调用来处理这些值。如果 Observable 发出错误，则 `error` 回调将被调用来处理错误。当 Observable 完成时，`complete` 回调将被调用来处理完成通知。

    > 可以将 Observer 中的 `next` 类比为 Promise 中的 `resolve`，而 `error` 则类比为 `reject`

    - `next` 回调函数用于处理 Observable 发出的值，类似于 Promise 的 `resolve` 处理异步操作成功时的情况。
    - `error` 回调函数用于处理 Observable 发生的错误，类似于 Promise 的 `reject` 处理异步操作失败时的情况。
    - `complete` 回调函数表示 Observable 完成了数据流的发射，不再发出任何值，这与 Promise 中没有对应的情况。

    因此，在某种程度上，Observable 和 Promise 都是用于处理异步操作的方式，Observer 中的回调函数与 Promise 的状态（resolved/rejected）处理方式相似。

    **[⬆ 返回顶部](#目录)**

    

32. ### Promise 和 Observable 之间的区别是什么？

    下面是 Promise 和 Observable 之间的区别列表：

    | 特征     | Promise                                           | Observable                               |
    | -------- | ------------------------------------------------- | ---------------------------------------- |
    | 执行时间 | 创建时立即执行                                    | 订阅时才开始执行                         |
    | 返回值   | 提供单个值                                        | 可以提供多个值                           |
    | 错误处理 | 通过 `.catch()` 或 `.then()` 方法链中的第二个参数 | 通过订阅方法的第二个参数（错误处理程序） |
    | 可取消性 | 不支持取消                                        | 支持取消订阅                             |
    | 链式调用 | 使用 `.then()` 和 `.catch()` 方法                 | 可以使用操作符和订阅方法进行链式调用     |

    **Observable的错误处理：**

    ```typescript
    someObservable.subscribe(
      result => {
        // 处理成功情况
      },
      error => {
        // 处理失败情况
      }
    );
    ```

    **Observable的链式调用：**

    Observable 使用操作符和订阅方法进行链式调用。

    ```typescript
    someObservable
      .pipe(
        // 应用操作符
        map(data => processData(data)),
        catchError(error => handleError(error))
      )
      .subscribe(
        result => {
          // 处理成功情况
        },
        error => {
          // 处理失败情况
        }
      );
    ```

    **[⬆ 返回顶部](#目录)**

    

33. ### subscribe 方法的简写是什么？

    `subscribe()` 方法可以接受内联的回调函数定义，用于 `next`、`error` 和 `complete` 处理程序。这被称为简写表示法或具有位置参数的 Subscribe 方法。

     ```javascript
     myObservable.subscribe(
         x => console.log('Observer got a next value: ' + x),
         err => console.error('Observer got an error: ' + err),
         () => console.log('Observer got a complete notification')
     );
     ```

    **[⬆ 返回顶部](#目录)**

    

34. ### 如何在非 Angular 应用程序中使用 Angular 组件？

    使用 `@angular/elements` 模块中的 `createCustomElement` 函数将 Angular 组件转换为自定义元素，并将其在不同的 Web 应用程序中使用。

    假设我们有一个简单的 Angular 组件 `HelloComponent`，它只是显示一个简单的问候语。现在我们希望将这个组件转换为自定义元素，并在普通的 HTML 页面中使用它。

    首先，创建 `HelloComponent` 组件：

    ```typescript
    // hello.component.ts
    
    import { Component } from '@angular/core';
    
    @Component({
      selector: 'app-hello',
      template: '<h1>Hello, World!</h1>',
    })
    export class HelloComponent {}
    ```

    接下来，创建一个 Angular 模块，并将 `HelloComponent` 声明为 `entryComponents`，以便 `@angular/elements` 能够将其转换为自定义元素：

    ```typescript
    // app.module.ts
    
    import { BrowserModule } from '@angular/platform-browser';
    import { Injector, NgModule } from '@angular/core';
    import { createCustomElement } from '@angular/elements';
    
    import { HelloComponent } from './hello.component';
    
    @NgModule({
      declarations: [
        HelloComponent,
      ],
      imports: [
        BrowserModule,
      ],
      entryComponents: [
        HelloComponent,
      ],
    })
    export class AppModule {
      constructor(private injector: Injector) {
        const customElement = createCustomElement(HelloComponent, { injector });
        customElements.define('app-hello', customElement);
      }
    
      ngDoBootstrap() {}
    }
    ```

    在上面的代码中，我们使用 `createCustomElement` 函数将 `HelloComponent` 转换为自定义元素，并在模块的构造函数中使用 `customElements.define` 方法注册该自定义元素。

    然后，编译 Angular 应用程序并生成单个脚本包：

    ```bash
    ng build --prod --output-hashing none
    ```

    生成的脚本包将在 `dist` 目录下生成一个 JavaScript 文件，我们将在 HTML 页面中使用它。

    最后，在 HTML 页面中使用自定义元素：

    ```html
    <!-- index.html -->
    
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Angular Custom Element Example</title>
      <script src="path/to/angular-elements-bundle.js"></script>
    </head>
    <body>
      <app-hello></app-hello>
    </body>
    </html>
    ```

    在上面的 HTML 页面中，我们只需引入生成的 JavaScript 文件，并使用 `<app-hello>` 标签来使用自定义元素。

    这样，我们就可以将 Angular 组件转换为自定义元素，并在任何支持自定义元素的 Web 应用程序中使用它。

    **[⬆ 返回顶部](#目录)**

    

35. ### 指令有哪些种类？
    主要有三种类型的指令：

    1. **Components** — 这些指令带有一个模板。
    2. **Structural directives** — 这些指令通过添加和移除 DOM 元素来改变 DOM 布局。
    3. **Attribute directives** — 这些指令改变元素、组件或其他指令的外观或行为。

    **[⬆ 返回顶部](#目录)**

    

36. ### base href 标签的目的是什么？

    路由应用程序应该在 index.html 中的 `<head>` 标签中作为第一个子元素添加 `<base>` 元素，以指示如何组合导航 URL。如果 app 文件夹是应用程序根目录，则可以将 href 值设置为以下内容：

    ```html
    <base href="/">
    ```

    **[⬆ 返回顶部](#目录)**

    

37. ### 什么是RouterLinkActive？

    RouterLinkActive 是一个指令，根据当前 RouterState，在活动的 RouterLink 绑定上切换 CSS 类。即当此链接处于活动状态时，路由器会添加 CSS 类，当链接处于非活动状态时，它会移除。

    [点这里看在线例子](https://stackblitz.com/edit/angular-routerlinkactive?file=app%2Fapp.component.ts)

    **[⬆ 返回顶部](#目录)**

    

38. ### router events是什么？

    在每次导航期间，路由器通过 Router.events 属性发出导航事件，允许你跟踪路由的生命周期。

    路由器事件的顺序如下：

    1. NavigationStart,
    2. RouteConfigLoadStart,
    3. RouteConfigLoadEnd,
    4. RoutesRecognized,
    5. GuardsCheckStart,
    6. ChildActivationStart,
    7. ActivationStart,
    8. GuardsCheckEnd,
    9. ResolveStart,
    10. ResolveEnd,
    11. ActivationEnd
    12. ChildActivationEnd
    13. NavigationEnd,
    14. NavigationCancel,
    15. NavigationError
    16. Scroll

    **[⬆ 返回顶部](#目录)**

    

39. ### Angular中两种不同的编译模式是什么？性能差异是什么？

    1. Just-in-Time (JIT)

       即时编译（JIT）是一种在运行时在浏览器中编译应用程序的编译类型。在 Angular 8 之前，JIT 编译是默认的，现在默认是 AOT。当你运行 ng build（仅构建）或 ng serve（构建并本地提供服务）CLI 命令时，编译类型（JIT 或 AOT）取决于在 angular.json 中指定的构建配置中的 aot 属性的值。默认情况下，aot 设置为 true。

    2. Ahead-of-Time (AOT)

       预编译（AOT）是一种在构建时编译您的应用程序的编译类型。这是从 Angular 9 开始的默认值。当你运行 ng build（仅构建）或 ng serve（构建并本地提供服务）CLI 命令时，编译类型（JIT 或 AOT）取决于在 angular.json 中指定的构建配置中的 aot 属性的值。默认情况下，aot 设置为 true。

    **差异：**

    ​	在Angular中，JIT编译和AOT编译对性能的影响主要表现在应用程序的启动速度、响应速度和包的大小上。下面详细说明这两种编译方式的性能差异：

    - 启动速度：

      - **JIT**：启动速度较慢，因为浏览器需要加载Angular编译器以及应用程序本身的代码，然后在客户端实时编译模板和组件。这一过程会增加首次加载的时间。

      - **AOT**：启动速度更快，因为应用程序的模板和组件在构建阶段已被编译成有效的JavaScript代码，浏览器可以直接执行这些预编译的代码，无需等待编译过程。

    - 响应速度：

      - **JIT**：由于需要在运行时编译视图，可能会导致应用程序在运行时的响应速度稍慢。

      - **AOT**：应用程序的视图已经被预编译，因此响应速度通常更快，特别是在复杂的数据绑定和模板渲染时。

    - 包的大小：

      - **JIT**：生成的包会包含Angular的编译器，这会导致应用程序的最终体积更大。

      - **AOT**：由于不需要将Angular编译器包含在最终的JavaScript包中，因此AOT编译的结果通常会有更小的体积。

    **总结：**

    AOT编译能够提供更快的应用程序启动速度和更小的文件体积，这对于用户体验和性能优化都是有利的。在用户设备上不需要额外进行编译，这可以减少首次加载时间并提高应用的响应速度。而JIT编译则适合开发过程中，因为它能够提供快速的编译周期和灵活的调试选项。

    在生产环境中使用AOT编译是Angular官方推荐的最佳实践，因为它为最终用户提供了更好的性能。

    **[⬆ 返回顶部](#目录)**

    

40. ### 如何控制AOT编译的方式？

    您可以通过两种方式来控制应用程序的编译：

    1. 在 `tsconfig.json` 文件中提供模板编译器选项。
    2. 使用`装饰器`（@Injectable @Component等等）配置 Angular 元数据。

    **[⬆ 返回顶部](#目录)**

    

41. ### AOT有哪三个阶段？

    AOT 编译器分为三个阶段：

    1. **代码分析：** 编译器记录源代码的表示形式。
    2. **代码生成：** 处理解释并对其进行限制。
    3. **验证：** 在此阶段，Angular 模板编译器使用 TypeScript 编译器验证模板中的绑定表达式。

    **[⬆ 返回顶部](#目录)**

    

42. ### Angular中元数据 JSON 文件是什么？目的是什么？

    metadata.json 文件可以被视为装饰器元数据整体结构的图表，表示为抽象语法树（AST）。

    当您构建一个 Angular 应用时，会生成许多 `.metadata.json` 文件，这些文件包含了各个组件、指令、服务等的元数据信息。让我们以一个简单的组件为例：

    假设您有一个名为 `app.component.ts` 的组件文件，其中定义了一个简单的 Angular 组件：

    ```typescript
    import { Component } from '@angular/core';
    
    @Component({
      selector: 'app-root',
      templateUrl: './app.component.html',
      styleUrls: ['./app.component.css']
    })
    export class AppComponent {
      title = 'My App';
    }
    ```

    在构建 Angular 应用时，会生成一个 `app.component.metadata.json` 文件，其中包含了 `AppComponent` 类装饰器的元数据信息。这个 `.metadata.json` 文件可能包含类似以下内容的信息：

    ```json
    {
      "decorators": [
        {
          "type": "Component",
          "args": [
            {
              "selector": "app-root",
              "templateUrl": "./app.component.html",
              "styleUrls": [
                "./app.component.css"
              ]
            }
          ]
        }
      ]
    }
    ```

    这个 JSON 文件中描述了 `AppComponent` 类的装饰器的元数据，包括了组件的选择器、模板 URL 和样式表 URL。这些信息在构建时或运行时被 Angular 框架使用，以便正确渲染和处理组件。在分析阶段，AOT 收集器会扫描记录在 Angular 装饰器中的元数据，并将元数据信息输出到 .metadata.json 文件中，每个 .d.ts 文件对应一个文件。

    **[⬆ 返回顶部](#目录)**

    

43. ### 如何提供配置继承？

    Angular 编译器通过在 tsconfig.json 中的 angularCompilerOptions 上使用 extends 实现配置继承。即，首先加载基本文件中的配置（例如，tsconfig.base.json），然后由继承配置文件中的配置进行覆盖。

    ```json
    {
      "extends": "../tsconfig.base.json",
      "compilerOptions": {
        "experimentalDecorators": true,
        ...
      },
      "angularCompilerOptions": {
        "fullTemplateTypeCheck": true,
        "preserveWhitespaces": true,
        ...
      }
    }
    ```

    **[⬆ 返回顶部](#目录)**

    

44. ### 什么是非空断言操作符？

    在 Angular 中，非空断言操作符 `!` 用于告诉 TypeScript 编译器一个表达式的结果一定不会为 `null` 或 `undefined`。这通常用于在模板中访问对象的属性时，明确告诉编译器对象不会为空。这有助于避免 TypeScript 编译器可能产生的 "Object is possibly 'null' or 'undefined'" 错误。

    在 Angular 模板中，当你有一个对象并且确定该对象不会为 `null` 或 `undefined` 时，你可以使用非空断言操作符来访问该对象的属性。例如：

    ```html
    <div *ngIf="user">
      {{ user!.name }} <!-- 使用非空断言操作符 -->
    </div>
    ```

    在这个例子中，我们假设 `user` 对象不会为 `null` 或 `undefined`，因此我们使用 `user!.name` 来访问 `user` 对象的 `name` 属性，而不需要进行空值检查。

    **[⬆ 返回顶部](#目录)**

    

45. ### 什么是 Zone（区域）？

    在 Web 开发中，Zone（区域）是一种执行上下文的概念，用于跟踪和管理异步任务。Zone.js 是一个库，用于实现和管理 Zones 的概念。**Angular 应用程序利用 Zone.js 来管理变更检测和事件循环**。

    具体来说，Zone 可以捕获和跟踪异步任务的开始和结束，并在任务执行期间拦截和处理错误。这使得 Angular 能够在每次发生异步操作时执行变更检测，并在异步任务结束时更新视图。Zone 还提供了对事件循环的控制，使得 Angular 能够在适当的时间点执行变更检测，确保应用程序状态和视图保持同步。

    总的来说，Zone 提供了一种机制，使得 Angular 能够**感知**和响应异步操作，从而确保应用程序的稳定性和性能。

    **[⬆ 返回顶部](#目录)**

    

46. ### 什么是 Codelyzer？

    Codelyzer 提供了一组用于 Angular TypeScript 项目的静态代码分析的 tslint 规则。你可以在 Web 应用程序、NativeScript、Ionic 等上运行静态代码分析器。Angular CLI 对此提供了支持，可以像下面这样使用：

    ```bash
    ng new codelyzer
    ng lint
    ```

    **[⬆ 返回顶部](#目录)**

    

47. ### 什么是 Angular 动画？

    Angular 的动画系统是建立在 CSS 功能之上的，可以用来动画化浏览器认为可动画的任何属性。这些属性包括位置、尺寸、变换、颜色、边框等。Angular 动画模块是 **@angular/animations** 和 **@angular/platform-browser**，在使用 Angular CLI 创建项目时，这些依赖项会自动添加到你的项目中。

    **[⬆ 返回顶部](#目录)**

    

48. ### 如何在 Angular 中注入动态脚本？

    使用 DomSanitizer，我们可以注入动态的 HTML、样式、脚本和 URL。

    ```typescript
    import { Component } from '@angular/core';
    import { DomSanitizer } from '@angular/platform-browser';
    
    @Component({
      selector: 'my-app',
      template: `
        <div [innerHTML]="htmlSnippet"></div>
      `,
    })
    export class AppComponent {
      htmlSnippet: string = this.sanitizer.bypassSecurityTrustScript("<script>safeCode()</script>");
      
      constructor(protected sanitizer: DomSanitizer) {}
    }
    ```

    **[⬆ 返回顶部](#目录)**

    

49. ### 什么是 Angular Ivy？

    Angular Ivy 是 Angular 的新渲染引擎。您可以选择从 Angular 8 版本开始使用 Ivy 的预览版本。

    1. 您可以通过在 ng new 命令中使用 --enable-ivy 标志，在新项目中启用 ivy。

       ```bash
       ng new ivy-demo-app --enable-ivy
       ```

    2. 您可以通过在项目的 tsconfig.app.json 中的 angularCompilerOptions 中添加 enableIvy 选项来将其添加到现有项目中。

       ```json
       {
         "compilerOptions": { ... },
         "angularCompilerOptions": {
           "enableIvy": true
         }
       }
       ```

    **Ivy优势：**

    1. 生成的代码在运行时更易于阅读和调试
    2. 更快的重新构建时间
    3. 改进的载荷大小
    4. 改进的模板类型检查

    **[⬆ 返回顶部](#目录)**

    

50. ### Angular 中有哪些命名规则类型？

    1. **驼峰命名法（camelCase）**：
       - 符号、属性、方法： `selectedUser`, `firstName`, `getUserById()`
       - 管道名称： `truncateText`, `formatDate`
       - 非组件指令选择器： `appHeader`, `appFooter`
       - 常量： `maxItemCount`, `apiBaseUrl`
    2. **大驼峰命名法（PascalCase）**：
       - 类名： `AppComponent`, `UserService`, `ProductDetailComponent`
       - 定义组件、接口、NgModules、指令和管道的类： `UserListComponent`, `ProductService`
    3. **短划线命名法（kebab-case）**：
       - 文件名的描述性部分： `app.component.ts`, `user-list.component.html`, `product-detail.component.css`
       - 组件选择器： `<app-header>`, `<app-footer>`, `<user-list>`
    4. **大写下划线命名法**：
       - 常量： `MAX_NUMBER_OF_USERS`, `DEFAULT_API_BASE_URL`, `PI_VALUE`

    **[⬆ 返回顶部](#目录)**

    

51. ### Angular的DSL是什么？

    领域特定语言（DSL）是专门针对特定应用领域的计算机语言。Angular 有自己的领域特定语言（DSL），它允许我们在普通 HTML 之上编写 Angular 特定的类似 HTML 的语法。它有自己的编译器，用于将此语法编译为浏览器能够理解的 HTML。此 DSL 在 NgModules 中定义，例如动画、表单和路由导航。

    1. `()`：用于输出和 DOM 事件。
    2. `[]`：用于输入和特定的 DOM 元素属性。
    3. `*`：结构指令（*ngFor 或 *ngIf）将影响/更改 DOM 结构。、

    **[⬆ 返回顶部](#目录)**

    

52. ### 什么是 Angular 中的 RxJS 的 Subject？

    RxJS（Subject）是一种特殊类型的 Observable，它允许值被多播到许多观察者。而普通的 Observables 是单播的（每个订阅的观察者都拥有一个独立的 Observable 执行），主题（Subject）是多播的。

    Subject类似于 Observable，但可以向许多观察者进行多播。主题（Subject）类似于 EventEmitter：它们维护一个许多监听器的注册表。

    **Observable：**

    - **基础构建块**：`Observable` 是 RxJS 中定义和处理数据流的核心概念。它代表了可随时间推送值的数据流。
    - **单播**：`Observable` 是单播的，这意味着每个订阅者都会获得对数据流的独立执行。每次调用 `.subscribe()` 方法时，都会创建一个新的执行环境。
    - **只是数据生产者**：`Observable` 仅负责数据的产出，它不持有状态，不分享执行上下文。

    **Subject：**

    - **多播**：`Subject` 是多播的，也就是说它可以共享单个执行环境给多个订阅者。因此，使用 `Subject`，每个订阅者都会接收到相同的数据流。
    - **既是数据生产者，也是数据消费者**：`Subject` 可以发出新的值，这使其可以作为数据的生产者。同时，它也能够被订阅，充当数据的消费者。
    - **持有状态**：`Subject` 能够通过 `.next()` 方法持有并发送新的值，这种特性使得它可以在多个订阅者之间广播值。

    **[⬆ 返回顶部](#目录)**

    

53. ### 单播和多播的区别是什么？

    让我们通过一个简单的例子来说明单播（Unicast）和多播（Multicast）的区别。首先是单播的例子，我们使用 `Observable` 来创建一个单播数据流：

    **单播（Unicast）示例：**

    ```javascript
    import { Observable } from 'rxjs';
    
    // 创建一个Observable对象
    const unicastObservable = new Observable(subscriber => {
      // 模拟网络请求
      setTimeout(() => {
        subscriber.next(Math.random()); // 发送一个随机数
        subscriber.complete();
      }, 1000);
    });
    
    // 第一个订阅者
    unicastObservable.subscribe(value => {
      console.log(`订阅者1收到的值: ${value}`);
    });
    
    // 第二个订阅者，稍后订阅
    setTimeout(() => {
      unicastObservable.subscribe(value => {
        console.log(`订阅者2收到的值: ${value}`);
      });
    }, 1500);
    ```

    在上面的例子中，每个订阅者都会收到一个不同的随机数，因为每次调用 `subscribe` 方法都会触发 `Observable` 的新执行，导致每个订阅者收到的数据流是独立的。

    **多播（Multicast）示例：**

    ```javascript
    import { Subject } from 'rxjs';
    
    // 创建一个Subject对象
    const multicastSubject = new Subject();
    
    // 第一个订阅者
    multicastSubject.subscribe(value => {
      console.log(`订阅者1收到的值: ${value}`);
    });
    
    // 第二个订阅者
    multicastSubject.subscribe(value => {
      console.log(`订阅者2收到的值: ${value}`);
    });
    
    // 模拟网络请求，并发出一个随机数
    setTimeout(() => {
      multicastSubject.next(Math.random());
      multicastSubject.complete();
    }, 1000);
    ```

    在多播的例子中，使用 `Subject` 对象时，不管有多少订阅者，当我们通过 `.next()` 发送数据时，所有的订阅者都会收到相同的数据。这就是多播的行为，`Subject` 共享了数据流给所有的订阅者。

    这两个例子清晰地展示了单播和多播的不同行为。在单播中，每次订阅都获得独立的数据流；而在多播中，所有的订阅者共享同一个数据流。

    **[⬆ 返回顶部](#目录)**

    

54. ### 什么是 Bazel 工具？

    Bazel 是一个强大的构建工具，由 Google 开发并广泛使用，它可以跟踪不同包和构建目标之间的依赖关系。在 Angular8 中，你可以使用 Bazel 来构建你的 CLI 应用程序。 **注意：** Angular 框架本身就是使用 Bazel 构建的。

    **[⬆ 返回顶部](#目录)**

    

55. ### 如何在 Angular 中检测路由变化？

    在 Angular7 中，你可以订阅路由事件来检测变化。订阅路由事件的方式如下：

    ```javascript
    this.router.events.subscribe((event: Event) => {})
    ```

    让我们来看一个简单的组件来检测路由变化：

    ```javascript
    import { Component } from '@angular/core';
    import { Router, Event, NavigationStart, NavigationEnd, NavigationError } from '@angular/router';
    
    @Component({
        selector: 'app-root',
        template: `<router-outlet></router-outlet>`
    })
    export class AppComponent {
    
        constructor(private router: Router) {
    
            this.router.events.subscribe((event: Event) => {
                if (event instanceof NavigationStart) {
                    // 显示加载指示器并执行操作
                }
    
                if (event instanceof NavigationEnd) {
                    // 隐藏加载指示器并执行操作
                }
    
                if (event instanceof NavigationError) {
                    // 隐藏加载指示器并执行操作
                    console.log(event.error); // 用于调试的错误日志
                }
            });
       }
    }
    ```

    **[⬆ 返回顶部](#目录)**

    

56. ### 如何为 HTTP 客户端传递标头？

    你可以直接传递对象映射给 http 客户端，或者创建 HttpHeaders 类来提供标头。

    ```javascript
    constructor(private _http: HttpClient) {}
    this._http.get('someUrl',{
       headers: {'header1':'value1','header2':'value2'}
    });
    
    (or)
    let headers = new HttpHeaders().set('header1', headerValue1); // 创建标头对象
    headers = headers.append('header2', headerValue2); // 添加一个新标头，创建一个新对象
    headers = headers.append('header3', headerValue3); // 再添加一个标头
    
    let params = new HttpParams().set('param1', value1); // 创建参数对象
    params = params.append('param2', value2); // 添加一个新参数，创建一个新对象
    params = params.append('param3', value3); // 再添加一个参数
    
    return this._http.get<any[]>('someUrl', { headers: headers, params: params })
    ```

    **[⬆ 返回顶部](#目录)**

    

57. ### Angular 支持动态导入吗？

    ```javascript
    {path: ‘user’, loadChildren: () => import('./users/user.module').then(m => m.UserModule)};
    ```

    **[⬆ 返回顶部](#目录)**

    

58. ### 什么是懒加载？
    懒加载是 Angular 路由中最有用的概念之一。它帮助我们将网页以块的方式下载，而不是一次性下载所有内容。它通过异步加载特性模块来实现懒加载，每当需要路由时就加载。我们可以按以下方式懒加载 `Customer` 和 `Order` 特性模块：
    ```javascript
    const routes: Routes = [
      {
        path: 'customers',
        loadChildren: () => import('./customers/customers.module').then(module => module.CustomersModule)
      },
      {
        path: 'orders',
        loadChildren: () => import('./orders/orders.module').then(module => module.OrdersModule)
      },
      {
        path: '',
        redirectTo: '',
        pathMatch: 'full'
      }
    ];
    ```

    **[⬆ 返回顶部](#目录)**

    

59. ### 什么是workspace APIs？

    Angular 8.0 版本引入了工作区 API，以使开发人员更轻松地读取和修改 angular.json 文件，而不是手动修改它。当前，唯一支持的存储格式是 Angular CLI 使用的基于 JSON 的格式。您可以按以下方式启用或添加构建目标的优化选项：

    ```javascript
    import { NodeJsSyncHost } from '@angular-devkit/core/node';
    import { workspaces } from '@angular-devkit/core';
    
    async function addBuildTargetOption() {
        const host = workspaces.createWorkspaceHost(new NodeJsSyncHost());
        const workspace = await workspaces.readWorkspace('path/to/workspace/directory/', host);
    
        const project = workspace.projects.get('my-app');
        if (!project) {
          throw new Error('my-app 不存在');
        }
    
        const buildTarget = project.targets.get('build');
        if (!buildTarget) {
          throw new Error('构建目标不存在');
        }
    
        buildTarget.options.optimization = true;
    
        await workspaces.writeWorkspace(workspace, host);
    }
    
    addBuildTargetOption();
    ```

    - 首先，我们导入了 `NodeJsSyncHost` 和 `workspaces` 模块，它们是 Angular 工作区 API 的一部分。
    - 然后，我们创建了一个异步函数 `addBuildTargetOption()`，用于向构建目标添加优化选项。
    - 在函数内部，我们创建了一个工作区主机实例，并使用 `readWorkspace()` 方法读取工作区。您需要将工作区的路径作为参数传递给 `readWorkspace()` 方法。
    - 接下来，我们获取了名为 `my-app` 的项目，并检查它是否存在。如果项目不存在，则抛出错误。
    - 然后，我们获取了构建目标，并检查它是否存在。如果构建目标不存在，则抛出错误。
    - 最后，我们将 `optimization` 选项设置为 `true`，表示启用了优化。
    - 最后，我们使用 `writeWorkspace()` 方法将更新后的工作区写回到 `angular.json` 文件中。

    这段代码允许您通过编程方式修改 Angular 项目的配置，而无需手动编辑 `angular.json` 文件。

    **[⬆ 返回顶部](#目录)**

    

60. ### Angular怎么升级版本？

    参考官方升级文档(#https://update.angular.io/)

    ```cmd
    $ ng update @angular/cli @angular/core
    ```

    **[⬆ 返回顶部](#目录)**

    

61. ### 如何使用 CLI 测试 Angular 应用程序？

    Angular CLI 会使用 Jasmine 测试框架下载并安装所需的一切。你只需要运行 `ng test` 来查看测试结果。默认情况下，此命令会在观察模式下构建应用程序，并启动 `Karma 测试运行器`。测试结果的输出如下，

    ```bash
    10% building modules 1/1 modules 0 active
    ...INFO [karma]: Karma v1.7.1 server started at http://0.0.0.0:9876/
    ...INFO [launcher]: Launching browser Chrome ...
    ...INFO [launcher]: Starting browser Chrome
    ...INFO [Chrome ...]: Connected on socket ...
    Chrome ...: Executed 3 of 3 SUCCESS (0.135 secs / 0.205 secs)
    ```

    **注意：** Chrome 浏览器也会打开，并在 "Jasmine HTML Reporter" 中显示测试输出。

    **[⬆ 返回顶部](#目录)**

    

62. ### 如何在 Angular 应用程序中使用 polyfills？

    Angular CLI 官方提供了对 polyfills 的支持。当你使用 ng new 命令创建新项目时，会在项目文件夹中创建一个 `src/polyfills.ts` 配置文件。该文件包含了必需的和许多可选的 polyfills 作为 JavaScript import 语句。让我们将 polyfills 分类，

    1. **必需的 polyfills：** 在使用 ng new 命令创建项目时会自动安装这些 polyfills，并在 'src/polyfills.ts' 文件中启用相应的导入语句。
    2. **可选的 polyfills：** 你需要安装它的 npm 包，然后在 'src/polyfills.ts' 文件中创建导入语句。 例如，首先你需要安装以下 npm 包以添加 web 动画（可选）polyfill。 `bash npm install --save web-animations-js `然后在 polyfill 文件中创建导入语句。 `javascript import 'web-animations-js';`

    **[⬆ 返回顶部](#目录)**

    

63. ### 触发 Angular 中变更检测的方式有哪些？

    你可以将 ApplicationRef、NgZone 或 ChangeDetectorRef 注入到你的组件中，并应用以下特定方法来触发 Angular 中的变更检测。也就是说，有 3 种可能的方式：

    1. **ApplicationRef.tick():** 调用此方法来显式处理变更检测及其副作用。它会检查整个组件树。
    2. **NgZone.run(callback):** 它在 Angular 区域内评估回调函数。
    3. **ChangeDetectorRef.detectChanges():** 它仅检测组件及其子组件。

    **[⬆ 返回顶部](#目录)**

    

64. ### Angular 的各个版本有什么区别？

    Angular 框架有不同的版本。让我们看看各个版本的特性，

    1. Angular 1:

       - Angular 1（AngularJS）是于 2010 年发布的第一个 Angular 框架。
       - AngularJS 不适用于移动设备。
       - 它基于具有 MVC 架构的控制器。

    2. Angular 2:

       - Angular 2 于 2016 年发布。Angular 2 是 Angular1 版本的完全重写。
       - Angular 2 解决了 Angular 1 版本存在的性能问题。
       - Angular 2 从头开始为移动设备构建。
       - Angular 2 是基于组件的。

    3. Angular 3:

       - Angular 2 中有不同的包版本：
         - @angular/core v2.3.0
         - @angular/compiler v2.3.0
         - @angular/http v2.3.0
         - @angular/router v3.3.0
       - 路由器包已经版本化为 3，为了避免混淆，跳过了 3 版本，直接切换到 Angular 4 版本。

    4. Angular 4:

       - AOT 模式下编译器生成的代码文件大小大大减少。
       - Angular 4 中的生产包大小减少了数百 KB。
       - 动画功能从 angular/core 中删除，并形成了一个单独的包。
       - 支持 TypeScript 2.1 和 2.2。
       - Angular Universal
       - 新的 HttpClient

    5. Angular 5:

       - Angular 5 使 Angular 更快。它改进了加载时间和执行时间。
       - 附带了新的构建优化器。
       - 支持 TypeScript 2.5。
       - Service Worker

    6. Angular 6:

       - 它于 2018 年 5 月发布。
       - 包括 Angular 命令行界面（CLI）、组件开发工具包（CDK）、Angular 材料包和 Angular 元素。
       - Service Worker 问题修复。
       - 国际化（i18n）
       - Ivy 的实验模式。
       - RxJS 6.0
       - 树摇（Tree Shaking）

    7. Angular 7:

       - 它于 2018 年 10 月发布。
       - TypeScript 3.1
       - RxJS 6.3
       - 新的 Angular CLI
       - CLI 提示功能提供了在用户运行之前向用户询问问题的能力。它类似于用户和 CLI 之间的交互式对话。
       - 借助改进的 CLI 提示功能，开发人员可以做出决策。新的 ng 命令在询问用户路由和 CSS 样式类型（SCSS）以及 ng add @angular/material 在询问主题、手势或动画。

    8. Angular 8:

       - 它于 2019 年 5 月发布。
       - TypeScript 3.4

    9. Angular 9:

       - 它于 2020 年 2 月发布。
       - TypeScript 3.7
       - 默认启用 Ivy

    10. Angular 10:

        - 它于 2020 年 6 月发布。
        - TypeScript 3.9
        - TSlib 2.0

    11. Angular 11:

        - 发布于 2020 年 11 月。
        - 改进了 Angular 的构建和部署速度。
        - 更好的组件测试速度和质量。
        - 支持 TypeScript 4.0。
        - 更新了对 Webpack 5 的实验性支持。
        - 引入了自动内联字体的功能。

    12. Angular 12:

        - 发布于 2021 年 5 月。
        - 正式废弃了对 IE11 的支持。
        - 支持 TypeScript 4.2。
        - 引入了对 Webpack 5 的稳定支持。
        - 为了简化 API，对表单验证有所优化。
        - Nullish Coalescing 的支持在模板中添加。

    13. Angular 13:

        - 发布于 2021 年 11 月。
        - 支持 TypeScript 4.4。
        - Ivy 库的全面采用，不再支持 View Engine。
        - 更简单的 Angular Package Format (APF)，以简化第三方库的构建和发布。
        - RxJS 7.4 默认支持，提高性能和更小的打包体积。
        - 改进了对严格模式的支持。

    14. Angular 14:

        - 发布于 2022 年 6 月。
        - 引入了独立的组件，无需 Angular 模块即可使用。
        - 支持类型化的表单，增强了静态类型检查。
        - 改进了开发者诊断和错误消息。
        - 支持 TypeScript 4.7。
        - 加强了对宽松模式的支持，使得严格模式下的迁移更容易。

    15. Angular 15:

        - 发布于 2022 年 11 月。
        - 继续改进了性能和开发体验。
        - 引入了新的特性和 API 改进。
        - 更好的路由功能和开发者工具。
        - 更新了对最新 JavaScript 和 TypeScript 特性的支持。

        **[⬆ 返回顶部](#目录)**

    

65. ### Angular 中的安全原则是什么？

    下面是 Angular 中的安全原则列表，

    1. 应避免直接使用 DOM API。
    2. 应启用内容安全策略 (CSP) 并配置您的 Web 服务器以返回适当的 CSP HTTP 标头。
    3. 应使用离线模板编译器。
    4. 应使用服务器端 XSS 保护。
    5. 应使用 DOM Sanitizer。
    6. 应防止 CSRF 或 XSRF 攻击。

    **[⬆ 返回顶部](#目录)**

    

66. ### Angular 针对预防 XSS 攻击的安全模型是什么？

    Angular 默认将所有值视为不受信任。也就是说，当从模板中插入值到 DOM 时，通过属性、属性绑定、样式绑定或插值等方式，Angular 会对不受信任的值进行消毒和转义。

    **[⬆ 返回顶部](#目录)**

    

67. ### 模板编译器(AOT)在预防 XSS 攻击中的作用是什么？

    离线模板编译器可以防止模板注入导致的漏洞，并极大提高了应用程序的性能。因此，建议在生产部署中使用离线模板编译器，不要动态生成任何模板。

    **[⬆ 返回顶部](#目录)**

    

68. ### 什么是Sanitization（消毒）？Angular是否支持它？

    **Sanitization（消毒）** 是对不受信任的值进行检查，将其转换为可以安全插入DOM的值。是的，Angular支持消毒。它会为HTML、样式和URL对不受信任的值进行消毒，但无法对包含任意代码的资源URL进行消毒。

    **[⬆ 返回顶部](#目录)**

    

69. ### 插值内容和innerHTML之间有什么区别？

    插值内容和innerHTML代码的主要区别在于代码解释的行为。

    **插值内容始终会被转义，即HTML不会被解释，浏览器会在元素的文本内容中显示角括号。**

    而在innerHTML绑定中，内容会被解释，即浏览器会将< and >字符转换为HTML实体。例如，模板中的用法如下：

    ```html
    <p>Interpolated value:</p>
    <div >{{htmlSnippet}}</div>
    <p>Binding of innerHTML:</p>
    <div [innerHTML]="htmlSnippet"></div>
    ```

    以及组件中定义的属性。

    ```javascript
    export class InnerHtmlBindingComponent {
        htmlSnippet = 'Template <script>alert("XSS Attack")</script> <b>Code attached</b>';
    }
    ```

    即使innerHTML绑定存在XSS攻击的可能性，但Angular将该值识别为不安全，并自动对其进行消毒处理。

    **[⬆ 返回顶部](#目录)**

    

70. ### 如何防止自动消毒？

    1. 注入DomSanitizer：您可以将DomSanitizer作为构造函数中的参数注入组件。

    2. 调用以下某些方法标记可信值

       - bypassSecurityTrustHtml

       - bypassSecurityTrustScript

       - bypassSecurityTrustStyle

       - bypassSecurityTrustUrl

       - bypassSecurityTrustResourceUrl

    **[⬆ 返回顶部](#目录)**

    

71. ### Angular是否能防止HTTP级别的漏洞？

    Angular内置支持防止诸如跨站请求伪造（CSRF或XSRF）和跨站脚本包含（XSSI）等HTTP级别漏洞。尽管这些漏洞需要在服务器端进行缓解，但Angular提供了辅助工具，使客户端集成更容易。

    1. HttpClient支持令牌机制，用于防止XSRF攻击。

       当使用Angular的HttpClient进行HTTP通信时，可以通过以下方式使用令牌机制来防止XSRF攻击：

       假设服务器在每次用户会话期间生成一个名为 `csrfToken` 的令牌，并将其包含在响应的HTTP头部中。客户端在发出请求时，需要将这个令牌作为请求的一部分发送给服务器。

       下面是一个示例代码片段，演示了如何使用HttpClient发送带有XSRF令牌的POST请求：

       ```typescript
       import { HttpClient, HttpHeaders } from '@angular/common/http';
       
       @Injectable()
       export class MyDataService {
         constructor(private http: HttpClient) {}
       
         postData(data: any): Observable<any> {
           // 假设从服务器获取的XSRF令牌存储在cookie或者local storage中
           const xsrfToken = localStorage.getItem('csrfToken');
       
           // 设置请求头部，包含XSRF令牌
           const headers = new HttpHeaders({
             'Content-Type': 'application/json',
             'X-XSRF-TOKEN': xsrfToken  // 在请求头中添加XSRF令牌
           });
       
           // 发送POST请求
           return this.http.post<any>('https://example.com/api/data', data, { headers });
         }
       }
       ```

    2. HttpClient库识别了带有前缀JSON响应的约定（其中包含非可执行的js代码和 ")]}',\n" 字符），并在进一步解析之前自动从所有响应中剥离字符串 ")]}',\n" 。

       演示代码片段：

       ```json
       )]}',
       {
         "id": 1,
         "name": "John Doe"
       }
       ```

       会自动剥离

    **[⬆ 返回顶部](#目录)**

    

72. ### 什么是HTTP拦截器？

    HTTP拦截器是@angular/common/http的一部分，它检查并转换您的应用程序发送到服务器的HTTP请求，以及HTTP响应。这些拦截器可以执行各种隐式任务，从身份验证到日志记录。

    HttpInterceptor接口的语法如下所示，

    ```typescript
    interface HttpInterceptor {
      intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>>
    }
    ```

    您可以通过声明实现HttpInterceptor接口的intercept()方法的服务类来使用拦截器。

    ```typescript
    @Injectable()
    export class MyInterceptor implements HttpInterceptor {
        constructor() {}
        intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
            ...
        }
    }
    ```

    然后，您可以在您的模块中使用它，

    ```typescript
    @NgModule({
        ...
        providers: [
            {
                provide: HTTP_INTERCEPTORS,
                useClass: MyInterceptor,
                multi: true
            }
        ]
        ...
    })
    export class AppModule {}
    ```

    **[⬆ 返回顶部](#目录)**

    

73. ### HTTP拦截器的应用有哪些？

    HTTP拦截器可以用于各种任务，

    1. 身份验证
    2. 日志记录
    3. 缓存
    4. 伪造后端
    5. URL转换
    6. 修改标头

    **[⬆ 返回顶部](#目录)**

    

74. ### Angular是否支持多个拦截器？

    是的，Angular支持同时使用多个拦截器。您可以在providers属性中定义多个拦截器：

    ```typescript
    providers: [
      { provide: HTTP_INTERCEPTORS, useClass: MyFirstInterceptor, multi: true },
      { provide: HTTP_INTERCEPTORS, useClass: MySecondInterceptor, multi: true }
    ],
    ```

    拦截器将按提供的顺序调用。即，在上述拦截器配置中，MyFirstInterceptor将首先被调用。

    **[⬆ 返回顶部](#目录)**

    

75. ### Angular如何简化国际化？

    Angular简化了以下国际化方面的处理：

    1. 以本地格式显示日期、数字、百分比和货币。
    2. 为组件模板中的文本进行翻译准备。
    3. 处理单词的复数形式。
    4. 处理备用文本。

    **[⬆ 返回顶部](#目录)**

    

76. ### 如何手动注册区域数据？

    默认情况下，Angular只包含了en-US（美国英语）的区域数据。但如果你想设置其他区域，你必须导入该新区域的区域数据。之后，你可以使用 `registerLocaleData` 方法注册它，该方法的语法如下所示：

    ```typescript
    registerLocaleData(data: any, localeId?: any, extraData?: any): void
    ```

    例如，让我们导入德语区域数据并在应用程序中注册它：

    ```typescript
    import { registerLocaleData } from '@angular/common';
    import localeDe from '@angular/common/locales/de';
    
    registerLocaleData(localeDe, 'de');
    ```

    **[⬆ 返回顶部](#目录)**

    

77. ### ngIf和hidden属性之间的区别是什么？

    主要区别在于*ngIf会从DOM中移除元素，而[hidden]实际上通过设置`display:none`来操纵CSS样式。通常在频繁的操作中，向DOM中添加和移除元素是比较昂贵的。

    1. **隐藏方式：**
       - `hidden` 属性：隐藏元素是通过在DOM中保留元素的位置并设置其 `display` 属性为 `none` 来实现的。这意味着元素在DOM中仍然存在，只是不可见。
       - `ngIf` 指令：隐藏元素是通过从DOM中完全移除元素来实现的。这意味着当 `ngIf` 的条件为假时，元素将从DOM中移除，不再存在于DOM树中。
    2. **性能：**
       - `hidden` 属性：即使元素被隐藏，但它仍然存在于DOM中，可能会影响性能，尤其是在处理大量隐藏元素时。
       - `ngIf` 指令：当条件为假时，元素将从DOM中移除，因此不会影响性能。
    3. **应用场景：**
       - `hidden` 属性：适用于当元素需要在页面上保留位置，但在某些条件下需要隐藏时，比如根据用户权限隐藏某些功能。
       - `ngIf` 指令：适用于当元素在某些条件下需要完全移除时，比如根据用户登录状态显示不同的视图。

    **[⬆ 返回顶部](#目录)**

    

78. ### ngFor 的 trackBy 属性的目的是什么？

    使用 *ngFor 和 trackBy 选项的主要目的是性能优化。通常，如果你使用 NgFor 处理大型数据集，对一个项目进行小的更改（删除或添加一个项目）可能会触发一系列 DOM 操作。在这种情况下，Angular 只会看到一组新的对象引用，然后用所有新的 DOM 元素替换旧的 DOM 元素。通过提供一个 `trackBy` 函数，你可以帮助 Angular 跟踪添加或删除的项目，该函数接受索引和当前项目作为参数，并需要返回该项目的唯一标识符。

    假设你有一个待办事项（todo）的列表，每个待办事项都有一个唯一的标识符（ID）和一个名称。

    ```typescript
    interface Todo {
      id: number;
      name: string;
    }
    
    @Component({
      selector: 'todo-list',
      template: `
        <div *ngFor="let todo of todos; trackBy: trackByTodos">
          ({{ todo.id }}) {{ todo.name }}
        </div>
      `
    })
    export class TodoListComponent {
      todos: Todo[] = [
        { id: 1, name: '完成 Angular 项目' },
        { id: 2, name: '学习 TypeScript' },
        { id: 3, name: '阅读一本好书' }
      ];
    
      trackByTodos(index: number, item: Todo): number {
        return item.id;
      }
    }
    ```

    在这个组件中，我们有一个 `todos` 数组，其中包含了几个待办事项。组件的模板使用 *ngFor 指令来循环遍历 `todos` 数组中的每个待办事项，并为每个待办事项显示其 ID 和名称。

    这里有几个要点：

    1. `*ngFor` 指令会循环遍历 `todos` 数组，并为数组中的每个元素生成一个 div 元素。
    2. `trackBy: trackByTodos` 部分告诉 Angular 使用 `trackByTodos` 方法来跟踪循环的每个元素。
    3. `trackByTodos` 方法接收两个参数：`index` 表示当前元素在数组中的索引，`item` 表示当前循环的元素。该方法返回当前待办事项的唯一标识符，这里我们选择使用每个待办事项的 ID 作为标识符。
    4. 当数据发生变化时，Angular 使用 `trackBy` 函数来比较新数据和旧数据，以确定哪些元素发生了变化，从而减少 DOM 更新的数量，提高性能。

    总的来说，这段代码实现了一个简单的待办事项列表组件，并使用 `trackBy` 函数来优化性能，以避免在数据更新时重新渲染整个列表。

    **[⬆ 返回顶部](#目录)**

    

79. ### ngSwitch指令的目的是什么？

    **ngSwitch** 指令类似于 JavaScript 的 switch 语句，根据一个条件切换来显示多个可能的元素中的一个。在这种情况下，只有选定的元素放置到 DOM 中。它通常与 `NgSwitch`、`NgSwitchCase` 和 `NgSwitchDefault` 指令一起使用。

    例如，让我们使用 ngSwitch 指令根据选择的浏览器显示浏览器详情。

    ```html
    <div [ngSwitch]="currentBrowser.name">
      <chrome-browser    *ngSwitchCase="'chrome'"    [item]="currentBrowser"></chrome-browser>
      <firefox-browser   *ngSwitchCase="'firefox'"     [item]="currentBrowser"></firefox-browser>
      <opera-browser     *ngSwitchCase="'opera'"  [item]="currentBrowser"></opera-browser>
      <safari-browser     *ngSwitchCase="'safari'"   [item]="currentBrowser"></safari-browser>
      <ie-browser  *ngSwitchDefault           [item]="currentItem"></ie-browser>
    </div>
    ```

    **[⬆ 返回顶部](#目录)**

    

80. ### 什么是安全导航运算符？

    安全导航运算符（?）（也称为 Elvis 运算符）用于在属性路径中防止 `null` 和 `undefined` 值，当您不确定路径是否存在时。即，如果对象路径存在，则返回该路径的值，否则返回 null 值。

    例如，您可以轻松访问用户配置文件的嵌套属性，而不会出现空引用错误，如下所示：

    ```html
    <p>用户的 firstName 是：{{user?.fullName.firstName}}</p>
    ```

    使用这个安全导航运算符，Angular 框架在第一个空值出现时停止评估表达式，并在没有任何错误的情况下渲染视图。

    **[⬆ 返回顶部](#目录)**

    

81. ### 什么是入口组件？

    入口组件是 Angular 根据类型在 imperative 方式下加载的任何组件（即，在模板中没有引用的组件）。由于这种行为，它们在编译过程中无法被 Angular 编译器找到。这些组件是通过 `ComponentFactoryResolver` 动态创建的。

    基本上，有两种主要类型的入口组件，分别是

    1. 在路由中指定的引导根组件
    2. 通过路由加载的组件

    **[⬆ 返回顶部](#目录)**

    

82. ### 什么是引导组件？

    引导组件是在启动过程或应用程序启动时由 Angular 加载到 DOM 中的入口组件。通常，这个引导或根组件在根模块中使用 `bootstrap` 属性命名为 `AppComponent`：

    ```typescript
    @NgModule({
      declarations: [
        AppComponent
      ],
      imports: [
        BrowserModule,
        FormsModule,
        HttpClientModule,
        AppRoutingModule
      ],
      providers: [],
      bootstrap: [AppComponent] // 需要在此处声明引导的入口组件
    })
    ```

    **[⬆ 返回顶部](#目录)**

    

83. ### 什么是路由入口组件？

    在路由配置中引用的组件称为路由入口组件。在路由定义中，将这些路由入口组件定义如下：

    ```typescript
    const routes: Routes = [
      {
        path: '',
        component: TodoListComponent // 路由入口组件
      }
    ];
    ```

    **[⬆ 返回顶部](#目录)**

    

84. ### 什么是 Angular 编译器？

    Angular 编译器用于将应用程序代码转换为 JavaScript 代码。它读取模板标记，将其与相应的组件类代码组合，并发出组件工厂，该工厂创建组件的 JavaScript 表示以及 @Component 元数据的元素。

    **[⬆ 返回顶部](#目录)**

    

85. ### ngModule 元数据在编译过程中的作用是什么？

    `@NgModule` 元数据用于告诉 Angular 编译器应该为该模块编译哪些组件，并且如何将此模块与其他模块链接。

    **[⬆ 返回顶部](#目录)**

    

86. ### 什么是特性模块？

    特性模块是用于组织代码的 NgModules。可以使用 Angular CLI 在根目录中使用以下命令创建特性模块：

    ```cmd
    ng generate module MyCustomFeature
    ```

    Angular CLI 将在根目录中创建一个名为 `my-custom-feature` 的文件夹，并在其中创建一个名为 `my-custom-feature.module.ts` 的文件，内容如下：

    ```typescript
    import { NgModule } from '@angular/core';
    import { CommonModule } from '@angular/common';
    
    @NgModule({
      imports: [
        CommonModule
      ],
      declarations: []
    })
    export class MyCustomFeature { }
    ```

    **注意：** 名称中不应该包含 "Module" 后缀，因为 CLI 会自动添加它。

    **[⬆ 返回顶部](#目录)**

    

87. ### 如果在特性模块中使用 BrowserModule 会发生什么？

    如果将 `BrowserModule` 导入到延迟加载的特性模块中，则 Angular 会返回错误消息，告诉您使用 `CommonModule` 替代。因为 BrowserModule 的提供者适用于整个应用程序，所以它只应该在根模块中使用，而不是在特性模块中。特性模块只需要 CommonModule 中的常见指令。

    **[⬆ 返回顶部](#目录)**

    

88. ### 特性模块的类型有哪些？

    以下是特性模块的五种类型：

    1. **领域模块：** 专门为特定应用领域提供用户体验（例如，下订单、注册等）。
    2. **路由模块：** 这些是领域特性模块，其顶级组件是路由导航路由的目标。
    3. **路由配置模块：** 为其他模块提供路由配置。
    4. **服务模块：** 提供实用服务，如数据访问和消息传递（例如，HttpClientModule）。
    5. **小部件模块：** 将组件、指令和管道提供给外部模块（例如，Material UI 等第三方库）。

    **[⬆ 返回顶部](#目录)**

    

89. ### 什么是提供者（Provider）？

    提供者是对依赖注入系统的一条指令，用于告诉系统如何获取依赖项的值（也就是创建的服务）。你可以使用 Angular CLI 提供服务，例如：

    ```cmd
    ng generate service my-service
    ```

    Angular CLI 创建的服务如下所示：

    ```typescript
    import { Injectable } from '@angular/core';
    
    @Injectable({
      providedIn: 'root', //Angular 在根注入器中提供服务
    })
    export class MyService {
    }
    ```

    **[⬆ 返回顶部](#目录)**

    

90. ### 对提供者的作用域有何推荐？

    除非有特定的情况需要，否则应该始终将服务提供给根注入器。除此之外，你还可以选择将服务提供给特定模块。

    **[⬆ 返回顶部](#目录)**

    

91. ### 如何将提供者作用域限制在一个模块内？

    可以通过以下两种方式将服务提供者的作用域限制在特定模块内：

    1. 在服务的 @Injectable() 装饰器中设置 providedIn 属性。

       ```typescript
       import { Injectable } from '@angular/core';
       
       @Injectable({
         providedIn: 'root' // 或者指定其他模块，如 'MyModule'
       })
       export class MyService {
         constructor() { }
       }
       ```

    2. 在模块的 providers 数组中声明服务。

       ```typescript
       import { NgModule } from '@angular/core';
       import { MyService } from './my.service';
       
       @NgModule({
         providers: [MyService] // 在 providers 数组中提供 MyService
       })
       export class MyModule { }
       ```

       **[⬆ 返回顶部](#目录)**

    

92. ### 如何提供一个单例服务？

    有两种常见的方法来提供一个单例服务。

    1. 将 @Injectable() 的 providedIn 属性设置为 "root"。这是创建单例服务的首选方式（从 Angular 6.0 开始），因为它使你的服务可被树摇晃（tree-shakable）。

       ```typescript
       import { Injectable } from '@angular/core';
       
       @Injectable({
         providedIn: 'root',
       })
       export class MyService {
       }
       ```

    2. 将服务包含在根模块或仅由根模块导入的模块中。

       ```typescript
       @NgModule({
         ...
         providers: [MyService],
         ...
       })
       ```

    **[⬆ 返回顶部](#目录)**

    

93. ### 有哪些消除重复Service注册的不同方法？

    如果一个模块同时定义了提供商（provides）和声明（declarations），那么在多个特性模块中加载该模块将导致服务的注册重复。以下是消除此重复行为的不同方法。

    1. 使用providedIn语法，而不是在模块中注册服务。
    2. 将服务分离到它们自己的模块中。
    3. 在模块中定义forRoot()和forChild()方法。

    **[⬆ 返回顶部](#目录)**

    

94. ### forRoot方法如何帮助避免重复的路由实例？

    如果`RouterModule`模块没有forRoot()静态方法，那么每个特性模块都会实例化一个新的路由器实例，这会导致应用程序出现问题，因为会存在重复的实例。使用forRoot()方法后，根应用程序模块导入`RouterModule.forRoot(...)`并获取一个路由器实例，所有特性模块导入`RouterModule.forChild(...)`，这样就不会实例化另一个路由器。

    **[⬆ 返回顶部](#目录)**

    

95. ### 什么是shared共享模块？

    共享模块是一个模块，您可以在其中将常用的指令、管道和组件放入一个模块中，并在整个应用程序中共享（导入它）。

    例如，下面的共享模块根据需要导入了CommonModule、FormsModule用于常见的指令和组件，以及基于需要的管道和指令。

    ```typescript
    import { CommonModule } from '@angular/common';
    import { NgModule } from '@angular/core';
    import { FormsModule } from '@angular/forms';
    import { UserComponent } from './user.component';
    import { NewUserDirective } from './new-user.directive';
    import { OrdersPipe } from './orders.pipe';
    
    @NgModule({
     imports:      [ CommonModule ],
     declarations: [ UserComponent, NewUserDirective, OrdersPipe ],
     exports:      [ UserComponent, NewUserDirective, OrdersPipe,
                     CommonModule, FormsModule ]
    })
    export class SharedModule { }
    ```

    **[⬆ 返回顶部](#目录)**

    

96. ### 可以使用模块共享服务吗？

    不推荐通过导入模块来共享服务。即，只有在您想要使用指令、管道和组件时才导入模块。获取共享服务的最佳方法是通过“Angular依赖注入”，因为**导入模块将导致新的服务实例**。

    **[⬆ 返回顶部](#目录)**

    

97. ### 什么是 ngcc？

    ngcc（Angular 兼容编译器）是一个工具，用于将使用非 Ivy ngc 编译的 node_module 升级为符合 Ivy 规范的格式。package.json 中的 `postinstall` 脚本将确保您的 node_modules 与 Ivy 渲染器兼容。

    ```typescript
    "scripts": {
       "postinstall": "ngcc"
    }
    ```

    **[⬆ 返回顶部](#目录)**

    

98. ### 什么是 NgZone？

    Angular 提供了一个名为 NgZone 的服务，它创建了一个名为 `angular` 的区域，当满足以下条件时会自动触发变更检测。

    1. 当同步或异步函数被执行时。
    2. 当没有微任务被调度时。

    **[⬆ 返回顶部](#目录)**

    

99. ### 什么是 NoopZone？

    在 Angular 应用中，默认加载/需要 Zone，并且它帮助 Angular 知道何时触发变更检测。这样，它确保开发人员专注于应用程序开发而不是 Angular 的核心部分。你也可以在没有 Zone 的情况下使用 Angular，但需要自行实现变更检测，并在引导过程中配置 `noop zone`。 下面是移除 zone.js 的两个步骤：

    1. 从 polyfills.ts 中移除 zone.js 的导入。

       ```typescript
       /***************************************************************************************************
        * Angular 自身默认需要 Zone JS。
        */
       // import 'zone.js/dist/zone';  // 包含在 Angular CLI 中。
       ```

    2. 在 src/main.ts 中使用 noop 区域来引导 Angular。

       ```typescript
       platformBrowserDynamic().bootstrapModule(AppModule, {ngZone: 'noop'})
         .catch(err => console.error(err));
       ```

    **[⬆ 返回顶部](#目录)**

    

100. ### 变更检测的可能数据更新场景有哪些？

     变更检测在以下情景下起作用，即数据发生变化时需要更新应用程序的 HTML。

     1. 组件初始化： 在引导 Angular 应用程序时，Angular 会触发 `ApplicationRef.tick()` 来调用变更检测和视图渲染。

     2. 事件监听器：

         DOM 事件监听器可以更新 Angular 组件中的数据并触发变更检测。

        ```typescript
        @Component({
          selector: 'app-event-listener',
          template: `
            <button (click)="onClick()">Click</button>
            {{message}}`
        })
        export class EventListenerComponent {
          message = '';
        
          onClick() {
            this.message = '数据已更新';
          }
        }
        ```

     3. HTTP 数据请求：

         可以通过 HTTP 请求从服务器获取数据。

        ```typescript
        data = '默认值';
        constructor(private httpClient: HttpClient) {}
        
        ngOnInit() {
            this.httpClient.get(this.serverUrl).subscribe(response => {
              this.data = response.data; // 变更检测将自动发生
            });
        }
        ```

     4. 宏任务 setTimeout() 或 setInterval()：

         可以在 setTimeout 或 setInterval 的回调函数中更新数据。

        ```typescript
        data = '默认值';
        
        ngOnInit() {
            setTimeout(() => {
                this.data = '数据已更新'; // 变更检测将自动发生
            });
        }
        ```

     5. 微任务 Promises：

         可以在 promise 的回调函数中更新数据。

        ```typescript
        data = '初始值';
        
        ngOnInit() {
            Promise.resolve(1).then(v => {
                this.data = v; // 变更检测将自动发生
            });
        }
        ```

     6. 异步操作，如 WebSockets 和 Canvas： 可以使用 WebSocket.onmessage() 和 Canvas.toBlob() 异步地更新数据。

     **[⬆ 返回顶部](#目录)**

     

101. ### 什么是zone context（区域上下文）？

     执行上下文是一个抽象概念，它保存了当前代码执行的环境信息。区域提供了一个跨异步操作持久存在的执行上下文，称为区域上下文。例如，区域上下文在 setTimeout 回调函数的外部和内部都是相同的

     ```typescript
     zone.run(() => {
        // 在区域外部
        expect(zoneThis).toBe(zone);
        setTimeout(function() {
          // 同样的区域外部也存在于此处
          expect(zoneThis).toBe(zone);
        });
     });
     ```

     **[⬆ 返回顶部](#目录)**

     

102. ### zone的生命周期钩子是什么？

     zone.js 提供了四个针对异步操作的生命周期钩子。

     1. **onScheduleTask:** 当一个新的异步任务被调度时触发该钩子。例如，当调用 setTimeout() 时。

        ```typescript
        onScheduleTask: function(delegate, curr, target, task) {
            console.log('new task is scheduled:', task.type, task.source);
            return delegate.scheduleTask(target, task);
        }
        ```

     2. **onInvokeTask:** 当一个异步任务即将执行时触发该钩子。例如，当 setTimeout() 的回调即将执行时。

        ```typescript
        onInvokeTask: function(delegate, curr, target, task, applyThis, applyArgs) {
            console.log('task will be invoked:', task.type, task.source);
            return delegate.invokeTask(target, task, applyThis, applyArgs);
        }
        ```

     3. **onHasTask:** 当区域内某种类型的任务状态从稳定（区域内无任务）变为不稳定（区域内调度了新任务）或从不稳定变为稳定时触发该钩子。

        ```typescript
        onHasTask: function(delegate, curr, target, hasTaskState) {
            console.log('task state changed in the zone:', hasTaskState);
            return delegate.hasTask(target, hasTaskState);
        }
        ```

     4. **onInvoke:** 当一个同步函数即将在区域中执行时触发该钩子。

        ```typescript
        onInvoke: function(delegate, curr, target, callback, applyThis, applyArgs) {
            console.log('the callback will be invoked:', callback);
            return delegate.invoke(target, callback, applyThis, applyArgs);
        }
        ```

     **[⬆ 返回顶部](#目录)**

     

103. ### NgZone 的哪些方法用于控制变更检测？

     NgZone 服务提供了一个 `run()` 方法，允许您在 Angular 区域内执行函数。此函数用于执行第三方 API，这些 API 不受 Zone 控制，并在正确的时间自动触发变更检测。

     ```typescript
     export class AppComponent implements OnInit {
       constructor(private ngZone: NgZone) {}
       ngOnInit() {
         // 使用 ngZone.run() 在 Angular 区域内执行异步操作
         this.ngZone.run(() => {
           someNewAsyncAPI(() => {
             // 更新组件的数据
           });
         });
       }
     }
     ```

     而 `runOutsideAngular()` 方法用于在您不希望触发变更检测时使用。

     ```typescript
     export class AppComponent implements OnInit {
       constructor(private ngZone: NgZone) {}
       ngOnInit() {
         // 当您知道不会更新数据时使用此方法
         this.ngZone.runOutsideAngular(() => {
           setTimeout(() => {
             // 更新组件数据，但不触发变更检测
           });
         });
       }
     }
     ```

     **[⬆ 返回顶部](#目录)**

     

104. ### 如何更改 zonejs 的设置？

     你可以通过在一个单独的文件中配置来更改 zone 的设置，并在导入 zonejs 后立即导入该文件。

     例如，你可以禁用 `requestAnimationFrame()` 的猴子补丁，以防止在没有数据更新时触发变更检测，还可以防止 DOM 事件（如鼠标移动或滚动事件）触发变更检测。假设新文件名为 `zone-flags.js`，

     ```typescript
     // 禁用 requestAnimationFrame 补丁
     (window as any).__Zone_disable_requestAnimationFrame = true;
     
     // 禁用指定事件名称的补丁
     (window as any).__zone_symbol__UNPATCHED_EVENTS = ['scroll', 'mousemove'];
     ```

     上述配置文件可以在 `polyfills.ts` 文件中导入，如下所示：

     ```typescript
     /***************************************************************************************************
      * Angular 默认需要 Zone JS。
      */
     import './zone-flags';
     import 'zone.js/dist/zone';  // 包含在 Angular CLI 中。
     ```

     **[⬆ 返回顶部](#目录)**

     

105. ### 什么是可选依赖项？

     可选依赖项是一个参数装饰器，用于标记构造函数参数，表示该参数是一个可选依赖项。因此，如果找不到依赖项，DI 框架将提供 null。

     例如，如果你没有在任何地方注册日志记录器提供程序，则注入器会将 logger（或日志记录器服务）的值设置为 null，如下所示：

     ```typescript
     import { Optional } from '@angular/core';
     
     constructor(@Optional() private logger?: Logger) {
       if (this.logger) {
         this.logger.log('这是一个可选的依赖项消息');
       } else {
         console.log('未注册日志记录器');
       }
     }
     ```

     **[⬆ 返回顶部](#目录)**

     

106. ### 注入器层次结构有哪些类型？

     在 Angular 中有两种类型的注入器层次结构：

     1. **ModuleInjector 层次结构：** 它在模块级别上使用 @NgModule() 或 @Injectable() 注解进行配置。
     2. **ElementInjector 层次结构：** 它在每个 DOM 元素上隐式创建。默认情况下是空的，除非你在 @Directive() 或 @Component() 的 providers 属性中对其进行配置。

     **[⬆ 返回顶部](#目录)**

     

107. ### 什么是响应式表单？

     响应式表单是一种以响应式风格（表单输入随时间变化）创建表单的模型驱动方法。这些表单围绕可观察流建立，其中表单输入和值被提供为输入值流。以下是创建响应式表单的步骤：

     1. 注册响应式表单模块，在你的应用程序中声明响应式表单指令。
        ```typescript
        import { ReactiveFormsModule } from '@angular/forms';
        
        @NgModule({
          imports: [
            // 其他导入...
            ReactiveFormsModule
          ],
        })
        export class AppModule { }
        ```

     2. 创建一个新的 FormControl 实例并将其保存在组件中。
        ```typescript
        import { Component } from '@angular/core';
        import { FormControl } from '@angular/forms';
        
        @Component({
          selector: 'user-profile',
          styleUrls: ['./user-profile.component.css']
        })
        export class UserProfileComponent {
          userName = new FormControl('');
        }
        ```

     3. 在模板中注册 FormControl。
        ```html
        <label>
          用户名：
          <input type="text" [formControl]="userName">
        </label>
        ```

     最终，带有响应式表单控件的组件如下所示：
     ```typescript
     import { Component } from '@angular/core';
     import { FormControl } from '@angular/forms';
     	
     @Component({
       selector: 'user-profile',
       styleUrls: ['./user-profile.component.css'],
       template: `
         <label>
           用户名：
           <input type="text" [formControl]="userName">
         </label>
       `
     })
     export class UserProfileComponent {
       userName = new FormControl('');
     }
     ```

     **[⬆ 返回顶部](#目录)**

     

108. ### 什么是模板驱动表单？

     模板驱动表单是一种模型驱动表单，其中你在代码的模板部分使用指令编写逻辑、验证、控件等。它们适用于简单的场景，并使用 [(ngModel)] 语法进行双向绑定。

     例如，你可以按照以下简单步骤轻松创建注册表单：

     1. 将 FormsModule 导入到应用程序模块的导入数组中。
        ```typescript
        import { BrowserModule } from '@angular/platform-browser';
        import { NgModule } from '@angular/core';
        import { FormsModule } from '@angular/forms';
        import { RegisterComponent } from './app.component';
        
        @NgModule({
          declarations: [
            RegisterComponent,
          ],
          imports: [
            BrowserModule,
            FormsModule
          ],
          providers: [],
          bootstrap: [RegisterComponent]
        })
        export class AppModule { }
        ```

     2. 使用 ngModel 语法将表单从模板绑定到组件。
        ```html
        <input type="text" class="form-control" id="name"
          required
          [(ngModel)]="model.name" name="name">
        ```

     3. 在 <form> 标签中附加 NgForm 指令，以创建 FormControl 实例并注册它们。
        ```html
        <form #registerForm="ngForm">
        ```

     4. 为表单控件应用验证消息。
        ```html
        <label for="name">Name</label>
        <input type="text" class="form-control" id="name"
               required
               [(ngModel)]="model.name" name="name"
               #name="ngModel">
        <div [hidden]="name.valid || name.pristine"
             class="alert alert-danger">
          Please enter your name
        </div>
        ```

     5. 使用 ngSubmit 指令提交表单，并在表单底部添加 type="submit" 按钮以触发表单提交。
        ```html
        <form (ngSubmit)="onSubmit()" #heroForm="ngForm">
        // 表单内容
        <button type="submit" class="btn btn-success" [disabled]="!registerForm.form.valid">Submit</button>
        ```

     最终，完成的模板驱动注册表单将如下所示：

     ```html
     <div class="container">
       <h1>Registration Form</h1>
       <form (ngSubmit)="onSubmit()" #registerForm="ngForm">
         <div class="form-group">
           <label for="name">Name</label>
             <input type="text" class="form-control" id="name"
                    required
                    [(ngModel)]="model.name" name="name"
                    #name="ngModel">
             <div [hidden]="name.valid || name.pristine"
                  class="alert alert-danger">
               Please enter your name
             </div>
         </div>
         <button type="submit" class="btn btn-success" [disabled]="!registerForm.form.valid">Submit</button>
         </form>
     </div>
     ```

     **[⬆ 返回顶部](#目录)**

     

109. ### 响应式表单和模板驱动表单之间有哪些区别？

     下面是响应式表单和模板驱动表单之间的主要区别：

     | 特征           | 响应式                                                  | 模板驱动                              |
     | -------------- | ------------------------------------------------------- | ------------------------------------- |
     | 表单模型设置   | 在组件中显式创建（FormControl 实例）                    | 由指令创建                            |
     | 数据更新       | 同步                                                    | 异步                                  |
     | 表单自定义验证 | 定义为函数                                              | 定义为指令                            |
     | 测试           | 不与变更检测周期交互                                    | 需要了解变更检测过程                  |
     | 可变性         | 通过始终返回新值来保持不可变性（对于 FormControl 实例） | 可变（属性总是修改为新值）            |
     | 可扩展性       | 使用底层 API 更具可扩展性                               | 由于 API 的抽象程度较高，可扩展性较低 |

     **[⬆ 返回顶部](#目录)**

     

110. ### 表单控件分组有哪些不同的方法？

     响应式表单提供了两种将多个相关控件分组的方式。

     1. **FormGroup：** 它定义了一个具有固定一组控件的表单，这些控件可以一起在一个对象中进行管理。它具有与 FormControl 实例类似的属性和方法。
        
        可以通过嵌套 FormGroup 来创建复杂的表单，示例如下：

        ```typescript
        import { Component } from '@angular/core';
        import { FormGroup, FormControl } from '@angular/forms';
        
        @Component({
          selector: 'user-profile',
          templateUrl: './user-profile.component.html',
          styleUrls: ['./user-profile.component.css']
        })
        export class UserProfileComponent {
          userProfile = new FormGroup({
            firstName: new FormControl(''),
            lastName: new FormControl(''),
            address: new FormGroup({
              street: new FormControl(''),
              city: new FormControl(''),
              state: new FormControl(''),
              zip: new FormControl('')
            })
          });
        
          onSubmit() {
            // 将 this.userProfile.value 存储在数据库中
          }
        }
        ```

        ```html
        <form [formGroup]="userProfile" (ngSubmit)="onSubmit()">
        
          <label>
            First Name:
            <input type="text" formControlName="firstName">
          </label>
        
          <label>
            Last Name:
            <input type="text" formControlName="lastName">
          </label>
        
          <div formGroupName="address">
            <h3>Address</h3>
        
            <label>
              Street:
              <input type="text" formControlName="street">
            </label>
        
            <label>
              City:
              <input type="text" formControlName="city">
            </label>
        
            <label>
              State:
              <input type="text" formControlName="state">
            </label>
        
            <label>
              Zip Code:
              <input type="text" formControlName="zip">
            </label>
           </div>
           <button type="submit" [disabled]="!userProfile.valid">Submit</button>
        
        </form>
        ```

     2. **FormArray：** 它定义了一个以数组格式的动态表单，可以在运行时添加和删除控件。当您不知道组中会有多少控件时，这非常有用。

        ```typescript
        import { Component } from '@angular/core';
        import { FormArray, FormControl } from '@angular/forms';
        
        @Component({
          selector: 'order-form',
          templateUrl: './order-form.component.html',
          styleUrls: ['./order-form.component.css']
        })
        export class OrderFormComponent {
          constructor () {
            this.orderForm = new FormGroup({
              firstName: new FormControl('John', Validators.minLength(3)),
              lastName: new FormControl('Rodson'),
              items: new FormArray([
                new FormControl(null)
              ])
            });
          }
        
          onSubmitForm () {
            // 将 this.orderForm.value 中的项目保存在数据库中
          }
        
          onAddItem () {
            this.orderForm.controls.items.push(new FormControl(null));
          }
        
          onRemoveItem (index) {
            this.orderForm.controls['items'].removeAt(index);
          }
        }
        ```

        ```html
        <form [formControlName]="orderForm" (ngSubmit)="onSubmit()">
        
          <label>
            First Name:
            <input type="text" formControlName="firstName">
          </label>
        
          <label>
            Last Name:
            <input type="text" formControlName="lastName">
          </label>
        
          <div>
            <p>Add items</p>
            <ul formArrayName="items">
              <li *ngFor="let item of orderForm.controls.items.controls; let i = index">
                <input type="text" formControlName="{{i}}">
                <button type="button" title="Remove Item" (click)="onRemoveItem(i)">Remove</button>
              </li>
            </ul>
            <button type="button" (click)="onAddItem">
              Add an item
            </button>
          </div>
        </form>
        ```

     **[⬆ 返回顶部](#目录)**

     

111. ### 如何更新表单模型的特定属性？

     您可以使用 `patchValue()` 方法来更新表单模型中定义的特定属性。例如，您可以在单击更新按钮时更新某个配置文件的名称和街道，如下所示：

     ```typescript
     updateProfile() {
       this.userProfile.patchValue({
         firstName: 'John',
         address: {
           street: '98 Crescent Street'
         }
       });
     }
     ```

     ```html
     <button (click)="updateProfile()">Update Profile</button>
     ```

     您也可以使用 `setValue` 方法来更新属性。

     **注意：**请记住根据确切的模型结构更新属性。

     **[⬆ 返回顶部](#目录)**

     

112. ### FormBuilder 的目的是什么？

     FormBuilder 用作 FormControl、FormGroup 或 FormArray 的实例的轻量级语法糖。这有助于减少构建复杂响应式表单所需的样板代码量。它作为 `@angular/forms` 包的一个可注入辅助类而提供。

     例如，用户配置文件组件的创建变得更加简单，如下所示：

     ```typescript
     export class UserProfileComponent {
       profileForm = this.formBuilder.group({
         firstName: [''],
         lastName: [''],
         address: this.formBuilder.group({
           street: [''],
           city: [''],
           state: [''],
           zip: ['']
         }),
       });
         
       constructor(private formBuilder: FormBuilder) { }
     }
     ```

     **[⬆ 返回顶部](#目录)**

     

113. ### 如何验证表单中模型的更改？

     在Angular中，有时候我们需要确保表单数据正确地流动到模型中，以及从模型正确地流向表单控件。为了方便验证这些数据流，您可以在组件中添加一个名为 `diagnostic` 的属性，用来返回模型的 JSON 表示。这样一来，您就可以轻松地检查表单数据是否正确地映射到了模型上。

     首先，我们假设您有一个名为 `UserProfileComponent` 的组件，并且在组件中有一个叫做 `model` 的属性，表示用户的数据模型。现在，我们希望在开发过程中能够实时地查看模型的数据，以便验证数据流。

     ```typescript
     export class UserProfileComponent {
       model = new User('John', 29, 'Writer');
     
       // 用于显示模型数据的 getter 属性
       get diagnostic() { 
         return JSON.stringify(this.model); 
       }
     }
     ```

     在模板中，我们将 `diagnostic` 属性绑定到一个地方，这样它就会在界面上显示模型的 JSON 表示。通常，您会在表单的顶部或底部添加此绑定。

     ```html
     <div class="container">
       <!-- 显示模型数据的地方 -->
       <p>{{ diagnostic }}</p>
     
       <!-- 其他表单控件 -->
     </div>
     ```

     这样，在开发过程中，您就可以随时查看模型的实时数据，并验证表单数据是否与模型同步更新。这对于调试和确保数据正确流动非常有用。

     **注意：** 一旦验证完毕，记得将 `diagnostic` 属性从组件中移除，因为这只是为了方便开发期间的调试和验证。

     希望这样更详细的解释能够帮助您理解。

     **[⬆ 返回顶部](#目录)**

     

114. ### ngModel 提供的状态 CSS 类是什么？

     ngModel 指令通过特殊的 Angular CSS 类来更新表单控件的状态。让我们以表格形式列出这些类：

     | 表单控件状态 | 如果为 true | 如果为 false |
     | ------------ | ----------- | ------------ |
     | 已访问       | ng-touched  | ng-untouched |
     | 值已更改     | ng-dirty    | ng-pristine  |
     | 值有效       | ng-valid    | ng-invalid   |

     1. **已访问（Visited）**:
        - 如果控件已经被访问过，则会添加 `ng-touched` 类。
        - 如果控件尚未被访问，则会添加 `ng-untouched` 类。

     2. **值已更改（Value has changed）**:
        - 如果控件的值已经被修改过，则会添加 `ng-dirty` 类。
        - 如果控件的值尚未被修改，则会添加 `ng-pristine` 类。

     3. **值有效（Value is valid）**:
        - 如果控件的值是有效的，则会添加 `ng-valid` 类。
        - 如果控件的值是无效的，则会添加 `ng-invalid` 类。

     您可以使用这些状态 CSS 类来动态地更新或修改表单控件的样式或者在模板中编写样式，以根据控件的状态进行渲染。例如，您可以根据表单控件是否已被访问过来更改其边框颜色，或者根据控件值的有效性来显示错误消息。

     以下是一个简单的示例，演示了如何使用 ngModel 提供的状态 CSS 类来根据表单控件的状态修改样式：

     ```html
     <input type="text" [(ngModel)]="username" name="username" #username="ngModel" required>
     
     <!-- 根据控件的状态动态应用样式 -->
     <div [ngClass]="{'visited': username.touched, 'changed': username.dirty, 'valid': username.valid, 'invalid': username.invalid}">
       用户名：
     </div>
     ```

     在这个示例中，我们使用了 ngClass 指令，根据 ngModel 提供的状态 CSS 类来动态地应用不同的样式类。这样，当用户访问控件、修改控件的值或者控件的值有效或无效时，会自动应用相应的样式类，从而改变控件的外观。

     请注意，这只是一个简单的示例，实际上您可以根据自己的需求使用这些状态 CSS 类来设计各种不同的样式或者添加更多的行为。

     **[⬆ 返回顶部](#目录)**

     

115. ### 验证器函数有哪些类型？
     在响应式表单中，验证器函数可以是同步的或异步的函数，

     1. **同步验证器（Sync validators）：** 这些是同步函数，它们接受一个控件实例，并立即返回一组验证错误或 null。此外，这些函数作为第二个参数传递给表单控件的实例化过程中。主要用例是简单的检查，比如检查字段是否为空，是否超过了最大长度等。
     2. **异步验证器（Async validators）：** 这些是异步函数，它们接受一个控件实例，并返回一个 Promise 或 Observable，后者稍后会发出一组验证错误或 null。同样，这些函数作为第二个参数传递给表单控件的实例化过程中。主要用例是复杂的验证，比如向服务器发送请求检查用户名或电子邮件的可用性。

     这些验证器的表示形式如下：

     ```typescript
     this.myForm = formBuilder.group({
         firstName: ['value'],
         lastName: ['value', *一些同步验证函数*],
         email: ['value', *一些验证函数*, *一些异步验证函数*]
     });
     ```

     **[⬆ 返回顶部](#目录)**

     

116. ### 能举一个内置验证器的例子吗？

     在响应式表单中，您可以在输入表单控件上使用内置的验证器，例如 `required` 和 `minlength`。例如，注册表单可以在姓名输入字段上具有这些验证器

     ```typescript
     this.registrationForm = new FormGroup({
         'name': new FormControl(this.hero.name, [
           Validators.required,
           Validators.minLength(4),
         ])
     });
     ```

     而在模板驱动的表单中，`required` 和 `minlength` 验证器都作为属性提供。

     **[⬆ 返回顶部](#目录)**

     

117. ### 如何优化异步验证器的性能？

     由于所有验证器都在每次表单值更改后运行，使用异步验证器会对性能产生重大影响，因为它会在每次按键时都向外部 API 发送请求。可以通过将 updateOn 属性从 change（默认）更改为 submit 或 blur 来延迟表单的有效性来避免这种情况。 根据表单类型，使用方式略有不同，

     1. 模板驱动表单：

        在 ngModelOptions指令上设置属性

        ```html
        <input [(ngModel)]="name" [ngModelOptions]="{updateOn: 'blur'}">
        ```

     2. 响应式表单：

        在 FormControl 实例上设置属性

        ```javascript
        name = new FormControl('', {updateOn: 'blur'});
        ```

     **[⬆ 返回顶部](#目录)**

     

118. ### 如何在同一个元素上设置 ngFor 和 ngIf？

     有时您可能需要在同一个元素上同时使用 ngFor 和 ngIf，但不幸的是，您会遇到以下模板错误。

     ```cmd
     模板解析错误：无法在同一个元素上有多个模板绑定。
     ```

     在这种情况下，您需要使用 ng-container 或 ng-template。 例如，如果您尝试仅在项目可用时循环遍历项目，下面的代码将在浏览器中抛出错误

     ```html
     <ul *ngIf="items" *ngFor="let item of items">
       <li></li>
     </ul>
     ```

     可以通过以下方式修复

     ```html
     <ng-container *ngIf="items">
       <ul *ngFor="let item of items">
         <li></li>
       </ul>
     </ng-container>
     ```

     **[⬆ 返回顶部](#目录)**

     

119. ### CSS 中的 host 属性是什么？

     `:host` 伪类选择器用于针对承载组件的元素中的样式。由于宿主元素位于父组件的模板中，您无法通过其他方式从组件内部访问宿主元素。 例如，您可以如下为父元素创建边框，

     ```css
     // app.component.css 中的其他样式
     //...
     :host {
       display: block;
       border: 1px solid black;
       padding: 20px;
     }
     ```

     **[⬆ 返回顶部](#目录)**

     

120. ### 什么是内容投影（Content Projection）？

     内容投影（Content Projection）是 Angular 中一种重要的模式，它允许您在一个组件内部插入、投影其他组件或 HTML 内容。通过内容投影，您可以在一个组件中定义一些特定的插槽（slots），然后在使用该组件时，将外部的内容插入到这些插槽中。这样可以使组件更加灵活和可重用，因为它可以适应各种不同的内容。

     具体来说，内容投影通过使用 `<ng-content></ng-content>` 标签来实现。当 Angular 渲染组件时，`<ng-content>` 标签会被替换为组件使用时提供的内容。这样，您就可以在组件的模板中定义插槽，然后在组件的使用处插入自定义内容。

     例如，假设您有一个通用的面板组件，您希望用户可以在面板中放置不同的内容。您可以在面板组件中使用 `<ng-content></ng-content>` 定义一个插槽，然后在使用该面板组件时，将内容插入到这个插槽中。

     这种模式使得组件更加灵活，因为它允许开发者在组件内部动态地插入不同的内容，从而实现各种定制化的效果。

     总之，内容投影是 Angular 中一种强大的模式，可用于增强组件的灵活性和可重用性。

     **[⬆ 返回顶部](#目录)**

     

121. ### 什么是ng-template？

     `ng-template` 是 Angular 中的一个内置指令，用于定义一个模板块，但不会在 DOM 中渲染任何内容。它通常用于延迟渲染或条件渲染，以及在组件之间共享模板。

     `ng-template` 的主要作用包括：

     1. **延迟渲染（Lazy Rendering）**：可以在需要时动态地将模板内容渲染到 DOM 中，而不是在页面加载时就进行渲染。
     2. **条件渲染（Conditional Rendering）**：可以根据条件决定是否渲染特定的模板内容。
     3. **复用模板（Template Reusability）**：可以将 `ng-template` 视为一个可重复使用的模板片段，可以在不同的地方引用和重用。

     以下是一个简单的示例，展示了如何使用 `ng-template`：

     ```html
     <ng-template #myTemplate>
       <p>This is a template content.</p>
     </ng-template>
     
     <!-- 使用ng-template -->
     <ng-container *ngTemplateOutlet="myTemplate"></ng-container>
     ```

     在上面的示例中，`ng-template` 定义了一个模板，其中包含一个段落元素。然后，通过 `ngTemplateOutlet` 指令将模板插入到 `<ng-container>` 中进行渲染。

     通过 `ng-template` 可以实现更灵活的模板控制和复用，特别是在创建动态组件、条件性渲染以及自定义结构型指令时非常有用。

     **[⬆ 返回顶部](#目录)**

     

122. ### ng-content、ng-template和ng-container三者的用途？

     在Angular中，`ng-content`, `ng-container`, 和 `ng-template` 是三个非常有用的指令，它们在组件开发中扮演着不同的角色。

     1. `ng-content`: 它用于实现内容投影（Content Projection），允许你将外部内容传递到组件的模板中。这个指令通常用于创建可复用的组件，让你可以插入自定义的内容到组件的指定位置。

     html

     ```html
     <!-- parent.component.html -->
     <app-child-component>
       <p>这里的内容会被投影到 ChildComponent 中的 ng-content 位置。</p>
     </app-child-component>
     
     <!-- child.component.html -->
     <div>
       <!-- 这里的内容会被替换为父组件插入的内容 -->
       <ng-content></ng-content>
     </div>
     ```

     1. `ng-container`: 这是一个逻辑容器，用于帮助组织模板结构，但它不会被渲染成任何真实的DOM元素。它经常被用来作为结构性指令的宿主（比如 `*ngIf`, `*ngFor`）。

     html

     ```html
     <ng-container *ngIf="condition">
       <div>只有当 condition 为 true 时，这个 div 才会被渲染。</div>
     </ng-container>
     ```

     1. `ng-template`: 它是一个Angular模板，可以定义一段HTML结构，然后可以在其他地方调用并渲染它。它通常与 `*ngIf` 和 `ngTemplateOutlet` 结合使用，用于定义可复用的模板片段。

     html

     ```html
     <!-- 定义一个模板 -->
     <ng-template #myTemplate>
       <div>这是一个可复用的模板片段。</div>
     </ng-template>
     
     <!-- 在其他地方使用这个模板 -->
     <ng-container *ngTemplateOutlet="myTemplate"></ng-container>
     ```

     使用 `ng-template` 还可以与结构性指令一起使用，在某些条件下显示模板内容，例如使用 `*ngIf` 的 `else` 子句：

     html

     ```html
     <div *ngIf="condition; else myTemplate">
       当 condition 为 true 时显示。
     </div>
     
     <ng-template #myTemplate>
       当 condition 为 false 时显示。
     </ng-template>
     ```

     上述代码示例可以帮助你了解这三个指令的基本用法，实际项目中它们的使用会根据不同的需求进行变化。

     **[⬆ 返回顶部](#目录)**

     

123. ### 什么是路由守卫？

     在Angular中，路由守卫（Route Guards）是一种用于控制导航到某个路由是否允许的机制。它们是一组接口，可以通过实现这些接口来创建守卫服务，以执行诸如认证和授权等逻辑，从而决定是否允许用户访问特定的路由或离开当前路由。

     Angular提供了几种不同类型的路由守卫：

     1. `CanActivate`: 决定是否可以激活某个路由。
     2. `CanActivateChild`: 决定是否可以激活某个路由的所有子路由。
     3. `CanDeactivate`: 决定是否可以离开当前路由。
     4. `Resolve`: 在路由激活之前获取路由数据。
     5. `CanLoad`: 决定是否可以异步加载某个功能模块。

     下面是一个简单的`CanActivate`守卫的示例：

     ```typescript
     import { Injectable } from '@angular/core';
     import { CanActivate, ActivatedRouteSnapshot, RouterStateSnapshot, Router } from '@angular/router';
     
     @Injectable({
       providedIn: 'root',
     })
     export class AuthGuard implements CanActivate {
       constructor(private router: Router) {}
     
       canActivate(
         next: ActivatedRouteSnapshot,
         state: RouterStateSnapshot
       ): boolean {
         const isAuthenticated = //... 你的认证逻辑
         if (isAuthenticated) {
           return true;
         } else {
           this.router.navigate(['/login']); // 用户未认证时导航到登录页
           return false;
         }
       }
     }
     ```

     在这个示例中，`AuthGuard`服务实现了`CanActivate`接口。当用户尝试访问受保护的路由时，`canActivate`方法将被调用。如果用户已经认证（`isAuthenticated`返回`true`），则返回`true`允许导航；如果未认证，则重定向到登录页面，并返回`false`阻止导航。

     要使用路由守卫，你需要在路由配置中指定它：

     ```typescript
     const routes: Routes = [
       {
         path: 'protected',
         component: ProtectedComponent,
         canActivate: [AuthGuard] // 在这里指定守卫
       },
       // 其他路由配置...
     ];
     ```

     当路由被访问时，`AuthGuard`会根据其`canActivate`方法的返回值决定是否允许导航。通过这种方式，路由守卫在应用程序的安全性和用户体验方面起到了重要作用。

     **[⬆ 返回顶部](#目录)**

     

124. ### 路由守卫可以用来做什么？

     路由守卫在Angular中可以用来执行多种任务，主要包括但不限于：

     1. **用户认证（Authentication）**: 确保用户在访问需要认证的路由时已经登录。如果用户未登录，守卫可以重定向用户到登录页面。
     2. **用户授权（Authorization）**: 校验用户是否拥有访问特定路由的权限。如果用户没有相应的权限，守卫可以重定向到一个错误页面或主页。
     3. **保存草稿**: 如果用户在填写表单或其他活动中并且尝试离开当前页面，守卫可以询问用户是否保存更改或确认是否真的想要离开。
     4. **预加载数据（Pre-fetching Data）**: 在路由激活之前预先加载数据，确保当用户到达页面时所需的数据已经可用。
     5. **防止重复加载**: 如果某个功能模块已经加载过了，守卫可以防止应用程序再次加载它。
     6. **日志记录和分析**: 在路由变化时记录日志信息，用于后续的用户行为分析。
     7. **动态路由**: 根据特定的业务逻辑动态决定路由的激活和重定向。

     举个例子，以下是一个简单的认证守卫，用于检查用户是否登录：

     ```typescript
     @Injectable({
       providedIn: 'root'
     })
     export class AuthGuard implements CanActivate {
       constructor(private authService: AuthService, private router: Router) {}
     
       canActivate(
         route: ActivatedRouteSnapshot,
         state: RouterStateSnapshot
       ): boolean {
         const isLoggedIn = this.authService.isLoggedIn(); // 检查用户登录状态
         if (isLoggedIn) {
           return true; // 用户已登录，允许访问路由
         } else {
           this.router.navigate(['/login']); // 用户未登录，重定向到登录页面
           return false; // 阻止访问路由
         }
       }
     }
     ```

     在路由配置中使用这个守卫：

     ```typescript
     const routes: Routes = [
       {
         path: 'dashboard',
         component: DashboardComponent,
         canActivate: [AuthGuard] // 在这里指定AuthGuard
       },
       // 其他路由...
     ];
     ```

     在这个例子中，只有当`AuthService`报告用户已登录时，`AuthGuard`才允许用户访问`dashboard`路由。如果用户未登录，守卫会将用户重定向到登录页面，并且不允许访问`dashboard`路由。这样可以保证敏感页面或需要权限的页面不会被未授权的用户访问。

     **[⬆ 返回顶部](#目录)**

     

125. ### 路由守卫怎么优化angular性能的？

     路由守卫可以帮助优化Angular应用程序的性能，主要通过以下几种方式：

     1. **按需加载（Lazy Loading）**: 利用`CanLoad`守卫，你可以实现模块的按需加载，即只有当用户需要访问特定功能时才加载对应的模块。这减少了应用程序的初始加载时间和总体大小，因为不需要在启动时加载所有功能模块。
     2. **防止不必要的视图渲染**: `CanActivate`守卫可以防止未授权或未认证的用户访问特定路由，从而避免加载不必要的组件和数据，减少了不必要的计算和渲染，这有助于保持应用程序的响应性和高效性。
     3. **数据预加载（Pre-fetching Data）**: 使用`Resolve`守卫，可以在路由激活之前获取必要的数据。这意味着用户在到达目标页面时不需要等待数据的加载，从而提高了用户体验，并且减少了视图在数据到达之前的不必要的重复渲染。
     4. **避免不必要的导航**: `CanDeactivate`守卫可以在用户离开当前页面之前进行检查，例如表单尚未保存时提醒用户。这防止了不必要的导航和可能的数据重新加载，节省了资源。
     5. **动态路由管理**: 通过结合业务逻辑，路由守卫可以动态地允许或阻止访问某些路由，这意味着应用程序可以根据用户的状态、权限或其他条件来高效地管理和优化路由。

     通过上述方式，路由守卫确保了只有在需要时才执行某些操作，减少了不必要的加载和渲染，提高了应用程序的整体性能。这对于大型应用程序和复杂的路由结构尤为重要，因为它们可能涉及到大量的数据处理和视图更新。

     **[⬆ 返回顶部](#目录)**
