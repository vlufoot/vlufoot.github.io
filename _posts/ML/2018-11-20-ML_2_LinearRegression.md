---
layout: post
title: "ML_2_LinearRegression"
excerpt_separator: "<!--more-->"
categories:
  - Data Science
tags:
  - Machine Learning
---

## Regression

- 연속형 변수들에 대해서 두 변수의 관계에 대한 모형  
- 공부한 시간과 점수가 선형에 있다고 가정하면 Linear regression

| X(hours)        | Y(score)| 
| --------         | ------ |
| 10               | 90     |
| 9                | 80     | 
| 3                | 50     | 
| 2                | 30     |  

## (Linear) Hypothesis

세상의 많은 경우가 Linear하게 모델을 세울 수 있어요. 집이 클수록 비싸다던지 훈련을 많이 할수록 달리기 속도가 빨라진다던지요. 
매우 간단하지만 powerful한 모델 입니다. 즉 Linear하게 Hypothesis를 한다는 것은 데이터에 잘 맞는 선을 찾는 것.

```
# 선형 회귀의 가설(1차 방정식)
H(x)=Wx+b
```  

![linear_1](/assets/linear_1.PNG)  

이 중 어떤 선이 우리의 데이터에 가장 맞는 가설 일까요? 실제 데이터와 우리 가설의 거리를 비교해서 가까우면 좋다고 계산을 합니다.
그 거리를 계산하는 것은 **Cost function**이라고 합니다. 차이가 음수일수로 있으므로 제곱을 합니다. 이는 차이가 클때 더 큰 페널티를 주는 것을 의미 합니다.
(절댓값은 컴퓨팅에서 부담이 큼)  

![costfunction_1](/assets/costfunction_1.PNG)  

1부터 m까지 (가설의 각각의 예측값- 실제 값)의 제곱을 하여 더한 뒤 m으로 나눠 평균  
리니어 리그레션의 학습이라는 것은 cost function을 최대한 작게 만들기 위한 W와 b를 구하는 것 입니다.


## references
모두를 위한 딥러닝 / Sung Kim / Youtube







