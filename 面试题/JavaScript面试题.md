# JavaScript面试题

## 类型

### 1. 基本类型有哪些？

1. **数字（Number）**：表示整数和浮点数，如1, 3.14等。
2. **字符串（String）**：表示文本数据，如"Hello, World!"等。
3. **布尔值（Boolean）**：表示逻辑值，true或false。
4. **空值（Null）**：表示一个空值或者“无”。
5. **未定义（Undefined）**：表示一个未定义的值。
6. **符号（Symbol）**（ES6新增）：表示唯一的标识符。
7. **BigInt**（ES11新增）：表示任意精度的整数。

这些基本类型是 JavaScript 中最基本的数据类型，它们不是对象，不具有方法。

在内存中占据固定大小，保存在栈内存中。



### 2. 栈内存和堆内存的区别是什么？

在计算机内存管理中，栈内存（Stack）和堆内存（Heap）是两种不同的内存分配方式，它们有以下区别：

1. **分配方式**：
   - **栈内存**：栈内存是一种**连续的内存空间**，数据在栈上的分配和释放是由系统自动管理的，采用**先进先出**的方式分配内存。当一个函数被调用时，函数的局部变量和参数等数据会被分配到栈上，函数执行完毕后，这些数据会被自动释放。
   - **堆内存**：堆内存是一种**离散的内存空间**，数据在堆上的分配和释放需要手动管理。在堆上分配的数据的生命周期由程序员控制，需要手动释放内存，否则可能导致内存泄漏。

2. **速度**：
   - **栈内存**：栈内存的分配和释放是由系统自动管理的，分配和释放的速度较**快**。
   - **堆内存**：堆内存的分配和释放需要手动管理，因此速度较慢。

3. **存储方式**：
   - **栈内存**：栈内存通常用于存储函数调用时的局部变量、函数参数等数据，数据的大小是固定的，存储的是**基本类型数据**。
   - **堆内存**：堆内存用于存储动态分配的数据，如对象、数组等，数据的大小和结构可以动态改变，存储的是**引用类型数据**。

4. **作用域**：
   - **栈内存**：栈内存中的数据的作用域仅限于所属的函数，函数执行完毕后，数据**会被自动释放**。
   - **堆内存**：堆内存中的数据的作用域可以跨越函数和代码块，由程序员**手动管理内存的释放**。

总的来说，栈内存适合存储函数调用时的局部变量和参数等数据，而堆内存适合存储动态分配的数据，如对象、数组等。



### 3. 引用类型有哪些？

1. **对象（Object）**：对象是JavaScript中最基本的引用类型，用于存储多个键值对。对象可以通过字面量、构造函数或对象字面量的方式创建。

2. **数组（Array）**：数组是一种特殊的对象，用于存储有序的数据集合。数组的元素可以是任意数据类型，包括基本类型和其他引用类型。

3. **函数（Function）**：函数也是一种对象，用于封装可执行的代码块。函数可以被调用执行，并且可以接收参数和返回值。

4. **日期（Date）**：日期对象用于处理日期和时间，包括日期的获取、设置和计算等操作。

5. **正则表达式（RegExp）**：正则表达式对象用于进行字符串的模式匹配和替换操作。

6. **Map**：Map是ES6新增的引用类型，它是一种键值对的集合，其中键可以是任意数据类型。

7. **Set**：Set是ES6新增的引用类型，它是一种值的集合，其中每个值都是唯一的。

8. **Symbol**：Symbol是ES6新增的基本类型，但它也可以作为引用类型使用，用于创建唯一的标识符。

这些引用类型都具有自己的特性和方法，用于处理不同类型的数据和实现不同的功能。



### 4. null和undefined之间的区别是什么？

- null用于显式地表示一个变量没有值。
- undefined用于表示变量未赋值或访问不存在的属性时的返回值。
- 在实际编程中，null通常用于初始化一个变量为“无值”，而undefined通常用于表示变量未初始化或某些操作的结果。



### 5. 类型强制转换是什么？

- 在显式转换中，我们使用内置函数或操作符，如`Number()`和`String()`，来将值转换为特定类型。
- 隐式转换中，JavaScript根据运算、比较或其他操作的需要，自动进行类型转换。
- 通常会优先考虑字符串类型。



### 6. 如何检查 JavaScript 中变量的类型？

`typeof`运算符可以用于检查任何类型的变量，包括基本类型和引用类型。

`typeof null`返回 "object"，因为进制前几位和object一样。所以可以用 `=== null`来判断。

可以使用 `instanceof` 运算符来检查一个对象是否是特定类型的实例。

可以使用`Object.prototype.toString.call()`方法来获取其内部属性 `[[Class]]` 的值，然后根据该值返回一个表示变量类型的字符串。



### 7. `==` 和 `===` 有什么区别？

`==` 是相等运算符，如果比较的变量类型不同，会进行类型强制转换。`===` 是严格相等运算符，不进行类型转换，只有值和类型完全相同才返回 true。



### 8.`instanceof` 运算符是什么？它是如何工作的？

`instanceof` 运算符用于检查一个对象是否是某个构造函数的实例。



### 9. let、const 和 var 有什么区别？

`var` 是函数作用域，而 `let` 和 `const` 是块作用域。`const` 用于声明不能重新赋值的变量，而 `let` 和 `var` 可以重新赋值。



### 10. 暂时性死区是什么？

也就是let和const不能变量提升。



### 11. [] == ![] 的结果是什么？

这个表达式的结果是 `true`，因为 `![]` 被强制转换为 `false`，而 `[]` 在比较之前被强制转换为空字符串 `""`，而空字符串接着被强制转换为 `0`。因此，`0 == false` 被评估为 `true`。



### 12. 对象的key可以是数字吗？

可以。



### 13. 浅拷贝/深度拷贝的区别？

**浅拷贝（Shallow Copy）：**

浅拷贝是指创建一个新对象或数组，将原始对象或数组的属性或元素复制到新对象或数组中。但是，如果原始对象或数组的属性或元素是引用类型（如对象、数组等），则浅拷贝只会复制它们的引用，而不会复制它们的值。因此，如果修改新对象或数组中的属性或元素，原始对象或数组中对应的属性或元素也会受到影响。

`Object.assign({}, obj);`

**深拷贝（Deep Copy）：**

深拷贝是指创建一个新对象或数组，并递归地将原始对象或数组的所有属性或元素以及它们的值复制到新对象或数组中。深拷贝会完全复制原始对象或数组的结构和值，因此修改新对象或数组不会影响到原始对象或数组。

```javascript
function deepCopy(obj) {
  // 检查是否为对象或数组，如果不是则直接返回
  if (typeof obj !== 'object' || obj === null) {
    return obj;
  }
  
  // 创建一个新的对象或数组，根据原始对象或数组的类型来决定
  let copy = Array.isArray(obj) ? [] : {};
  
  // 遍历原始对象或数组的属性或元素，并递归地复制到新对象或数组中
  for (let key in obj) {
    if (obj.hasOwnProperty(key)) {
      copy[key] = deepCopy(obj[key]);
    }
  }
  
  return copy;
}

// 测试深拷贝函数
const obj1 = { a: 1, b: { c: 2 } };
const obj2 = deepCopy(obj1);

obj2.a = 3;
obj2.b.c = 4;

console.log(obj1); // 输出: { a: 1, b: { c: 2 } }
console.log(obj2); // 输出: { a: 3, b: { c: 4 } }
```

总的来说，浅拷贝只会复制对象或数组的第一层属性或元素，而深拷贝会递归地复制所有的属性或元素，包括嵌套的对象或数组。因此，在需要复制对象或数组时，根据具体的需求选择使用浅拷贝还是深拷贝。



### 14. 闭包是什么，闭包形成的原因和闭包的用途 ？

闭包（Closure）是指在 JavaScript 中，一个函数能够访问其外部作用域中的变量，即使在函数被调用后外部作用域已经销毁的情况下仍然可以访问这些变量。换句话说，闭包是由函数和其相关的引用环境（Lexical Environment）组合而成的。

闭包形成的原因：

1. **函数嵌套**：当一个函数内部定义了另一个函数时，内部函数可以访问外部函数的变量。
2. **函数作为返回值**：当一个函数返回另一个函数时，返回的函数仍然可以访问其定义时所在的作用域中的变量。

闭包的用途：

1. **保护变量**：通过闭包可以创建私有变量，避免全局变量污染，提高代码的安全性和可维护性。
2. **封装变量**：闭包可以将变量封装在内部函数中，隐藏实现细节，提供更清晰的接口。
3. **延长变量的生命周期**：闭包可以使变量的生命周期得到延长，即使外部函数执行完毕，闭包仍然可以访问这些变量。
4. **实现函数记忆**：闭包可以用于实现函数记忆（Memoization），缓存函数的计算结果以提高性能。
5. **实现柯里化**：闭包可以用于实现柯里化（Currying），将多参数的函数转化为单参数的函数序列。
6. **实现回调函数**：闭包可以用于实现回调函数，例如在异步编程中。

举例来说，下面是一个简单的闭包示例：

```javascript
function outerFunction() {
  const outerVariable = 'I am from outer function';

  function innerFunction() {
    console.log(outerVariable); // 内部函数可以访问外部函数的变量
  }

  return innerFunction;
}

const innerFunc = outerFunction(); // 内部函数被返回并赋值给变量
innerFunc(); // 输出: "I am from outer function"
```

在这个例子中，`innerFunction` 是一个闭包，它可以访问外部函数 `outerFunction` 中定义的变量 `outerVariable`，即使外部函数已经执行完毕。通过返回内部函数，我们创建了一个闭包，使得 `innerFunction` 在执行时仍然能够访问 `outerVariable`。



### 15. 数据对象有那些属性值？

JavaScript 中的数据对象（Object）具有多种属性值，这些属性值可以分为两类：数据属性和访问器属性。

数据属性（Data Properties）：

1. **value**：属性的值。
2. **writable**：属性是否可写，即是否可以修改属性的值。
3. **enumerable**：属性是否可枚举，即是否可以通过 for...in 循环遍历到该属性。
4. **configurable**：属性是否可配置，即是否可以通过 delete 关键字删除属性，或者修改属性的特性。

访问器属性（Accessor Properties）：

1. **get**：获取属性值的函数，当访问该属性时调用。
2. **set**：设置属性值的函数，当修改该属性时调用。
3. **enumerable**：同数据属性中的 enumerable，属性是否可枚举。
4. **configurable**：同数据属性中的 configurable，属性是否可配置。

除了以上列出的属性值，对象还具有原型链相关的属性：

1. **[[Prototype]]**：对象的原型，指向该对象继承属性和方法的原型对象。
2. **constructor**：构造函数，用于创建该对象的构造函数。



### 16. ES6有哪些函数声明方式？

ES6（ECMAScript 2015）引入了一些新的函数声明方式，让 JavaScript 编程更加灵活和便捷。以下是 ES6 中常见的函数声明方式：

1. **箭头函数（Arrow Functions）**：
   - 箭头函数是 ES6 中最显著的新特性之一，它提供了一种更简洁的函数声明方式。
   - 箭头函数使用箭头 (=>) 语法来定义函数，可以省略 function 关键字、return 关键字以及大括号（当函数体只有一条语句时）。
   - 箭头函数的 this 绑定规则与普通函数不同，它的 this 始终指向函数定义时所在的对象。
   - 示例：
     ```javascript
     // 普通函数
     function add(a, b) {
       return a + b;
     }
     
     // 箭头函数
     const add = (a, b) => a + b;
     ```

2. **函数默认参数（Default Parameters）**：
   - ES6 允许在函数参数列表中为参数设置默认值，当调用函数时未传递参数时，将使用默认值。
   - 示例：
     ```javascript
     function greet(name = 'World') {
       console.log('Hello, ' + name + '!');
     }
     greet(); // Hello, World!
     greet('Alice'); // Hello, Alice!
     ```

3. **展开操作符（Spread Operator）**：
   - 展开操作符（...）可以将数组或类数组对象展开为独立的参数序列，或者将字符串展开为字符数组。
   - 在函数声明中，可以使用展开操作符来接收不定数量的参数。
   - 示例：
     ```javascript
     function sum(...args) {
       return args.reduce((acc, curr) => acc + curr, 0);
     }
     console.log(sum(1, 2, 3)); // 6
     ```

4. **剩余参数（Rest Parameters）**：
   - 剩余参数（Rest Parameters）用于接收函数调用时传递的剩余参数，并将它们存储在一个数组中。
   - 与展开操作符相反，剩余参数用于函数声明的参数列表中。
   - 示例：
     ```javascript
     function printArgs(firstArg, ...restArgs) {
       console.log('First argument:', firstArg);
       console.log('Rest arguments:', restArgs);
     }
     printArgs(1, 2, 3, 4); // First argument: 1, Rest arguments: [2, 3, 4]
     ```

这些 ES6 中的函数声明方式为 JavaScript 编程带来了更多的灵活性和便捷性，使得代码更加清晰、简洁。



### 17. 数组和对象怎么互相转换？

**从对象到数组的转换**

1. **Object.keys()**：将对象的键转换为一个数组。

```javascript
const obj = { a: 1, b: 2, c: 3 };
const arr = Object.keys(obj); // ['a', 'b', 'c']
```

2. **Object.values()**：将对象的值转换为一个数组。

```javascript
const obj = { a: 1, b: 2, c: 3 };
const arr = Object.values(obj); // [1, 2, 3]
```

3. **Object.entries()**：将对象的键值对转换为一个二维数组。

```javascript
const obj = { a: 1, b: 2, c: 3 };
const arr = Object.entries(obj); // [['a', 1], ['b', 2], ['c', 3]]
```

**从数组到对象的转换**

1. **Array.reduce()**：通过数组的某些属性来创建一个新对象。

