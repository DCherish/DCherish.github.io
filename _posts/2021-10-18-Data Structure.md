---
layout: page
title:  "Data Structure"
subtitle: "Computer Science of Data Structure"
date:   2021-10-18 11:11:11 +0530
categories: ["CS"]
comments: true
---
## Pointer
👉 **자료형**과 **주소값**을 저장하는 변수  
👉 int *ptr = &a;  
👋 포인터 변수 앞 * 붙이면 해당 주소에 저장된 값을 의미  
👋 int a = 3; (가정) // cout << *ptr << endl; // 3 출력  
👋 & : 주소 연산자 (ampersand)  
👋 * : 역참조연산자 (asterisk)  

<br>

## Call-by-Value 🆚 Call-by-Reference ✔️
👉 Call-by-Value  
　　👉 **함수 호출 시 인자로 값(Value)**을 넘겨주는 방식  
　　👉 데이터를 복사하는 과정에서 발생  
👉 Call-by-Reference  
　　👉 **함수 호출 시 인자로 레퍼런스(Value)**을 넘겨주는 방식  
　　👉 따로, 데이터의 복사 연산이 필요하지 않아 성능 향상  
　　👉 원본 데이터 변경 막을때는 const  
　　👋 1. 포인터를 넘겨주는 방식 // add(&a, &b), void add(int *a, int *b)  
　　👋 2. 레퍼런스를 이용하는 방식 // add(a, b), void add(int &a, int &b)  

<br>

## 함수 오버로딩(Overloading) ✔️
👉 **동일한 이름을 가진 함수를 중복해서 정의**하는 것  
👉 단, 반드시 인자 개수 혹은 타입이 달라야 함  
👉 가능한 이유 : 호출할 함수를 매개변수의 정보까지 참조하기 때문  
👉 return 타입만 다를 경우는 error  

<br>

## 오버라이딩(Overriding) ✔️
👉 **상속** 받았을 때 **부모 클래스의 함수를 사용하지 않고** 다른 기능을 실행할 때 함수를 **자식 클래스에서 같은 이름으로 재정의**해서 사용하는 것  

<br>

## 프로그래밍 패러다임
👉 프로그래머에게 **프로그래밍의 관점**을 갖게하고 **코드를 어떻게 작성할 지 결정**하는 역할  
　　👉 명령형 프로그래밍  
　　　　👉 **무엇(What)**을 할 것인지를 나타내기보다 **어떻게(How)** 할 것인지를 설명하는 방식  
　　　　　　👉 객체 지향 프로그래밍 ✔️  
　　　　　　　　👉 프로그래밍에서 필요한 데이터를 **추상화**시켜 **상태와 행위를 가진 객체**를 만들고 그 **객체들 간의 유기적인 상호작용을 통해 로직을 구성**하는 프로그래밍 패러다임  
　　　　　　　　👋 코드 재사용이 용이하며, 유지 보수가 쉬우므로 대형 프로젝트에 적합  
　　　　　　　　👋 But, 처리속도가 상대적으로 느리므로, 객체가 많으면 용량이 커질 수 있음  
　　　　　　👉 절차 지향 프로그래밍(절차적 프로그래밍)  
　　　　　　　　👉 **순차적인 처리가 중요시** 되며 **프로그램 전체가 유기적으로 연결**이 되도록 만드는 프로그래밍 패러다임  
　　👉 선언형 프로그래밍  
　　　　👉 **어떻게(How)** 할 것인지를 나타내기보다 **무엇(What)**을 할 것인지를 설명하는 방식  
　　　　　　👉 함수형 프로그래밍  
　　　　　　　　👉 부수 효과를 없애고 순수 함수**를 만들어 **모듈화 수준을 높이는** 프로그래밍 패러다임  
　　　　　　　　👉 객체 지향 프로그래밍에서 멤버 변수를 다룸에 있어 예상치 못한 버그가 일어날 수 있기에 이를 보완하기 위해 쓰임  

<br>

## 제네릭 프로그래밍(Generic Programming) 🔥
👉 데이터 형식에 의존하지 않고, 하나의 값이 여러 다른 데이터 타입들을 가질 수 있는 기술에 중점을 두고 재사용성을 높일 수 있는 프로그래밍 방식  
👋 Generic Programming is a style of computer programming in which algorithms are written in terms of types to be specified-later that are then instantiated when needed for specific types provided as parameters  

