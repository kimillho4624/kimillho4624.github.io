---
layout: post
title:  "JAVA의 정석 공부 1일차"
date:   2021-05-30 13:00:00 +0900
category: sample
---

#  변수

### 변수란?
=> 단 하나의 값을 저장 할 수 있는 공간


### 변수의 선언 

ex) int number; 

###변수의 명명규칙

1. 대소문자가 구분되며 길이의 제한이 없다.
2. 예약어를 사용해서는 안 된다.
3. 숫자로 시작해서는 안 된다.
4. 특수문자는 `_` 와 `$`만을 허용 한다.

### 변수 타입 

=> 기본형 , 참조형

### 논리형 - boolean

true와 false 중 하나를 저장 할 수있다. default는 false 이다.

### 문자형 - char

char 한 가지 자료형 밖에 없다.

### 정수형 - byte , short , int , long

long 타입은 반드시 접미사 L , l 붙여야 한다. 안붙이면 int로 간주한다.

### 실수형 - float , double

float 보다 double 이 정밀도가 높다.

### 형변환

=> 변수 또는 리터럴 타입을 다른 타입으로 변환하는 것이다.


# 연산자

증감 연산자(++)

전위형 : 값이 참조되기 전에 증가 시킨다.
후위형 : 값이 참조된 후에 증가 시킨다.

ex) ++i 가 i=i+1 보다 더 적은 명령만으로 작업하기 때문에 더 빠르다.

삼항 연산자

=> (조건식) ? 식 1 : 식 2

# 조건문과 반복문

### 조건문

문자열 비교는 ==가 아닌 equals()를 사용해야 한다.

### 반복문

이름 붙은 반복문

// for문에 Loop1이라는 이름을 붙인다.
Loop1 : for(int i=2; i <=9; i++) {  
    for(int j=1; j<=9; j++>){  
        if(j==5)  
            break Loop1;  
            System.out.println(i+"*"+j + "-" + i+j);  
    }  
}  

for문에 Loop1이라는 이름을 붙였다. 그리고 j가 5일때 break문을 수행하도록 했다.  
break문은 자신이 속한 하나의 반복문만 벗어날 수 있다. 하지만  
반복문에 이름을 붙여주고 break문에 반복문 이름을 지정해주면 하나 이상의 반복문도 벗어날 수 있다.  

# 배열

## 배열의 선언

ex) int[] score = new int[5]
ex) int[] score;  
    score = new int[5];

ex) int[] score = {100, 90, 80, 70, 60}

ex) int[] score;  
    score = new int[]{100,90,80,70,60}


## 배열의 복사

System 클래스의 arraycopy()를 사용 하면 된다.

ex) System.arraycopy(arr1,0,arr2,0,arr1.length);  
                    => arr1[0]에서 arr2[0]으로 arr1.length개의 데이터를 복사  

## System.currentTimeMillis();

=> 현재시간을 보여준다

해당 자바 로직이나 쿼리가 동작하는 시간이 얼마나 걸렸는지 궁금할때 시작 , 종료 부분에 찍어놓으면 좋을 것 같다.