```javascript
const arr = [['a', 1], ['b', 2], ['c', 3]];
const obj = arr.reduce((acc, [key, value]) => {
  acc[key] = value;
  return acc;
}, {});
// { a: 1, b: 2, c: 3 }
```

2. **Array.reduceRight()**：从数组的右侧开始，按照某些属性来创建一个新对象。

```javascript
const arr = [['a', 1], ['b', 2], ['c', 3]];
const obj = arr.reduceRight((acc, [key, value]) => {
  acc[key] = value;
  return acc;
}, {});
// { c: 3, b: 2, a: 1 }
```

3. **Object.fromEntries()**：根据一个包含键值对的数组创建一个新对象。

```javascript
const arr = [['a', 1], ['b', 2], ['c', 3]];
const obj = Object.fromEntries(arr);
// { a: 1, b: 2, c: 3 }
```



### 18. 数组如何进行浅拷贝？

1. 使用扩展运算符（Spread Operator）

```javascript
const originalArray = [1, 2, 3, 4, 5];
const shallowCopy = [...originalArray];
```

2. 使用Array.from()

```javascript
const originalArray = [1, 2, 3, 4, 5];
const shallowCopy = Array.from(originalArray);
```

3. 使用Array.slice()

```javascript
const originalArray = [1, 2, 3, 4, 5];
const shallowCopy = originalArray.slice();
```

4. 使用Array.concat()

```javascript
const originalArray = [1, 2, 3, 4, 5];
const shallowCopy = originalArray.concat();
```

5. 使用Array.map()

```javascript
const originalArray = [1, 2, 3, 4, 5];
const shallowCopy = originalArray.map(item => item);
```



### 19. 数组对象和原生对象的区别是什么？

**宿主对象（Host Objects）：**

宿主对象是由 JavaScript 运行环境提供的对象，它们的行为由宿主环境定义。在浏览器环境中，宿主对象包括 `window`、`document`、`XMLHttpRequest` 等；在 Node.js 环境中，宿主对象包括 `global`、`process` 等。

宿主对象通常是由宿主环境（如浏览器或 Node.js）提供的，它们不是 ECMAScript 标准的一部分，因此它们的行为可能会因不同的宿主环境而异。

**原生对象（Native Objects）：**

原生对象是由 JavaScript 语言规范定义的对象，它们是 ECMAScript 标准的一部分。原生对象包括以下几种主要类型：

1. **基本数据类型的包装对象（Primitive Wrapper Objects）**：包括 `String`、`Number`、`Boolean`、`Symbol` 和 `BigInt` 等。它们允许对基本数据类型（字符串、数字、布尔值、符号和大整数）进行对象操作。

2. **内置对象（Built-in Objects）**：包括 `Object`、`Array`、`Function`、`Date`、`RegExp`、`Math` 等。这些对象是 JavaScript 语言核心功能的一部分，提供了许多常见的功能和方法。

3. **错误对象（Error Objects）**：包括 `Error`、`SyntaxError`、`TypeError`、`RangeError` 等。这些对象用于表示各种类型的错误。

4. **其他原生对象**：还有一些其他的原生对象，如 `Promise`、`Set`、`Map`、`WeakMap`、`WeakSet` 等，它们提供了更高级的功能和数据结构。



### 20. 简述attribute和property的区别 ？

**Attribute（属性）：**

- **定义**：属性（Attribute）是 HTML 元素在 HTML 文件中声明的特性，它们以键值对的形式出现在 HTML 标签中，用于提供附加信息或配置元素的行为。例如，`<input type="text" value="Hello">` 中的 `type` 和 `value` 就是元素的属性。
- **访问方式**：在 JavaScript 中，可以使用 `getAttribute()` 方法来获取 HTML 元素的属性值，例如 `element.getAttribute('type')`。
- **更新方式**：可以通过设置 HTML 元素的属性值来更新属性，例如 `element.setAttribute('value', 'New Value')`。
- **注意事项**：属性值始终为字符串，即使在 HTML 中它们可能是其他类型的数据。

**Property（属性）：**

- **定义**：属性（Property）是 DOM 元素的 JavaScript 对象表示中的成员，它们是对象的属性，用于描述和控制元素的状态和行为。例如，`element.value` 就是元素的属性。
- **访问方式**：在 JavaScript 中，可以直接访问和修改 DOM 元素的属性，例如 `element.value`。
- **更新方式**：可以通过直接赋值来更新属性，例如 `element.value = 'New Value'`。
- **注意事项**：属性值的数据类型可以是任意类型，取决于具体的属性。有些属性是只读的，不能通过赋值来修改。

**区别总结：**

1. **来源**：Attribute 是 HTML 元素在 HTML 文件中声明的特性，而 Property 是 DOM 元素的 JavaScript 对象表示中的成员。
2. **访问方式**：Attribute 使用 `getAttribute()` 方法进行访问，而 Property 直接通过属性名进行访问。
3. **更新方式**：Attribute 使用 `setAttribute()` 方法进行更新，而 Property 直接通过赋值来更新。
4. **数据类型**：Attribute 的值始终为字符串，而 Property 的值可以是任意类型。
5. **是否只读**：有些 Property 是只读的，不能通过赋值来修改，而 Attribute 可以随时通过设置来更新。



### 21. 简述在Javascript中什么是伪数组？如何将伪数组转化为标准数组？

在 JavaScript 中，伪数组（Pseudo-array）是指具有类似数组的结构和行为，但并不是真正的数组实例的对象。这些对象通常具有类数组的特性，例如具有 `length` 属性和按索引访问元素的能力，但缺少数组的方法和原型属性。

常见的伪数组包括函数的 `arguments` 对象、DOM 元素集合（如 `document.querySelectorAll()` 返回的结果）、和一些内置方法的返回结果等。

**如何将伪数组转化为标准数组？**

有几种方法可以将伪数组转换为标准数组：

1. **Array.from() 方法**：`Array.from()` 方法可以将具有可迭代属性的对象（包括伪数组）转换为一个新的数组。

   ```javascript
   var pseudoArray = document.querySelectorAll('div');
   var newArray = Array.from(pseudoArray);
   ```

2. **Array.prototype.slice.call() 方法**：通过 `Array.prototype.slice.call()` 方法将伪数组转换为数组。

   ```javascript
   var pseudoArray = document.querySelectorAll('div');
   var newArray = Array.prototype.slice.call(pseudoArray);
   ```

3. **扩展运算符 (...)**：使用扩展运算符可以将伪数组转换为数组。

   ```javascript
   var pseudoArray = document.querySelectorAll('div');
   var newArray = [...pseudoArray];
   ```

以上方法都可以将具有类数组结构的对象转换为标准数组，使其可以使用数组的方法和属性。这在处理一些内置方法返回的伪数组或 DOM 元素集合时非常有用。



### 22. ES6有哪些新引入的概念？

1. 箭头函数
2. 块级作用域
3. 解构赋值
4. 模板字面量
5. 默认参数
6. 展开运算符
7. 类
8. Promise
9. 模块化



### 23. 举三个隐式类型强制的例子？

1. 字符串拼接
2. 数值运算
3. 逻辑运算



### 24. JavaScript 是静态类型语言还是动态类型语言？这是什么意思？

JavaScript 是一种动态类型语言。

静态类型语言和动态类型语言的区别在于变量的类型检查时机不同：

1. **静态类型语言**：
   - 在编译阶段进行类型检查，即在代码编写阶段或编译阶段确定变量的数据类型。
   - 在声明变量时必须明确指定变量的类型，并且在编译阶段会进行类型检查，确保变量的使用符合其声明的类型规定。
   - 典型的静态类型语言包括 Java、C++、C# 等。

2. **动态类型语言**：
   - 在运行时进行类型检查，即在代码执行阶段确定变量的数据类型。
   - 变量的类型可以在运行时根据赋值操作自动推断，而不需要显式声明。
   - 变量的类型可以在运行时动态改变。
   - 典型的动态类型语言包括 JavaScript、Python、Ruby 等。

JavaScript 是一种动态类型语言，它的变量类型是在运行时根据赋值操作自动推断的，而不需要显式声明。这意味着可以在任何时候给变量赋任何类型的值，而 JavaScript 引擎会根据当前值的数据类型来确定变量的类型。例如：

```javascript
var x = 10; // x 是一个整数类型
x = 'Hello'; // 现在 x 是一个字符串类型
x = true; // 现在 x 是一个布尔类型
```

这种灵活性和动态性使得 JavaScript 在开发过程中更加灵活和便捷，但也可能导致一些潜在的类型错误。因此，在编写 JavaScript 代码时需要格外注意类型的转换和类型的检查，以避免潜在的错误。



### 25. JavaScript 中的柯里化是什么？用bind或者apply怎么实现？

将一个接受多个参数的函数转换为一系列接受单个参数的函数的过程。

**使用 apply 实现柯里化：**

```javascript
function curriedAdd(x) {
  return function(y, z) {
    return x + y + z;
  };
}

const add5 = curriedAdd.bind(null, 5); // 将第一个参数绑定为 5
console.log(add5.apply(null, [6, 7])); // 输出: 18，相当于调用 add(5, 6, 7)
```

**使用 bind 实现柯里化：**

```javascript
function curriedAdd(x, y, z) {
  return x + y + z;
}

const add5 = curriedAdd.bind(null, 5); // 将第一个参数绑定为 5
console.log(add5(6, 7)); // 输出: 18，相当于调用 add(5, 6, 7)
```



### 26. JavaScript 中的回调函数是什么？为什么要使用回调函数？

回调函数是一种函数，它作为参数传递给另一个函数，并在特定事件发生或异步操作完成后被调用。

使用原因：

1. **处理异步操作**：JavaScript 中的很多操作都是异步的，比如定时器、事件监听、Ajax 请求等。使用回调函数可以在异步操作完成后执行特定的逻辑，以处理异步操作的结果。
2. **避免阻塞**：由于 JavaScript 是单线程执行的，如果某个操作是阻塞的，会导致整个页面无法响应。通过使用回调函数，可以在执行耗时的操作时不阻塞页面的其他操作。
3. **事件驱动编程**：JavaScript 是一种事件驱动的语言，通过事件机制可以实现页面的交互和响应。回调函数常用于处理事件的响应，如点击事件、鼠标移动事件等。
4. **异步编程模式**：回调函数是实现异步编程的重要手段之一，它允许在异步操作完成后执行特定的操作，而不需要等待结果返回。这种模式可以提高程序的性能和响应速度。
5. **代码复用和模块化**：通过将回调函数作为参数传递给其他函数，可以将函数的执行逻辑和处理逻辑分离开来，实现代码的复用和模块化。



### 27. 什么是 JavaScript 中的严格模式？

JavaScript 的严格模式（Strict Mode）是一种 ECMAScript 5 引入的特性，它旨在提供更严格的 JavaScript 解析和错误处理，以改善代码质量、安全性和性能。启用严格模式后，JavaScript 引擎会执行额外的检查，并且会对一些不安全或不规范的语法和行为进行限制。

严格模式可以通过在代码文件或函数体的顶部添加 `'use strict';` 来启用。以下是严格模式的一些特点：

1. **禁止使用全局变量**：在严格模式下，不允许使用未声明的变量。这可以帮助捕获代码中的拼写错误或意外的全局变量声明。

2. **禁止删除变量**：在严格模式下，无法通过 `delete` 操作符删除变量或函数。这有助于防止意外删除全局对象的属性。

3. **禁止使用 `with` 语句**：在严格模式下，禁止使用 `with` 语句。因为 `with` 语句会创建新的作用域链，可能导致代码混淆和性能问题。

4. **禁止对只读属性赋值**：在严格模式下，禁止对只读属性赋值，比如对 `arguments` 和 `caller` 的赋值操作。

5. **禁止使用 `eval` 和 `arguments.callee`**：在严格模式下，`eval` 和 `arguments.callee` 都被禁止使用。因为它们会导致代码执行的不可预测性和安全风险。

6. **强制使用 `this` 的固定化**：在严格模式下，函数中的 `this` 默认为 `undefined`，而不是全局对象。这有助于减少意外的 `this` 绑定错误。

7. **限制 `eval` 在局部作用域中的影响范围**：在严格模式下，使用 `eval` 创建的变量和函数只能在 `eval` 语句内部访问，不会泄漏到周围的作用域。

通过启用严格模式，可以帮助开发人员捕获一些潜在的错误，并使代码更加规范、安全和可靠。因此，在编写新代码时，推荐使用严格模式来提高代码质量和可维护性。



### 28. 为什么要使用严格模式？

1. **更严格的语法和错误检查**：严格模式会对一些不安全或不规范的语法和行为进行限制，并且会在出现错误时抛出异常，这有助于提前发现并修复潜在的问题。

2. **避免全局变量污染**：在严格模式下，不允许使用未声明的变量，这可以帮助捕获代码中的拼写错误或意外的全局变量声明，避免全局变量污染。

3. **提高代码的安全性**：严格模式禁止一些不安全的行为，比如使用 `eval`、`with` 语句等，这可以减少代码被恶意利用的可能性。

4. **固定化 `this` 的值**：在严格模式下，函数中的 `this` 默认为 `undefined`，而不是全局对象，这有助于减少意外的 `this` 绑定错误，并提高代码的可靠性。

5. **提高性能**：由于严格模式下 JavaScript 引擎执行的额外检查，可以提前发现一些潜在的问题，从而提高代码的执行效率和性能。

6. **支持未来的 ECMAScript 标准**：严格模式是 ECMAScript 5 引入的特性，它提供了一些将来 JavaScript 标准中可能引入的特性，使得代码更易于迁移到未来的标准版本中。



### 29. 如何删除属性及其值？

delete



### 30. 简述标签中 defer和 async属性的区别 ？

