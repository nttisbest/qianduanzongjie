# javascript

## js三种书写方式

### 行内写法

### 内联写法

### 外联写法

## js常用的五句话

### 弹出提示框

```javascript
alert('欢迎大家来到黑马程序员学习大前端');
```

### 在控制台打印数据（不是给用户看的，而是给程序员自己看的）

```javascript
console.log('爱是一道光，绿到你发亮');
```

### 弹出一个输入框（用户可以输入数据）

```javascript
prompt('班长你今年多大啦？');
```

### 弹出一个确认框（有确定和取消按钮）

```javascript
confirm('班长，确定不加个钟吗?');
```

### 给网页添加内容

```javascript
//不常用，因为可能会覆盖网页原本的内容
document.write('<h1>我是班长，我为自己袋盐</h1>');
```



## js数据类型

### js数据类型：七种

值类型（5种基本数据类型）:  string number boolean undefined null

引用类型（2两种复杂数据类型）：

array

object

 function属于对象类型

### 直接量

### string字符串类型

作用：用于显示网页的文本

```javascript
console.log("123");
console.log('哈哈哈');
```

### number数字类型

作用：用于网页的数学计算

```javascript
console.log('10');
console.log('9.9');
```

### boolean 布尔类型

作用：表示事物的对立面  真/假   成立/不成立

```
console.log(true);
console.log(false);
```

**谷歌浏览器： string类型是黑色    number类型是蓝线**



### 检测数据类型

得到数据所属类型的字符串

**语法** ： （1）typeof数据     （2）typeof（数据）

**关键字：**一些特定的拥有特殊功能的单词

```javascript
console.log(typeof '123');//string
console.log(typeof 123);//number
console.log(typeof true);//boolean
```

检测```typeof 123``` 这个语法的结果返回什么类型的数据

相当于（1）```typeof 123 = 'number'```(2) ```typeof('number');```   

```console.log(typeof(typeof 123));//string```

## 变量

### 如何在存储中存储数据？

```javascript
var age = prompt('班长请输入你的年龄');
console.log(age);
```

var:variable 变量

### 变量的作用

**作用**：在内存中存储数据

### 变量的语法

#### 声明变量

在内存中开辟一块空间：

```javascript
var 变量名;
```

#### 变量的赋值

**赋值：**将数据存入变量中```变量名=数据```

```=```:将赋值运算符  将```=```号右边的数据存入左边的变量中

```javascript
num = 10;
```

#### 取值

取出变量中存储的数据：变量名

```console.log(num);//10```

#### 变量的初始化

```var num = 10;//(1)var num; (2)num = 10;```

#### 变量的批量的声明

```var num1,num2,num3;```

#### 变量的批量声明赋值

```javascript
var num1 = 10,num2 = 10; num3  = 10;
```

#### 变量的重新赋值

先摧毁旧值，然后存入新值

```javascript
num = 20;
console.log(num);//20
```

#### 变量的重新声明

会覆盖已经存在的变量

```javascript
var num = 30;
console.log(num);//30
```

#### 变量的值是另一个变量的值

```javascript
var a =10;
var b = a;//将变量a的值拷贝一份赋值给b
console.log(b);//10
console.log(a);//10
```

> 注意点:不要把变量名与字符串搞混淆

```javascript
var a =10;

var b = "a";//不是取变量a的值拷贝,而是将字符串a赋值给b
console.log(b);//'a'
```

### 变量名的命名规则和规范

#### 1.命名规则:

> 必须要遵守的规则,如果不遵守,程序会报错

a.变量名必须以 字母, $ , 下划线_开头,后面可以是 字母, $ ,下划线_,数字.

#### 2.命名规范:所有程序员都遵守的一种习惯.

a.尽量以名词作为变量名

b.使用驼峰命名法:第一个英语单词首字母小写,后面的英语单词首字母大写.

```javascript
//命名规则
var a1_2 = 10;
//命名规范
var name = "隔壁老刘":
var age  = 18;
var pingYing = "拼音";
var girlFriend = "苍老师";
var oldFe = "老铁";
```

### 交换两个变量的值

**需求**:交换两个变量值```(num1= 30; num2=20)```

```javascript
var num1 = 20;
var num2 = 30;
```

```javascript
//此方法不能交换变量的值?
//原因是:变量重新赋值会先把旧值摧毁
num1 = num2;
num2 = num1;
console.log(num1);//30
console.log(num2);//30
```

**使用第三方变量来交换**

```javascript
var temp = num1;
num1 = num2;
num2 = temp;
console.log(num1);
console.log(num2);
```

## js中+号的作用

```javascript
var name = "老宋";
var age = 38;
```

这样写无法取出name变量中的值,会把name当作字符串的一部分

```php console.log('我的名字是name')```

### 1.字符串的连接符:

将+号左右两边的字符串连接起来组成一个新的字符串

#### 条件:

+号的两边至少有一个是string类型

```javascript
console.log("我的名字是"+name+"我的年龄是"+age);
```

### 数学加法

两边都要是number数字

```javascript
console.log(1+5);//6
```

### 例子

```js
console.log(1+"1");//11
console.log(1+1);//2
console.log(1+'1'+1)//111
console.log(1+1+'1');//21
```

> 字符串的数字和数字拼接会组成新的字符串

## 算数运算符与算数表达式

### 1.算数运算符:数学上的算数运算

```javascript
+:加法
-:减法;
*:乘法;
/:除法;
%:取余数(求模)
```

### 2.运算符只是一种运算的符号,单独写是没有意义的,通常要与数字一起组成表达式.

### 表达式

由运算符组成的式子

```javascript
1+1;
10*2
```

#### 算数表达式

由运算符组成的式子

#### 只要是表达式一定有结果

> **要么直接打印,要么存入变量中**

```javascript 
console.log(1+1);//2打印 算数表达式的结果
var res = 10*2; //将10*2 算数表达式存入变量res中
console.log(res);//20
```

### 除法

a.数学上0不能作为除数,如果一个数字除以0,则会得到infinity.

b.除法会得到无限循环小数,js只会保留小数点后面的15-17位,对开发没有影响可以忽略.

```javascript
console.log(1/2);//infinity
console.log(10/3);//3.3333333333333333
```

#### 求模

```javascript
console.log(10%3);//1
```

## 复合算数运算符

```javascript
+=:在自身的基础上加多少
-=:在自身的基础上减多少
*=:在自身的基础上乘多少
/=:在自身的基础上除多少
%=:在自身的基础上模以多少
eg:
10+=10;   ==  res=10+10;
```

## 自增自减运算符

### 自增

```javascript
++//自身的变量+1
```

#### 自增表达式

```javascript
num++
```

#### 最常用

```javascript
var num = 10;
num++;//(1)num = num +1 (2)num +=1
console.log(num);//11
```

### 自减

```javascript
num--//自身-1
```

#### 自减表达式

```javascript
num--;
var num1 = 20;
num1--;
console.log(num1);//19
```

## 关系运算符与关系表达式

### 关系(比较)运算符

比较两个数字之间的关系(判断某种条件是否成立)

```javascript
> >= < <= ==(相等) !=(不等) ===(全等)  !==(不全等)
```

### 关系表达式

由关系运算符组成的式子 ```1>0```

### 关系表达式的结果一定是布尔类型

```javascript
true;成立
false;不成立

console.log(1>0);//true
console.log(1<0);//false
```

### 相等运算符

只比较数据的值,不比较数据类型

```
注意
=:赋值运算符  将等号右边的数据赋值给左边的变量
==:比较运算符  比较两个数据之间的关系
```

```javascript
console.log(1 == 1);//true
console.log("1" == 1);//true 只比较数据的值,不比较数据类型
```

### 全等运算符

先比较值,后比较数据类型

```javascript
console.log("1" === 1);//false

//与 1=== 1 的结果相反
console.log(1 !== 1);//false
```

## 逻辑运算符

计算多个条件之间的关系

```javascript
&&:逻辑与 读作并且
||:逻辑或 读作或者
!: 逻辑非 读作相反
```

### 逻辑表达式

由逻辑运算符组成的式子```38>32 && 100>1000```

#### 逻辑与表达式

一假则假

| 左边的式子 | 右边的式子 | 逻辑与表达式的结果 |
| :--------: | :--------: | :----------------: |
|     真     |     真     |         真         |
|     假     |     真     |         假         |
|     假     |     假     |         假         |
|     真     |     假     |         假         |

```javascript
console.log(1>10 && 10>11);
```

> 有为青年找女朋友:白富美(要白还要富还要美),多个条件都要满足,缺一不可

#### 逻辑或表达式

一真则真

| 左边的式子 | 右边的式子 | 逻辑或表达式 |
| :--------: | :--------: | :----------: |
|     真     |     真     |      真      |
|     假     |     真     |      真      |
|     假     |     假     |      真      |
|     真     |     假     |      假      |

```javascript
console.log(1>10||10>11);
```

> 普通青年找女朋友:或者白或者富或者美  多个条件满足任意一个即可

#### 逻辑非表达式

取反

true变false

false变true

```javascript
console.log(!true);//false
console.log(!false);//true
```

> 屌丝青年找女朋友:只要不是充气的(充气取反)

## 运算符优先级

不同的运算符运算的顺序不一样

> 谁让谁先算就给谁加个小括号

