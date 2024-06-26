자바 기초 정리
==============

## 목차
1. [OOP](#1-oop)
2. [Object](#2-object)
3. [Overloading](#3-overloading)
4. [Overriding](#4-overriding)
5. [JDBC](#5-jdbc)
6. [Interface vs Abstract](#6-interface-vs-abstract)

---
## 1. OOP
### 객체지향 프로그래밍
* Object-Oriented Programming
* 객체와 객체의 상호작용을 통해 프로그램이 동작함
* 객체가 서로 독립적이므로 코드간 결합이 느슨하여 유연한 코드 작성 가능
---

## 2. Object
### Object
* 객체지향에서 객체는 데이터(변수), 데이터에 관련된 동작(함수)을 모두 포함한 개념
* 같은 성질, 같은 구조와 형태를 가지는 객체는 등급으로 정의하고 등급에 속하는 객체를 그 등급의 인스턴스라 칭함
* ex)
기차역에서 승차권을 예약하는 경우 매표할 손님, 발매하는 동작이 하나의 객체
표를 발매하는 역무원과 동작인 승차권 발매가 하나의 객체임

---

## 3. Overloading
### 오버로딩
* 같은 이름의 메소드를 여러개 정의함
* 매개변수의 타입이 다르거나 갯수가 달라야함

```
public int add(int a){}
public int add(int a, int b){}
public int add(float a){}
```

---

## 4. Overriding
### 오버라이딩
* 상속에서 나온 개념
* 상위 클래스의 메소드를 하위 클래스에서 재정의

```
Class number{
  public int a;
  public int b;
  
  public void info(){}
}

Class add extends a {
  public void info(){   //  부모 클래스의 info() 재정의 오버라이딩
    int c = a + b;
  }
} 
```

---
## 5. JDBC
### Java Data Base Connection
* 자바에서 DB 프로그래밍을 하기 위해 사용되는 API
* 데이터베이스 종류에 상관없음
![image](https://user-images.githubusercontent.com/37949471/167779387-1fb479f3-43e4-4333-972f-4dc0558c44d9.png)
### JDBC 드라이버
* DBMS와 통신을 담당하는 자바 클래스
* DBMS 별로 맞는 JDBC 드라이버 필요 (jar)

---
## 6. Interface vs Abstract
### Interface
* 추상적인 틀을 구현하여 그 틀에 맞게끔 코드를 유도함
* 클래스와 달리 다중상속이 가능함
* 모든 메소드가 추상메소드
```
public interface 인터페이스명 {
  //상수
  public int a = 0;
  
  // 추상 메소드
  void add(매개변수, ...);
  
  // Java8에서 가능한 default 메소드
  default String c(String id){}
  
  // Java8에서 가능한 정적 메소드
  static void d(String id){}
}
```
### Abstract
* 추상메소드를 하나 이상 가진 클래스
* 자신의 생성자로 객체 생성 불가능

---

## 자바 메모리 영역
### 메서드 영역
* static 변수, 전역변수 클래스 정보 등이 저장됨

### 스택 영역
* 지역 변수, 매개변수, 메서드 등이 할당됨
* LIFO 방식 메모리


### 힙 영역
* new 연산자를 통해 동적할당 된 객체들이 저장됨
* 메모리는 GC를 통해 관리

---

### 메모리 상수풀 영역
* 힙 영역에서 생성되어 자바 프로세스 종료까지 유지되는 메모리 영역
* JVM에서 관리함








