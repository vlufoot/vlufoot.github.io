---
layout: post
title: "biz_statistics_intro"
excerpt_separator: "<!--more-->"
categories:
  - Data Science
tags:
  - Basic Statistics
---

## Objective
Can explain the concepts and statistical techniques used to data analysis.

<!--more-->

## WHY
* Number occupy the largest part of the information.
* We can make a desicion more effectively and predict result.
* Statics can be applicale to all field.

<!--more-->

## [History of Statistics](https://en.wikipedia.org/wiki/History_of_statistics)
The term "statistics" coined in 1749 in German. But There have been changes to the interpretion of the word over time. In early times, the meaning was restricted to information about states, particularly demographics such as population. This was later extended to include all collections of information of all types(Aliis Exterendum). In modern terms, it was extended to include the analysis and interpretation of such data. 

<!--more-->

## Process
통계란 더 나은 의사결정을 위해서 데이터를 수집하고 분석/구성하며 이를 표현하고 해석하는 학문이다.  
* Collect -> Organize(analysis) -> Present -> Interpret
* GIGO : Garbage in, garbage out (we should review causality)
<!--more-->

## Total inspection? Sampling inspection!

* Population(모집단) : All students in my school
* Sample(표본집단) : Students in our class
* Parameter(모수) : Measures used to describe a population
* Statics(통계량) : Measures computed from sample data  

COST Problem(All resource include time, money, human resource, etc)

- Viewer ratings(by using sampling)
- But we can do total inspection recently(big data era)
- 사실 시청률도 샘플링이기 때문에 신뢰구간과 오차범위를 제시해주는게 맞음
- 만약 스마트티비가 100% 보급되고 네트워크가 다 연결되면 실시간 전수조사로 시청률 계산 가능

<!--more-->

## Descriptive Statistics(기술통계학)

Describes and summarises data in an intuitive form. 데이터를 보기 편하게 정리하는 것. 보통 회사마다 form을 정해서 쓰기 때문에 잘 따라하면 됨.
* table
* graph

<!--more-->

## Inferential statistics(추리통계학)

make inferences about the popluation by using sampling data. 단, 집단은 다수의 개별 객체로 구성(표본집단은 랜덤하게 샘플링 되야함)  
ex)우리 반 40명의 몸무게를 재보니 평균 60kg네? 우리 학교 200명 전체의 몸무게 평균은 60kg +-오차범위 3kg 신뢰구간 95% 일거야!  
이제 오차범위는 어떻게 구하고 신뢰구간은 어떻게 정하냐? 이런거 배울거에요. 통계적 추론은 크게 두 가지로 나뉨

1. 추정(estimate) - 표본 집단의 몸무게를 측정해서 모집단의 평균 몸무게 추론
2. 가설 검정 - 모집단의 몸무게 평균이 70kg라는 가설을 세우고 검증

<!--more-->

## type of data

1. Categorical(정성) - 수치화 할 수 없는 정보
* 성별
* 지역
* 색깔

2. Numerical(정량) - 수치화 할 수 있는 정보  
  2-1. Discrete variable(이산) : the number of cups in my house  
  2-2. Continuous variable(연속) : weight, height
* 통장 잔고
* 자녀의 수
실제 세상에는 정성정보가 더 많음, 통계적으로는 정량적 변수들이 좋음

<!--more-->

## Type of scale

| 척도 | 설명 | 예시 |
| -------- | ------ |  ------ |
|Ratio Scale| Differences between measurements, true zero exists | Height, Age | 
|Interval Scale|Differences between measurements but no true zero|Temperature|
|Ordinal Scale|Ordered Categories (rankings, order, or scaling)|good 10 / soso 20 / bad 15|
|Nominal Scale|Categories (no ordering or direction)|What workers want? Salary / WLB / Better retirement|

통계분석하기에는 데이터간의 거리를 알기 쉽기 때문에 비율척도가 좋지만 실제로는 명목척도가 제일 많다.



<!--more-->



## reference
* wikipedia
* 경영통계 상명대 유태종교수님

