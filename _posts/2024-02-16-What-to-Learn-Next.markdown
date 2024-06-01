---
layout: post
title: Java
date: 2024-02-16 21:07:20 +0900
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: java.png # Add image post (optional)
fig-caption: Java Logo #
tags: [Backend, Java]
---
`contains()`: 해당 문자열에 지정한 문자열이 포함되어 있는지 확인하는 함수(대/소문자 구분)   
```java
String str = "StringContains"

System.out.println(str.contains("String")); // true
System.out.println(str.contains("lmnd")); // false
System.out.println(str.contains("ingCo")); // true
```

`toUpperCase()`: 문자열을 대문자로 변환   
`toLowerCase()`: 문자열을 소문자로 변환   
`trim()`: 문자열의 앞/뒤 공백문자를 제거하고 리턴
   
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
Stringd은 immutable 성질이여서 바뀌지 않지만      
StringBuilder는 String과 다르게 mutable한 성질을 가지고 있어 값이 변할 수 있다.     
StringBuilder는 새로운 객체를 생성하는 것이 아니라 기존의 데이터에 더하는 방식을 사용하기 때문에 속도도 빠르고 상대적으로 부하가 적다.      
긴 문자열을 더하는 상황이 오면 StringBuffer, StringBuilder를 사용하는 게 좋다.      
---        
`StringBuilder`(java.lang.StringBuilder) 기본생성자     
```java
StringBuilder sb = new StringBuilder();
```     

`append()`: 합치고 싶은 문자열 메소드 
```java
StringBuiler sb = new StringBuilder();
sb.append("String");
sb.append("Builder");
// "StringBuilder"
```     

`insert()`: index위치에 문자열 추가
```java
sb.insert(index, String); // String 이외에도 다른 기본형도 들어갈 수 있다 검색 ㄱ

sb.insert(6, "+++");
// String+++Builder
```

`toString()`: String으로 변환
```java
sb.toString();
// "StringBuilder
```

`reverse()`: 문자 뒤집기
```java
sb.revers();
// redliuBgnirtS
```

`deleteCharAt()`: 특정 index에 위치한 문자 하나 삭제
```java
sb.deleteCharAt(int index);

sb.deleteCharAt(6);
// "Stringuilder
```

`delete()`: start부터 end 이전까지 문자를 삭제 (start이상 end미만)
```java
sb.delete(int start, int end);

sb.delete(6, sb.length());
// "String"
```

`setCharAt`: 특정 index에 위치의 문자를 변경
```java
sb.setCharAt(int index, char);

sb.setCharAt(6, '9');
// String9uilder
```
---     



## Java

![Java Logo](/assets/img/java.png)