```javascript
1.();
2.++;--;自增自减运算符
3.算数运算符 + - * / %
4.关系运算符
5.逻辑运算符
6.赋值运算符 =
```

## Math 对象

> js作者已经提前写好了的函数

### 圆周率

```javascript
console.log(Math.PI);//3.14159265358973  Π
```

### 绝对值

> 数字距离坐标原点的单位长度

```javascript
console.log(Math.abs(-2));//2
```

### 天花板函数

> 往大的取整

```javascript
console.log(Math.ceil(5.1));//6
```

### 地板函数

> 往小的取整

```javascript
console.log(Math.floor(5.1));//5
```

### 求最大的值

```javascript
console.log(Math.max(10,20,10,30,50));//50
```

### 求最小值

```javascript
console.log(Math.min(10,20,30,40,50));//10
```

### 幂运算

求x的y次方

```javascript
Math.pow(x,y);//求x的y次方
```

```javascript
console.log(Math.pow(2,3));//8
```

### 四舍五入

```javascript
console.log(Math.round(9.4));//9
```

### 求随机数

```javascript
console.log(Math.random());
```

## 前自增与后自增的区别

**相同点**:无论是前自增还是后自增,对于变量而言没有区别,都是自身加+

**异同点**:表达式结果不同

**前自增**:先自增(变量先+1),后赋值(变量将自己的值赋值给表达式结果)

**后自增**:先赋值,后自增.

```javascript
var a = 1;
    var b = a++ + a++;//两个自增表达式结果求和
    // var r1 = a++;  左边自增表达式  r1 = 1  a = 2
    //var r2 = a++;  右边自增表达式  r2 = 2  a=3
    // var b = r1 + r2 = 3
    console.log ( a );//3
    console.log ( b );//3

    var c = 10;
    var d = c++ + ++c + --c + c--;
    /*    表达式结果/变量的值 */
    //  var d = 10/c=11 + 12/c=12 + 11/c=11 + 11/c = 10
    console.log ( c );//10
    console.log ( d );//44
```

## null和undefined

### null

**null是一个空值**

null只有一个值就是null,使用typeof检测null会得到obj

```javascript
var num1 = null;
console.log(num1);
console.log(typeof num1);//Object 
//细节:使用typeof检测null会得到object
```

```javascript
//真正检测null的类型,用此方法
console.log ( Object.prototype.toString.call ( num1 ) );//[object Null]
```

### null和undefined的区别

```javascript
console.log(undefined == null);true
console.log(undefined === null);//false
```



### undefined

未定义.如果一个变量只声明,未赋值,默认值就是undefined

```javascript
var num;
console.log(num);//undefined
console.log(typeof num);//undefined 检测num中数据的数据类型
```

## Nan和sNaN的介绍

### NaN:not a number

#### 如果一个算数运算的结果不是一个数字,则会得到NaN

```javascript
console.log("张三" - 100);NaN
```

#### NaN是number类型中一个特殊值:表示错误的数学计算结果

```javascript
console.log(typeof("张三" - 100));
```

#### NaN与任何数字计算的结果都是NaN

```javascript
console.log(NaN - 100);//NaN
```

#### NaN与任何数字都不等

```javascript
console.log(NaN == 0);//false
console.log(NaN == NaN);//false
```

#### 检测一个数据是不是NaN:    isNaN(数据) 

```javascript
console.log ( isNaN ( 10 ) );//false
console.log ( isNaN ( NaN ) );//true
```

## 其他数据类型转换

### 其他数据类型转换number

#### 1.转换成整数 parseInt();

> 工作原理:从左往右一次解析字符,遇到非数字字符结束解析,并且将已经解析好的整数返回

```javascript
var str = '38.1a';
console.log(parseInt(str));
console.log(typeof parseInt(str));
```

#### 2.转换成小数  parseFloat();

> 工作原理:与parseInt完全一致,唯一的区别是可以识别字符中的第一个小数点
>
> Float:浮点数

```javascript
var str1 = '38.1.2a';
console.log(parseFloat(str1));
```

#### 3.其他数据类型转数字 Number();

> 工作原理:1.可以转换成整数和小数 2.只要有一个非数字字符则会得到NaN

```:-1:
console.log(Number("38.1a"));//NaN
```

#### 布尔类型转数字

> 布尔类型转数字会得到 0 (false)和 1 (true)

```javascript
console.log(Number(true));//1
console.log(Number(false));//0

console.log(Number(undefined));//NaN
console.log(Number(null));//0
```

### 其他类型转成string

#### 1.常用方式:string(数据)

> 特点:可以识别undefined 与 null

```:100:
console.log(String(num));
console.log(typeof String(num));//string
```

#### 2.变量名 .toString()

> 特点:不能识别undefined与null  程序会报错

```:100:
console.log(num.toString());
```

### 其他类型转成boolean类型

> boolean 类型
>
> ​	得到 false :0 -0 NaN undefined null false ''
>
> ​	得到true : 除开false 的八种数据之外的一切数据

```javascript
 console.log ( Boolean ( 0 ) );
    console.log ( Boolean ( -0 ) );
    console.log ( Boolean ( NaN ) );
    console.log ( Boolean ( undefined ) );
    console.log ( Boolean ( null ) );
    console.log ( Boolean ( false ) );
    console.log ( Boolean ( '' ) );
    console.log ( Boolean ( document.all() ) );
```

## 隐式类型转换

> 1.显示类型转换: 程序员主动的调用语法来转换的数据类型(常用,因为语义明确)
>
> 2.隐式类型转换:当运算符两边数据类型不一样的时候,编译器会自动帮我们转换成一致再计算(不常用,易读性不高).

### 其他类型转number

```javascript
+ : 数学正号  +str
算数运算符 : + - * / %
其他数据类型转string : 字符串连接符 +
其他数据类型转boolean  !
```

### 其他数据类型转number

```javascript
+ :数学正号 (经常使用)
console.log(+"10");
var age = +prompt('班长,请输入你的年龄');
console.log(age);
```

### 算数运算符

```javascript
//算数运算符 : + - * / %
console.log('10'*5);//50 number('10)
console.log('10'-1);//9 number('10')-1
console.log('张三'-100)//NaN Number('张三')-100
```

## 其他数据类型转string 

```javascript
+ 字符串连接符
console.log('1'+1);//11 '1'+string(1)
```

> 容易混淆的地方 **将算术运算符 + 与字符串连接符+ 隐式转换搞混淆**

```javascript
console.log(1+true);//2 
//算数运算符 1+Number(true) = 2;
console.log('1'+true);//1true
//字符串连接符  '1'+String(true)=1true
```

### 其他数据类型转boolean

逻辑非 ! :取反 true 变false   false变true

```javascript
console.log(!1);//false  !boolean(1)
```

## if分支结构

#### 顺序结构(默认)

代码从上往下顺序依次执行

```javascript
console.log ( "我今天上学了" );
console.log ( "我今天考试了" );
console.log ( "我回家了" );
console.log ( "爸爸打我了" );
console.log ( "我睡觉了" );
```

> 需求:考试不及格,爸爸才打我

#### 分支结构

> 代码根据条件执行

```javascript
if(条件 true/false){
   条件成立时需要执行的代码
   }
```

执行步骤:1.判断条件  

​                 2.1 成立  则执行大括号里面的代码

​		2.2 不成立 直接执行大括号后面的代码

```javascript
if (1>0){
   console.log ( "爱是一道光，绿到你发慌" );
};
//只有大括号里面的代码才是根据条件执行，大括号后面的代码还是顺序执行
console.log ( "11111" );
```

> 实现需求:考试不及格,爸爸才打我

```javascript
 var score = 59;
    console.log ( "我今天上学了" );
    console.log ( "我今天考试了" );
    console.log ( "我回家了" );
   if (score<60){
       console.log ( "爸爸打我了" );
   }
    console.log ( "我睡觉了" );
```

### if-else

> if-else结构:两个互斥条件判断
>
> 优点:两个互斥条件只需要判断一次

```:arrow_left:
  if(条件 ture/false){
        条件满足时需要执行的代码
    }else{
        条件不成立时需要执行的代码
    }
```

***if-else注意点:**if大括号中的代码和else 大括号中的代码一定只会执行一个(即不会同时执行,也不会同时不执行)

```javascript
    if(5>30){
        console.log ( "我爱你们" );
    }else{
        console.log ( "世界上最遥远的距离不是生与死的距离，而是你在if中，我在else中，看起来隔的那么近，却永远不能一起执行" );
    }
```

### if-else if-else 分支结构

**注意点:**a.必须以if开头,中间的else if可以多个,最后面的else可以省略(一般不会省略)

b.所有的大括号中的代码最多只会执行一个

```javascript
  var score = 50
    console.log ( "我今天上学了" )
    console.log ( "我今天考试了" )
    console.log ( "我回家了" )
    //只有上面的条件不满足，才会判断下面的条件
    if ( score >= 90 ) {
        console.log ( "爸爸给我法拉利" )
    } else if ( score >= 80 ) {//隐藏条件  score<90
        console.log ( "爸爸给我买保时捷" )
    } else if ( score >= 60 ) {//隐藏条件  score<80
        console.log ( "爸爸给我买奥迪" )
    } else {//隐藏条件  score<60
        console.log ( "爸爸打我" )
    }
    console.log ( "我睡觉了" )
```

#### 注意点

