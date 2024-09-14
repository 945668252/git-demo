# 构造函数方法集合

## 对象

### find和findIndex：找到第一个符合的元素，参数一致，find的浅拷贝

第一个参数是回调函数：当前val，当前index，整个原数组arr

find返回对象值，findIndex返回索引

![image-20240906151249934](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20240906151249934.png)

第二个参数：对象或者数组，没区别都是返回第一个找到的值。

用来绑定回调函数Fn的this对象，可在回调中直接使用第二个参数

![image-20240906151618447](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20240906151618447.png)



### copyWithin()指定位置覆盖元素，会改变数组

三个参数，target(必须)，start，end

target 从哪开始？负数从后面开始

start 从哪复制？

![image-20240906150316676](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20240906150316676.png)

## 数组

### from方法：将类对象转为真数组

包含：类数组的对象，即：带有索引和length属性。可遍历iterable的对象（如Set和Map结构）

![image-20240906145205326](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20240906145205326.png)

同时，可以传入真数组，from方法第二个参数是处理每个元素

![image-20240906145305446](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20240906145305446.png)

### of方法：将一串数据转为数组

参数>=1个，返回新数组

参数为空，返回空数组

# var和let和const

var声明的变量存在变量提升，既是全局变量/顶层变量。浏览器环境：window对象，node环境：global对象

let,相同作用域声明，会报错。

正确

```
let a=10
{
	let a=20
}
```

错误

```
function test(arg){
	let arg;
}
test();
```

