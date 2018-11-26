---
layout : post
title : "biz_statistics_Probability"
categories :
  - Data Science
tags :
  - Basic Statistics
---

## Terminology
- Probability distribution: 확률분포
- Mutually exclusive event: 상호배반(배반사건)
- Independent event: 독립사건
- Empirical probability: 경험적확률
- Conditional probability: 조건부확률
- Joint probability: 동시확률
- Contingency table: 분할표
- Bayes’ theorem: 베이즈정리
- Prior probability: 사전확률
- Posterior probability: 사후확률
- Likelihood: 우도
- permutation : 순열
- combination : 조합


## Probability
* A value between zero and one, inclusive, describing the relative possibility(chance or likelihood) an event will occur
* 실험(Experiment) : 주사위 던지기, 국내 100대 기업이 60년 후에 살아있는 확률
* 결과(Outcome) : 1~6 , 0~100
* 사건(Event) : 3이 나오는 것, 10개가 살아있음

### 조건

1. Events are *mutually exclusive(상호 배반)* if the occurrence of any one event means that
none of the others can occur at the same time
2. Events are *collectively exhaustive(총체적 망라)* if at least one of the events must occur
when an experiment is conducted. ( outcome이 반드시 다 고려되야 함 - 전체집합 )
3. Events are *independent(독립)* if the occurrence of one event does not affect the occurrence of another.

### 종류
1. 고전확률  
가정을 바탕으로 구하는 확률 (동전이 설 확률은 없다고 가정)

2. 실증적확률(empirical)  
실제로 실행해보는 확률  
Law of large numbers(대수의 법칙) : 경험적 확률은 실험 횟수가 많아질 수록 고전 확률 값에 가까워 짐

3. 주관적확률(subjective)  
실험자의 주관에 의한 확률  
내일 엄마가 아침밥을 해줄확률  





### 덧셈법칙

1. 상호 배반일 때 : 
```
P(A or C)=P(A)+P(C)
```

2. 일반적인 경우 :
```
P(A or C)=P(A)+P(C)-P(A교C)
```

### 동시확률(교집합), Joint probability
* 곱셈법칙 : Two events A and B are *independent* 일때만
```
P(A and B)=P(A)P(B)
```

### 조건부 확률 ,Conditional probability
* 특정 사건 B가 일어난 상태에서 A가 일어날 확률
* 두 사건이 종속 사건일 때, 동시 사건을 계산하는 일반적인 곱셈 법칙
```
P(A|B)
P(AandB)=P(A)P(B|A)
P(B|A)=P(A n B) / P(A)
```



## 분할표

* 각 개체를 어떤 특성에 따라 분류할 때에 얻어지는 자료 정리표.
* 두가지 변수로 구성할 때 가장 인지하기 좋다.
* 조건부 확률 같은거 계산하기 매우 편함

EX)



## 순열과 조합

* permutation 순열 : 서로 다른 n개에서 r개를 선택해서 일렬로 세우는 수
```
nPr=n!/(n-r)!
```
ex)


* combination 조합 : 순서를 생각하지 않고, n개 중에 r개를 단순히 선택하는 경우의 수
순열에 순서만큼 나눠주면 됨
```
nCr=n!/r!(n-r)!
```
ex)



## 베이즈 정리

P(B|A)=P(B)*P(A|B)/P(A)

어떠한 사건이 일어났을 때 확률값 =아무일도 안일어났을때 가정했을 때 확률값 * 뭔지 모르는 가능성

실제 세상을 적용한 앞면이 나올 확률
동전이 앞면이 나올확률 = 1/2 (가정 : 동전은 휘지 않음)
뭔지모르는 가능성 = 999/1000 (휜놈이 1000개중에 1개가 있다)
Posterior probability = 1/2 * 999/1000

ex) 그림
ex) 병에 걸릴 확률



* 이세상에는 서로 영향을 주는 인자가 너무 많기 때문에 정확한 확률을 계산하는 건 불가능
* 데이터가 많아질 수록 점점 정확한 확률 계산