> if小括号里面的条件可以写哪些代码呢?
>
> a.最常用:关系表达式,结果一定式布尔类型
>
> b.直接写布尔类型的值
>
> c.其他的值:编译器会自动转成布尔类型来判断是否成立

### switch case

适用于固定值匹配(全等)

```javascript
switch(匹配值){
        case 值1:
            匹配值 === 值1，则需要执行的代码
            break;
        case 值2:
            匹配值 === 值2，则需要执行的代码
            break;
        case 值3:
            匹配值 === 值3，则需要执行的代码
            break;
        default:
            如果匹配值与上面所有的case后面的值都不全等，则需要执行的代码
            break;
    }
```

**switch-case注意点**

a.匹配值与case后面的值一定要全等的关系

b.default代码块可以写在任何位置,但是一般写在最后面.

c.break关键字不能省略

​      作用:结束switch-case语句

​	如果省略:发生穿透现象(代码从上一个case代码块无条件执行到下一个case代码块)

```javascript
 //示例：用户输入黑马学科编号，告诉用户学习什么学科  1-前端  2-PHP  3-java  4-UI

    var subject = +prompt('请输入你选择的学科   1-前端  2-PHP  3-java  4-UI');
    switch (subject){

        case 1:
            alert('欢迎选择2018年最有钱途的学科');
            break;
        case 2:
            alert('欢迎选择拍簧片这个学科');
            break;
        case 3:
            alert('恭喜走上了搞基不归路');
            break;
        case 4:
            alert('恭喜你选择了UI，妹子给我留一个');
            break;
        default :
            alert('脑子有包');
            break;

    }
```

### 合理利用switch-case穿透现象

​    某些情况下，合理的利用switch-case穿透现象可以让你的代码更简洁

​    什么情况需要合理穿透： 多个值需要执行的代码相同.

```:zero:
//需求：让用户输入月份，告诉用户季节
    /*春季：3 4 5
    夏季：6 7 8
    秋季：9 10 11
    冬季：12 1 2
    
var month = +prompt('请输入月份');
    switch (month){
        case 12:
        case 1:
        case 2:
            alert('冬季');
            break;
        case 3:
        case 4:
        case 5:
            alert('春季');
            break;
        case 6:
        case 7:
        case 8:
            alert('夏季');
            break;
        case 9:
        case 10:
        case 11:
            alert('秋季');
            break;
        default:
            alert('滚回火星去');
            break;
    }
```

## 三元表达式

运算符根据计算的数字的数量分为一元运算符、二元运算符、三元运算符

- 一元运算符：计算一个数： ++/-- 逻辑非！
- 二元运算符：计算两个数字：算数运算符、关系运算符
- 三元运算符：计算三个数字：

## 循环结构

## 关键字

### break关键

**结束循环语句,立即执行大括号后面的代码**

```javascript
break关键字用于:(1).三种循环结构 (2).switch-case
```

### continue关键字

结束本次循环体(本次循环体后面的代码不立即执行,立即进入下一次循环判断)**只用于if**

### 案例

```javascript
for (var i =1;i<=10;i++){
    break://吃到第五个包子，吃饱了。后面所有的包子都不吃
    //不会再走if语句
   if (i == 5){
       console.log ( "我吃到第五个吃饱了，后面的包子我不吃" );
       break;
       //走到这里立即执行大括号外面的代码,
};
```

```javascript
//  吃到第五个包子，吃到虫子了。只是第五个包子不吃，没吃饱后面的包子继续吃
 if(i == 5){
  console.log ( "我吃到一坨黄黄的虫子，第五个包子不吃了，但是没吃饱，后面的包子继续吃" );
   continue;
}
   console.log ( "我吃第" + i + "个包子" );
};
   console.log ( "吃完啦" );
```



### 乘法口诀案例

```javascript
//1.找出外层循环（行）
//2.找出内层循环（列） 与 外层循环变量i的关系
//i =1 行，内层循环（列）  =1
//i =2 行，内层循环（列）  =2
//i =3 行，内层循环（列）  =3
//………………
//i =9 行，内层循环（列）  =9
//内层循环(列) = i


document.write('table style="border: 1px solid red;"');
//外层循环次数9
for(var i = 1; i<=9;i++){
    //内层循环次数:列+1
    document.write('<tr>');
    for(var j=1;j<=i;j++){
        document.write('<td>');
        document.write(j+ '*'+i+'='+j*i+'&nbsp;&nbsp');
        document.write('</td>');
    }
    document.write('</tr>');
}
document.write('</table>');
//当i=1;j=1;输出 1*1=2;
//当i=2;j=1;输出 2*1 = 2  当i=2;j=2;输出 2*2=4;
```

## 数组

数组的弊端:(1)代码冗余  (2)不变维护

```javascript
var num1 = 88;
var num2 = 99;
var num3 = 101;
var num4 = 59;
var num5 = 70;
//数组的三要素
//元素：数组中的数据
//长度：记录元素的数量
```

### 数组遍历

   **数组的遍历：**获取一个数组中所有的元素

**数组的遍历是一个固定的for循环结构**

```javascript
for(var i = 0;i<数组名.length;i++){
  数组名[i]
}
```

```javascript
eg.
var arr = [20,55,60,88,100,200];
for(var i =0;i<arr.length;i++){
    console.log(arr[i]);
}

console.log ( arr[ 0 ] );
console.log ( arr[ 1 ] );
console.log ( arr[ 2 ] );
console.log ( arr[ 3 ] );
console.log ( arr[ 4 ] );
```

### 萝卜框思想求和



- 求数组中元素的平均值

```javascript
//箩筐思想求和
//1.1 声明空箩筐
var sum = 0;
//1.2 遍历萝卜数量
for (var i = 0;i<arr.length;i++){
   sum += arr[i];//3.萝卜放入箩筐中
};
console.log ( sum / arr.length );
```



- 求数组中元素的最大值

```javascript
var arr = [100,88,95,60,70];
//擂台思想
//1 声明空擂主：
var max = -Infinity;
//2 遍历挑战者（数组元素）
for(var i = 0;i<arr.length;i++){
//3.依次和擂主pk，谁大谁做擂台
if (arr[i] >= max){
    max = arr[i];
   }
};
console.log ( max );
```

- 将1-100中3的倍数放入数组中

```javascript
//1.遍历指定范围符合条件的数
//2.数组后面添加元素
var newArr = [];
for (var i = 1;i<=100;i++){
    if(i%3 == 0){
        newArr[newArr.length]=i;
    }
}
console.log(newArr);
```

- 斐波那契额数列 翻转

**翻转法**

```javascript
 var arr = [20,60,88,100,55];
//1.1 翻转法
var newArr = [];
//1.倒着遍历arr
for (var i = arr.length-1;i>=0;i--){
	console.log ( arr[ i ] );
newArr[newArr.length] = arr[i];//2.将元素添加到新数组中
};
// console.log ( newArr );
```

**交换法**

- 不需要声明新的数组
- 不需要全部遍历

```javascript
1.遍历数组一半
2.首尾交换
第一个元素： 0   与 倒数第一个元素 arr.length-1   交换     0 +  arr.length-1 = arr.length-1
第二个元素： 1   与 倒数第二个元素 arr.length-2   交换     1 +  arr.length-2 = arr.length-1
第三个元素： 2   与 倒数第三个元素 arr.length-3   交换     2 +  arr.length-3 = arr.length-1
i   与   arr.length-1 - i 交换


//(1)遍历数组的一半
for (var i = 0;i<arr.length/2;i++){
//(2)让下标为i的元素和 下标为  arr.length-1-i的元素交换位置
  var temp = arr[i];
  arr[i] = arr[arr.length-1-i];
  arr[arr.length-1-i] = temp;
};
console.log ( arr );
```

- 斐波那契额数列 交换法

```javascript
//1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233，377，610，987，1597，2584，4181，6765，10946，17711，28657，46368........
//a.前面两个元素固定  1,1
//b.从第三个数字(下标2)开始  每一个元素都是前面两个元素的和

//需求：求斐波那契数列第十列数字是多少
var arr = [1,1];
for (var i = 2;i<10;i++){
  arr[i] = arr[i-1] + arr[i-2];
};
console.log ( arr );
console.log ( arr[ arr.length - 1 ] );
```

### 冒泡法排序

**核心原理**:数组中相邻的元素比较大小,然后交换位置

```javascript
var arr = [18,15,10,20,5]; //[5,10,15,18,20]
for (var j = 0;j<arr.length-1;j++){
console.log ( "第" + ( j + 1 ) + "次pk" + arr[ j ] + "和" + arr[ j + 1 ] + "比较大小" );
	if (arr[j] > arr[j+1]){//相邻元素比较大小
		var temp = arr[j];
		arr[j] = arr[j+1];
		arr[j+1] = temp;
		};
	console.log ( arr );
};
 console.log ( arr );
```

### 冒泡法精简版本

```javascript
 步骤3：
        1.外层循环决定比较的轮数：   arr.length-1
        2.内层循环决定每一轮比较的次数：   arr.length-1-i
        3.比较大小，然后交换位置
    */

    var arr = [88,100,-20,66,50,70,30];

    //1.外层循环：比较轮数
    for (var i = 0;i<arr.length-1;i++){
        //2.内层循环：每一轮比较次数
        for (var j = 0;j<arr.length-1-i;j++){
            //3.比较大小，交换位置
            if (arr[ j] > arr[j+1]){
                var temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            };
        };
    };

    console.log ( arr );
```

