---
title: 用Java编写一个简易的计算器
tags: []
id: '193'
categories:
  - - Java
date: 2020-04-27 09:48:43
---

思路： 利用Scanner建立一个扫描对象，在用switch语句进行判断。

```java
public class Calculator {
    public static void main(String[] args) {
        Scanner scanner =new Scanner(System.in);
        System.out.println("请输入计算的A值");
        double a =scanner.nextDouble();
        System.out.println("运算符");
        String b =scanner.next();
        System.out.println("请输入计算B值");
        double c =scanner.nextDouble();
        switch (b){
            case "+" :
                System.out.println(add(a,c));
                break;
            case "-" :
                System.out.println(sub(a,c));
                break;
            case "*" :
                System.out.println(multiply(a,c));
                break;
            case "/" :
                System.out.println(div(a,c));
                break;
        }
        scanner.close();
    }
    public static  double add(double a ,double b){
        double c=a+b;
        return c;
    }
    public static  double sub(double a ,double b){
        double c=a-b;
        return c;
    }
    public static  double multiply(double a ,double b){
        double c=a*b;
        return c;
    }
    public static  double div(double a ,double b){
        double c=a/b;
        return c;
    }
```

也可以把判断的内容从main里面分开来进行调用的。