---
title: TypeScript的浅显理解
categories:
  - [学习, 前端, TypeScript]
date: 2024-03-12 08:54:41
tags:
---

# 引言
:::primary no-icon
TypeScript是JavaScript的超集 
可以被编译成纯净的JavaScript 
与JS区分的就是[强类型语言].{purple}的特点
:::
![image.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/36561e7654a34197a31724ed0bfb6857~tplv-k3u1fbpfcp-watermark.image?)

# TypeScript基础 

## 基本数据类型 
1. boolean 布尔
```TypeScript 
let flag: boolean = true;
```
2. number 数字
```TypeScript 
let num: number = 5.20;
```

3. string 字符串
```TypeScript 
let str: string = "Mayuri";
```
4. array 数组
```TypeScript 
let arr1: number[] = [6,6,6,6,6,6];
let arr2: Array<string> = ['JavaScript','TypeScript'];
let arr3: string[] = ['js','ts']; 
```
5. tuple 元组
```TypeScript 
// 元组类型可以指定元组类的每个元素的类型
let tup: [boolean, number, string] = [true, 1, 'Mua']
```

6. enum 枚举
```TypeScript 
enum Color{
  Red = '红色',
  Yellow = '黄色',
  Blue = '蓝色'
}
let singleColor: Color = Color.Red;
```

7. any 任意类型
```TypeScript 
// 不指定具体类型，类似js
let element1: any = 4;
let element2: any = 'string';
```

8. void 空类型
```TypeScript 
// 常用于函数无返回值
function printLog(): void {
  console.log('this is a log');
}

let a: void = undefined;
let b: void = null;
```

9. Null/Undefined
```TypeScript 
// 默认情况下该类型是所有类型的子类型 
// 可以赋值给其他类型 
let a: null = null;
let b: undefined = undefined;
``` 
10. Never 
```TypeScript 
// never类型比较特殊 表示为永不存在 
// never也同样是所有类型的子类型

// 返回never的函数必须存在无法达到的终点
function error(message: string): never {
    throw new Error(message);
}

// 推断的返回值类型为never
function fail() {
    return error("Something failed");
}

// 返回never的函数必须存在无法达到的终点
function infiniteLoop(): never {
    while (true) {
    }
}
```
11. Object
```TypeScript 
// 非原始类型
let obj = {
  name: 'Steve',
  age: 25
}
```