### 二位数组

**需求**:波多老师开了一间学校，有三个班级，每个班级有5个学生，一次考试存储全校学生的分数

```javascript
//使用三个数组实现    弊端：代码冗余
var arr1 = [55,78,90,77,60];//一班
var arr2 = [90,88,95,98,100];//二班
var arr3 = [20,40,35,50,59];//三班
```



### 数组排序

**冒泡法排序核心原理:数组中相邻的元素比较大小,然后交换位置**

```javascript
步骤3：
 1.外层循环决定比较的轮数：   arr.length-1
 2.内层循环决定每一轮比较的次数：   arr.length-1-i
 3.比较大小，然后交换位置
```

```javascript
var arr = [88,100,-20,66,50,70,30];
for(var i =0;i<arr.length-1;i++){
	for(var j=0;j<arr.length-1-i;j++)
    //比较大小,交换位置
    if(arr[j]>arr[j+1]){
        var temp = arr[j];
        arr[j]=arr[j+1];
        arr[j+1]=temp;
    }
  }
}
console.log(arr);

```

### 数组的去重

#### 第一种方式:对数组排序

```javascript
//先对数组排序
//1.外层循环：比较轮数
for (var i = 0;i<arr.length-1;i++){
  //2.内层循环：每一轮比较次数
  for (var j = 0;j<arr.length-1-i;j++){
    //3.比较大小，交换位置
   if (arr[j] > arr[j+1]){
     var temp = arr[j];
     arr[j] = arr[j+1];
     arr[j+1] = temp;
   };
  };
};
console.log ( arr );

//遍历顺序后的数组,如果相邻元素不等,则添加到新数组的后面
var newArr = [];//声明空数组,储存
for(var i =0;i<arr.length;i++){
    if(arr[i]!=arr[i+1]){
        newArr[newArr.length]=arr[i];
    }
}
console.log(newArr);

```



#### 第二种方式:开关思想

```javascript
//开关思想:当某种操作结果只有两种状态,可以用布尔类型表示这两种状态;
//提出假设:var canAdd = true;
//验证假设
//根据开关状态实现需求
//声明一个空数组
var newArr = [];
//遍历
for(var i =0;i<arr.length;i++){
//声明一个布尔类型表示在与不在
var canAdd = true;
//遍历newArr 检查在不在
for(var j =0;j<newArr.length;j++){
    if(arr[i]==newArr[j]){
        canAdd=false;//只要有任何元素相等,开关状态编程false(在,不能添加)
        break;
    }
};
//根据开关状态实现需求
if(canAdd == true){
    newArr[newArr.length] = arr[i];
  }
}
console.log(newArr);
```



## 对象

### 定义

对象与数组的异同点
​    相同点：一个变量存储多个数据
​    不同点：存储的方式不一样
​    数组：有序存储（元素与下标一一对应）

​    对象：无序存储（属性名与属性值一一对象  键值对）

### 取值和赋值

声明对象    var 对象名 = { 属性名1：属性值1 ， 属性名2：属性值2 };

```javascript
var person = {
   name:'林绿裙',
   age:38,
   sex:'男'
};
```

对象的取值语法 ： 点语法 ：  对象名.属性名

对象有该属性名，则是获取属性对应的值

   ``` console.log ( person.name );//林绿裙```



对象没有该属性名，则获取的是undeifend

​    ```console.log ( person.girlFirend );//undefined```

对象的赋值：     对象名.属性名 = 值

对象有该属性名,则是修改属性值

```javascript
person.sex = '女';

console.log ( person );
```

对象没有该属性名

```javascript
person.girlFirend = '大桥老师';

console.log ( person );
```



### 对象的初始化语法

```javascript
//1.声明空对象
    var person = {};
    person.age = 18;//赋值语法
    person.name = '保健坤';//赋值语法
    console.log ( person.age );//取值语法
    console.log ( person );

    //2.初始化对象：声明的时候就赋值

    var student = {
        //初始化   属性名:属性值    ----键值对关系
        name:'陈红桥', //多个属性之间逗号
        age:18,
        girlFriend:['苍老师','波多老师','吉泽老师'],
        wife:{
            name:'孙笑川',
            age:38,
            sex:'男',
            play:function (  ) {
                console.log ( "今晚你要学习什么技术" );
            }
        },
        sayHi:function (  ) {
            console.log ( "大吉大利，今晚吃鸡" );
        }
    };

    student.age++;
    student.girlFriend[3] = '天海老师';

    console.log ( student );
    console.log ( student.name );//陈红桥

    console.log ( student.wife.name );//孙笑川

    student.sayHi();//调用student的sayHi方法

    student.wife.play();//调用student的wife的play方法

    /*
    函数： 变量
    方法：也是函数，这种叫法有归属感。 对象的属性值的数据类型是函数
     */
```

### 字符串语法介绍

```javascript
    //声明对象
var person = {
    name:'右护法',
    age:38,
    sex:'男'
};

//对象的取值语法有两种: 这两种语法没有任何区别，只是语法不同而已
//1.点语法;   对象名.属性名
 console.log ( person.age );
//2.字符串语法;   对象名['属性名']
console.log ( person[ "age" ] );
person['age'] = 18;
console.log ( person );

```

### 对象遍历

> 对象没有下标

```javascript
for ( var key in person ) {
   console.log ( key )//属性名字符串
    /*注意：不能用点语法取值  */
   console.log ( person.key )//  点语法取key属性值
   /*只能用字符串语法*/
  console.log ( person[ key ] )//  字符串语法取key变量中存储的字符串对应的属性值
    }

```

### this关键字

谁调用这个方法,this就代表谁

```javascript
    var person3 = {
        name:'陈红桥',
        age:32,
        sex:'男',
        play:function (  ) {
            console.log ( "今晚我要请坤哥精油开背" );
        },
        sayHi:function (  ) {
            //弊端：如果对象名修改了，方法中的person全部都要修改
            // console.log ( "大家好，我系" + person.name + "我的年龄是" + person.age + "我的爱好是：足疗爱好者" );
            console.log ( "大家好，我系" + this.name + "我的年龄是" + this.age + "我的爱好是：足疗爱好者" );
        }
    };


    person3.name = '社会桥';
    console.log ( person3.age );
    person3.sayHi();

```

### 对象的另一种声明方式

```javascript
    //1.（最常用）简洁方式：   var 对象名 = { 属性名：属性值 }
    var p1 = {name:'张三'};

    //2.构造函数：
    //构造函数：如果调用一个函数使用了new关键字，这个函数成为构造函数
    var p2 = new Object( {name : '张三'} );

    /*这两种方式没有任何区别，只是语法不同而已*/
    console.log ( p1 );

    console.log ( p2 );

```

### 使用工厂函数创建多个对象

使用函数解决创建多个对象代码冗余问题

工厂函数创建多个对象

```javascript
    function  creatPerson( name,age,sex ) {
        //1.创建空对象
        var person = {};
        //2.对象赋值
        person.name = name;
        person.age = age;
        person.sex = sex;
        //3.返回造好的对象
        return person;
    };

    var banzhang = creatPerson('班长',38,'男');
    console.log ( banzhang );

    var sheHuiQiao = creatPerson('社会桥',18,'男');
    console.log ( sheHuiQiao );

```

### 使用自定义构造函数创建多个对象new

new关键字工作原理（4个流程）

​    1.创建空对象

​    2.将this指向这个空对象

​    3.执行对象的赋值代码

​    4.自动返回这个对象

new关键字作用：  （1）创建空对象  （2）返回创建的这个对象

**构造函数创建对象注意点**

​    a.自定义构造函数不能省略new关键字

​        \* 如果是js作者写好的构造函数，可以省略的

​    b.构造函数一般首字母大写（为了提醒别人不要省略new关键字）

​    c.如果手动在构造函数中return

​        \* 基本数据类型： 无效

​        \* 复杂数据类型： 有效，会覆盖默认的new创建的对象

```javascript
使用构造函数方式(最常用)

function CreatePerson (name,age,sex  ) {
//1.创建空对象
//2.赋值
this.name = name;
this.age = age;
this.sex = sex;
//3.返回
};
var banzhang = new CreatePerson('徐晨',38,'男');
// console.log ( banzhang );
```

### Date对象最常用的API

```javascript
//1.创建日期对象
    var myDate = new Date();

    console.log ( myDate );

    //2.转换格式

    console.log ( myDate.toLocaleDateString () );//2018/12/10
    console.log ( myDate.toLocaleTimeString () );//下午5:03:51
    console.log ( myDate.toLocaleString () );//2018/12/10 下午5:04:09

    //3.获取年月日时分秒

    console.log ( myDate.getFullYear () );//2018
    /*月份范围 0-11 */
    console.log ( myDate.getMonth() );//11下标   第12个月
    console.log ( myDate.getDate() );//10
    /* 星期范围  0-6   日-六  */
    console.log ( myDate.getDay () );//1

    console.log ( myDate.getHours () );//17
    console.log ( myDate.getMinutes());//7
    console.log ( myDate.getSeconds());//32
    console.log ( myDate.getMilliseconds());//ms  149

    //创建自定义时间
    //(1) 参数格式： 年月日时分秒
    var date1 = new Date(2017,11,20,10,30,30);//2017/12/20 10:30:30
    console.log ( date1 );

    //(2) 参数格式字符串： ‘yyyy-mm-dd HH:mm:ss’
    var date2 = new Date('2018-10-25 23:30:30');
    console.log ( date2 );
```