在 `<script>` 标签中用于控制脚本的加载方式和执行时机，以优化页面性能和用户体验。

1. **defer 属性**：
   - `defer` 属性用于延迟（defer）脚本的执行，直到整个文档解析完成后再执行。
   - 多个拥有 `defer` 属性的脚本按照它们在文档中出现的顺序依次执行。
   - 脚本会在文档的 `DOMContentLoaded` 事件之前执行，但在 `DOMContentLoaded` 事件触发时可能还没有完成执行。
   - 适用于不需要立即执行的脚本，但需要在文档解析完成后执行的场景。

```html
<script src="script.js" defer></script>
```

2. **async 属性**：
   - `async` 属性用于异步（asynchronously）加载脚本，即脚本的下载和执行不会阻塞文档的解析和渲染过程。
   - 多个拥有 `async` 属性的脚本无法保证执行顺序，它们会在下载完成后立即执行，不会等待其他脚本。
   - 脚本的执行时机不确定，可能在文档的解析过程中执行，也可能在文档解析完成后执行，取决于脚本的下载速度和执行上下文。
   - 适用于不需要依赖其他脚本，且不需要等待其他脚本加载完成的场景。

```html
<script src="script.js" async></script>
```

总的来说，`defer` 属性用于延迟脚本的执行，保证脚本在文档解析完成后执行，而 `async` 属性用于异步加载脚本，不会阻塞文档的解析和渲染，但执行时机不确定。根据具体需求和脚本之间的依赖关系，选择合适的属性可以提高页面加载性能和用户体验。



### 31. 为什么不建议在 JavaScript中使用 innerHTML？

在 JavaScript 中使用 `innerHTML` 会带来一些潜在的安全风险和性能问题，因此不建议过度使用。

1. **安全风险**：
   - 直接使用 `innerHTML` 可能导致跨站脚本攻击（XSS），特别是当将未经过滤的用户输入作为 `innerHTML` 的内容插入到页面中时。攻击者可以注入恶意代码或脚本，从而对用户进行钓鱼、窃取敏感信息等攻击。

2. **性能问题**：
   - 使用 `innerHTML` 会导致浏览器重新解析整个 HTML 结构，并重新构建 DOM 树。这个过程可能会消耗大量的 CPU 和内存资源，尤其是当操作大型 HTML 结构时，性能影响会更加显著。
   - 如果只是想更新某个元素的部分内容，使用 `innerHTML` 会比较笨重，因为它会重新渲染整个元素及其所有子元素，而不仅仅是更新目标内容。

3. **可维护性**：
   - 直接使用 `innerHTML` 会使代码变得难以理解和维护，因为它将 HTML 结构和 JavaScript 代码耦合在一起。这样会使代码变得混乱，并且不利于团队合作和代码重构。



### 32. 对象的创建方式有哪些 ?

1. 字面量
2. 构造函数
3. Object.create()
4. ES6中的Class
5. 工厂函数（就是一个函数return一个新的对象实例）



### 33. 为什么说函数是第一类对象？

在 JavaScript 中，函数被认为是第一类对象（First-Class Citizens），这意味着函数具有与其他数据类型相同的特性，可以像普通对象一样被传递、赋值、存储和作为参数传递给其他函数。函数作为第一类对象的特性包括以下几点：

1. **可以被赋值给变量**：
   - 函数可以被赋值给变量，成为变量的值。

   ```javascript
   function greet() {
     console.log('Hello, world!');
   }
   
   let sayHello = greet;
   sayHello(); // 输出: Hello, world!
   ```

2. **可以作为参数传递给其他函数**：
   - 函数可以作为参数传递给其他函数。

   ```javascript
   function greet(name) {
     console.log('Hello, ' + name + '!');
   }
   
   function sayHello(callback) {
     callback('John');
   }
   
   sayHello(greet); // 输出: Hello, John!
   ```

3. **可以作为返回值从其他函数返回**：
   - 函数可以作为另一个函数的返回值返回。

   ```javascript
   function createGreeting() {
     return function(name) {
       console.log('Hello, ' + name + '!');
     };
   }
   
   let greet = createGreeting();
   greet('John'); // 输出: Hello, John!
   ```

4. **可以存储在数据结构中**：
   - 函数可以存储在数组、对象等数据结构中。

   ```javascript
   let functions = [
     function() { console.log('Function 1'); },
     function() { console.log('Function 2'); }
   ];
   
   functions[0](); // 输出: Function 1
   functions[1](); // 输出: Function 2
   ```



### 34. 函数声明与函数表达式的区别？

1. **语法**：
   - 函数声明使用 `function` 关键字，后面跟着函数名和函数体，如 `function myFunction() { // 函数体 }`。
   - 函数表达式将函数赋值给变量，可以是匿名函数或具名函数，如 `let myFunction = function() { // 函数体 }` 或 `let myFunction = function myFunc() { // 函数体 }`。

2. **提升（Hoisting）**：
   - 函数声明会被提升到当前作用域的顶部，因此可以在函数声明之前调用函数，而不会报错。
   - 函数表达式不会被提升，只有在执行到函数表达式所在的代码行时才会被解析和赋值，因此不能在声明之前调用函数。

```javascript
// 函数声明
myFunction(); // 可以调用，不会报错

function myFunction() {
  console.log('Function Declaration');
}

// 函数表达式
// myFunctionExpression(); // 会报错，函数表达式尚未赋值

let myFunctionExpression = function() {
  console.log('Function Expression');
};

myFunctionExpression(); // 可以调用
```

3. **命名**：
   - 函数声明可以有一个名称（函数名），可以在函数内部调用自身（递归调用）。
   - 函数表达式可以是匿名的，也可以有一个名称，但是函数名只在函数内部有效，不能在外部使用。

```javascript
// 函数声明
function myFunction() {
  console.log('Function Declaration');
  myFunction(); // 可以调用自身
}

// 函数表达式（匿名函数）
let myFunctionExpression = function() {
  console.log('Function Expression');
};

// 函数表达式（具名函数）
let myNamedFunctionExpression = function myNamedFunc() {
  console.log('Named Function Expression');
  // myNamedFunc(); // 可以调用自身，但只能在函数内部调用
};
```



### 35. 如何将对象转换为数组？

使用 JavaScript 中的 `Object.values()` 方法。



### 36. 事件冒泡机制是什么？

事件冒泡机制的特点包括：

1. **由内向外的传播**：事件从触发事件的元素开始向外传播，逐级触发父元素的事件处理程序。
2. **逐级触发**：在冒泡过程中，每个父元素上相同类型的事件处理程序都会被触发，直到到达根节点。
3. **可以取消**：在冒泡过程中，可以通过调用 `event.stopPropagation()` 方法来阻止事件继续向上传播，即停止事件冒泡。



### 37. 数组去重的方式有哪些？

1. **使用Set数据结构**：
   - Set是一种集合类型，其中的元素是唯一的，可以利用这个特性实现数组去重。
   ```javascript
   let arr = [1, 2, 2, 3, 3, 4, 5, 5];
   let uniqueArr = [...new Set(arr)];
   console.log(uniqueArr); // [1, 2, 3, 4, 5]
   ```

2. **利用indexOf或includes方法**：
   - 遍历原数组，判断新数组中是否已经包含当前元素，若不包含则添加到新数组中。
   ```javascript
   let arr = [1, 2, 2, 3, 3, 4, 5, 5];
   let uniqueArr = [];
   arr.forEach(item => {
       if (!uniqueArr.includes(item)) {
           uniqueArr.push(item);
       }
   });
   console.log(uniqueArr); // [1, 2, 3, 4, 5]
   ```

3. **使用filter方法**：
   - 利用filter方法和indexOf或includes方法实现去重。
   ```javascript
   let arr = [1, 2, 2, 3, 3, 4, 5, 5];
   let uniqueArr = arr.filter((item, index, array) => {
       return array.indexOf(item) === index;
   });
   console.log(uniqueArr); // [1, 2, 3, 4, 5]
   ```

4. **利用reduce方法**：
   - 使用reduce方法遍历原数组，将不重复的元素添加到新数组中。
   ```javascript
   let arr = [1, 2, 2, 3, 3, 4, 5, 5];
   let uniqueArr = arr.reduce((prev, curr) => {
       if (!prev.includes(curr)) {
           prev.push(curr);
       }
       return prev;
   }, []);
   console.log(uniqueArr); // [1, 2, 3, 4, 5]
   ```



### 38. 简述Set、Map、WeakSet 和 WeakMap 的区别 ？

| 特点                | Set                            | Map                    | WeakSet          | WeakMap            |
| ------------------- | ------------------------------ | ---------------------- | ---------------- | ------------------ |
| 类型                | 集合                           | 键值对集合             | 弱引用集合       | 弱引用键值对集合   |
| 元素唯一性          | 是                             | 键唯一，值可重复       | 是               | 键弱引用，值可重复 |
| 元素类型            | 任意类型（基本类型和引用类型） | 任意类型（键和值均可） | 引用类型         | 引用类型           |
| 有序性              | 有序                           | 有序                   | 无序             | 无序               |
| 可枚举性            | 是                             | 是                     | 否               | 否                 |
| 键的可直接访问      | 否                             | 否                     | 否               | 否                 |
| 键/值的个数获取方法 | size 属性                      | size 属性              | 无法获取         | 无法获取           |
| 主要用途            | 存储唯一值                     | 存储键值对             | 存储对象的弱引用 | 存储对象的弱引用   |



### 39. 简述ES6 的 class 和构造函数的区别 ？

1. **语法**：
   - ES6 的 class 是一种语法糖，提供了更加清晰和面向对象的语法，使得创建和继承类更加简洁和易读。
   - 构造函数是 JavaScript 中传统的创建对象的方式，使用函数来定义对象的结构和行为。

2. **继承机制**：
   - ES6 的 class 提供了更加直观的继承机制，通过 extends 关键字可以轻松地实现类的继承。
   - 构造函数通过原型链来实现继承，需要手动设置子类的原型对象指向父类的实例，实现起来较为复杂。

3. **构造函数**：
   - ES6 的 class 中使用 constructor 方法来定义构造函数，用于初始化实例对象的状态和行为。
   - 构造函数可以通过函数声明、函数表达式或箭头函数来定义，没有特定的关键字。

4. **静态方法和实例方法**：
   - ES6 的 class 中可以定义静态方法和实例方法，通过 static 关键字来定义静态方法，直接在类上调用；实例方法则定义在类的原型上。
   - 构造函数也可以定义静态方法和实例方法，但语法上没有特定的关键字来区分，需要手动判断方法是添加在构造函数上还是原型上。

5. **严格模式**：
   - 在 ES6 的 class 中，类的所有方法（包括静态方法和实例方法）默认都是严格模式。
   - 构造函数中，如果没有明确声明使用严格模式，方法执行时将默认使用非严格模式。

综上所述，ES6 的 class 提供了更加现代化和直观的语法来创建和继承类，使得面向对象编程更加容易和优雅。与传统的构造函数相比，class 更符合人们对于面向对象编程的直觉和需求。



### 40. class的本质是构造函数吗？

是的，ES6 中的 class 本质上还是构造函数。尽管 class 语法提供了更加清晰和面向对象的语法，但在 JavaScript 引擎内部，class 仍然是基于原型和构造函数的实现。

在 JavaScript 中，class 声明只是一种语法糖，它实际上是构造函数的一种简洁写法，提供了更加直观和易读的方式来定义对象的结构和行为。当使用 class 声明一个类时，实际上是在创建一个构造函数，并将类中定义的方法添加到该构造函数的原型对象上。

下面是一个使用 class 声明类的简单示例：

```javascript
class MyClass {
    constructor(name) {
        this.name = name;
    }
    
    greet() {
        console.log(`Hello, ${this.name}!`);
    }
}

const obj = new MyClass('World');
obj.greet(); // 输出: Hello, World!
```

上述代码实际上等价于以下使用构造函数的写法：

```javascript
function MyClass(name) {
    this.name = name;
}

MyClass.prototype.greet = function() {
    console.log(`Hello, ${this.name}!`);
};

const obj = new MyClass('World');
obj.greet(); // 输出: Hello, World!
```

因此，虽然 class 语法让 JavaScript 看起来更像传统的面向对象语言，但在底层实现上，class 本质上还是构造函数和原型的组合。



### 41. 简述如何监听对象属性的改变？

在 JavaScript 中，要监听对象属性的改变，可以使用以下几种方法：

1. **Object.defineProperty()**：
   - 使用 `Object.defineProperty()` 方法可以定义或修改对象的属性，并在属性的读取或赋值时触发 getter 和 setter 函数。
   ```javascript
   const obj = {};
   Object.defineProperty(obj, 'name', {
       get() {
           return this._name;
       },
       set(value) {
           this._name = value;
           console.log('name属性被修改了');
       }
   });
   obj.name = 'Alice'; // 输出: 'name属性被修改了'
   ```

2. **Proxy**：
   - 使用 Proxy 对象可以代理另一个对象并拦截该对象的操作，包括读取和设置属性的操作。
   ```javascript
   const obj = {};
   const handler = {
       set(target, key, value) {
           target[key] = value;
           console.log(`${key}属性被修改了`);
           return true;
       }
   };
   const proxy = new Proxy(obj, handler);
   proxy.name = 'Bob'; // 输出: 'name属性被修改了'
   ```











## API

### 1. map和foreach的异同是什么？

`map` 和 `forEach` 都是 JavaScript 中用于遍历数组的方法，它们有相似之处，也有一些区别。

相同点：

1. **用途**：`map` 和 `forEach` 都用于遍历数组中的每个元素，并对每个元素执行指定的操作。

2. **参数**：它们都接受一个回调函数作为参数，回调函数会在遍历数组的每个元素时被调用。

