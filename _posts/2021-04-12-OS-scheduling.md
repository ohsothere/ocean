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
##### 일들의 순서를 정하는 일  
처리율과 CPU 이용률 증가, 오버헤드/ 응답시간/ 반환시간/대기시간 최소화 시키는 기법, CPU가 쉬지않고 계속 열심히 일 할 수 있도록 계획을 잡아줌  

#### 프로세스 스케줄링  
CPU를 사용하려는 프로세스들 사이의 우선순위를 관리하는 일  
  

![](https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/images/Chapter3/3_02_ProcessState.jpg){: .align-center}
  
  
  
## FCFS(First-Come, First-Served) 스케줄링
![](https://www.studytonight.com/operating-system/images/fcfs.png){: .align-center}  
  
FCFS는 먼저 프로세스를 요청한 프로세스부터 CPU를 할당한다. CPU가 할당되면 끝나 반납할 때 까지 다른 프로세스들은 기다려야한다. 선점 방식보다 스케줄러 호출 빈도가 낮고 문맥 교환에 의한 오버헤드도 적다. 일괄처리 시스템에 적합하며 CPU 사용 시간이 긴 하나의 프로세스 짧은 여러 프로세스를 오랫동안 대기시킬 수 있으므로, 처리율이 떨어질 수 있다는 단점도 있습니다.  

단점: 평균 대기시간이 길어진다, 처리율이 떨어진다.
  
  
## RR 프로세스 스케줄링  

컴퓨터 운영에서 컴퓨터 자원을 사용할 수 있는 기회를 공정하게 프로세스들에게 부여한다. 각 프로세스에게 일정 시간을 할당하고 시간이 지나면 그 프로세스는 잠시 보류한 후 다른 프로세스에게 기회를 주는 식으로 기회를 부여하는 방식이다. CPU를 강제로 빼앗아 사용할 수 있으니 빠른 응답시간을 요하는 대화식 시분할 시스템에 적합하고 긴급한 프로세서를 제어할 수 있다.
  
![](https://s3.ap-south-1.amazonaws.com/s3.studytonight.com/tutorials/uploads/pictures/1604904974-71449.png){: .align-center}

단점: 겉보기에 공평해 보여도 짧은 작업이 긴 시간을 기다리기도 한다.  
중요한 프로세스가 나중에 수행될 수 있다.  
  
  
  
### FCFS vs RR

FCFS(First-Come, First-Served)는 (실행 -> 대기), (실행 -> 종료) 
RR(Round-Robin)는 (실행->대기) (실행->준비)(대기->준비)(수행-종료) 적용  


#### 오버헤드(overhead)
어떤 처리를 하기 위해 들어가는 간접적인 처리 시간 · 메모리 등을 말한다. 예를 들어 A라는 처리를 단순하게 실행한다면 10초 걸리는데, 안전성을 고려하고 부가적인 B라는 처리를 추가한 결과 처리시간이 15초 걸렸다면, 오버헤드는 5초가 된다

#### 시분할 시스템(time-sharing)

컴퓨터를 대화식으로 사용하려는 시도에서 탄생하였다. 시분할 운영 체제는 CPU 스케줄링과 다중 프로그래밍을 이용해서 각 사용자들에게 컴퓨터 자원을 시간적으로 분할하여 사용할 수 있게 해 준다.  