### ARRAY对象常用的API

```javascript
 var arr =[10,20,30];//new Array(10,20,30)

    //1.concat():连接数组
    console.log ( arr.concat ( [ 100, 200, 300 ] ) );
    //2.join():将数组中所有的元素拼成一个字符串
    console.log ( arr.join () );//10,20,30
    //参数：分隔符
    console.log ( arr.join ( "|" ) );

    //3. pop（）：删除最后一个元素  相当于：arr.length--;
    // arr.length--;
    // console.log ( arr );
    arr.pop();
    console.log ( arr );

    /*4.push（）：往数组后面加内容  */
    // arr[arr.length] = 40;
    arr.push(40);
    console.log ( arr );

    /*5.reverse（）:翻转数组 */
    var arr = [66,88,100,20,30];
    arr.reverse();
    console.log ( arr );

    /*6.shift():删除数组第一个元素*/
    var arr = [10,20,30,40,50];
    arr.shift();
    console.log ( arr );

    //7. slice():查询数组某些元素
    var arr = [10,20,30,40,50,60,70,80];
   // arr.slice(start,end)      start<=  范围 < end
    console.log ( arr.slice ( 2, 5 ) );//[30, 40, 50]

    /*8.sort() :排序 */

    var arr = [20,10,5,88,100,66];
    /*参数是一个固定格式的函数
        从小到大： function (a, b) {
            return a-b;
        }
       从大到小： function (a, b) {
            return b-a;
        }
     */
    arr.sort(function (a, b) {
        return b-a;
    });
    console.log ( arr );

    //数组去重：

    var arr = [10,20,30,10,66,25,88,66];

    //1.声明空数组
    var newArr = [];
    //2.遍历arr,检查arr[i]在不在newArr中  在：不添加 不在：添加
    /*利用  数组.indexOf(元素)  方法  检查一个元素在不在数组中
        在：则返回这个元素的下标
        不在：返回固定值 -1
     */
    for(var i = 0;i<arr.length;i++){
        if (newArr.indexOf(arr[i]) == -1){//不在
            newArr.push(arr[i]);
        }
    };

    console.log ( newArr );
```

### string对象常用的api

```javascript
 var str = '欢迎大家来到黑马程序员学习大前端，爱你么么哒';
    //字符串类似于数组；多个字符组成的组合


    //1.chatAt():获取某个字符
    console.log ( str[ 6 ] );//常用
    console.log ( str.charAt ( 6 ) );

    //2.length：长度
    console.log ( str.length );

    //3.concat():连接字符串
    // console.log ( str.concat ( "老铁" ) );
    //str += '老铁';//常用
    console.log ( str );

    /***4.  indexOf() : 检测一个字符串在不在另一个字符串中 */
    console.log ( str.indexOf ( "黑马" ) );
    if (str.indexOf('班长') == -1){//不在
        console.log ( "班长不在str中" );
    }

    /*5.substr(): 截取字符串 */
   // str.substr(strat,length)    start:开始的位置  length：后面截取几个字符

    console.log ( str.substr ( 6, 2 ) );//黑马

    /* 6 replace（）：修改字符串*/
    //str.replace(旧字符串，新字符串)
    console.log ( str.replace ( "黑马程序员", "传智播客" ) );
    //删除字符串： 替换成空字符串
    console.log ( str.replace ( "黑马程序员", "" ) );

    /* 7.split（）：分割字符串    将字符串按照指定分隔符分成多个部分放入数组中*/
    //返回值一定是数组
    var str = '我爱$你么&么哒';
    console.log ( str.split ( "&" ) );
    console.log ( str.split ( "$" ) );
    console.log ( str.split ( "|" ) );

    //8 .字符串大小写转换:(中文没有大小写)

    var str = 'sdkjvgbksSLKBGNDSLFBHNLsdkjvbsxlk';
    console.log ( str.toLocaleLowerCase () );
    console.log ( str.toLocaleUpperCase() );


```



## 函数

### 函数与循环的区别

本质的区别

a.作用不同:

​	循环:一段代码在一个地方执行多次

​	函数:一段代码在多个地方执行一次

b.本质不同:

​	循环:一段代码在一个地方执行多次

​	函数:是一种数据类型,存储的是代码

```javascript
//声明函数:function 函数名(){ 函数体代码 }
//调用函数: 函数名();
//变量取值: 函数名(不会执行函数体代码,只是以字符串形式将变量存储的东西打印出来)
```

**作用**：将一段代码存入变量中，实现代码复用

## 函数参数

参数：调用者传递数据给函数

```javascript
function fn(形参){
}
fn(实参);
```

传参本质:是一个赋值过程.实参给形参赋值.

实参给形参赋值是按照顺序赋值.

```javascript
function bigSword ( jishi,yinliao ) {//形式参数
    //jishi:相当于在函数内部声明了一个变量，接收调用者传递的数据
        console.log ( jishi );
        console.log ( yinliao );
        console.log ( "大宝剑开始了" );
        console.log ( "天黑请闭眼，我是本次服务的" + jishi + "号技师" );
        console.log ( "不知不觉中，两个小时过去了……快乐的时光总是短暂的" );
        console.log ( "您好，本次消费188元，请喝杯" + yinliao + "压压惊" );
        console.log ( "大宝剑结束了" );
    };
```

## return

类似于break,结束函数体执行

break:结束循环体,和switch-case

### 返回值

返回值：  函数传递数据给调用者

传：函数

function 函数名(){    函数体代码    return 返回值  }

 收：调用者

var 变量名 =  函数名()

```javascript
function getArea ( radiu ) {
        var area = Math.PI * Math.pow(radiu,2);
        // console.log ( area );

        return area;//返回值
    };


```

### 函数内部调用其他函数

函数调用语法： 函数名()

不管写在任何位置作用都是一样：执行函数体代码

```javascript
    //1.声明函数：
    function a (  ) {
        console.log ( "哈哈" );
    };

    //2.调用函数
    if (1>0){
        a();
    };

    for (var i =1;i<=3;i++){
        a();
    }


    function b (  ) {
        console.log ( "呵呵" );
        a();
    };

    b();
```

### 变量的作用域

变量起作用的范围

a.全局作用域:变量可以在任何地方起作用

​	全局变量:在函数外面声明的变量

b.局部作用域(局部变量):在函数里面声明的变量,只能在函数里起作用

```javascript
//1.全局作用域
    var age = 38;

    function fn (  ) {
        console.log ( age );
        age = 40;
        console.log ( age );
    };

    fn();

    //2.局部作用域

    function fn(){
        var num = 10;//局部变量
        console.log ( num );
    };

    fn();

    // console.log ( num ); 程序会报错
```

### 作用域链

默认情况下代码处于全局作用域(0级链),声明了函数之后形成局部作用域(1级链),如果在函数的里面又声明的函数,就是会开辟一个新的作用域(2级),以此类推就会形成作用域链.

变量在作用域链的访问规则：就近原则

当在一个作用域中访问变量的时候，会先从当前作用域寻找变量的声明，如果有则访问该变量，如果没有则从父级链寻找

声明，如果有则访问，没有则继续往父级链寻找声明，以此类推直到顶级链（0级），如果还找不到则程序报错：  xxxx is not undefined

```javascript
    var num = 10;//0级链

    function fn (  ) {//0级链：  只有函数中才是1级链，函数本身fn本身还是0级链
        //局部作用域：1级链
         var num = 20;
        console.log ( num );//20

        function fn1 (  ) {//1级链
            //局部作用域：2级链
            var num = 30;//2级链
            console.log ( num );//30
        };

        fn1();
    }

    fn();

    console.log ( num );//10
```

### 预解析

js代码从上往下逐一执行---不严谨

js从上往下执行代码之前，会先将代码看一眼，这个看一眼的过程叫做预解析。 在预解析的过程中，编译器会做一件事：变量的提升

变量的提升：

a. 将var关键字声明提升到当前作用域最顶端，赋值语句原地

b. function关键字函数声明也会提前，调用语句在原地

   4.预解析意义：让函数可以在任何地方被调用

 如果一个变量没有使用var声明：不参与预解析，也不参与作用域（一定是全局变量）

**强烈建议不要使用**

### 函数另一种声明方式

```
//2.表达式声明：  var 函数名 = 匿名函数

// fn2();//程序报错：表达式声明只能在声明后调用
 var fn2 =  function  (  ) {
    console.log ( "低着头做事，夹着尾巴做人" );
};
 fn2();

 /*唯一的区别
 函数式声明：可以在任何调用
 表达式声明：只能在声明之后调用
  */

```

### arguments

作用:获取函数所有的实参

```javascript
function fn(a){
//是一个特殊的数组（伪数组，有数组的三要素，没有数组的方法）
console.log ( arguments );
console.log ( [ 10, 20, 30, 40 ] );
//2.注意点： 与形参一一对应
//2.1 如果修改了arguments，则形参也会修改
arguments[0] = 100;
console.log ( arguments );
console.log ( a );
//2.2 如果修改了形参，arguments也会改
a = 500;
console.log ( arguments );
console.log ( "1111" );
};
fn(10,20,30,40);

```