<br>

## 객체 지향 프로그래밍의 5가지 키워드 ✔️
👉 클래스/객체, 추상화, 캡슐화, 상속, 다형성  

<br>

## Class ✔️
👉 어떠한 **객체**를 만들기 위해 **변수와 메서드를 정의**하는 **틀**  

<br>

## Object 🆚 Instance ✔️
👉 Object  
　　👉 소프트웨어 세계에 **구현할 대상**  
　　👉 클래스의 타입으로 선언되었을 때  
👉 Instance  
　　👉 소프트웨어 세계에 **구현된 실체**  
　　👉 객체가 메모리에 할당되어 실제 사용될 때  
　　👋 An Object is an Instance of a Class  
　　👋 a = Cookie() // a 객체는 Cookie 클래스의 인스턴스  

<br>

## 데이터 추상화(Data Abstraction) ✔️
👉 현실 세계의 사물을 **데이터적인 측면**과 **기능적인 측면으로 모델링**하여 시스템 내의 사물로 정의  

<br>

## 다형성(Polymorphism) ✔️
👉 **보이는 모습은 하나**이지만 **실질적**으로 **쓰이는 기능은 여러 가지로 수행 가능**하다는 것  
👋 Polymorphism is the provision of a single interface to entities of different types or the use of a single symbol to represent multiple different types  
👋 Overloading, Overriding  

<br>

## 상속(Inheritance) ✔️
👉 **이미 존재하는 클래스**로 부터 **기본적인 특성(멤버 함수 및 변수)을 물려받아 새로운 클래**스를 작성하는 것  
👋 Inheritance is when an object or class is based on another object or class, using the same implementation  
👋 Inheritance in most class-based object oriented languages is a mechanism in which one object acquires all the properties and behaviors of parent object  

<br>

## 캡슐화(Encapsulation) ✔️
👉 **관련있는 데이터와 함수를 하나의 단위**로 묶는 것  
👋 코드를 재수정없이 재활용할 수 있음  
👉 또한, 객체가 **기능을 어떻게 구현했는지 외부에 감추는** 것  
👉 즉, 정보 은닉의 의미를 포함하고 있음  

<br>

## 정보 은닉(Information hiding) ✔️
👉 객체 내의 데이터 및 함수에 대한 **접근 권한을 제어**  
👋 객체 안의 데이터가 다른 객체에게 잘못 조작되는 것을 막아줌으로 에러를 방지  
👋 public, private, protected  

<br>

## 접근 제한자 getter, setter 쓰는 이유
👋 getter, setter는 정보 은닉이라는 특성을 잘 보여주고 있음  
👉 사용하는 결정적인 이유는 **객체의 무결성을 보장**하기 위함  
👉 메서드를 통해서만 접근할 수 있기 때문에, **객체 안의 데이터가** 다른 객체에게 **잘못 조작되는 것을 막아줌**  
👉 또한, 메서드 안에서 매개변수같이 어떤 올바르지 않은 입력에 대해 사전에 처리할 수 있게 제한하거나 조절할 수 있음  

<br>

## OOP의 5대 원칙
👉 SOLID  
　　👉 단일 책임 원칙(Single Responsibility Principle) : 객체는 단 하나의 책임만 가져야 함  
　　👉 개방-폐쇄 원칙(Open Closed Principle) : 기존의 코드를 변경하지 않으면서 기능을 추가할 수 있도록 설계되어야 함  
　　👉 리스코프 치환 원칙(Liskov Substitution Principle) : 일반화 관계에 대한 이야기, 자식 클래스는 최소한 자신의 부모 클래스에서 가능한 행위는 수행할 수 있어야 함  
　　👉 인터페이스 분리 원칙(Interface Segregation Principle) : 인터페이스를 클라이언트에 특화되도록 분리시키라는 설계 원칙  
　　👉 의존 역전 원칙(Dependency Inversion Principle) : 의존 관계를 맺을 때 변화하기 쉬운 것 또는 자주 변화하는 것보다는 변화하기 어려운 것, 거의 변화가 없는 것에 의존하라는 것  

