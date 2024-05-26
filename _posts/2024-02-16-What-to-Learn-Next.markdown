---
layout: post
title: Java
date: 2024-02-16 21:07:20 +0900
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: java.png # Add image post (optional)
fig-caption: Java Logo #
tags: [Backend, Java]
---
`substring()`   
java.lang.String 클래스의 메소드   
문자열의 특정 부분을 잘라내는 데 사용   
`substring(int startIndex)` 설정한 startIndex번호부터 끝까지 리턴   
`substring(int startIndex, endIndex)` 설정한 startIndex번호부터 endIndex이전까지   
   
`valueOf()`: ()안에 객체를 형변환   
`valueOf(boolean)`   
`valueOf(double)`   
`valueOf(float)`   
`valueOf(int)`   
`valueOf(long)`   
`valueOf(String)`   
etc   

`StringBuilder`     
```java
String str1 = "String";
String str2 = "Builder";
str1 += str2;

System.out.println(str); // "StringBuilder"
```
2개의 String객체를 연산할 때 새로운 String을 생성된다.   
String 객체는 한 번 생성되면 변경할 수 없으므로 연산을하게 될 시 새로운 문자열이 생성이 되는 것이다.   
이전에 있던 문자열은 JVM의 GC가 처리하게 된다.   
String 객체끼리 더하게 되면 메모리 할당과 메모리 해제를 발생기켜 더하는 연산이 많아지므로 성능적으로 좋지 않음   
---
이를 해결하는게 `StringBuilder`이다.   
StringBuilder는 String과 다르게 mutable한 성질을 가지고 있어 값이 변할 수 있다.     
StringBuilder는 새로운 객체를 생성하는 것이 아니라 기존의 데이터에 더하는 방식을 사용하기 때문에 속도도 빠르고 상대적으로 부하가 적다.      
긴 문자열을 더하는 상황이 오면 StringBuffer, StringBuilder를 사용하는 게 좋다.


## Java

![Java Logo](/assets/img/java.png)