不同点：

1. **返回值**：
   - `map` 方法返回一个新数组，其中包含回调函数的返回值。
   - `forEach` 方法没有返回值，它只是用于遍历数组，而不会生成新的数组。

2. **使用场景**：
   - `map` 通常用于对数组中的每个元素进行操作，并将操作结果存储在新数组中。例如，可以使用 `map` 方法将数组中的每个元素都加倍。
   - `forEach` 通常用于遍历数组并执行一些操作，例如打印数组的每个元素或对数组中的元素进行更改，但它不会创建新的数组。

3. **可中断性**：
   - `forEach` 方法无法被中断，它会遍历完整个数组，不论是否在回调函数中返回 `false`。
   - `map` 方法在回调函数返回 `false` 时会终止遍历，并返回已经处理的元素构成的新数组。



### 2. JavaScript阻止默认事件？

- 阻止元素的默认事件：

  `event.preventDefault()`

- 阻止元素冒泡事件：

  `event.stopPropagation()`



### 3. for...in、for...of、for三种区别？

- for...in

  输出对象的key

- for...of

  遍历数组中的元素

- for

  正常循环



### 4. 常用的数组方法？

JavaScript 中常用的数组方法包括：

1. **push()**：向数组末尾添加一个或多个元素，并返回新数组的长度。
2. **pop()**：从数组末尾移除最后一个元素，并返回移除的元素。
3. **shift()**：从数组头部移除第一个元素，并返回移除的元素。
4. **unshift()**：向数组头部添加一个或多个元素，并返回新数组的长度。
5. **splice()**：从数组中添加或删除元素，可以灵活操作数组。
6. **concat()**：合并两个或多个数组，返回一个新数组。
7. **slice()**：返回数组的指定部分（浅拷贝），不修改原数组。
8. **indexOf()**：返回指定元素在数组中的索引，如果不存在返回 -1。
9. **lastIndexOf()**：返回指定元素在数组中的最后一个索引，如果不存在返回 -1。
10. **includes()**：判断数组是否包含某个元素，返回布尔值。
11. **forEach()**：遍历数组的每个元素，执行指定的回调函数。
12. **map()**：遍历数组的每个元素，执行指定的回调函数，并返回执行结果组成的新数组。
13. **filter()**：遍历数组的每个元素，执行指定的回调函数，并返回满足条件的元素组成的新数组。
14. **reduce()**：对数组的每个元素执行指定的累积函数，返回一个累积值。
15. **every()**：检测数组的每个元素是否满足指定条件，如果全部满足返回 true，否则返回 false。
16. **some()**：检测数组的至少一个元素是否满足指定条件，如果有满足的返回 true，否则返回 false。
17. **find()**：返回数组中满足指定条件的第一个元素，如果找不到返回 undefined。
18. **findIndex()**：返回数组中满足指定条件的第一个元素的索引，如果找不到返回 -1。
19. **sort()**：对数组进行排序，默认是按照字符串 Unicode 编码进行排序。
20. **reverse()**：颠倒数组中元素的顺序。

这些数组方法可以帮助开发者对数组进行各种操作，包括增删改查、遍历、筛选、转换等。



### 5. 常用字符串方法 ？

JavaScript 中常用的字符串方法包括：

1. **charAt()**：返回指定索引位置的字符。
2. **charCodeAt()**：返回指定索引位置的字符的 Unicode 编码。
3. **concat()**：连接两个或多个字符串，并返回新字符串。
4. **indexOf()**：返回指定字符第一次出现的索引位置，如果未找到返回 -1。
5. **lastIndexOf()**：返回指定字符最后一次出现的索引位置，如果未找到返回 -1。
6. **slice()**：提取字符串的片段，并返回新字符串。
7. **substring()**：提取字符串的片段，与 slice() 类似，但不支持负索引。
8. **substr()**：提取字符串的片段，从指定位置开始指定长度，并返回新字符串。
9. **startsWith()**：检查字符串是否以指定字符开头，返回布尔值。
10. **endsWith()**：检查字符串是否以指定字符结尾，返回布尔值。
11. **includes()**：检查字符串是否包含指定字符，返回布尔值。
12. **toUpperCase()**：将字符串转换为大写。
13. **toLowerCase()**：将字符串转换为小写。
14. **trim()**：去除字符串两端的空格。
15. **replace()**：替换字符串中的指定字符或模式。
16. **split()**：将字符串分割为数组，根据指定的分隔符。
17. **charAt()**：返回指定索引位置的字符。
18. **match()**：检测字符串中是否匹配指定的正则表达式，返回匹配的结果。
19. **search()**：检索字符串中指定的子字符串，返回匹配的位置。
20. **repeat()**：将字符串重复指定次数。

这些字符串方法可以帮助开发者对字符串进行各种操作，包括查找、替换、截取、转换大小写、分割、连接等。



### 6. Set和Map的异同是什么？

好的，让我们使用 Set 和 Map 来举例说明它们的用法。

Set 示例：

```javascript
// 创建一个 Set 对象
let uniqueNumbers = new Set();

// 添加元素到 Set 中
uniqueNumbers.add(1);
uniqueNumbers.add(2);
uniqueNumbers.add(3);
uniqueNumbers.add(2); // 重复添加相同的值，不会产生效果

// 判断 Set 中是否包含某个元素
console.log(uniqueNumbers.has(2)); // true
console.log(uniqueNumbers.has(4)); // false

// 获取 Set 中元素的个数
console.log(uniqueNumbers.size); // 3

// 删除 Set 中的元素
uniqueNumbers.delete(2);

// 清空 Set 中的所有元素
uniqueNumbers.clear();

// 查看最终的 Set 对象
console.log(uniqueNumbers); // Set {}
```

Map 示例：

```javascript
// 创建一个 Map 对象
let userData = new Map();

// 添加键值对到 Map 中
userData.set('name', 'John');
userData.set('age', 30);
userData.set('name', 'Jane'); // 覆盖已有的键值对

// 获取 Map 中指定键的值
console.log(userData.get('name')); // 'Jane'
console.log(userData.get('gender')); // undefined

// 判断 Map 中是否包含某个键
console.log(userData.has('age')); // true
console.log(userData.has('gender')); // false

// 获取 Map 中键值对的个数
console.log(userData.size); // 2

// 删除 Map 中的键值对
userData.delete('age');

// 清空 Map 中的所有键值对
userData.clear();

// 查看最终的 Map 对象
console.log(userData); // Map {}
```

这些示例展示了如何使用 Set 和 Map 对象，以及它们的常用方法。Set 适合用于存储一组唯一的值，而 Map 则适合用于存储键值对。



### 7. map和weakmap的区别是什么？

Map：

1. **引用类型**：Map 是一种强引用类型，它的键是强引用，不会被垃圾回收机制回收。

2. **键类型**：Map 的键可以是任意类型的值，包括基本类型和对象引用。

3. **迭代器**：Map 提供了用于迭代其键值对的方法，如 `forEach()`、`entries()`、`keys()`、`values()` 等。

4. **内存管理**：Map 中的键值对在不再被引用时，仍然会占用内存，不会被自动释放。

WeakMap：

1. **引用类型**：WeakMap 是一种弱引用类型，它的键是弱引用，有可能被垃圾回收机制回收。

2. **键类型**：WeakMap 的键必须是对象类型，不能是基本类型，否则会抛出 TypeError。

3. **迭代器**：WeakMap 不提供用于迭代的方法，因为无法确定键是否被垃圾回收。

4. **内存管理**：WeakMap 中的键值对在不再被引用时，会被自动释放，因此可以用于临时存储对象的私有数据，避免内存泄漏。

总结：

- Map 适合用于存储键值对，并且键值对需要长期保留的情况。
- WeakMap 适合用于临时存储对象的私有数据，避免内存泄漏，并且键值对的生命周期与键的引用一致。



### 8. 箭头函数的特性？

- 箭头函数没有自己的this，会捕获其所在的上下文的this值，作为自己的this值
- 箭头函数没有constructor，是匿名函数，不能作为构造函数，不能通过new 调用；
- 没有new.target 属性。在通过new运算符被初始化的函数或构造方法中，new.target返回一个指向构造方法或函数的引用。在普通的函数调用中，new.target 的值是undefined
- 箭头函数不绑定arguments 对象。取而代之用rest参数...解决。由于 箭头函数没有自己的this指针，通过 call() 或 apply() 方法调用一个函数时，只能传递参数（不能绑定this），他们的第一个参数会被忽略。（这种现象对于bind方法同样成立）
- 箭头函数通过 call() 或 apply() 方法调用一个函数时，只传入了一个参数，对 this 并没有影响。
- 箭头函数没有原型属性 Fn.prototype 值为 undefined
- 箭头函数不能当做Generator函数,不能使用yield关键字



### 9. document.onload和document.ready两个事件的区别？

**区别总结：**

1. **触发时机**：`document.onload` 在整个页面和外部资源加载完成后触发，而 `document.ready` 在 DOM 结构构建完成后触发。
2. **适用范围**：`document.onload` 适用于整个页面加载完成后执行操作，而 `document.ready` 适用于在 DOM 结构构建完成后立即执行操作，不需要等待所有外部资源加载完成。
3. **跨浏览器兼容性**：`document.onload` 是原生 JavaScript 的事件，跨浏览器兼容性好；而 `document.ready` 是 jQuery 提供的，需要引入 jQuery 库才能使用，且不同的库可能实现方式不同。



### 10. 函数参数arguments是数组吗？

`arguments` 是一个类数组对象，而不是一个真正的数组。它包含了函数调用时传递的所有参数，并且具有一些数组的特性，但不是一个真正的数组。

`arguments` 对象具有以下特点：

1. **类数组对象**：`arguments` 对象类似于数组，可以通过索引访问参数，例如 `arguments[0]` 访问第一个参数，但它不具有数组的所有方法，如 `push()`、`pop()` 等。
2. **动态性**：`arguments` 对象是动态的，它会随着函数调用时传递的参数而变化，无论函数定义时有多少个参数，都可以通过 `arguments.length` 访问到传递的参数数量。
3. **不具有数组的方法**：`arguments` 对象虽然类似于数组，但不具有数组的方法，例如 `push()`、`pop()`、`forEach()` 等。但是可以使用数组的方法间接操作 `arguments`，比如通过 `Array.prototype.slice.call(arguments)` 将其转换为真正的数组后再操作。
4. **不具有数组的原型**：`arguments` 对象不继承自 `Array`，而是继承自 `Object`，因此它不具有数组的原型方法和属性。



### 11. eval 的作用？

`eval()` 是 JavaScript 中的一个内置函数，用于将字符串作为代码来执行。它的作用是将传入的字符串作为 JavaScript 代码进行解析和执行，从而动态地生成并执行代码。

**注意事项：**

1. **性能问题**：`eval()` 函数会在执行时动态解析和执行字符串，可能会导致性能问题。此外，由于 `eval()` 可以执行任意 JavaScript 代码，因此可能存在安全风险，尤其是当执行的字符串来自不可信来源时。

2. **变量提升**：在 `eval()` 中定义的变量会提升到 `eval()` 所在的作用域，而不是保持在 `eval()` 的作用域中。这可能会导致变量提升的意外行为。

3. **严格模式**：在严格模式下，`eval()` 的行为会有所不同，其中一些限制和安全性提高的机制会生效。



### 12. split、slice、splice函数区别？

这三个函数在 JavaScript 中都用于操作字符串或数组，但它们的功能和用法有所不同。

**1. `split()` 方法：**

- **功能**：`split()` 方法用于将字符串分割成子字符串，并将结果存储在数组中。
- **语法**：`string.split(separator, limit)`
- **参数**：
  - `separator`：指定分割字符串的分隔符。
  - `limit`（可选）：指定返回的数组的最大长度。
- **示例**：

```javascript
var str = "Hello, world!";
var parts = str.split(", "); // 分割字符串，结果为 ["Hello", "world!"]
```

**2. `slice()` 方法：**

- **功能**：`slice()` 方法从数组或字符串中提取指定范围的子数组或子字符串。
- **语法**：
  - 数组：`array.slice(start, end)`
  - 字符串：`string.slice(start, end)`
- **参数**：
  - `start`：指定提取的起始位置（包含）。
  - `end`（可选）：指定提取的结束位置（不包含）。
- **示例**：

```javascript
var arr = [1, 2, 3, 4, 5];
var subArray = arr.slice(1, 4); // 提取索引为 1 到 3 的子数组，结果为 [2, 3, 4]

var str = "Hello, world!";
var subString = str.slice(7); // 提取从索引为 7 开始的子字符串，结果为 "world!"
```

**3. `splice()` 方法：**

- **功能**：`splice()` 方法用于修改数组，可以删除、替换或插入元素，并返回被删除的元素组成的数组。
- **语法**：`array.splice(start, deleteCount, item1, item2, ...)`
- **参数**：
  - `start`：指定修改的起始位置。
  - `deleteCount`：指定要删除的元素个数。
  - `item1, item2, ...`（可选）：要插入到数组中的新元素。
- **示例**：

```javascript
var arr = [1, 2, 3, 4, 5];
var removedItems = arr.splice(1, 2); // 删除从索引为 1 开始的两个元素，结果为 [2, 3]
// arr 变成 [1, 4, 5]

var arr2 = [1, 2, 3];
arr2.splice(1, 1, 'a', 'b'); // 从索引为 1 的位置删除一个元素，并插入 'a' 和 'b'
// arr2 变成 [1, 'a', 'b', 3]
```

**区别总结：**

1. `split()` 方法用于字符串的分割，`slice()` 方法用于提取字符串或数组的子字符串或子数组，`splice()` 方法用于修改数组。
2. `split()` 方法返回一个新数组，`slice()` 方法返回一个新的字符串或数组，`splice()` 方法返回被删除的元素组成的数组。
3. `split()` 方法只适用于字符串，`slice()` 方法适用于字符串和数组，`splice()` 方法只适用于数组。