<br>

## Preprocessor
👉 **전처리기 구문(#으로 시작하는 구문)을 처리**하는 역할 // .cpp -> .i  
👋 A **Preprocessor** is a program that processes its input data to produce output that is used as input to another program  

<br>

## Compiler
👉 **고수준의 언어**를 기계어와 가장 유사한 상태인 **어셈블리어로 변환**하는 역할 // .i -> .s  
👋 A **Compiler** is a computer program that translates computer code written in one programming language into another language  

<br>

## Assembler
👉 **완전히 기계어로 변환**하는 역할 // .s -> .o  
👋 An **Assembler** program creates object code by translating combinations of mnemonics and syntax for operations and addressing modes into their numerical equivalents  

<br>

## Linker
👉 여러 개의 **오브젝트 파일들을 합치거나 라이브러리를 합쳐주는** 역할 // .o -> .exe  
👋 **Linker** is a computer program that takes one or more object files generated by a compiler and combines them into a single executable file, etc  

<br>

## Compile ✔️
👉 사람이 이해하는 언어를 **컴퓨터가 이해할 수 있는 언어로 바꾸어주는 과정**  
👋 컴파일 과정은 위의 4가지 과정(P -> C -> A -> L)을 거침  

<br>

## Build
👉 **소스코드 파일**을 실행 가능한 **소프트웨어 산출로 만드는** 과정  

<br>

## Interpreter
👉 고급 언어로 작성된 **코드를 한 줄씩 읽어 내려가며 실행하는** 프로그램  

<br>

## Compile Error
👉 **컴파일시 발생하는 에러**, 주로 **syntax 오류**로 인해 발생하는 에러  

<br>

## Runtime Error
👉 **프로그램 실행시 발생하는 에러**, 주로 **논리적 오류**로 인해 발생하는 에러  
👋 논리적 오류 ; Divide by Zero, Infinite Loop, Out of Bounds 등  

<br>

## Struct(C++)
👉 사용자가 **기본 타입을 가지고 새롭게 정의**할 수 있는 **사용자 정의 타입**  

<br>

## Template(C++)
👉 C++ 프로그래밍 언어의 한 기능으로, 함수와 클래스가 제네릭 형과 동작할 수 있게 도와줌  
👋 Templates are a feature of the C++ Programming language that allows functions and classes to operate with generic types  

<br>

## 프로그램 실행 순서
👉 1. 사용자가 OS에게 프로그램 실행을 요청함  
👉 2. OS는 프로그램의 정보를 읽어 메모리에 로드함  
👉 3. CPU는 프로그램 코드를 가져다 메모리를 관리하고 명령문을 실행  
👉 4. 동적메모리가 할당되면 FreeStore 영역을 사용 (아래쪽으로 이동)  
👉 5. 스택메모리가 할당되면 FreeStore 영역을 사용 (위쪽으로 이동)  

<br>

## 메모리 구조 ✔️
👉 Code  
　　👉 **작성한 소스코드가 들어가는 부분**, 텍스트 영역  
　　👉 실행 파일을 구성하는 구성하는 명령어들이 올라가는 메모리 영역  
　　👋 함수, 제어문, 상수 등이 이곳에 지정됨  
👉 Data  
　　👉 **프로그램의 시작과 동시에 할당되고, 프로그램이 종료되어야 소멸되는 영역**  
　　👋 **전역변수와 static 변수**가 이곳에 할당  
👉 Heap  
　　👉 **프로그래머가 할당/해제하는 메모리 영역**, 이 공간에 메모리 할당하는 것을 동적 할당이라고 함  
　　👉 런 타임에 크기가 결정됨  
👉 Stack  
　　👉 **프로그램이 자동으로 사용하는 임시 메모리 영역**  
　　👉 컴파일 타임에 크기가 결정됨  
　　👋 함수 호출시 생성되는 지역 변수와 매개변수가 이곳에 저장됨  
　　👋 함수 호출이 완료되면 사라짐  

⚠️ Heap과 Stack은 같은 공간을 공유  
⚠️ Heap은 위쪽 주소부터 할당되며, Stack은 아래쪽부터 할당되는 방식  
⚠️ 각 영역이 상대 공간을 침범하는 일이 발생할 수 있음  
⚠️ 이를, Heap Overflow, Stack Overflow  
⚠️ Stack 영역이 크면 클수록 Heap 영역이 작아지고, 반대도 동일함  

<br>

## static 변수
👉 **여러 객체가 하나의 변수를 공유하고자 할 때** 쓰이는 변수  
👉 compile 타임에 주소 및 크기가 결정, main 함수 실행되기 전 static area에 자리함  
👉 이 변수는 각각의 객체의 멤버로 존재하는 것이 X  
👉 접근할 수 있는 권한이 부여되는 개념

<br>

## using namespace std
👉 std ; C++ 표준 라이브러리의 모든 것은 std라는 namespace에 존재  
👉 namespace ; 모든 식별자(변수, 함수)가 고유하도록 보장하는 코드 영역  
👉 using ; 사용하겠다  

<br>

## Library
👉 **자주 사용하는 코드를 함수로 가공하여 정리해 놓은** 것을 재사용할 수 있게끔 해놓은 **일종의 코드 모음집**  

<br>

## Framework
👉 소프트웨어의 **구체적인 부분에 해당하는 설계와 구현**을 재사용이 가능하게끔 **일련의 협업화된 형태로 클래스들을 제공**하는 것  

<br>

## Library 🆚 Framework
👉 Library : **사용자가 흐름에 대한 제어**를 하며 **필요한 상황**에 가져다가 쓸 수 있음  
👉 Framework : **전체적인 흐름을 자체적으로 제어**함  

<br>

## Bubble Sort
👉 **O(n^2)**  
👉 **stable sort**  
👉 **in-place sort**  
👋 13 7 9 3 ➡️ 7 13 9 3 ➡️ 7 9 13 3 ➡️ 7 9 3 **13**  
👋 7 9 3 **13** ➡️ 7 3 **9 13** ➡️ 3 **7 9 13** ➡️ **3 7 9 13**  
👋 2개씩 지정, swap  

<br>

## Insertion Sort
👉 **O(n^2)** // Best일 경우 **O(n)**  
👉 **stable sort**  
👉 **in-place sort**  
👉 **거의 정렬이 되어 있을 경우 빠름**  
👋 **13** 7 9 3 ➡️ 13 **7** 9 3 ➡️ **7 13** 9 3  
👋 7 13 **9** 3 ➡️ **7 9 13** 3 ➡️ 7 9 13 **3** ➡️ **3 7 9 13**  
👋 한 곳 기준 정렬, 자신에게 맞는 위치에 insert  

<br>

## Selection Sort
👉 **O(n^2)**  
👉 **unstable sort**  
👉 **in-place sort**  
👋 **13 9** 7 3 ➡️ **13** 9 **7** 3 ➡️ **13** 9 7 **3**  
👋 **3** 9 7 **13** ➡️ 3 **9** **7** 13 ➡️ 3 **7 9** 13  
👋 하나 기준, 제외 min/max 찾은 후 swap  

<br>

## Merge Sort
👉 **O(nlogn)**  
👉 **stable sort**  
👉 **not in-place sort**  
👋 **7 2 9 4** ➡️ **7 2** | 9 4 ➡️ **7** | **2** | 9 4  
👋 **2 7** | 9 4 ➡️ 2 7 | **9 4** ➡️ 2 7 | **9** | **4**  
👋 2 7 | **4 9** ➡️ **2 4 7 9**  
👋 먼저 반으로 나누고, 후에 병합  
👋 병합 시 비교하며 순서에 맞게 & temp 배열이 필요(not in-place)  

<br>

## Quick Sort
👉 **O(nlogn)** // Worst일 경우 **O(n^2)**  
👉 **unstable sort**  
👉 **in-place sort**  
👋 3 7 8 1 5 9 6 10 2 4  
👋 **3** '7' 8 1 5 9 6 10 2 "4"  
👋 **3** '7' 8 1 5 9 6 10 "2" 4  
👋 **3** '2' 8 1 5 9 6 10 "7" 4  
👋 **3** 2 '8' 1 5 9 6 10 "7" 4  
👋 **3** 2 '8' "1" 5 9 6 10 7 4  
👋 **3** 2 '1' "8" 5 9 6 10 7 4  
👋 **3** 2 "1" '8' 5 9 6 10 7 4  
👋 **1** 2 "**3**" '8' 5 9 6 10 7 4  
👋 **1** "'2'" | 3 | **8** '5' 9 6 10 7 "4"  
👋 ...  
👋 3개의 포인터(p, l, r), l > r 되는 순간 swap(p, r) 

<br>

## Heap Sort
👉 **O(nlogn)**  
👉 **unstable sort**  
👉 **in-place sort**  
👋 3 7 8 1 5 9 6 10 2 4 ➡️ **1 2 6 3 4 9 8 10 7 5**  
👋 **1** 2 6 3 4 9 8 10 7 **5** ➡️ **5** 2 6 3 4 9 8 10 7 **1**  
👋 5 2 6 3 4 9 8 10 7 | 1 ➡️ **2 3 6 5 4 9 8 10 7** | 1  
👋 **2** 3 6 5 4 9 8 10 **7** | 1 ➡️ **7** 3 6 5 4 9 8 10 **2** | 1  
👋 7 3 6 5 4 9 8 10 | 2 1 ➡️ ...  
👋 index 순으로 parent와 비교 후 swap -> heapify  
👋 heapify 후 root와 end_index swap, end_index - 1까지 다시 heapify  
👋 priority_queue의 원리  

<br>

## Shell Sort
👉 **O(n) ~ O(n^2)** // Avg **O(n^1.5)**  
👉 **stable sort**  
👉 **in-place sort**  
👋 **삽입 정렬을 보완**한 알고리즘  
👋 삽입 정렬은 요소들이 삽입될 때, 이웃한 위치로 이동 // 삽입 정렬의 최대 문제점  
👋 따라서, **거의 정렬이 되어 있을 경우 가장 빠름**  
👋 code  
```c++
void shellsort(int p[], int n)
{
	int s, j = 0;

	for (int h = 1; h < n; h = 3 * h + 1)
	{
		s = h; // find h maxsize
	}

	for (int h = s; h > 0; h = h / 3) // h decrease, h는 size 개념
	{
		for (int i = h + 1; i <= n; i++)
		{
			int v = p[i]; // 하나 기준
			j = i;

			while (j > h && p[j - h] > v) // 기준보다 큰 것이 h칸 앞에 있다면
			{
				p[j] = p[j - h]; // swap
				j = j - h; // h칸 앞으로
			}

			p[j] = v; // v go to p[j]
		}
	}
}
```  

<br>

## Counting Sort
👉 **O(n+k)** // k가 클 경우 비효율적  
👉 **stable sort**  
👉 **not in-place sort**  
👋 **누적 합 technic**을 이용한 알고리즘  
👋 정렬하는 숫자가 특정한 범위 내에 있을 때 꽤 유용한 sort  
👋 범위가 크거나 적합하지 않을 경우 사용하면 매우 비 효율적  
👋 또한, 메모리 낭비가 심할 수 있음  
👋 code (pseudo)  
```c++
void countingsort(A, B, C, min, max)
{
        for (i = min; i <= max; i++) C[i] = 0; // 초기화

        for (i = 0; i < A.size; i++) C[A[i]]++; // ex) 해당 점수 개수 + 1

        for (i = min + 1; i <= max; i++) C[i] += C[i - 1]; // 누적합
        
        for (i = A.size - 1; i >= 0; i++) // ex) A 역순으로 맞는 자리 찾아 B에 할당 & 해당 점수 개수 - 1
        {
                 B[C[A[i]]] = A[i];
                 C[A[i]]--;
        }
}
```  

<br>

## Radix Sort
👉 **O(n)** // 정확하게는 **O(d(n+k))**  
👉 **must be stable**  
👉 **not in-place sort**  
👋 k는 10 (0-9) or 26 (a-z) ...  
👋 code  
```c++
void Radix_Sort()
{
        int Radix = 1;
    
        while (true) // d 계산 (최대 자리수)
        {
                if (Radix >= Max_Value) break; // Max_Value는 배열 중 최대값
                Radix = Radix * 10;
        }

        for (int i = 1; i < Radix; i = i * 10) // 1의 자리부터 10씩 곱하면서 최대자릿수 까지 반복
        {
                for (int j = 0; j < MAX; j++) // 모든 배열 탐색
                {
                        int K;
                        if (Arr[j] < i) K = 0; // 만약 현재 배열 값 해당 자릿수보다 작으면 0
                        else K = (Arr[j] / i) % 10; // 그게 아니라면 배열 기수 삽입
                        Q[K].push(Arr[j]); // Queue에 순차 저장
                }

                int Idx = 0;
                
                for (int j = 0; j < 10; j++) // Queue에 저장된 값들 순차적으로 빼내기
                {
                        while (Q[j].empty() == 0) // 해당 Index번호의 Queue가 빌 때 까지 반복
                        {
                                Arr[Idx] = Q[j].front(); // 하나씩 빼며 배열에 다시 저장
                                Q[j].pop();
                                Idx++;
                        }
                }
        }
}
```  

<br>

## 왜 Heap Sort 대신 Quick Sort를 사용?
👉 Big-O notation은 대략적인 측정 방법  
👉 **평균적으로 성능적 측면에서 Quick이 더 우수**  
👉 **Heapify**, n이 크면 클수록 이 과정이 꽤 영향을 미치기에 Quick이 우수  

<br>

## 왜 Merge Sort 대신 Quick Sort를 사용?
👉 Big-O notation은 대략적인 측정 방법  
👉 **평균적으로 성능적 측면에서 Quick이 더 우수**  
👉 not in-place, **분할 및 병합 과정이 꽤 영향을 미치기에** Quick이 우수  

<br>

## 왜 C++ sort는 Quick? 성능이 낮지 않을까?
👉 정렬은 오래 전부터 연구되었던 분야이기에 매우 개선된 Quick Sort가 C++ sort()로 제공되고 있음  
👋 Median-of-Three, random pivot, Insert Sort와의 응용(일반적 size 기준 200, 작으면 Insert 크면 Quick) 등  

<br>

## Binary Search ✔️
👉 **O(logn)**  
👉 **완전 탐색에 비해 압도적으로 빠름**  
👉 left, right로 mid를 설정  
👉 mid와 탐색했던 key 값과 비교  
👉 key 값이 mid보다 크다면, left = mid + 1  
👉 key 값이 mid보다 낮다면, right = mid - 1  
👉 key 값이 mid와 같다면, 탐색 완료  
👋 sort가 되어 있다는 가정 하에 탐색이 가능함  

<br>

## Bitmasking
👉 **0과 1로 flag를 활용하는 technic**  
👉 **집합의 요소들의 구성 여부**를 표현할 때 유용한 technic  
👉 **보통 AND, OR, XOR, NOT, <<(LS), >>(RS) 연산자와 자주 쓰임**  
👉 작은 메모리와 빠른 수행시간으로 해결이 가능  
👉 일반적으로 원소의 수가 작을 경우에 사용  
👋 0번, 3번, 5번 visit / else not visit  
👋 101001(2) -> 41(10)을 활용  

<br>

## Dijkstra Algorithm ✔️
👉 **최단 경로 탐색 알고리즘**  
👉 하나의 최단 거리를 구할 때 그 이전까지 구했던 최단 거리 정보를 이용  
👉 Priority Queue를 활용하여 구현이 가능  

<br>

## 최소 신장 트리(MST, Minimum Spanning Tree)
👉 **최소 비용의 스패닝 트리를 구현**하는 것  
👋 Kruskal, Prim  

<br>

## Kruskal Algorithm
👉 **최소 비용 신장 트리**를 만드는 알고리즘  
👉 **간선 우선** 및 cycle 방지의 특징이 있음  
👉 **Union-Find(Disjoint-Set)을 이용하여 cycle을 검사**함  

<br>

## Prim Algorithm
👉 **최소 비용 신장 트리**를 만드는 알고리즘  
👉 임의 정점을 시작으로, **정점 우선** 및 cycle 방지의 특징이 있음  
👉 Tree를 확장해나가는 조건이 MST에 연결된 정점에서 **아직 연결이 안된 정점에 대해서 확장을 진행하므로 cycle이 발생하지 않음**  

<br>

## Dynamic Programming ✔️
👉 **복잡한 문제를 간단한 여러 개의 하위 문제로 나누어 푸는 방법**  
👉 같은 하위 문제를 가지고 있는 경우, 결과 값을 저장하여 단 한 번만 계산하도록 구현, 이를 memoization  
👉 주로, 점화식을 통해 문제를 해결  
👉 **재귀를 이용하는 Top-down**, **반복문을 이용하는 Bottom-Up** 두 가지의 방식이 있음  
👋 Bottom-Up 방식으로 해결하는 것이 권장됨  
👋 스택의 크기가 한정되어 있으므로, 시스템상 재귀를 이용할 경우 불리할 수 밖에 없음  

<br>

## LinkedList
👉 연속적인 메모리 위치에 저장되지 않는 선형 데이터 구조  
👉 배열의 크기는 정해져 있고, 새로운 요소를 삽입하는 것에 비용이 많이 들기에 LinkedList를 사용  
👉 즉, 동적인 크기와 삽입/삭제에 용이  
👉 임의로 액세스를 허용할 수 없어, 첫 번째 노드부터 순차적으로 요소에 액세스 하므로 탐색에 있어 불리  
👉 포인터를 사용하므로 메모리 공간이 각 요소에 필요  

<br>

## Array 🆚 List
👉 Array  
　　👉 **크기가 정해져 있으며(수정 불가), stack 영역에 메모리 할당**  
　　👉 **삽입과 삭제시 비용이 크지만 인덱스를 이용한 검색이 최적화**  
　　👉 연속적이므로 메모리 관리가 편리  
　　👋 배열은 메모리 공간에 연속적으로 있기 때문에 해당 주소값 + (AxN)byte로 검색  
👉 List  
　　👉 **크기가 고정적이지 않으며, heap 영역에 메모리 할당**  
　　👉 **삽입과 삭제시 전후 노드의 참조 관계만 수정하면 되기 때문에 효율적**  
　　👉 첫 번째 노드부터 순차적으로 요소에 액세스 하므로 **검색은 비효율적**  
　　👋 리스트는 메모리 공간에 연속적으로 있지 않기 때문에 포인터를 따라가며 그만큼 시간이 소요됨  

<br>

## Stack
👉 입력과 출력이 한 곳(방향)으로 이루어지는 자료구조  
👉 **LIFO(Last In First Out)** 특징을 가지고 있음  
👋 웹 페이지(돌아가기, 돌아가기 Undo) 적합  

<br>

## Queue
👉 입력과 출력이 한 쪽 끝으로 이루어지는 자료구조  
👉 **FIFO(First In First Out)** 특징을 가지고 있음  
👋 버퍼에 저장되어 들어온 순으로 처리하는 방식에 적합  

<br>

## Deque
👉 입력과 출력이 양방향 모두 가능한 자료구조  
👋 구현이 어려울 뿐, Queue & Stack 모두의 특성을 가지고 있음  

<br>

## Tree
👉 값을 가진 **Node**와 이들을 연결해주는 **Edge**로 이루어진 자료구조  
👉 cycle이 존재할 수 없으며, cycle이 존재할 경우 그것은 graph 자료구조  
👋 **index를 통한 빠른 접근에 적합**  

<br>

## Graph
👉 값을 가진 **Vertex**와 이들을 연결해주는 **Edge**로 이루어진 자료구조  
👉 두 Vertex를 연결하는 Edge에 방향이 있는 경우 방향 그래프  
👉 두 Vertex를 연결하는 Edge에 방향이 없는 경우 무방향 그래프  
👉 두 Vertex를 연결하는 Edge에 비용이 존재할 경우 가중치 그래프  
👋 **cycle 관계의 data 관리에 적합**  

<br>

## Hash ✔️
👉 **연관배열 구조를 이용**하여 **key에 결과 값(value)를 저장**하는 자료구조  
👉 **해시 함수를 구현**하여 **데이터 값(key)을 해시 값으로 Mapping**  
👉 적은 자원으로 많은 데이터를 효율적으로 관리하기 위해 사용  
👋 index를 통한 빠른 접근에 적합  
👋 key; 해시 함수의 input  
👋 hash; 해시 함수의 결과물, 저장소(Slot)에서 value와 매칭되어 저장  
👋 value; 저장소에 최종적으로 저장되는 값으로 키와 매칭되어 있음  

<br>

## Map 🆚 HashMap
👉 구현 알고리즘의 차이가 있음  
👉 **Map**은 **RB Tree**에 기반을 두고 있음  
👉 **HasgMap**은 **Hash**에 기반을 두고 있음  

<br>

## Set
👉 중복을 허용하지 않고, 순서 없이 key를 저장하는 **집합** 개념의 자료구조  

<br>

## Map
👉 key를 기준으로 데이터를 정렬하며, **key와 value를 원소**로 저장하는 자료구조  

<br>

## Trie 🔥
👉 문자열에서 검색을 빠르게 도와주는 자료구조  

<br>

## Binary Search Tree
👉 **이진 탐색의 빠른 탐색이 가능한 장점**과 **연결 리스트의 빠른 삽입 및 삭제가 가능한 장점**을 동시에 갖고 있는 자료구조  
👉 **각 노드 기준**으로 **왼쪽 자식은 작은 값**을 갖고 있고, **오른쪽 자식**은 **큰 값**을 갖고 있음  
👉 검색 목적 자료구조이므로 중복이 있거나 많을 경우 비효율적, 중복이 없어야 함  
👋 중위 순회로 정렬된 순서를 읽을 수 있음  

<br>

## B Tree & B+ Tree
👋 이진 트리는 하나의 부모가 두 개의 자식밖에 가지질 못하므로, 균형이 맞지 않을 때 검색 효율이 선형검색 급으로 매우 떨어짐  
👉 **B Tree**는 데이터베이스, 파일 시스템에서 널리 사용되는 자료구조, **이진 트리를 확장하여 더 많은 자식의 수를 가질 수 있도록 일반화 시킨 것**  
👉 트리의 균형이 항상 맞다는 특성을 가지고 있음  
👉 B+ Tree는 데이터의 빠른 접근을 위해 B Tree와 LinkedList를 응용하여 인덱스 역할만 하는 비단말 노드가 추가로 구현  
👉 B Tree는 각 노드에 데이터가 저장되는 반면, B+ Tree는 index 노드와 leaf 노드로 분리되어 저장됨  

<br>

## RB Tree(Red-Black Tree) 🔥
👉 각 노드는 red or black의 색을 가짐  
👉 root node의 색은 항상 black  
👉 각 leaf node의 색은 black  
👉 어떤 노드의 색이 red라면 두 개의 child node의 색은 모두 black  
👉 모든 leaf node에서 root node까지 가는 경로에서 만나는 black 노드의 개수는 동일  
👉 이러한 특성을 만족하는 BST를 RB Tree  
👉 삽입되는 모든 노드의 색은 red, 하지만 조건을 만족하기 위해 경우에 따라 recoloring 혹은 restructuring 적용  

<br>

## Hash Table 충돌 방지 기법 🔥
👋 해시 충돌; 다른 내용의 데이터 값이 해시 값으로 Mapping 했을 때 같아진 상황  
👋 너무 많은 해시 충돌은 Hash Table의 성능을 저하  
👋 해시 함수를 잘 정의하여 해시 충돌을 최소화 해야함  
👉 1. Chaining; 해시 충돌이 발생하면 LinkedList로 데이터들을 연결하는 방식  
👉 2. Open Addressing; 해시 충돌이 일어나면 다른 버켓에 데이터를 삽입하는 방식  
　　👉 1) 선형 탐색; 다음 버켓 혹은 몇 개를 건너뛰어 데이터를 삽입  
　　👉 2) 제곱 탐색; 제곱만큼 건너뛴 버켓에 데이터를 삽입  
　　👉 3) 이중 해시; 다른 해시함수를 한 번 더 적용한 결과를 이용  

<br>
<br>

<script src="https://utteranc.es/client.js"
        repo="DCherish/DCherish.github.io"
        issue-term="pathname"
        theme="boxy-light"
        crossorigin="anonymous"
        async>
</script>