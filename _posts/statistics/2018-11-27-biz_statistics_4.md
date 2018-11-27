---
layout : post
title : "biz_statistics_Discrete Probability Distribution"
categories :
  - Data Science
tags :
  - Basic Statistics
---

## Terminology
Probability Density Function: 확률밀도함수
Cumulative Density Function: 누적분포함수
Continuos Probabiliy distribution : 연속확률분포
Discrete Probability Distribution : 이산확률분포
Binomial distribution: 이항분포
Poisson distribution: 푸아송분포



## 확률분포
* 확률변수 X에 대해 그 변수가 발생할 확률
* 확률값은 0~1, 모든 결과는 상호 배반, 총체적 망라를 만족하면 확률값의 합은 1
- 이산확률분포와 연속확률분포로 나뉨

EX) 동전 던지기

| X | p(x)|
|--------|
|0 | 1/8 |
|1 | 3/8 |
|2 | 3/8 |
|3 | 1/8 |
|T | 1   |

#### 확률 변수 Random Variable  

일정한 확률을 가지고 발생하는 결과에 수치가 부여되는 변수  

* 이산 확률 변수 : 변수 사이에 값이 존재x (학생 수, 시간 당 자동차 대수)
* 연속 확률 변수 : 변수 사이에 값이 존재 (시간, 온도, 돈같은것도 조단위 엄청 크면 1,2원 갭을 0 처럼 취급 가능)


#### 확률 분포 함수  
P(x) = 1/8 (x=0,3)  
       3/8 (x=1,2)  


#### 누적 분포 함수 ( Cumulative Distribution Function )


|X | p(x)       |
|--|------------|
|1 | 1/6 (x<=1) |
|2 | 2/6 (x<=2) |
|3 | 3/6 (x<=3) |
|4 | 4/6 (x<=4) |
|5 | 5/6 (x<=5) | 
|6 | 6/6 (x<=6) |
|T | 1          |


#### 확률 분포의 평균, 분산

- 이 확률 분포의 평균과 분산은 어떻게 이루어져 있을까~?
- 차가 팔린 댓수별 확률

|X | P(x)| XP(x) | (X-E(x))^2P(x) |
|--|-----|-------|----------------|
|0 | 0.1 |  0    |  0.441         |
|1 | 0.2 |  0.2  |  0.242         |
|2 | 0.3 |  0.6  |  0.003         |
|3 | 0.3 |  0.9  |  0.243         |
|4 | 0.1 |  0.4  |  0.361         |
|T | 1   | E(x)= 2.1 |  V(x) = 1.290 |



* 예제 : 이 확률을 어떻게 구했을까? 과거의 데이터를 통해 최근에 가중치를 주는 방식으로 구했을 지도!

* 테이블
* 즉, 2.1대 +- 표준편차 정도 팔 확률이 몇%다. 라고 말해야 함





## 1. 이산 확률 분포
* 확률값 사이사이에 값이 없는 경우 ( 주사위 값이 1.5가 나올 순 없다 )









## 이항 확률분포 (Binomial Probability Distribution)

* 2가지 상호 배반적인 결과만 갖고 반복 실행 (각각의 시행은 *독립*이라 가정)
* 함수로 표현하기 쉬움

```
P(X)=nCx 파이^x (1-파이p)^n-x
```
* 예제
* 엑셀
x | p(x)
0 | binom.dist(number_s, trials, probability_s, cumulative)

* 이항분포의 특징 (p.26)
n*파이=뮤
n*파이(1-파이)=시그마제곱

* 이항분포 테이블 보는 법

* 이항분포 그래프는 파이가 0.5에 가까울수록 정규분포 모양
* 이항분포 그래프는 n이 커질수록 정규분포 모양


## 푸아송분포

* 특정 간격 내에서 사건의 발생횟수를 확률 변수로 하는 확률 분포
* 시간, 거리, 지역, 부피 등
* 확률 값은 간격의 길이에 비례
* 간격과 간격 사이는 독립
-> 과거데이터를 고려하지 않음! (지금부터 일어날 일만)
-> 예1) 2시간 내에 열차가 안왔으므로 1시간 내에 열차가 올 확률은 매우 높지만 푸아송은 무시
-> 예2) 전등의 평균수명이 3000시간인데 현재까지 이용한 시간 고려X

```
공식
엑셀 식
푸아송 테이블 보기
```

### 예시
* 뉴스 1페이지 내에 오탈자의 갯수
* 한시간 내에 컴플레인 전화 수
* 하루에 팔리는 커피 수
*축구 게임 90분 내에 골 수

### 비행기 예제
* 과거 데이터를 통한 확률 갖고 있어야 함


### 특징
* 기본적으로 왼쪽에 치우침
* 뮤 값이 커질수록 대칭형태
* 이항분포와 달리 실험의 횟수(n)이 없으므로 무한대까지 나옴(물론 0에가까운 확률) => 한계점
* 즉, 오늘 우리 커피숍에 100명 올 확률 N명 올 확률 계산 가능



## 푸아송과 이항 분포
* n이 충분히 크고(100이상), 파이가 충분히 작다면(0.001) 이항확률분포는 푸아송분포로 대체 가능
* 특히, 'n*파이<5'를 만족하면 대체가능














## references

경영통계 / 유태종교수님