### 13. isNaN(-1/0)结果是什么？

isNaN(-Infinity)，结果是false



### 14. documen.wrte和 innerHTML的区别是什么？

`document.write()` 和 `innerHTML` 都是用于向 HTML 文档中插入内容的方法，但它们之间有一些重要的区别：

1. **作用对象**：
   - `document.write()` 方法直接作用于整个文档，它可以在文档加载过程中的任何时候调用，并将指定的内容写入到文档流中。如果在文档已经加载完毕后调用 `document.write()`，它会清空整个文档并重写内容。
   - `innerHTML` 属性是 DOM 元素的属性，用于设置或获取元素的 HTML 内容。它通常用于替换或更新特定元素的内容，而不影响其他部分的文档结构。

2. **执行时机**：
   - `document.write()` 方法在文档加载过程中的任何时候都可以调用，会立即将内容写入到文档流中，对页面的渲染产生影响。如果在文档加载完毕后调用 `document.write()`，它会清空整个文档并重写内容，因此通常不推荐在文档加载完成后使用。
   - `innerHTML` 属性可以在文档加载后任何时候修改，它不会影响文档的加载和渲染过程，只会修改指定元素的内容。

3. **安全性**：
   - 由于 `document.write()` 方法直接操作文档流，因此在动态生成内容时可能会导致不可预料的结果，例如在文档加载完成后调用 `document.write()` 可能会覆盖整个文档。
   - `innerHTML` 属性相对安全一些，因为它只会修改指定元素的内容，不会影响其他部分的文档结构。但是仍然需要注意防范 XSS 攻击，确保插入的内容是安全的。



### 15. JavaScript中读取文件的方法是什么？

在客户端 JavaScript 中，通常无法直接读取文件系统中的文件，因为浏览器限制了对文件系统的访问。然而，可以通过以下几种方式在浏览器中读取文件：

1. **使用 `<input type="file">` 元素**：
   - 可以通过在 HTML 中添加 `<input type="file">` 元素来让用户选择文件，并通过 JavaScript 来读取所选文件的内容。通过 `FileReader` 对象可以读取文件内容，并进行相应的操作。

   ```html
   <input type="file" id="fileInput">
   ```

   ```javascript
   let fileInput = document.getElementById('fileInput');
   
   fileInput.addEventListener('change', function() {
     let file = fileInput.files[0];
     let reader = new FileReader();
   
     reader.onload = function(event) {
       let contents = event.target.result;
       console.log(contents); // 输出文件内容
     };
   
     reader.readAsText(file);
   });
   ```

2. **使用 AJAX 请求**：
   - 可以通过 AJAX 请求来获取服务器上的文件内容。在服务器端提供一个接口，客户端发送 AJAX 请求到该接口，服务器返回文件内容。

   ```javascript
   let xhr = new XMLHttpRequest();
   xhr.open('GET', 'file.txt', true);
   xhr.onreadystatechange = function() {
     if (xhr.readyState === XMLHttpRequest.DONE && xhr.status === 200) {
       let contents = xhr.responseText;
       console.log(contents); // 输出文件内容
     }
   };
   xhr.send();
   ```

3. **使用 Fetch API**：
   - Fetch API 是 JavaScript 提供的现代的网络请求 API，可以方便地进行网络请求，包括获取文件内容。

   ```javascript
   fetch('file.txt')
     .then(response => response.text())
     .then(contents => {
       console.log(contents); // 输出文件内容
     })
     .catch(error => {
       console.error('Error:', error);
     });
   ```



### 16. 如何将base字符串转换为 integer？

可以使用 `parseInt()` 函数，并根据需要指定进制参数。



### 17. void(0)的作用是什么？

作用是在不改变当前页面的情况下防止浏览器执行默认的行为或跳转到新页面。

具体来说，`void` 是一个操作符，用于指示表达式的返回值为 undefined。在 `void(0)` 中，`(0)` 是一个被 `void` 操作符处理的数字表达式，其结果始终是 undefined。由于它返回 undefined，因此 `void(0)` 可以用来代替 JavaScript 中的 "javascript:void(0)"，在某些情况下用作 HTML 锚点的 href 属性，以防止页面跳转。

例如，在 HTML 中，你可能会看到类似以下的代码：

```html
<a href="javascript:void(0);" onclick="someFunction()">Click me</a>
```

这里的 `javascript:void(0);` 用于在用户点击链接时不触发页面跳转，而是执行 `someFunction()` 函数。使用 `void(0)` 的另一个常见场景是在 JavaScript 中的事件处理程序中，当你想要执行某个动作但不需要返回值时使用。

总之，`void(0)` 的作用是在 JavaScript 中生成一个永远返回 undefined 的表达式，用于阻止浏览器执行默认的操作或页面跳转。



### 18. 如何获得 CheckBox状态？

访问复选框的 `checked` 属性。这个属性返回一个布尔值，表示复选框是否被选中。

例如，假设你有一个 HTML 复选框元素：
```html
<input type="checkbox" id="myCheckbox">
```

你可以使用 JavaScript 来获取它的状态：
```javascript
var checkbox = document.getElementById("myCheckbox");
var isChecked = checkbox.checked;

if (isChecked) {
    console.log("Checkbox is checked.");
} else {
    console.log("Checkbox is not checked.");
}
```

在这个例子中，`isChecked` 变量将包含布尔值，表示复选框的状态。如果复选框被选中，`isChecked` 将为 `true`，否则为 `false`。



### 19. 如何判断当前节点类型？

要判断当前节点的类型，可以使用节点对象的 `nodeType` 属性。`nodeType` 属性返回一个表示节点类型的数字值，通过这个值可以判断节点的类型。

常见的 `nodeType` 值及对应的节点类型如下：

- 元素节点：`nodeType` 的值为 `1`。
- 文本节点：`nodeType` 的值为 `3`。
- 注释节点：`nodeType` 的值为 `8`。
- 文档节点：`nodeType` 的值为 `9`。
- 文档类型节点：`nodeType` 的值为 `10`。

例如，要判断一个节点是否是元素节点，可以这样写：

```javascript
if (node.nodeType === 1) {
    console.log("This node is an element node.");
}
```

或者，你也可以使用节点对象的 `nodeType` 属性和相应的常量来判断：

```javascript
if (node.nodeType === Node.ELEMENT_NODE) {
    console.log("This node is an element node.");
}
```

这样可以提高代码的可读性和可维护性。



### 20. Document Load 和 DOMContentLoaded 的区别？

文档加载（Document Load）和 DOMContentLoaded 事件都与网页加载和渲染相关，但它们发生的时机和目的略有不同：

1. **文档加载（Document Load）**：
   - 文档加载指的是浏览器完成解析 HTML 文件并加载了所有外部资源（如图片、样式表、脚本等）后的状态。当整个文档及其依赖资源都已加载完毕时，浏览器触发文档加载事件（通常是 `window` 对象的 `load` 事件）。
   - 通常情况下，文档加载事件表示整个页面已经完全加载并准备好与用户交互。这时，页面中的所有 DOM 元素和外部资源都已经可用。

2. **DOMContentLoaded 事件**：
   - DOMContentLoaded 事件在 HTML 文档解析完成并且 DOM 树构建完毕后触发。在这个时刻，页面的文档结构已经完全生成，但可能还有一些外部资源（如图片、样式表、脚本等）尚未加载完成。
   - DOMContentLoaded 事件的触发表示页面的 DOM 结构已经可以访问和操作，但页面的外部资源可能还在加载中。因此，DOMContentLoaded 事件常用于在页面加载完成后执行 JavaScript 初始化操作，而不需要等待所有外部资源加载完成。

总之，文档加载事件（如 `load` 事件）表示整个页面以及所有资源都已加载完成，而 DOMContentLoaded 事件表示页面的 DOM 结构已经构建完成，但页面的外部资源可能尚未加载完成。DOMContentLoaded 事件常用于执行与 DOM 结构相关的初始化操作，而不需要等待所有外部资源加载完成。



### 21. freeze() 方法有什么作用？

JavaScript 中的 `Object.freeze()` 方法用于冻结对象，使其不可修改。一旦一个对象被冻结，就无法向其添加新的属性、删除现有属性或修改属性的值。被冻结的对象也无法被解冻。

`Object.freeze()` 方法的作用包括：

1. **防止属性被修改**：冻结对象后，无法修改对象的属性值。
2. **防止属性被添加**：冻结对象后，无法向对象添加新的属性。
3. **防止属性被删除**：冻结对象后，无法删除对象的属性。

`Object.freeze()` 方法只能冻结对象自身的属性，而不能冻结对象内部的属性。如果对象的属性值是对象或数组等可变对象，则需要递归调用 `Object.freeze()` 来冻结其内部对象。



### 22. 如何获取对象的键列表？

要获取 JavaScript 对象的键列表，你可以使用以下方法：

1. **使用 Object.keys() 方法**：
   - `Object.keys()` 方法返回一个包含对象自身可枚举属性的键的数组。
   ```javascript
   const obj = {
     name: 'John',
     age: 30,
     gender: 'male'
   };
   
   const keys = Object.keys(obj);
   console.log(keys); // 输出：["name", "age", "gender"]
   ```

2. **使用 for...in 循环**：
   - 使用 for...in 循环遍历对象的属性，然后将每个属性添加到数组中。
   ```javascript
   const obj = {
     name: 'John',
     age: 30,
     gender: 'male'
   };
   
   const keys = [];
   for (let key in obj) {
     keys.push(key);
   }
   console.log(keys); // 输出：["name", "age", "gender"]
   ```

这两种方法都可以获取对象的键列表，但要注意，`Object.keys()` 方法只返回对象自身的可枚举属性的键，而不包括继承的属性。而 for...in 循环会遍历对象的自身和继承的可枚举属性。



### 23. 请问什么是箭头函数以及特性 ？

JavaScript 的箭头函数（Arrow Functions）是 ES6（ECMAScript 2015）中引入的一种新的函数声明语法，它提供了一种更简洁的方式来声明函数，并且改变了函数内部的 `this` 绑定。

箭头函数的基本语法如下：

```javascript
// 无参数箭头函数
const func = () => {
  // 函数体
};

// 单个参数箭头函数
const func = param => {
  // 函数体
};

// 多个参数箭头函数
const func = (param1, param2) => {
  // 函数体
};

// 简写的箭头函数（如果函数体只有一条语句，则可以省略大括号）
const func = () => expression;

// 如果函数体有多条语句，则需要使用大括号，并使用 return 显式返回值
const func = () => {
  // 逻辑
  return expression;
};
```

箭头函数与传统函数的不同之处在于：

1. **更简洁的语法**：箭头函数的语法更加简洁，特别是在函数体只有一条语句时，可以省略大括号和 `return` 关键字。

2. **没有自己的 `this` 绑定**：箭头函数没有自己的 `this` 绑定，它继承了外部作用域的 `this` 值。这意味着在箭头函数内部访问的 `this` 是定义时所在的作用域的 `this`，而不是执行时的 `this`。

3. **不能作为构造函数**：由于箭头函数没有自己的 `this`，因此不能用作构造函数，也就是说不能使用 `new` 关键字来调用箭头函数。

箭头函数通常用于编写短小的匿名函数或回调函数，以及在函数内部需要访问外部作用域的 `this` 值时。然而，由于箭头函数没有自己的 `this` 绑定，因此不适合用于需要动态绑定 `this` 的场景，例如在对象的方法中。



### 24. new 一个构造函数，如果函数返回 return {} 、 return null ， return 1 ， return true 会发生什么情况 ？

1. 如果构造函数返回一个对象（使用 `return {}` 或类似的方式返回一个新创建的对象），那么 `new` 操作将返回该对象，而不是新创建的实例对象。
   
   ```javascript
   function Example() {
       return {};
   }
   
   let instance = new Example();
   console.log(instance); // 输出 {}
   ```

2. 如果构造函数返回 `null`，那么 `new` 操作将忽略该返回值，返回的仍然是新创建的实例对象。

   ```javascript
   function Example() {
       return null;
   }

   let instance = new Example();
   console.log(instance instanceof Example); // 输出 true
   ```

3. 如果构造函数返回一个非对象的值，如 `1` 或 `true`，那么 `new` 操作将忽略该返回值，返回的仍然是新创建的实例对象。

   ```javascript
   function Example() {
       return 1;
   }
   
   let instance = new Example();
   console.log(instance instanceof Example); // 输出 true
   ```



### 25. 如何判断一个对象是不是空对象 ？

1. **使用Object.keys()方法**：
   ```javascript
   function isEmpty(obj) {
       return Object.keys(obj).length === 0;
   }
   ```

2. **使用for...in循环**：
   ```javascript
   function isEmpty(obj) {
       for (let key in obj) {
           if (obj.hasOwnProperty(key)) {
               return false;
           }
       }
       return true;
   }
   ```

3. **使用Object.getOwnPropertyNames()方法**：
   ```javascript
   function isEmpty(obj) {
       return Object.getOwnPropertyNames(obj).length === 0;
   }
   ```

4. **使用JSON.stringify()方法**：
   ```javascript
   function isEmpty(obj) {
       return JSON.stringify(obj) === '{}';
   }
   ```



### 26. 简述document.write的用法 ？

`document.write()` 是 JavaScript 中的一个方法，用于向文档中写入 HTML 文本或内容。它的基本用法如下：

```javascript
document.write(text);
```

其中，text 是要写入文档的 HTML 文本或内容。

