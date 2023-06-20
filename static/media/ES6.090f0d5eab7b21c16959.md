### insertAdjacentHTML()

  var section = `<section class="conactive">新选项卡内容</section>`

  that.item_content.insertAdjacentHTML('beforeend',section)

  //高级做法 利用 insertAdjacentHTML() 可以直接将字符串格式元素添加到父元素当中

### remove()

可以直接删除指定的元素

### 禁止双击选中功能

  window.getSelection?window.getSelection().removeAllRanges():document.getSelection.empty();

### constructor()

当使用 Star.prototype = {} 对原型赋值的时候必须在{}里重新让constructor指向回Star

Star.prototype = {

​	coustructor:Star,

​	...

}

### call(参数1，参数2，...)

可以调用函数

改变函数的this指向 函数中的**this**指向**参数1**

### forEach(function(value,index,arr){})

遍历数组 value值 index索引 arr数组本身

### filter(function(currentValue,index,arr){return 条件})

创建新数组  新数组总的元素时符合条件的元素 用于**筛选数组**

currentValue:数组当前项的值

index：数组当前项的索引 

arr:数组对象本身

### array.some(function(currentValue,index,arr){return 条件})

查找数组中是否有满足条件的元素

有 返回true

没有 返回false

找到第一个后 后续代码不再执行

### str.trim()

trim方法将一个将字符串两端的空白符号

### Object.defineProperty(obj,prop,descriptor)

obj: 必需。目标对象

prop: 必需。需定义或修改的属性的名字

descriptor ; 必需。目标属性所拥有的特性

第三个属性descriptor说明：以对象{}的形式书写

- value:设置属性的值默认为 undefined
- writable:值是否可以重写。true|false 默认false
- enumerable：目标属性是否可以被枚举（不允许遍历）。true|false  默认为false
- configurable：目标属性是否可以被删除或是否可以再次修改特性true|false 默认为false 
  - 不允许修改第三个参数里的特性

### Object.keys()

遍历对象

### func.apply(参数1,[参数2,参数3])

参数1：func中this的指向

传递的参数必须是数组(伪数组)

利用apply求最大值

**Math.max.apply(Math,arr)**

## bind()方法

**func.bind(thisArg,arg1,arg2,...)**

- thisArg: 在fun函数运行时指定的this值
- arg1，arg2：传递的其他参数
- 返回有指定的this值和初始化参数改造的原函数拷贝

###  <script

​	**'use strict';**

//开启严格模式

### <script

## 严格模式

1. 变量名必需先声明在使用
2. 不能随意使用删除已经声明好的变量
   1. **delete** num 是错误的
3. 严格模式下**全局作用域中函数**中的**this**是**undefined**
4. 严格模式下，如果 构造函数不加**new**调用，this会报错

### 高阶函数

**高阶函数**是对其他函数进行操作的函数，它**接收函数作为参数**或**将函数作为返回值输出**

### 闭包

​	闭包(closure)指有权访问另一个作用域中变量的函数

​		一个作用域可以访问零为一个函数内部的局部变量

闭包的**主要作用**：**延申了变量的作用范围**