## 引用类型与值类型

值类型：（基本数据类型）  栈中存储的是数据，赋值的时候拷贝的是数据，修改拷贝后的数据对原数据没有影响

引用类型：（复杂数据类型）栈中存储的是地址，数据存在堆中。赋值的时候拷贝的是地址，修改拷贝后的数据对原数据有影响

```javascript
var a = 10;
    var b = a;
    b = 20;
    console.log ( b );//20
    console.log ( a );//10

    //2.
    var arr1 = [10,20,30];
    var arr2 = arr1;
    arr2[0] = 100;
    console.log ( arr2 );//[100,20,30]
    console.log ( arr1 );//[100, 20, 30]
```



# webapi

## id获取元素

```javascript
var banzhang = document.getElementById('div1');
    console.log ( banzhang );
    console.log ( typeof banzhang );

 //2.如果没有这个id，则返回null
    var a = document.getElementById('a');
    console.log ( a );
```

由于id具有唯一性，某些浏览器可以直接使用id名表示这个元素.不推荐： （1）有的浏览器不支持   （2）语义不明确

### 获取元素的属性

```javascript
//需求：修改班长的颜色（绿色）

    //1.获取元素(dom对象： 存储的是页面元素的信息 )
    var div1 = document.getElementById('div1');

    //2.对象的取值    (1)点语法  ： 对象名.属性名   (2)字符串语法： 对象名['属性名']
    console.log ( div1.id );//div1
    console.log ( div1['id'] );//div1

    console.log ( div1.style );//元素的style属性是一个对象（存储了元素的样式信息）
    console.log ( div1.style.width );//100px  带单位的字符串

    /*如果html中属性带-， font-  border- padding-  ,js获取属性需要转成驼峰命名法
        原因：  -不符合js命名规则
        驼峰命名法： 去掉-，将-后面的首字母大写

     */
    console.log ( div1.style.backgroundColor );//red

    //3.对象的赋值     取值 = 值;

    div1.style.backgroundColor = 'green';
    div1.style.width = '200px';
```

### 根据标签名获取元素

```javascript
 /**1.根据标签名获取页面所有的元素
     * @param 标签名字符串
     * @return 一定是数组  （伪数组，只有数组的三要素，没有数组的api）
     */
    var liList = document.getElementsByTagName('li');
    console.log ( liList );

    // liList.reverse();//伪数组不能使用数组的api
    //获取班长1
    var banzhang1 = liList[0];
    console.log ( banzhang1 );

    //2.如果找不到元素，则返回空数组
    var aList = document.getElementsByTagName('a');
    console.log ( aList );

    //3.获取父元素中的标签名元素： 使用父元素来调用getElementsByTagName
    var ul1 = document.getElementById('ul1');
    var ulLiList = ul1.getElementsByTagName('li');

    console.log ( ulLiList );

    //4. 根据id获取元素： id不能由父元素调用，只能是document调用
    // console.log ( ul1.getElementById ( "li2" ) );//程序报错

    /*根据标签名获取元素总结
    1.如果想要获取整个页面的标签名元素：  就使用document来调用getElementsByTagName
    2.如果想要获取某个父元素的标签名元素：  就使用父元素来调用getElementsByTagName
    3.如果Element后面没有s，则返回 元素|null ，如果Element后面有s，返回值一定是数组（伪数组）
    4.获取id，只能使用document来调用，因为id在整个页面都是唯一的
     */
```

### 根据类名获取元素

```javascript
    /**
     * 1.根据类名获取页面所有元素
     * @type {HTMLCollectionOf<Element>}  一定是数组
     */
   var oneList =  document.getElementsByClassName('one');
   console.log ( oneList );

   //2.类名开发中使用不多，因为IE8浏览器不支持
```

### 根据name值获取元素

```javascript
    /** 1.根据name属性值获取表单元素
    @param name属性值
     @return 表单元素数组
     */
    var userList = document.getElementsByName('check');
    console.log ( userList );
```

### 根据选择器获取元素

```javascript
    /** 1.根据选择器获取页面元素
    @param 选择器字符串
     querySelector:只会找到满足条件的第一个元素
     querySelectorAll: 会找到满足条件的的所有元素
     */

    var oneList = document.querySelector('.one');
    console.log ( oneList );

    var oneList1 =  document.querySelectorAll('.one');
    console.log ( oneList1 );
```

### 点语法取属性值 注意

```javascript
/*点语法操作元素属性注意点
            a. 只能获取行内属性，无法获取行外
            b. 获取的是string，带单位
            c. 既可以获取，也可以设置
            d.修改类名可以修改元素样式
     */

    //a. 只能获取行内属性，无法获取行外
    console.log ( box.style.width );//100px

    //b.获取的是string，带单位
    console.log ( box.style.height );// ''  空字符串


    //c. 点语法修改元素属性：没有行外行内限制，可以修改任何属性
    box.style.width = '200px';
    box.style.height = '200px';

    //d.修改元素类名 : 可以修改元素样式
    /*细节：获取类名需要使用 className   原因：class是js中的关键字*/
    console.log ( box.className );

    //1.1 直接赋值：会把以前的类名给替换掉
    // box.className = 'two';
    //1.2 添加类样式: 可以使用字符串连接符
    box.className += ' two';  //注意多个类名之间的空格
```

## querySelector

```javascript
//它可以让你像jQuery那样，传入选择器就找到对应的元素
// 总而言之，这个方法可以传入CSS的所有选择器
//document.querySelector('p'); //什么符号都不加，标签选择器
//document.querySelector('.p');//前面加.就是类
//document.querySelector('#p');//前面加#就是id
```

```javascript
//这个方法有个特点：永远只找到第一个，所以得到的一定是DOM对象，找不到得到null
// var li = document.querySelector('li');
// console.log(li);
// var test = document.querySelector('.test');
// console.log(test);
```

## 案例

### 原生js 隔行变色

```javascript
  /*1.分析需求： 点击按钮，修改li元素的颜色（单数行显示绿色，双数行显示粉色）
       2.思路分析：
            1.获取元素： 按钮  li元素列表
            2.注册事件：给按钮注册点击事件
            3.事件处理：修改li元素的颜色（单数行显示绿色，双数行显示粉色）
     */

    //1.获取元素
    var btn = document.getElementById('btn');
    var liList = document.getElementsByTagName('li');

    //2.注册事件
    btn.onclick = function (  ) {
        alert(1111);
        //3.事件处理：修改li元素的颜色（单数行显示绿色，双数行显示粉色）
        for(var i = 0;i<liList.length;i++){
            if (i%2==0){//单数行
                liList[i].style.backgroundColor = 'green';
            }else{//双数行
                liList[i].style.backgroundColor = 'pink';
            };
        };
    };
```

### 禁用表单元素

```javascript
//表单元素
//禁用表单元素
//启用时:将表单元素disabled 为false
//禁用时:将表单属性
```

## 表单

### 案例:一个按钮实现禁用启用表单

```javascript
    //1. 获取元素：
    var jy = document.getElementById('jy');

    var inputList = document.getElementsByTagName('input');

    /*如何获取一个元素的文字
    innerText
     */
    console.log ( jy.innerText );

    //2.注册事件：
    jy.onclick = function (  ) {
        //this:谁调用这个方法 this代表谁
        //3.事件处理
        //如果文字是禁用
        if (this.innerText == '禁用'){
            //（1）设置表单元素distable属性为true
            for(var i = 0;i<inputList.length;i++){
                inputList[i].disabled = true;
            }
            // (2)自身文字变成启用
            this.innerText = '启用';
        }else{//启用
            //（1）设置表单元素distable属性为false
            for(var i = 0;i<inputList.length;i++){
                inputList[i].disabled = false;
            }
            // (2)自身文字变成禁用
            this.innerText = '禁用';
        }
    }
```

## input输入框 焦点 onfocus用法

```javascript
//1.获取元素
    var search = document.getElementById('search');
    //2 注册事件

    //2.1 成为焦点
    search.onfocus = function (  ) {
        console.log ( "我出现光标了，此时可以输入文字" );

        if (this.value == '请输入搜索内容'){
            this.value = '';
        };
    };

    //2.2 失去焦点
    search.onblur = function (  ) {
        console.log ( "光标消失，我现在不能输入文字" );

        if (this.value.length == 0){
            this.value = '请输入搜索内容';
        };
    };
```

## 案例 全选全不选 反选

```javascript
//1. 获取元素：
      var checkList = document.getElementsByClassName('check');//选择框列表
      var checkAll = document.getElementById('checkAll');//全选
      var unCheckAll = document.getElementById('unCheckAll');//全不选
      var reverseCheck = document.getElementById('reverseCheck');//反选
      //2.注册事件：

      //2.1 全选
      checkAll.onclick = function (  ) {
          //3.事件处理：设置选择框列表的checked值为true
          for(var i = 0;i<checkList.length;i++){
              checkList[i].checked = true;
          };
      };

      //2.2 全不选
      unCheckAll.onclick = function (  ) {
          //3.事件处理：设置选择框列表的checked值为false
          for(var i = 0;i<checkList.length;i++){
              checkList[i].checked = false;
          };
      }

      //2.3 全不选
      reverseCheck.onclick = function (  ) {
          //3.事件处理：设置选择框列表的checked值与自身当前值相反

          for(var i = 0;i<checkList.length;i++){
              console.log ( checkList[ i ].checked );
              checkList[i].checked = !checkList[i].checked;

              // checkList[i].checked =  checkList[i].checked?false:true;

              // if (checkList[i].checked == true){
              //     checkList[ i ].checked = false;
              // }else{//false
              //     checkList[ i ].checked = true;
              // }
          };
      }
```