`document.write()` 方法会将指定的文本直接写入到当前文档的输出流中。如果在文档加载完成后调用 `document.write()`，它会将新的文本直接写入到文档中，并覆盖掉原来的文档内容。因此，一般不推荐在页面加载完成后再使用 `document.write()`，因为这样会覆盖掉整个文档。

通常情况下，`document.write()` 主要用于在文档加载过程中动态生成 HTML 内容。例如，在脚本中动态生成一些内容，并将其直接写入到文档中：

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>document.write Example</title>
</head>
<body>

<script>
document.write('<h1>Hello, World!</h1>');
</script>

</body>
</html>
```

在这个示例中，`document.write()` 方法被用来动态生成一个 `<h1>` 标题，并将其写入到文档中。当浏览器解析到这个脚本时，会立即执行 `document.write()` 方法，将生成的标题直接写入到文档中。

总的来说，`document.write()` 方法是一个比较简单的方法，主要用于在文档加载过程中动态生成 HTML 内容，但在实际开发中需要谨慎使用，避免不必要的副作用。



### 27. 为什么多次document.write()不会覆盖又覆盖？

`document.write()` 的行为取决于它被调用的时机。

1. **在文档加载过程中**：
   - 如果 `document.write()` 在文档加载过程中被调用，它会将新的文本直接写入到文档中，并覆盖掉之前的文档内容。每次调用 `document.write()` 都会覆盖前一次写入的内容。

2. **在文档加载完成后**：
   - 如果 `document.write()` 在文档加载完成后被调用，它会将新的文本写入到文档中的当前位置。每次调用 `document.write()` 都会在之前的文本后面追加新的内容。

因此，如果 `document.write()` 在文档加载过程中被多次调用，每次调用都会覆盖掉之前的文档内容；但如果在文档加载完成后调用，每次调用都会在文档末尾追加新的内容，而不会覆盖掉之前的内容。



### 28. 怎么识别是文档加载完还是加载过程中？

要识别文档是否已经加载完成，可以通过检查 `document.readyState` 属性。这个属性表示当前文档的加载状态，有以下几个可能的值：

- `"loading"`：文档正在加载。
- `"interactive"`：文档已经完成加载，正在解析。
- `"complete"`：文档已经完全加载完成。

你可以在 JavaScript 中监听 `DOMContentLoaded` 事件来检测文档何时完成解析，而在 `load` 事件中检测文档何时完全加载完成。这样，你就可以根据 `document.readyState` 的值来判断文档加载的状态。

以下是一个示例：

```javascript
document.addEventListener('DOMContentLoaded', function() {
    if (document.readyState === 'interactive' || document.readyState === 'complete') {
        console.log('Document parsing is complete.');
    } else {
        console.log('Document is still loading.');
    }
});

window.addEventListener('load', function() {
    if (document.readyState === 'complete') {
        console.log('Document is fully loaded.');
    } else {
        console.log('Document is still loading.');
    }
});
```

在这个示例中，我们监听了 `DOMContentLoaded` 和 `load` 事件，并在事件处理函数中检查 `document.readyState` 的值。根据文档加载的状态输出不同的信息。

`window.onload` 事件是当整个页面及所有依赖资源（例如图片、样式表等）都加载完成后触发的事件。与 `DOMContentLoaded` 事件不同，`window.onload` 等待页面中所有资源加载完成后才会触发，包括图片、样式表、脚本等。

因此，使用 `window.onload` 事件来检测文档是否加载完成是非常可靠的方法。以下是一个示例：

```javascript
window.onload = function() {
    console.log('Document and all resources are fully loaded.');
};
```

在这个示例中，当整个文档及其所有依赖资源都加载完成后，`window.onload` 事件被触发，然后执行指定的事件处理函数。











## This

### 1. this的绑定规则是什么？

实际上this 是在运行时进行绑定的，并不是在编写时绑定，它的上下文取决于函数调 用时的各种条件。

this 的绑定和函数声明的位置没有任何关系，只取决于函数的调用方式。 总结: 函数被调用时发生 this 绑定，this 指向什么完全取决于函数在哪里被调用。

1. 默认绑定（严格/非严格模式）

   window

2. 隐式绑定

   函数调用的this绑定到上下文对象

3. 显式绑定

   call，bind，apply

4. new绑定

   执行[prototype]链接，绑定到函数调用的this



### 2. call，bind和apply的异同是什么？

`bind`、`apply` 和 `call` 是 JavaScript 中用于修改函数执行上下文的方法，它们有一些相似之处，但也有一些不同之处。

相同点：

1. **修改函数执行上下文**：`bind`、`apply` 和 `call` 都可以用于修改函数的执行上下文，即指定函数中 `this` 关键字所指向的对象。

不同点：

1. **参数传递方式**：
   - `bind`：返回一个新函数，新函数会将指定的对象作为执行上下文，并将指定的参数作为新函数的参数。
   - `apply`：接受两个参数，第一个参数是要绑定的执行上下文，第二个参数是一个数组或类数组对象，数组中的元素会作为参数传递给函数。
   - `call`：接受一个参数列表，第一个参数是要绑定的执行上下文，后续参数是要传递给函数的参数，每个参数都会直接传递给函数。

2. **返回值**：
   - `bind`：返回一个绑定了指定上下文的新函数，但不会立即执行该函数。
   - `apply` 和 `call`：立即调用函数，并指定函数的执行上下文和参数，返回函数执行的结果。

3. **使用场景**：
   - `bind`：常用于绑定函数的执行上下文，并在稍后的时间点调用该函数。
   - `apply` 和 `call`：常用于立即调用函数，并指定函数的执行上下文和参数。`apply` 适用于参数以**数组形式**存在的情况，而 `call` 适用于参数以**单独列举**的情况。

总的来说，`bind`、`apply` 和 `call` 都是用于修改函数执行上下文的方法，它们的主要区别在于参数传递方式、返回值和使用场景。



### 3. 自己如何实现一个bind？

实现一个简单的 `bind` 方法可以帮助理解函数的 `this` 绑定机制。

`bind` 方法用于创建一个新函数，并将指定的对象绑定为新函数的上下文（即函数内部的 `this` 指向指定的对象）。下面是一个简单的 `bind` 方法的实现：

```javascript
Function.prototype.myBind = function(context) {
    const fn = this; // 当前函数
    const args = Array.prototype.slice.call(arguments, 1); // 获取除第一个参数（context）外的其他参数

    return function() {
        const bindArgs = Array.prototype.slice.call(arguments); // 获取新函数的参数
        return fn.apply(context, args.concat(bindArgs)); // 将原函数的参数和新函数的参数合并，并以指定的上下文调用原函数
    };
};
```

使用示例：

```javascript
const person = {
    name: 'Alice'
};

function greet(message) {
    console.log(`${message}, ${this.name}!`);
}

