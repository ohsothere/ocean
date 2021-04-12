---
title:  "FCFS와 RR 프로세스 스케줄링 알고리즘"
excerpt: "선점형과 비선점형 프로세스 스케줄링"
toc: true
toc_sticky: true
categories:
  - 공부
tags:
  - 운영체제
last_modified_at: 2021-04-12T07:06:00-05:00
---

### 스케줄링이란?  
일들의 순서를 정하는 일  

##### 프로세스 스케줄링: 
CPU를 사용하려는 프로세스들 사이의 우선순위를 관리하는 일  

##### 디스크 스케줄링: 
디스크를 사용하려고 하는 프로세스들의 우선순위를 관리하는 일  

![OS프로세스](https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/images/Chapter3/3_02_ProcessState.jpg){: .align-center}

스케줄링은 처리율과 CPU 이용률 증가시키고 오버헤드/응답시간/반환시간/대기시간 최소화 시키는 기법이다. CPU가 쉬지않고 계속 열심히 일 할 수 있도록 계획을 잡아준다.

대표적인 비선점 스케줄링
FCFS 스케줄링
![](
FCFS는 먼저 프로세스를 요청한 프로세스부터 CPU를 할당한다. CPU가 할당되면 끝나 반납할 때 까지 다른 프로세스들은 기다려야한다. 

단점: 평균 대기시간이 길어진다
중요한 프로세스가 나중에 실행될 수 있다.

RR 
