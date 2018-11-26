---
layout: post
title: "biz_statistics_2_DescriptiveStatistics"
excerpt_separator: "<!--more-->"
categories:
  - Data Science
tags:
  - Basic Statistics
---

## Descriptive Statistics
첫 글에서 말했듯이 통계학은 크게 기술통계학과 추리통계학으로 나뉩니다. 기술 통계는 수집한 데이터를 요약 묘사하는 통계 기법이에요. 크게 두가지를 알면 데이터를 잘 묘사할 수 있습니다.  

1. 집중화 경향(Central Tendency)  
우리가 수집한 데이터들을 대표하는 값은 무엇일까요? 어떤 값에 집중되어 있는지 알아야겠죠. 대표적으로 네 가지 종류의 대표값이 있습니다.

- 산술평균(Arithmetic mean)  
데이터가 *등간척도* 이상이어야 함

- 가중평균(Weighted mean)  
중요도에 따라 가중치를 곱하여 평균을 구한 값  
w값을 얼마나 잘 정의하느냐가 중요

- 중앙값(median)  
데이터들을 크기 순서로 늘어놨을때, 총 수가 n일때 이 홀수면 (n+1)/2번째의 데이터, n이 짝수일때는 n/2번째와 (n+2)/2번째의 산술평균  
극단적으로 작거나 큰 값에 의해서 대표값에 영향을 크게 받지않는 장점  
비율, 등간, 서열 척도에서 계산 가능  
개방형 분포일때도 중앙값이 개방부분에 있지 않다면 산출 가능(정규분포)

- 최빈값(mode)  
가장 빈번히 관찰된 값


2. 분산도(Variation)  
우리가 수집한 데이터가 어떻게 퍼져있는지 알야야겠죠. 데이터가 한곳에 뭉쳐있는지 잘 퍼져있는지 알 수 있습니다.

- 분산  
항상 양수, 모든 값이 같을 때는 0 (커질수록 퍼짐)  

왜 표본분산은 N-1로 바뀔까? 분모가 작아면 분산이 커짐  
샘플을 뽑을때 모집단의 특징을 완전히 뽑을 수 없고 덜퍼져있는 애들을 뽑을 수 밖에 없다.  
모집단에 가깝게 하기 위해서 키우는 것  
내가 어떻게 할수 없는값 만큼 줄여줌(자유도의 특징)  
n이랑 X는 내가 정할 수 있지만 X바는 어떻게 할 수 없기 때문에 1 빼주는 것  

- 표준편차
- 사분위값  

예를 들어, 2013년의 서울의 집 한대의 평균 값이 10억이라고 합시다. 이는 산술평균을 이용한 서울 집 가격 데이터의 대표 값입니다. 하지만 서울 내에서 강남은 30억이 될 수도있고 다른 곳은 5억이 될 수도 있습니다. 그 편차가 크다면 분산이 크다는 것을 의미하고 이는 서울 내에서 집값의 차이가 크게 차이난다는 것을 알 수 있겠죠. 또한 대표값들이 다 똑같은 자동차 부품 공급처가 있다고 치자. 분산도가 높은 B공급처는 분산도가 낮은
A 공급처에 비해 불안정하기 때문에 공급 받는 회사 입장에선 RISK가 증가함.






## Frequency distribution (도수분포)

- 자료를 일정한 수의 범위 혹은 항목(명목일때)으로 나누어 분류하고, 각 범위 별로 수량을 정리한 표
- 이때, 범위는 반드시 상호 배타적(**mutually exclusive**)으로 분류되어야 함 => 영역별 겹치는 부분이 없어야 된다는 당연한 말

## Relative frequencies (상대 도수)
* 각 범위가 전체에서 차지하는 비율을 계산(합이 1이 되도록)





## Applewood$Location (명목척도)
- 변수 : Age, Profit, Location, Vehicle-Type, Previous
* 엑셀 피벗 테이블 활용하기 => 다차원의 데이터를 2차원 형태의 도수분포의 형태로 표현 가능
* 지역별 차량타입별 판매 수
* 우린 r로 해봅시다

```{r}
library(readxl)
library(ggplot2)
apple <- read_excel("Applewood_2011.xls")
table(apple$Location)
```
```{r}
# 도수분포
qplot(apple$Location)
```
```{r}
# 상대도수분포
freq <- prop.table(table(apple$Location))
barplot(freq)
```
```{r}
# 누적도수분포표
cumsum <- cumsum(freq)
barplot(cumsum)
```



## Applewood$Profit

- 계급 이란 변량을 일정한 간격으로 나눈 구간
- 계급의 크기를 어떻게 정할까?
- 절대적인 방법론은 없지만 *2 to the K-rule* 을 써보자


1.  2^k > n 을 만족하는 가장 작은 k
```{r}
# there were 180 vehicles sold, n=180.

k=1
while(2^k<180) {k=k+1}
print(k)
```

2. i>= (M-m)/k
```{r}
# 374.75 반올림해서 400
i = (max(apple$Profit) - min(apple$Profit)) / k
round(i, digits = -2)
```

3. 계급구간 확인 + 도수산출
```{r}
# 그냥 히스토그램쓰자..^^
hist <- hist(apple$Profit, breaks=k)
hist$breaks

hist(apple$Profit)
```

- cut 함수 활용
```{r}
table(cut(apple$Profit,breaks = k))

```

## Frequency polygon (도수분포 다각형)

- 히스토그램의 중간점을 이은것
- 집단간 비교를 할때 강점을 가짐

## Cumulative Frequency Distribution (누적도수)

- 75%안에 드는 사람이 누구냐 같은 것 알고 싶을 때
- 데이터분석 -> 히스토그램 -> 파레토+누적+차트출력 체크
- 위에 세구간이 우리의 75%차지함. 거기에 집중하자는 의사결정.
- Longtail이란?




## references
경영통계 / 