const boundGreet = greet.myBind(person, 'Hello');
boundGreet(); // 输出: Hello, Alice!
```

在上面的实现中，`myBind` 方法通过原型链将 `bind` 方法添加到 `Function.prototype` 上，从而使所有函数实例都可以调用 `bind` 方法。在返回的新函数内部，通过闭包的方式保存了原函数 `fn` 和绑定的上下文 `context`，然后调用 `fn.apply(context, args.concat(bindArgs))` 来将原函数的参数和新函数的参数合并，并以指定的上下文调用原函数。











## 原型链

### 1. 原型，原型链 ? 有什么特点？

JavaScript 中的原型（prototype）和原型链（prototype chain）是理解 JavaScript 面向对象编程的关键概念之一。它们具有以下特点：

1. **原型（prototype）**：
   - 每个 JavaScript 对象都有一个原型对象（prototype），它是对象的一个属性，可以是另一个对象或者 null。
   - 原型对象用于继承属性和方法，当对象访问一个不存在的属性或方法时，JavaScript 引擎会沿着原型链查找，直到找到对应的属性或方法或者到达原型链的尽头（null）。

2. **原型链（prototype chain）**：
   - 原型链是由对象的原型对象（prototype）组成的链式结构。
   - 当访问对象的属性或方法时，JavaScript 引擎会首先在对象本身上查找，如果找不到则沿着原型链向上查找，直到找到对应的属性或方法或者到达原型链的尽头。
   - 原型链的尽头是 Object.prototype，它是所有对象的根原型。

3. **特点**：
   - JavaScript 中的对象是通过原型链来实现继承的。
   - 对象的属性和方法可以在其原型对象上定义，所有该对象的实例都可以共享这些属性和方法。
   - 当修改对象的原型对象时，所有该对象的实例都会受到影响，因为它们共享同一个原型对象。
   - 原型链的存在使得 JavaScript 具有了动态性和灵活性，可以方便地扩展和修改对象的属性和方法。

总之，JavaScript 的原型和原型链是实现对象之间继承关系的机制，通过原型链，对象可以共享原型对象上的属性和方法，实现了高效的代码复用和扩展。











## 同步异步

### 1. async await 和promise和generator有什么区别？

`async/await` 和 Promise 是处理 JavaScript 异步编程的两种主要方式，而 Generator 函数也可以用于实现异步操作，但它们之间有一些区别和优劣势。

Promise：

- Promise 是 ES6 新增的一种异步编程解决方案，它可以更清晰、更简洁地处理异步操作。
- Promise 可以轻松地处理多个异步操作，通过链式调用 `then()` 方法或使用 `async/await` 来解决回调地狱问题。
- Promise 可以通过 `resolve()` 和 `reject()` 来返回异步操作的结果或错误。
- Promise 有三种状态：pending（进行中）、fulfilled（已成功）和rejected（已失败），可以通过 `then()` 方法或 `catch()` 方法处理这些状态。

async/await：

- `async/await` 是 ES2017（ES8）新增的一种异步编程语法糖，基于 Promise 实现，可以更优雅地处理异步代码。
- `async` 关键字用于定义一个异步函数，该函数内部可以使用 `await` 关键字来暂停执行并等待 Promise 解决或拒绝。
- `await` 关键字只能在 `async` 函数内部使用，用于等待 Promise 对象的状态改变，并返回异步操作的结果。
- `async/await` 让异步代码看起来像同步代码，提高了代码的可读性和可维护性。

Generator：

- Generator 是 ES6 新增的一种特殊函数，可以通过 `function*` 关键字来定义。
- Generator 函数内部使用 `yield` 关键字可以使函数执行停止，并返回一个可迭代对象，用于实现惰性计算和异步操作。
- Generator 函数的执行可以通过 `next()` 方法控制，每次调用 `next()` 方法会使函数执行到下一个 `yield` 关键字处，直到函数执行完毕或遇到 `return` 关键字为止。

总结：

- 使用 Promise 可以更灵活地处理异步操作，并且可以解决回调地狱问题。
- `async/await` 提供了一种更优雅、更直观的异步编程方式，让异步代码看起来像同步代码。
- Generator 函数可以用于实现惰性计算和异步操作，但相对于 Promise 和 `async/await`，它的语法更复杂，使用起来相对不那么直观。



### 2. 手写promise ？

参考手撕文件夹下的笔记。



### 3. promise.all()的作用？

1. **并行执行多个异步操作**：`Promise.all` 可以同时发起多个异步操作，并且在所有操作完成后才返回结果。这对于需要同时进行多个异步操作并且在所有操作完成后处理结果的场景非常有用。

2. **等待所有异步操作完成**：`Promise.all` 可以用于等待多个异步操作全部完成后再执行后续操作。例如，在前端开发中，可以使用 `Promise.all` 等待多个网络请求全部完成后再更新页面。



### 4. 异步编程有哪几种方式？

1. **回调函数（Callbacks）**：
   - 回调函数是 JavaScript 中最早的异步编程方式之一。通过将一个函数作为参数传递给另一个函数，在需要时调用这个函数来处理异步操作的结果。

2. **Promise 对象**：
   - Promise 是 ES6 引入的一种用于处理异步操作的对象。它表示一个异步操作的最终完成（或失败）及其结果的值。

3. **async/await**：
   - async/await 是 ES8 引入的异步编程新特性，它建立在 Promise 的基础之上，提供了一种更直观、更简洁的编程方式，使异步代码看起来像同步代码一样。



### 5. promises中的race method是什么意思？

`Promise.race()` 方法通常用于竞速操作，例如在多个异步操作中只关心第一个完成的情况，或者设置超时功能，等待第一个操作完成。



### 6. promise 的 finally 怎么实现的？

`finally` 方法是 Promise 的一个实例方法，它在 Promise 完成（无论是 resolve 还是 reject）后始终会执行，无论 Promise 的状态是成功还是失败。



### 7. Promise 构造函数是同步执行还是异步执行，那么 then 方法呢 ？

Promise 构造函数是同步执行的，而 then 方法是异步执行的。












## 通信

### 1. 跨域的解决方案有哪些？

在 JavaScript 中，跨域（Cross-Origin）指的是在浏览器中加载的网页尝试与不同源（即协议、域名或端口）的服务器进行交互，由于同源策略的限制，这种跨域请求通常会受到限制。为了解决跨域问题，可以采用以下几种方案：

1. **JSONP（JSON with Padding）**：JSONP 是一种利用 `<script>` 标签可以跨域加载的特性来实现跨域通信的方法。它的原理是通过在页面中动态创建 `<script>` 标签，指向一个包含 JSON 数据的 URL，服务器返回的数据会被当做 JavaScript 脚本执行，从而实现跨域数据的获取。

2. **CORS（Cross-Origin Resource Sharing）**：CORS 是一种由服务器端实现的跨域解决方案，通过在服务器端设置响应头来指示浏览器是否允许跨域请求。可以通过设置 `Access-Control-Allow-Origin` 头来允许特定源的请求，还可以设置其他 CORS 相关头来控制跨域请求的行为，比如允许的请求方法、允许的请求头等。

3. **代理（Proxy）**：通过在服务器端设置代理来转发请求，从而绕过浏览器的同源策略限制。例如，在前端将请求发送到同源的服务器，然后由同源服务器转发请求到目标服务器，最后将响应返回给前端，这样就实现了跨域请求。

4. **WebSocket**：WebSocket 是一种双向通信协议，可以在浏览器和服务器之间建立持久连接，实现实时通信。由于 WebSocket 不受同源策略的限制，因此可以用于跨域通信。

5. **跨文档消息传递（Cross-document Messaging）**：通过 `window.postMessage()` 方法来发送消息，实现不同窗口或 iframe 之间的跨域通信。这种方式适用于同一浏览器窗口下的跨域通信，但不适用于跨浏览器窗口的通信。

6. **跨域资源嵌入（Cross-Origin Resource Embedding）**：通过在 HTML 中使用 `<link>`、`<script>`、`<img>` 等标签来加载跨域资源，从而实现跨域数据的获取。例如，可以通过在页面中插入 `<img>` 标签来获取图片资源，或者通过 `<script>` 标签来加载 JSONP 数据。

这些方法各有优缺点，具体应根据实际情况选择合适的跨域解决方案。



### 2. 什么是长轮询？

长轮询（Long Polling）是一种实现实时数据更新的技术，它是一种 HTTP 长连接的变种。在长轮询中，客户端向服务器发送一个请求，服务器保持请求打开直到有新的数据可用或超时。一旦有新数据可用，服务器立即响应请求，客户端收到响应后立即再次发送新的请求，以保持连接。

长轮询的特点包括：

- **实时性较高**：长轮询允许服务器立即响应有新数据可用的请求，从而实现实时更新的效果。
- **较高的资源消耗**：由于长轮询需要维持大量的连接，因此会增加服务器的资源消耗。
- **延迟较高**：长轮询会导致客户端和服务器之间的延迟较高，因为客户端需要等待服务器响应才能发送新的请求。

长轮询适用于需要实时更新的应用场景，比如在线聊天、实时通知等。然而，由于其资源消耗较高和延迟较高的特点，随着 WebSocket 技术的发展，长轮询已经逐渐被 WebSocket 所取代，WebSocket 在实时通信方面更加高效和灵活。



### 3. HTTP 响应状态码都有哪些？

HTTP 响应状态码表示服务器对请求的处理结果，分为以下几类：

1. 1xx（Informational）：请求已接收，继续处理。
2. 2xx（Success）：请求成功接收并处理。
   - 200 OK：请求成功。
   - 201 Created：资源已被成功创建。
   - 204 No Content：请求成功，但响应不包含任何内容。
3. 3xx（Redirection）：需要进行额外操作以完成请求。
   - 301 Moved Permanently：资源已永久移动到新位置。
   - 302 Found：资源暂时移动到新位置。
   - 304 Not Modified：客户端已缓存的资源未修改。
4. 4xx（Client Error）：请求包含错误或无法完成请求。
   - 400 Bad Request：请求无效。
   - 401 Unauthorized：未授权访问。
   - 403 Forbidden：禁止访问资源。
   - 404 Not Found：未找到资源。
5. 5xx（Server Error）：服务器无法完成请求。
   - 500 Internal Server Error：服务器内部错误。
   - 502 Bad Gateway：上游服务器返回无效响应。
   - 503 Service Unavailable：服务器暂时无法处理请求。



### 4. 阐述Javascript的同源策略？

同源策略（Same-Origin Policy）是浏览器中一种重要的安全策略，用于限制来自不同源（Origin）的文档或脚本对当前文档的访问。

两个 URL 具有相同的 origin，如果它们具有相同的协议（protocol）、主机（host）和端口（port）。

同源策略的限制：

1. **JavaScript 限制**：来自不同源的 JavaScript 脚本不能访问当前文档的 DOM，也不能通过 AJAX 等方式获取当前文档的内容。

2. **Cookie 限制**：浏览器限制了来自不同源的页面对当前页面的 Cookie 的读取。即使在相同的浏览器标签页中，不同源的页面也无法访问彼此的 Cookie。

3. **DOM 限制**：来自不同源的页面无法通过 JavaScript 直接操作彼此的 DOM 结构。











## 场景

### 1. 手写防抖和节流，同时他们的区别是什么？

参考手撕文件夹下的笔记。



### 2. 常见的setInterval导致内存泄露的场景有哪些？

以下是一些常见的可能导致 `setInterval` 导致内存泄漏的场景：

1. **未清除定时器**：
   - 如果在使用 `setInterval` 后没有及时清除定时器，定时器会一直存在并周期性地执行指定的代码，这可能导致对执行过的代码仍然保持引用，从而造成内存泄漏。

   ```javascript
   let counter = 0;
   let intervalId = setInterval(function() {
     console.log('Counter:', counter);
     counter++;
   }, 1000);
   
   // 忘记清除定时器
   ```

2. **在循环中创建定时器**：
   - 如果在循环中创建定时器，并且每个定时器都在一段时间后执行，但未在每个循环迭代中清除上一个定时器，可能会导致大量的定时器实例积累，从而造成内存泄漏。

   ```javascript
   for (let i = 0; i < 10; i++) {
     setInterval(function() {
       console.log('Counter:', i);
     }, 1000);
   }
   ```

3. **定时器中保持了对外部变量的引用**：
   - 如果在定时器中使用了闭包，并且闭包中保持了对外部变量的引用，即使定时器执行完成，这些变量也不会被释放，可能会造成内存泄漏。

   ```javascript
   let someData = fetchData(); // 获取一些数据
   
   setInterval(function() {
     // 闭包中保持了对外部变量 someData 的引用
     process(someData);
   }, 1000);
   ```

4. **DOM 元素变量未被释放**：
   - 如果在定时器中引用了 DOM 元素，并且这些 DOM 元素在定时器执行完成后应该被销毁，但是却未被正确清除，可能会导致 DOM 元素及其关联的事件处理器等无法被释放，从而造成内存泄漏。

   ```javascript
   let element = document.getElementById('someElement');
   
   setInterval(function() {
     // 对 DOM 元素进行操作
     element.style.color = 'red';
   }, 1000);
   
   // element 应该在不需要时被清除
   ```



### 3. 简述Number() 的存储空间是多大？如果后台发送了一个超过最大自己的数字怎么办 ？

在 JavaScript 中，`Number` 类型使用双精度浮点数来表示所有数字。双精度浮点数使用 64 位（8 字节）来存储，其中 1 位用于符号位（0 表示正数，1 表示负数），11 位用于指数部分，剩下的 52 位用于尾数（即有效数字部分）。

JavaScript 中可以表示的最大数值为 `Number.MAX_VALUE`，约为 1.7976931348623157e+308，最小的数值为 `Number.MIN_VALUE`，约为 5e-324。超出这个范围的数字将被表示成 `Infinity`（正无穷大）或 `-Infinity`（负无穷大）。

如果后台发送了一个超过 JavaScript 能表示的最大数值的数字，通常情况下会导致该数字被表示成 `Infinity`。在处理这种情况时，可以考虑以下几种方式：

1. **使用科学计数法发送数据**：如果可能的话，将超过最大数值的数字表示成科学计数法形式，以便 JavaScript 能够正确解析。

2. **对数据进行分段处理**：如果超出最大数值的数字是作为一个整体来使用的，可以将其拆分成多个较小的数值进行处理，然后再进行合并或计算。

3. **进行数据截断或舍入**：根据具体的业务需求，可以将超出范围的数字截断或进行舍入处理，使其落在 JavaScript 能够表示的范围内。

4. **使用库或工具进行处理**：可以使用第三方库或工具来处理超出范围的数字，这些库通常提供了更灵活和高效的处理方式，可以更好地应对各种情况。



### 4. 请分别用深度优先思想和广度优先思想实现一个拷贝函数？

**深度优先思想：**

```javascript
function deepCopyDFS(obj) {
    if (typeof obj !== 'object' || obj === null) {
        // 如果不是对象或者为null，直接返回原始值
        return obj;
    }

    let newObj = Array.isArray(obj) ? [] : {};
    
    for (let key in obj) {
        if (obj.hasOwnProperty(key)) {
            newObj[key] = deepCopyDFS(obj[key]);
        }
    }
    
    return newObj;
}
```

深度优先思想的拷贝函数会递归地遍历对象的所有属性，并深度拷贝每个属性的值。如果属性值是对象，则继续递归地拷贝，直到遇到基本类型或 null。

**广度优先思想：**

```javascript
function deepCopyBFS(obj) {
    if (typeof obj !== 'object' || obj === null) {
        // 如果不是对象或者为null，直接返回原始值
        return obj;
    }

    let queue = [obj]; // 使用队列存储待拷贝的对象
    let cloned = {}; // 存储已经拷贝过的对象

    while (queue.length > 0) {
        let current = queue.shift();
        let keys = Object.keys(current);

        for (let key of keys) {
            let value = current[key];
            if (typeof value === 'object' && value !== null && !cloned[value]) {
                // 如果属性值是对象且没有被拷贝过，则将其放入队列中
                queue.push(value);
                cloned[value] = Array.isArray(value) ? [] : {}; // 初始化拷贝对象
            }
            cloned[current][key] = value;
        }
    }

    return cloned[obj];
}
```

广度优先思想的拷贝函数会按层级逐步拷贝对象的属性值，首先拷贝第一层属性值，然后逐层深入拷贝子对象的属性值，直到所有的属性值都被拷贝完成。



### 5. 简述拖拽功能的实现 ？

拖拽功能的实现通常涉及以下几个步骤：

1. **注册事件监听器**：
   - 首先，需要为要拖拽的元素注册事件监听器，通常包括 mousedown、mousemove 和 mouseup 事件。

2. **处理鼠标按下事件**：
   - 当鼠标按下时，记录下鼠标按下时的坐标和被拖拽元素的初始位置。

3. **处理鼠标移动事件**：
   - 当鼠标移动时，计算鼠标移动的距离，并更新被拖拽元素的位置。

4. **处理鼠标释放事件**：
   - 当鼠标释放时，清除事件监听器，完成拖拽操作。

下面是一个简单的拖拽功能实现的示例代码：

HTML：
```html
<div id="draggable" style="width: 100px; height: 100px; background-color: red;"></div>
```

JavaScript：
```javascript
const draggableElement = document.getElementById('draggable');
let isDragging = false;
let offsetX, offsetY;

draggableElement.addEventListener('mousedown', (event) => {
    isDragging = true;
    offsetX = event.clientX - draggableElement.getBoundingClientRect().left;
    offsetY = event.clientY - draggableElement.getBoundingClientRect().top;
});

document.addEventListener('mousemove', (event) => {
    if (isDragging) {
        const x = event.clientX - offsetX;
        const y = event.clientY - offsetY;
        draggableElement.style.left = `${x}px`;
        draggableElement.style.top = `${y}px`;
    }
});

document.addEventListener('mouseup', () => {
    isDragging = false;
});
```

在这个示例中，当鼠标按下时，记录下鼠标按下时的坐标和被拖拽元素的初始位置；当鼠标移动时，计算鼠标移动的距离，并更新被拖拽元素的位置；当鼠标释放时，清除事件监听器，完成拖拽操作。



### 6. 简述怎么控制一次加载一张图片，加载完后再加载下一张 ？

要实现一次加载一张图片，并在加载完一张图片后再加载下一张，可以使用 JavaScript 中的图片预加载技术和事件监听机制。下面是一种实现方式：

1. **准备图片资源**：
   - 首先，将所有需要加载的图片资源的 URL 存储在一个数组中。

2. **预加载图片**：
   - 使用 JavaScript 动态创建图片对象，并为每张图片添加 onload 事件监听器。
   - 每张图片加载完成后，在 onload 事件处理函数中检查是否还有未加载的图片，若有，则加载下一张图片。

下面是一个实现示例：

```javascript
const imageUrls = ['image1.jpg', 'image2.jpg', 'image3.jpg'];
let currentIndex = 0;

function preloadImage() {
    const image = new Image();
    image.onload = function() {
        console.log(`Image ${currentIndex + 1} loaded`);
        currentIndex++;
        if (currentIndex < imageUrls.length) {
            preloadImage();
        } else {
            console.log('All images loaded');
        }
    };
    image.src = imageUrls[currentIndex];
}

preloadImage();
```

在这个示例中，imageUrls 数组存储了需要加载的图片资源的 URL。preloadImage 函数用于预加载图片，它动态创建图片对象，并为每张图片添加 onload 事件监听器。每张图片加载完成后，在 onload 事件处理函数中，检查是否还有未加载的图片，若有，则加载下一张图片。当所有图片都加载完成后，输出 "All images loaded"。

**实际例子：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Image Preloading Example</title>
</head>
<body>

<div id="image-container"></div>

<script>
const imageUrls = ['image1.jpg', 'image2.jpg', 'image3.jpg'];
let currentIndex = 0;

function preloadImage() {
    const image = new Image();
    image.onload = function() {
        document.getElementById('image-container').appendChild(image);
        console.log(`Image ${currentIndex + 1} loaded`);
        currentIndex++;
        if (currentIndex < imageUrls.length) {
            preloadImage();
        } else {
            console.log('All images loaded');
        }
    };
    image.src = imageUrls[currentIndex];
}

preloadImage();
</script>

</body>
</html>
```



### 7. 实现所有对象的深度克隆 （ 包装对象Date 对象 ，正则对象）？

要实现 JavaScript 中所有对象的深度克隆，包括包装对象（如 Date 对象）和正则对象，可以使用递归和一些特殊处理来处理不同类型的对象。下面是一个实现深度克隆的示例函数：

