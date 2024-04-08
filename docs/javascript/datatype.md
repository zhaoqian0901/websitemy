# JS数据类型

JavaScript中，我们可以把数据类型分为两部分，分别为基本类型和引用类型。

#### 1基本类型

1.  Number

    数字类型，包含整数和浮点数。

    *   NaN是一种特殊的数字类型，表示Not A Number。
2.  String

    字符串类型，使用双引号（""）或者单引号（''）或者反引号（\`\`）表示。
3.  Boolean

    布尔类型，空指针对象，只有一个值，null类型也是空的对象引用。
4.  Null

    布尔类型，空指针对象，只有一个值，null类型也是空的对象引用。
5.  Undefined

    只有一个值，即undefined值。使用var声明了变量，但未给变量初始化值，那么这个变量的值就是undefined
6.  Symbol

    Symbol 指的是独一无二的值，这是ES6新增的数据类型。每个通过 Symbol() 生成的值都是唯一的。
7.  BigInt

    Javascript 中的任意精度整数，可以安全存储和操作大整数。即使超出 Number 能够表示的安全整数范围。是 chrome 67中的新功能。

#### 2引用类型

Object类型

我们将在JS中除了基本数据类型以外的都称为对象类型。里面包括我们常用的对象(Object)、数组(Array)、函数(Function)，以及特殊类型正则（RegExp）和日期（Date）等......

#### 3基本类型和引用类型的区别

基本类型存储在栈之中，是简单的数据类型，

引用类型的指针存储在栈之中，内容存储在堆之中。

*   将引用类型赋值给另一个变量，只是将在栈中的引用赋值给了他，两个地址指向同一个堆内存对象。

#### 4检测数据类型

1.  typeof 变量或表达式

    ```javascript
    typeof '123' === 'string'
    //只能判断处null以外的基本数据类型，引用类型会直接返回Object。
    ```
2.  instanceof

    ```javascript
    '123' instanceof String
    //无法检测基本数据类型，因为instanceof是检测当前判断的类是否出现在实例的原型对象，会循着原型链查找。
    ```
3.  constructor

    ```javascript
    '123'.constructor === String
    //constructor可以改变，会导致判断不准确；
    ```
4.  Object.prototype.toString.call()

    ```javascript
    Object.prototype.toString.call('123')；
    ```