## innertext 和 textcontent和innerHTML

innerText:获取元素的文本(包含子元素文本)

innerText不是w3c标准语法,而是微软自己的语法,火狐42版本之前不支持

textcontent:作用与innertext完全一致

w3c标准语法:但是微软IE8及之前不支持

```javascript
function  getText( ele ) {
//能力检测
  if (ele.textContent){//IE8浏览器  如果textContent可以获取则使用textContent
  return ele.textContent;
}else{//如果textContent不能获取，就是用innerText
  return ele.innerText;
   };
};
```

innerHTML:会解析标签和文本





# PHP

## 语法

### 注释

```php
//单行注释
/**/多行注释
```

### 输出语句

```echo```

```php
echo 'hello world';
echo "<br>";
echo "hahah";
echo rand();//产生随机数
```

### 解决中文输入乱码的问题

```
header('content-type:text/heml;charset=utf-8');
```

### php变量的使用

```php
$变量名 = 值;
```

变量名 不能用数字开头,可以用下划线,字母开头,符合驼峰命名法,要有意义.

```php
$name = "张三";
$age = 18;
echo $name;
```

### php中的字符串

php中单引号和双引号引起来的都是字符串.

```php
$name1 = '张三';
#name2 = "李四";
```

#### php中拼接字符串

php中拼接使用```.```,不是```+```.

## sleep()

让代码休息sleep(多少秒)

### php中单引号和双引号字符串的区别

> php双引号字符串中有变量,会把变量的值取出来.
>
> php单引号字符串中有变量,不会解析变量,会把变量作为字符串的一部分.

```
$age1 = 18;
$age2 = 20;
echo "我的年龄是$age1";//输出 我的年龄是18
echo "<br>";
echo "我的年龄是$age2";
```

### if - else 结构

```php
$age = 16;
if($age >=18){
  echo "成年了,可以进网吧拉拉":
}else{
  echo "未成年,偷偷进网吧";
}
```

### if-else if-else 结构

```php
$age = 22;
if($age >=18){
  echo "成年了,可以进网吧啦啦啦";
}else if{
  echo "未成年,偷偷进网吧";
}else {
  echo "键盘都够不着,去你妹的网吧呀..";
}
```

```
switch($variable){
  case "value":
  break;
  default;
  
}
```

### 循环结构

```php
for ($i=0;$i<5;$i++){
  echo "林哥好帅,我们好爱你!ex":
  echo "<br>"
}
```

### 函数

```php
function sb(){
echo "我是个sb函数";
}
sb();
```

#### 在函数外面声明的变量,如果要在函数内部访问.

> **就要在函数内部使用globle定义一下**

```php
$age = 18;
function sb(){
  global $age;
  echo $age;
  echo "我是一个sb函数";

}
sb();
```

### 前自增&&后自增

```php
$age = 19;
$age++;
echo $age;
```

### php语言类型

> php和js一样都是弱类型语言(声明的时候不需要指定类型)

声明的时候不会确定变量的类型,执行的时候确定$age的类型

```php
$age = "abc";
$age = 18;
```

```int num = 19;```强类型语言,声明变量的时候要指定变量的类型

编译型:把所有的代码编程一个中间文件

```php
$age1 = 18;
$age2 = 18;
echo $age1 === $age2;
```

## 数组

### 索引数组

```php
$arr1 = array(10,20,30,40);
echo $arr1;//报错
var_dump($arr1);
```

> **复杂类型的数据,要用var_dump();来输出**

#### 添加元素

```php
$arr1[]=50;
$arr1p[]=60;
var_dump($arr1);
```

#### 取元素

```php
echo $arr1[4];
```

#### 遍历

```
for($i=0;$i<count($arr1);$i++){
  echo $arr1[$1]."&nbsp;&nbsp;";
}
```

> **数组的长度用count();方法取**

### 关系型数组

```php
$arr2 = array('name'=>'张三','age'=>18,'gender'=>true);
```

#### 添加元素

```php
$arr2['score']=100;
var_dump($arr2);
```

#### 获取某个元素

```php
echo $arr2['age'];
```

#### 遍历

```php
foreach($arr2 as key => $value){
  //echo $key;
  echo $value;
}
```

> 注意:foreach遍历的时候,如果as后面是一个东西,不管这个东西是什么哪怕是$key,那取到的也是数组的值.

```php
foreach($arr2 as $key){
  echo $key;
}
```

### 二位数组

数组的元素又是一个数组

#### 索引数组的元素是一个个的索引数组

```php
$arr3 = array(
	array(10,20,30),
  	array(100,200,300),
  	array(1,2,3),
);
var_dump($arr3);
```

#### 取值

```php
echo $arr3[1][1];
```

#### 遍历

```php
for($i=0;$i<count($arr3);$i++){
    var_dump($arr3[$i]);
    echo "<br>"
    for($j=0;$j<count($arr3[$i]);$i++){
        echo $$arr3[$i][$j]."&nbsp;&nbsp;";
    }
    echo "<br>";
}
```

#### 索引数组的元素是一个个的关系数组

```php
$arr4 = array(
    array('name'=>"张三",'age'=>18,"gender"=>true),
    array('name'=>"李四",'age'=>19,"gender"=>true),
    array('name'=>"王五",'age'=>20,"gender"=>false),
)
```

#### 取值

```php
echo $arr4[1]['name'];
```

#### 遍历

```php
for	($i=0;$i<count($arr4);$i++){
  var_dump($arr4[$i]);
  echo '<br>';
  foreach($arr4[$i] as $key => $value){
    echo $value."$nbsp;$nbsp";
  }
  echo "<br>";
}
```

### php写法

#### php和html混写方法一

##### php执行的流程

> php执行环境把php代码翻译成计算机能够识别的二进制代码,交给cpu执行.

> php代码返回给浏览器的是php代码执行之后的结果

```php
$arr1 = array('张三','李四','王五','赵六');
echo "<ul>";
	for($i=0;$i<count($arr1);$i++){
      echo "<li>".$arr1[$i]."</li>"
	}
echo "</ul>"
```

#### php和html混写的方法二

```php+HTML
<ul>
<?php
$arr1 = array('张三','李四','王五','赵六');
//遍历数组$arr1
for($i=0;$i<count($arr1);$i++){
 ?>
//这里的代码不是php代码,但属于php的for循环里
<li><?php echo $arr1[$i]?></li>
<?php 
}//在把上一个php的for循环的括号补上

?>
</ul>
```

#### php指令式写法

```php+HTML
<?php 
for($i=0;$i<5;$i++):
?>
<li>我是li标签</li>
<?php endfor;?>//for循环的结束语句
```

#### 分支结构的指令式写法

##### if-else结构

```php+HTML
$age = 8;
if($age >=18):
echo "我成年了";
else:
	echo "未成年";
endif;
```

##### if-else if-else结构

```php+HTML
$age = 6;
if($age >= 18):
	echo "我成年了";
elseif($age >= 14);
	echo "我快成年了";
else:
	echo "我不满14岁";
endif;
```

## form表单

> 需求input表单提交,需要加form表单元素.才能提交给后台

```php+HTML
1.form表单要写action属性,因为这个属性是提交数据的目标页面
2.表单标签提交数据是给name属性,因为这个属性的值是目标页面取数据的键
3.提交按钮要使用submit而不是button
4.form表单有一个method属性,定义传值方式,如果不写默认就是个get传值

```

### 引入数组文件

```php
include "./xx.php"
```

## 传值方式

### GET

> ```GET```方式传值本质是**拼接url**

```php
//传值的url格式是:目标页面?键=值&键=值
//使用一个超全局变量$_GET来接收
//echo $_GET;//数组不能用echo输出的
//var_dump($_GET);//$_GET是一个关系型数组
//echo $_GET['starName'];
```

> index.html

```html
<form action="./data.php" method="GET">
	<input type="text" name="starName" id="" placholder="请输入你喜欢的明星">
    <br><br>
    <input type="text" name="songName" id="" placeholder="请输入你最喜欢他的哪首歌">
    <br><br>
    <input type="submit">
</form>
```

> data.php

```php
//1.取值
$mxName = $_GET['starName'];
$gqName = $_GET['songName'];
//两种写法  第一种是字符串拼接
echo "<h2>原来你喜欢".$mxName."啊,我也很喜欢他,我也很喜欢他的那首".$gqName."</h2>"
//第二种是使用大括号包住变量
echo "<h2>原来你喜欢{$mxName}啊,我也很喜欢他, 我也很喜欢他的那首{$gqName}<h2>";
```

> 渲染出的html样子

```html
<h2>原来你喜欢xx啊,我也很喜欢他,我也很喜欢他的那首xx</h2>
```

### POST

> ``post``方式传值:不是通过url拼接,隐秘传值,保证数据的安全.
>
> post传值也让网页的url变得简洁

> **使用POST传值,一定要在form表单行内属性里表明使用POST**

```html
<form action="./do.php" method='POST'></form>
```

