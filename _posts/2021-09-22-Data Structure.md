---
layout: page
title:  "Data Structure"
subtitle: "Computer Science of Data Structure"
date:   2021-10-14 11:11:11 +0530
categories: ["CS"]
comments: true
---
## Pointer
#### 👉 **자료형**과 **주소값**을 저장하는 변수  
#### 👉 int *ptr = &a; // & ; 주소 연산자 (ampersand)  
#### 👋 포인터 변수 앞 * 붙이면 해당 주소에 저장된 값을 의미  
#### 👋 int a = 3; (가정) // cout << *ptr << endl; // 3 출력  

<br>

## Call-by-Value  VS  Call-by-Reference ✔️
#### Call-by-Value
👉 함수 호출 시 인자 전달 과정에서 발생  
👉 데이터를 복사하는 과정에서 발생  
#### Call-by-Reference
👉 전달되는 인자를 레퍼런스로 받으면 데이터의 복사 연산이 필요하지 않음 ∴ 성능 향상  
👉 원본 데이터 변경 막을때는 const  
👋 1. 포인터를 넘겨주는 방식 ; add(&a, &b) // void add(int *a, int *b)  
👋 2. 레퍼런스를 이용하는 방식 ; add(a, b) // void add(int &a, int &b)  

<br>

## 함수 오버로딩 ✔️
👉 동일한 이름을 가진 함수를 중복해서 정의하는 것  
👉 단, 반드시 인자 개수 혹은 타입이 달라야 함  
👉 가능한 이유 : 호출할 함수를 매개변수의 정보까지 참조해서 호출하기 때문  
👉 return 타입만 다를 경우는 error  

<br>

## 오버라이딩 ✔️
👉 상속 받았을 때 부모 클래스의 함수를 사용하지 않고 다른 기능을 실행할 때 함수를 자식클래스에서 같은 이름으로 재정의해서 사용하는 것  

<br>

## 객체지향프로그래밍
👉 프로그래밍에서 필요한 데이터를 추상화시켜 상태와 행위를 가진 객체를 만들고 그 객체들 간의 유기적인 상호작용을 통해 로직을 구성하는 프로그래밍 패러다임  
👋 포인터 변수 앞 * 붙이면 해당 주소에 저장된 값을 의미  






<br>
<br>

<script src="https://utteranc.es/client.js"
        repo="DCherish/DCherish.github.io"
        issue-term="pathname"
        theme="boxy-light"
        crossorigin="anonymous"
        async>
</script>