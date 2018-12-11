---
layout : post
title : "biz_statistics_sampling"
categories : Data Science
tags : Basic statistics
---

## Terminology

- Sampling error : 표본오차 ( 우리반 30명중에 10명 표본을 뽑아서 몸무게를 잰다고 했을때 모집단의 몸무게와의 차이,
즉, 표본을 사용함으로써 생기는 오차)

- Non-sampling error : 비표본오차 ( 모델링을 잘못하거나 배경지식이 잘못되어 생기는 오차 / 이론적으로 잘못된 접근)

- Bias : 편의 (표본 추출할 때 가장 신경써야 하는 부분 -> 상명대 키평균 구하고싶은데 농구부 애들의 키를 재다니?? / 즉, unbiased하게 뽑아야 함)

- Probability sampling : 확률 표본 추출법
- Simple random sampling : 단순 무작위 추출법
- Statified sampling : 층별 추출법
- Cluster sampling : 군집 추출법
- Systemic sampling : 체계적 추출법

- Sampling distribution : 표본분포
- Central limit theorem : 중심극한정리
- Degree of freedom : 자유도


## Objective

- 샘플의 중요성
- 샘플링 방법
- 표본 오차
- 표본 평균의 표본분포
- 중심극한정리
- 평균의 표준오차


## 확률적 표본추출

1 부터 백만까지의 숫자에 1000개를 뽑으라고 사람에게 시키면? 사람은 편향되지 않게 동일한 확률로 뽑을 수 없다.  


#### 단순 무작위 추출
모집단의 구성분자들이 선택될 가능성이 모두 동일한 확률로 구성되도록 하는 표본 추출 방법.  
난수생성을 통해 무작위 표본추출을 할 수 있다.


#### 체계적 무작위표본 추출
모집단을 특정 기준에 의해서 여러개의 집단으로 나누고 집단 내에서 임의적으로 샘플링하는 것.  
예를 들어 1000명의 종사자를 6개의 집단(동일한 크기로 구분)으로 나누고 각각의 집단별 10명씩 추출하는 것.  
무작위 추출시 특정 집단에 몰려 뽑히는 것을 방지할 수 있음.


#### 층화 표본추출


#### 군집 표본추출





## references
경영통계 / 유태종교수님

