> 接收用户提交过来的用户名和密码

```php
var_dump($_POST);//也是一个关系型数组;
$userName = $_POST["userNmae"];
$userPwd = $_REQUEST["userPwd"];
```

### 总结

#### GET

1.GET传值用$_GET获取值

2.POST传值用$_POST获取值

3.不管GET还是POST,都可以用$_REQUEST获取值.

#### POST

1.POST方式传值,使用```$_POST``或者``$_REQUEST``来获取值.

2.POST传值不是拼接url,意味着没有大小限制.

3.POST传值不是拼接url,相对GET而言传递的数据更安全一些.

#### 那传递数据,选择GET还是POST

1.如果数据没有什么安全可言,那就可以使用GET.

2.如果数据很大,超出url的大小限制,那就不能使用GET了,就要使用POST.

3.GET侧重于获取;POST侧重于提交.

#### echo

```javascript
//echo $_GET;//数组不能用echo输出的
```

## header方法302重定向

```php
header('location:index.php');//后面跟着网页文件
```

# mysql数据库

## 数据库的执行语句

> 增.删.改.查

### 增

```mysql
insert into 表(键1,键2) values("值1","值2");
```

### 删

```mysql
delete from 表 where Id>=值;
```

### 改

```mysql
update 表 set 键1 = "值1",键2="值2"
```

### 查

```mysql
select * from 表;//查全部字段
select 字段1,字段2 from 表明 where 条件
```

### 排序

```mysql
order by 字段 desc/asc;
desc//
asc;//
```



### 使用php连接数据库

```php
<?php
    $link = mysqli_connect('数据库ip','数据库账号','数据库密码','数据库名称')
    ?>
```

### 返回结果

```php
$res = mysqli_query($连接的数据库,$执行的语句);
//res返回的是否成功
```

res返回的结果不是我们想要的,所以要对这个数据做一个处理.

如果不处理得到

```php
object(mysqli_result)#2 (5) { ["current_field"]=> int(0) ["field_count"]=> int(3) ["lengths"]=> NULL ["num_rows"]=> int(1) ["type"]=> int(0) }
```

所以我们必须使用```mysqli_fetch_all()``方法处理

**只有在查的时候需要使用此方法**

```php
eg:
$arr = mysqli_fetch_all($res,1);
```

处理完以后返回的结果是:

```php
array(1) { [0]=> array(3) { ["Id"]=> string(2) "13" ["userName"]=> string(2) "11" ["description"]=> string(2) "11" } }
```

### 关闭连接

```php
mysqli_close($link);
```

### 使用a链接的时候需要在href进行拼接

```php+HTML
<a href="./index.php?id=<?php echo $arr[0]['Id']?>">
```



### 使用input传文件

> 需要在form行内属性加enctype="multipart/form-data"

```html
<form enctype="multipart/form-data">
```

如果传带中文名字的文件,需要进行转码.网页传上去的是utf-8,而windows电脑默认是GBK编码.

```php
//转GBK
$file_newName = iconv('utf-8','gbk',$file_oldName);
```

#### 从tmp转移到指定的文件夹下

```php
$res = move_uploaded_file($tmp_path,$new_path)
```

### 增删改查封装成函数

### 增删改

```php
//增删改
function mysqli_excute_zsg($sql){
    //连接数据库
    $link = mysqli_connect('127.0.0.1','root','root','erjiuqi'); //括号中是连接数据库字符串
    //执行sql语句
    $res = mysqli_query($link,$sql);
    //获取受影响的行数.
    $rows = mysqli_affected_rows($link);
    //关闭数据库
    mysqli_close($link);

    //返回受影响的行数.
    return $rows;
}
```

### 查

```php
function mysqli_select($sql){
 //连接数据库
    $link = mysqli_connect('127.0.0.1','root','root','erjiuqi'); //括号中是连接数据库字符串
    //执行sql语句
    $res = mysqli_query($link,$sql);
    //处理结果.
    $arr = mysqli_fetch_all($res,1);
    //关闭数据库
    mysqli_close($link);

    //返回查询后的结果.
    return $arr;
}
```

#### 使用和测试方法

```javascript
//测试增删改方法.
// $sql1 = "insert into user(userName,description) values('洪桥','听说喜欢苍老师')"; 

//调用方法.
// echo  mysqli_excute_zsg($sql1);
```

### 引入php操作数据库工具文件

> 如果引入多次,也会当作一次引入

```javascript
include_once "./Tools/phpTools.php";
```



## cookie

> cookie是记录再本地浏览器中,所以一般我们不记录重要的数据,常记账号
>
> a.设置了cookie的过期时间,到了时间,就会自动删除.
>
> b.可以手动设置删除,给一个过去的事件.
>
> c.用户在浏览器端也可以删

### php中设置cookie

```php
setcookie();
//参数1:cookie名称
//参数2:cookie值
//参数3:过期时间 time()获取当前时间.  在当前时间基础上加上一些时间.
//eg.
setcookie('sb','sb123',time()+10);//20秒后过期
```

**修改**

```php
setcookie('sb','sbsbsb',time()+10);
//修改sb这个cookie的值为sbsbsb
echo "哈哈";
```

**删除**

```php
//手动设置删除,过期时间就给一个过去的时间
```

```php
setcookie('sb','sbsbsb',time()-10);//过期的时间是过去时间(当前时间前10秒);
```

```php
//cookie的值只能是字符串,不能是复杂类型的数据
setcookie('hahaha',array(10,20,30),time()+100);//报错了
```

**cookie有作用范围,同一个文件夹**

> 点击setcookie.php这个页面,实际上就是向服务器发送了一个请求报文.
>
> 服务器接受到这个请求后,就去执行这个页码中额php代码,把执行后的结果返回给浏览器.



## php中后去cookie

```php
//使用超全局变量$_COOKIE来取
echo $_COOKIE['userName'];
echo "<br>";
echo $_COOKIE['sb'];
```

### cookie案例:

```php
if($userName == 'admin' && $userPwd == '888888'){
   //登录成功! 
   echo "登录成功!";
   //设置一个cookie记录登录成功的用户名
   setcookie('userName',$userName,time()+60*60*24);
}else {
    echo "账号或密码错误!请<a href='index.php'>重新登录</a>";
}
```

```php+HTML
//案例:7天无广告
<?php
    if(!isset($_COOKIE['ad'])):
        //没有cookie,显示广告
    ?>
        <div class="ad">
            <p>这是你没有船新版本</p>
            <p>屠龙宝刀,点击就送</p>
            <p>点击<a href="./doCloseAd.php">关闭</a>,7天内不显示广告</p>
        </div>
    <?php endif;?> 
```

```php
//判断cookie中有没有账号
```

例如:

![](C:/Users/%E7%8E%8B%E5%8D%9A%E5%BA%86/Desktop/%E6%80%BB%E7%BB%93%E7%9A%84%E7%AC%94%E8%AE%B0/1521775614563.png)

```php
 <?php
    $value = "";
    //判断当前有没有userName的cookie.
    if(isset($_COOKIE['userName'])){
        //进到这里来,说明有userName这个cookie,说明刚才是登录成功了的.
        $value = $_COOKIE['userName'];
    }
    ?>
```

## session

### 定义

​    session可以理解为是服务器上的一个保险柜，把所有数据都保存在服务器的保险柜里，只给浏览器一把钥匙用来访问这些数据。

​    据都是存在服务器端，而浏览器端只存一把 `钥匙`。因为要把 `钥匙`给浏览器存起来，**存钥匙的技术还是cookie，所以说session技术是基于cookie的。**

### 新增session语法

```php
//一定要先调用此函数开启session!!!
session_start();
//通过超全局变量添加一条session记录
$_SESSION['名']= 值;
```

​     **cookie值一般是给字符串,但是在session中,除了可以给基本类型,还可以给复杂数据类型**

```php
//一定要先调用此函数开启session!!!
session_start();
//保存基本类型
$_SESSION['name'] = 'jack';
//保存复杂数据类型
$_SESSION['books'] = array('C语言从入门到入土','MySQL优化之道：从删库到跑路');
```

### 读取session语法

```php
//一定要先调用此函数开启session!!!
session_start();
//直接通过超全局变量可以取到session记录
var_dump($_SESSION);
//单独取出某条$_SESSION记录
echo $_SESSION['name'];
```

### 修改session语法

```php
// 开启session!!!
session_start();
//修改
$_SESSION['name'] = 'rose';
```

### 删除session语法

```php
// 开启session!!!
session_start();

// 删除保存的session
// 删除变量的值
unset($_SESSION['name']);
```

**session关闭浏览器删除了**

### session案例

> 检查session里面有没有这个记录值,如果有就说明登陆过,登陆成功,就直接登录
>
> 如果没有,则302跳转到登录页面,不会跳转到登陆后的页面.

```php
<?php
//这个首页不是什么时候都要被访问,只有登录成功才让访问这个首页.  (你都没有登录成功,那当然不让你访问这个首页啊)
//我这个首页这里,那我怎么知道你登录成功没有啊?
//就看你有没有名称为info的session. 如果有说明登录成功了.
session_start();
if(!isset($_SESSION['info'])){
    //进到这里来说明没有名字为info的session,说明没有登录. 那没有登录访问首页就应该打回到登录页面.
    header('location:login.html');
    return false;
}

?>
```





-