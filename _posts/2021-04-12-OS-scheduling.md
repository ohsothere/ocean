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

## 스케줄링이란?  
일들의 순서를 정하는 일  

#### 프로세스 스케줄링  
CPU를 사용하려는 프로세스들 사이의 우선순위를 관리하는 일  

#### 디스크 스케줄링  
디스크를 사용하려고 하는 프로세스들의 우선순위를 관리하는 일  
  

![](https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/images/Chapter3/3_02_ProcessState.jpg){: .align-center}

스케줄링은 처리율과 CPU 이용률 증가시키고 오버헤드/응답시간/반환시간/대기시간 최소화 시키는 기법이다. CPU가 쉬지않고 계속 열심히 일 할 수 있도록 계획을 잡아준다.  

## FCFS(First-Come, First-Served) 스케줄링
![](https://www.studytonight.com/operating-system/images/fcfs.png){: .align-center}  
  
FCFS는 먼저 프로세스를 요청한 프로세스부터 CPU를 할당한다. CPU가 할당되면 끝나 반납할 때 까지 다른 프로세스들은 기다려야한다.  

단점: 평균 대기시간이 길어진다.  


## RR 프로세스 스케줄링  

컴퓨터 운영에서 컴퓨터 자원을 사용할 수 있는 기회를 공정하게 프로세스들에게 부여한다. 각 프로세스에게 일정 시간을 할당하고 시간이 지나면 그 프로세스는 잠시 보류한 후 다른 프로세스에게 기회를 주는 식으로 기회를 부여하는 방식이다.  
  
![](https://s3.ap-south-1.amazonaws.com/s3.studytonight.com/tutorials/uploads/pictures/1604904974-71449.png){: .align-center}

단점: 겉보기에 공평해 보여도 짧은 작업이 긴 시간을 기다리기도 한다.  
중요한 프로세스가 나중에 수행될 수 있다.
