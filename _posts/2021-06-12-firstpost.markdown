---
layout: post
title:  "JAVA의 정석 공부 3일차"
date:   2021-06-12 13:00:00 +0900
category: sample
---

#  상속

### 상속이란?
=> 기존의 클래스를 재사용하여 새로운 클래스를 작성하는 것이다.  

ex)  

class Child extends Parent {  
  //...  
}

- 생성자와 초기화 블럭은 상속되지 않는다. 멤버만 상속된다.  
- 자손 클래스의 멤버 개수는 조상 클래스보다 항상 같거나 많다.  

### Object클래스 - 모든 클래스의 조상  

Object클래스는 모든 클래스 상속계층도의 제일 위에 위치하는 조상클래스이다.  
다른 클래스로부터 상속 받지 않는 모든 클래스들은 자동적으로 Object클래스로부터 상속받게 한다.  


# 오버라이딩

=> 조상 클래스로부터 상속받은 메소드의 내용을 변경하는 것을 오버라이딩이라고 한다.

### 오버라이딩의 조건

- 이름이 같아야 한다.  
- 매개변수가 같아야 한다.  
- 리턴타입이 같아야 한다.  
- 접근 제어자는 조상 클래스의 메소드보다 좁은 범위로 변경 할 수 없다.


### 오버로딩 vs 오버라이딩  

- 오버로딩 : 기존에 없는 새로운 메소드를 정의하는 것  
- 오버라이딩 : 상속받은 메소드의 내용을 변경하는 것  

# package와 import  

### 패키지

=> 패키지란 클래스의 묶음이다. 서로 관련된 클래스들끼리 그룹 단위로 묶어 놓음으로써 클래스를 효율적으로 관리 할 수 있다.  

- 하나의 소스파일에는 첫 번째 문장으로 단 한 번의 패키지 선언만을 허용한다.  
- 모든 클래스는 반드시 하나의 패키지에 속해야한다.  
- 패키지는 점을 구분자로 하여 계층구조로 구성 할 수 있다.
- 패키지는 물리적으로 클래스 파일을 포함하는 하나의 디렉토리이다.  

### 패키지의 선언

=> package 패키지명;

### import문

=> import 패키지명.클래스명; 또는 import 패키지명.*;

# 제어자

=> 제어자는 클래스,변수 또는 메소드의 선언부에 함께 사용되어 부가적인 의미를 부여한다.  
    제어자의 종류는 접근제어자 , 그 외의 제어자로 나눌 수 있다.  


### static

=> static은 '클래스의' 또는 '공통적인'의 의미를 가지고 있다.  

### final  

=> final은 '마지막의' 또는 '변경될 수 없는'의 의미를 가지고 있다.  

### abstract  

=> abstract는 '미완성'의 의미를 가지고 있다.  

### 접근 제어자  

=> 접근 제어자는 멤버 또는 클래스에 사용되어, 해당하는 멤버 또는 클래스를 외부에서 접근하지 못하도록 제한하는 역할을 한다.  

- private : 같은 클래스 내에서만 접근 가능하다.  
- default : 같은 패키지 내에서만 접근이 가능하다.  
- protected : 같은 패키지내에서 , 다른 패키지의 자손클래스에서 접근이 가능하다.  
- public : 접근 제한이 전혀 없다.  


# 다형성  

=> 조상클래스의 타입의 참조변수로 자손클래스의 인스턴스를 참조할 수 있도록 하였다.  

# 추상클래스

### 추상메소드  

=> 선언부만 작성하고 구현부는 작성하지 않은 채로 남겨 둔 것.  

ex) abstract 리턴타입 메소드이름();  

# 인터페이스

=> 인터페이스는 일종의 추상클래스이다. 
