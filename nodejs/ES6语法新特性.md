# ES6语法新特性

## ES5 变量声明

```
1.变量提升
2.没有块级作用域
```

eg

```javascript
console.log(a);//undefined
var a =10;

for(var i =1;i<+5;i++){
    
};
console.log(i)
```

## ES6

### let和const

```
1.没有变量提升
2.有块级作用域
```

```javascript
eg
console.log(num);
let num = 20;
//num is not defined

 for(let i = 1;i<=5;i++){
     console.log('循环里' + i);
 }

 //报错，说明有快级作用域
 console.log(i);
```

#### 区别

````
let 变量  类似于var 声明的变量允许修改
const 常量   只能在声明的时候赋值,后面不能修改
````

### 对象的快速赋值

```javascript
 let name = '李四';
 let age = 20;
 let saiHi = function(){
     console.log('1111');
 };

 let person = {
     name,//等价于 name:name
     age,//等价于 age:age
     saiHi//等价于saiHi:saiHi
 };

 console.log(person);
```

### 箭头函数

```javascript
let fn2 = (a,b)=>{
    console.log(a+b);
    return a+b;
};

fn2(100,200);
//如果形参只有一个,小括号可以省略
let fn3 = a=>console.log(a);
fn3(66);
```



