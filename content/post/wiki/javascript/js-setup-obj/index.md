---
title: "JavaScript中创建对象以及函数"
date: 2021-08-13T20:33:59+08:00
slug: js-setup-obj
image: javascript.png
draft: false
tags: [javascript]
categories: javascript
---

# JavaScript中创建对象以及函数

## **工厂模式**

```js
function creatPeople(XXX,XX){
         var people=new Object() //可以类比为加工对象的原材料
         people.name=XXX;
         people.weapon=XX;
         people.run=function(){
            return this.name+'text'+this.weapon
         }  //以上步骤可以类比为加工对象的过程
         return people //注意一定要讲创建的对象返回 
         //可以类比为产品加工完毕出厂的工作
       }
        var test1=creatPeople('XXX','XXX');
        var test2=creatPeople('XXX','XXX');
```

------

## 基本模式

```js
var people1=new Object();
       people1.name='XXX';
       people1.weapon='XXX';
       people1.run=function(){
         return this.name+'text'+this.weapon
       }
```

------

## 构造函数模式

```js
function People(XX,XXX){
         this.name=XX;
         this.weapon=XXX;
         this.run=function(){
            return this.name+'text'+this.weapon
         }  
       }
var Test=new People('XX','XXX');
```

------

## **函数（function）**

**⑴函数也是一个对象**

**⑵函数中可以封装一些功能（代码），在需要时可以执行这些功能（代码）**

**⑶函数中可以保存一些代码在需要的时候调用**

**⑷使用typeof检查一个函数对象时，会返回function**

**⑸创建函数的三种方式：**

**①构造函数**

**②函数声明**

**③函数表达式**

###  **构造函数**

```js
var fun = new Function("console.log('hello world');");
```

### **函数声明**

```js
function 函数名（[形参1，形参2. . .形参N]）{

                         语句.  .  .

               }
```

### **函数表达式**

```js
var functionName=function([形参1，形参2. . .形参N]){
      //函数体
}
```

