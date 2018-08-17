---
layout: '[layout]'
title: js小代码
date: 2018-06-05 17:22:08
tags: 代码
---
>将数字转化为金额:
   ```
   let num = 5262456.2158;
   num = toMoney(num);
   console.log(num);//打印结果    5,262,456.22


   //将数字转换成金额显示
   function toMoney(num){
       num = num.toFixed(2);
       num = parseFloat(num)
       num = num.toLocaleString();
       return num;//返回的是字符串23,245.12保留2位小数
   }
   ```

 >自定义log方法实现代理console.log()的功能，并在此基础上实现在每个输出前面增加一个递增的序号:
   var i = 0;
       function log(){
          i ++;
          var args = Array.prototype.slice.call(arguments); //为了使用unshift数组方法，将argument转化为真正的数组
          args.unshift(i);
          console.log.apply(console, args);
        };
      log('this num is 1'); // 1 this num is 1;
      log('this num is 2'); // 2 this num is 1;
    ```

1.
    arguments是传给log()函数的实参。比如你调用log('hello', 'world')，那么arguments就是['hello', 'world']。

    console.log.apply(console, arguments)这个主要是用来把arguments中的每个参数当作实参传递给console.log()的。如果直接像下面这样调用：

    console.log(arguments)

    那么会将arguments当作一个数组打印，而不是将其中的每一项作为参数传递给console.log()。也就是说，它的效果是：

    console.log(['hello', 'world']) // 打印数组的内容['hello', 'world']

    而我们希望的是：

    console.log('hello', 'world') // 这时才是打印字符串hello world

    apply就正好可以实现这种需求
2.
    console.log.apply(console, arguments)的意思是:
    让上面声明的那个log中的this由原来的指向切换到新的指向，即参数中的那个console——这句话是题主理解的重点咯~请看下面展开：
    如果不将第一个参数设置成console，你可以设置成window试试，于是上面的调用就变成console.log.apply(window, arguments)，那么因为log.apply中的this是指向第一个参数的即window`的，也就是：
    [纠正]因为console内部机制，用window调用是不合法的，只能用console自己调用！
    这是要这样写console.log.apply(console, arguments)的原因。

    而通过apply的调用，第二个目的是为了达到可以一次接受一个参数arguments列表。

    理解误区：
    console.log.apply(console, arguments)等同console.log(arguments)而不是console(arguments)，且此时的console.log是被apply处理过的，可以一次接受若干参数。
    表轻易的理解ax.apply(bx, arguments) ==> bx(arguments)

3.

如果function log2(x,y){console.log(arguments)}这里只能有arguments代替log2接收的不确定的参数，那么此时console.log(arguments)打印的是一个数组，不能真实打印出(x,y)，所以得用console.log.apply(arguments)。。



一道面试题:
var a = {n:1};
    var b = a;
    a.x = a = {n:2};
    console.log(a.x);
    console.log(b.x);

   step1 : a,b同时指向{n : 1};
   step2 : a.x的运算优先级高 ： 因此a.x = undefined;
   step3 : 此时 a = {n:2}, a重新指向了{n:2}; 因此a.x = undefined;
   step4 : b.x指向{n : 2}  因此b.x = {n : 2};