```javascript
function deepClone(obj) {
    // 如果是基本类型或 null，则直接返回
    if (typeof obj !== 'object' || obj === null) {
        return obj;
    }

    // 如果是日期对象，则创建一个新的日期对象
    if (obj instanceof Date) {
        return new Date(obj.getTime());
    }

    // 如果是正则对象，则创建一个新的正则对象
    if (obj instanceof RegExp) {
        return new RegExp(obj);
    }

    // 如果是数组，则递归地克隆数组的每个元素
    if (Array.isArray(obj)) {
        return obj.map(item => deepClone(item));
    }

    // 如果是对象，则递归地克隆对象的每个属性
    const clonedObj = {};
    for (let key in obj) {
        if (obj.hasOwnProperty(key)) {
            clonedObj[key] = deepClone(obj[key]);
        }
    }
    return clonedObj;
}
```

这个 deepClone 函数接受一个对象作为参数，返回该对象的深度克隆副本。

在函数体内部，首先检查对象的类型。如果是基本类型或 null，则直接返回。如果是日期对象，则创建一个新的日期对象，复制原日期对象的时间。如果是正则对象，则创建一个新的正则对象，复制原正则对象的模式和标志。如果是数组，则递归地克隆数组的每个元素。如果是对象，则递归地克隆对象的每个属性，并将克隆后的属性添加到新的对象中。

这样，通过递归调用 deepClone 函数，就可以实现对 JavaScript 中所有对象的深度克隆。



### 8. 简述  JS  的全排列 ？

在 JavaScript 中，可以使用递归的方式来实现全排列（Permutation）算法。全排列是一种将给定数组中的元素重新排列，使得所有可能的排列组合都被列举出来的算法。

下面是一个简单的 JavaScript 函数，用于生成给定数组的全排列：

```javascript
function permute(nums) {
    const result = [];

    function backtrack(current, remaining) {
        if (remaining.length === 0) {
            result.push(current);
            return;
        }

        for (let i = 0; i < remaining.length; i++) {
            const nextCurrent = current.concat(remaining[i]);
            const nextRemaining = remaining.slice(0, i).concat(remaining.slice(i + 1));
            backtrack(nextCurrent, nextRemaining);
        }
    }

    backtrack([], nums);
    return result;
}
```

这个 permute 函数接受一个数组 nums 作为参数，返回该数组的全排列。

在函数内部，定义了一个 backtrack 函数，用于递归地生成全排列。backtrack 函数接受两个参数：当前已生成的排列（current）和剩余待排列的元素（remaining）。

如果剩余待排列的元素为空数组，则将当前已生成的排列添加到结果数组中，然后返回。否则，遍历剩余待排列的元素，将每个元素依次加入当前排列，并递归地生成下一轮排列。

通过递归调用 backtrack 函数，不断地生成排列，直到所有可能的排列都被生成完成。最终，返回结果数组，其中包含了给定数组的所有全排列。

下面是一个使用示例：

```javascript
const nums = [1, 2, 3];
console.log(permute(nums)); // 输出所有全排列：[[1, 2, 3], [1, 3, 2], [2, 1, 3], [2, 3, 1], [3, 1, 2], [3, 2, 1]]
```

这样，通过递归生成全排列的算法，可以很方便地获取给定数组的所有排列组合。











## 性能

### 1. 垃圾回收方法？

JavaScript 的垃圾回收是自动进行的，开发者无需手动介入。JavaScript 的垃圾回收器会周期性地扫描内存中的对象，并标记那些不再被引用的对象，然后释放它们所占用的内存空间。

JavaScript 中的主要垃圾回收方法包括：

1. **标记-清除算法（Mark and Sweep）**：这是 JavaScript 中最常见的垃圾回收算法。它通过标记不再使用的对象，然后清除那些被标记的对象来回收内存。标记阶段会遍历所有的可访问对象，并标记为活动对象，而清除阶段会清除未标记的对象。

2. **引用计数（Reference Counting）**：这是一种比较简单的垃圾回收方法，在每个对象中维护一个引用计数器，记录有多少个引用指向该对象。当引用计数为零时，说明对象不再被引用，可以被回收。然而，引用计数方法容易出现循环引用的情况，导致内存泄漏。



### 2. 举一个闭包会影响垃圾回收的例子？

这种行为有时会导致内存泄漏的问题，特别是在使用闭包的时候需要注意避免循环引用。例如，在事件处理函数中创建了一个闭包，并将该事件处理函数绑定到 DOM 元素上，如果不及时解绑事件处理函数，那么闭包中引用的外部变量将会一直存在，即使 DOM 元素被销毁，也无法被垃圾回收器回收。



### 3. 封装 JavaScript源文件的全部内容到一个函数块有什么意义？

1. **隔离作用域**：
   - 将整个 JavaScript 文件的代码放入一个函数块中可以创建一个局部作用域，防止函数内部的变量和函数污染全局命名空间，避免命名冲突和意外修改全局变量。

2. **防止变量提升**：
   - JavaScript 中的变量提升可能导致意外的行为，将代码封装在函数块中可以避免这种情况。在函数内部声明的变量不会受到变量提升的影响，保证代码的可预测性和可维护性。

3. **创建闭包**：
   - 将代码封装在函数中可以创建闭包，使得内部变量和函数在函数外部无法直接访问，从而增加了数据的私有性和安全性。

4. **模块化开发**：
   - 使用 IIFE 可以将代码模块化，使得代码更易于管理、测试和维护。每个模块都可以独立地定义自己的作用域，从而提高代码的可重用性和可扩展性。

5. **优化性能**：
   - 在某些情况下，将代码封装在函数块中可以提高代码的执行效率，因为它可以减少全局作用域的搜索时间。

综上所述，将 JavaScript 源文件的全部内容封装到一个函数块中可以提高代码的可维护性、可读性和性能，并且可以防止全局作用域污染和意外的行为，是一种良好的编码实践。



### 4. 如何在页面加载后执行 JavaScript 代码？

在页面加载后执行 JavaScript 代码有多种方法，其中最常见的包括：

1. **使用 window.onload 事件**：
   - `window.onload` 事件在整个页面（包括其所有内部元素和外部资源）加载完成后触发。你可以将要执行的 JavaScript 代码放在 `window.onload` 事件处理程序中。
   ```html
   <script>
       window.onload = function() {
           // 在页面加载完成后执行的 JavaScript 代码
       };
   </script>
   ```

2. **使用 DOMContentLoaded 事件**：
   - `DOMContentLoaded` 事件在页面的 DOM 结构加载完成后触发，此时不需要等待外部资源（如图片、样式表）加载完成。这使得它比 `window.onload` 更早地触发，因此更适合执行不需要等待外部资源加载的 JavaScript 代码。
   ```html
   <script>
       document.addEventListener('DOMContentLoaded', function() {
           // 在 DOM 结构加载完成后执行的 JavaScript 代码
       });
   </script>
   ```

3. **将 JavaScript 代码放在 body 元素底部**：
   - 将 JavaScript 代码放在 `<body>` 元素的末尾，这样可以确保 JavaScript 代码在页面的 HTML 内容加载完成后执行，但在外部资源加载完成前执行。
   ```html
   <body>
       <!-- 页面内容 -->
       
       <script>
           // 在页面加载后执行的 JavaScript 代码
       </script>
   </body>
   ```

4. **使用 defer 或 async 属性加载外部脚本**：
   - 使用 `<script>` 标签的 `defer` 或 `async` 属性来加载外部 JavaScript 文件，可以在页面加载后异步执行脚本。
   ```html
   <script defer src="example.js"></script>
   ```
   或
   ```html
   <script async src="example.js"></script>
   ```

这些方法都可以在页面加载后执行 JavaScript 代码，你可以根据需要选择其中之一。



### 5. NoScript标签有什么作用？

如果用户的浏览器不支持JavaScript，或者用户主动禁用了JavaScript，那么被`<noscript>`标签包含的内容会被显示出来。











## 设计模式

### 1. 继承的多种方式有哪些？分别是什么？优缺点？

JavaScript 中实现继承的方式有多种，每种方式都有其特点和适用场景。以下是常见的几种继承方式：

1. **原型链继承**：
   - 原型链继承通过将子类的原型指向父类的实例来实现继承。
   - 缺点是所有子类实例共享同一个父类实例的属性，容易造成属性共享和污染的问题。
   - 示例：
     ```javascript
     function Parent() {
       this.name = 'Parent';
     }
     function Child() {}
     Child.prototype = new Parent();
     ```

2. **构造函数继承（借用构造函数）**：
   - 构造函数继承通过在子类构造函数内部调用父类构造函数来实现继承。
   - 缺点是不能继承父类原型上的属性和方法。
   - 示例：
     ```javascript
     function Parent() {
       this.name = 'Parent';
     }
     function Child() {
       Parent.call(this);
     }
     ```

3. **组合继承（原型链 + 构造函数）**：
   - 组合继承结合了原型链继承和构造函数继承的优点，既可以继承父类的原型属性和方法，又可以实现实例属性的独立。
   - 缺点是在创建子类实例时，会调用两次父类构造函数，导致父类实例属性被重复添加。
   - 示例：
     ```javascript
     function Parent() {
       this.name = 'Parent';
     }
     function Child() {
       Parent.call(this);
     }
     Child.prototype = new Parent();
     Child.prototype.constructor = Child;
     ```

4. **原型式继承**：
   - 原型式继承通过复制一个对象作为新对象的原型来实现继承。
   - 缺点是所有属性都是共享的，没有办法实现属性的独立。
   - 示例：
     ```javascript
     var parent = {
       name: 'Parent'
     };
     var child = Object.create(parent);
     ```

5. **寄生式继承**：
   - 寄生式继承是在原型式继承的基础上增强了对象，返回增强后的对象作为子类。
   - 缺点是同样无法实现属性的独立，且增强函数会产生额外的消耗。
   - 示例：
     ```javascript
     function createChild(obj) {
       var child = Object.create(obj);
       child.sayHello = function() {
         console.log('Hello!');
       };
       return child;
     }
     ```

6. **寄生组合式继承**：
   - 寄生组合式继承是组合继承的一种优化方式，避免了调用两次父类构造函数。
   - 缺点是增加了额外的函数调用，略微影响性能。
   - 示例：
     ```javascript
     function Parent() {
       this.name = 'Parent';
     }
     function Child() {
       Parent.call(this);
     }
     Child.prototype = Object.create(Parent.prototype);
     Child.prototype.constructor = Child;
     ```

以上是 JavaScript 中常见的几种继承方式，每种方式都有其优缺点，开发者根据实际需求选择适合的继承方式。



### 2. 事件委托是什么？

JavaScript 事件委托（Event Delegation）是一种优化技术，用于处理在父元素上监听子元素事件的方法。它的核心思想是利用事件冒泡（event bubbling）机制，将事件处理程序绑定到父级元素，而不是直接绑定到每个子元素。

**工作原理：**

1. 将事件处理程序绑定到父级元素上。
2. 当事件发生时，事件会冒泡到父级元素。
3. 在父级元素上捕获事件，并确定事件的目标（target）是哪个子元素。
4. 根据事件的目标执行相应的操作。

**优点：**

1. **性能优化**：减少了事件处理程序的数量，避免了为每个子元素都绑定事件处理程序的开销，尤其是在大型页面或动态内容加载时，可以提高性能。
2. **动态元素支持**：对于动态添加或移除的子元素，不需要重新绑定事件处理程序，因为事件委托是基于父元素的。

**示例：**

假设有一个 `ul` 元素，其中包含多个 `li` 元素，我们想要在点击任意 `li` 元素时输出其文本内容：

```html
<ul id="parentList">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

使用事件委托的方式：

```javascript
// 获取父元素
var parentList = document.getElementById('parentList');

// 添加事件监听器到父元素上
parentList.addEventListener('click', function(event) {
  // 检查事件目标是否是 li 元素
  if (event.target.tagName === 'LI') {
    // 输出点击的 li 元素的文本内容
    console.log(event.target.textContent);
  }
});
```

在这个示例中，我们只需将事件监听器绑定到父元素 `ul` 上，然后通过事件冒泡机制，监听到每个 `li` 元素上的点击事件，从而实现了对子元素的事件处理，而无需为每个 `li` 元素单独绑定事件处理程序。



### 3. 简述JavaScript修饰器 ？

JavaScript 修饰器是一种特殊的语法，用于修改类的行为。修饰器可以用来装饰类、方法、属性等，以便添加额外的功能或修改现有功能。修饰器最常用于面向对象编程中，特别是在框架和库中用于实现元编程和装饰模式。

修饰器在 JavaScript 中处于实验性阶段，并不是标准的 ECMAScript 特性，目前主要由 Babel 等工具提供支持。

修饰器有两种类型：类修饰器和方法/属性修饰器。

**类修饰器：**

类修饰器是一个函数，接收一个参数，即被修饰的类。它可以在类被声明时进行装饰，用于修改类的行为或元数据。类修饰器可以用来添加静态属性、实例属性、方法等。

```javascript
function log(target) {
    target.log = function(message) {
        console.log(message);
    };
}

@log
class MyClass {
    static log(message) {
        console.log(message);
    }
}

MyClass.log('Hello'); // 输出: Hello
```

**方法/属性修饰器：**

方法/属性修饰器是一个函数，接收三个参数：目标对象、属性名（或方法名）、修饰符描述符（PropertyDescriptor）。它可以用于修改属性的行为，比如添加 getter/setter、日志记录、权限控制等。

```javascript
function readonly(target, name, descriptor) {
    descriptor.writable = false;
    return descriptor;
}

class MyClass {
    @readonly
    method() {
        console.log('This method is readonly');
    }
}

const obj = new MyClass();
obj.method(); // 正常调用
obj.method = function() {
    console.log('This method is not allowed to be modified');
};
obj.method(); // 报错: Cannot assign to read only property
```

修饰器是一种强大的元编程工具，在框架和库中被广泛应用，用于实现切面编程、依赖注入、数据验证等功能。