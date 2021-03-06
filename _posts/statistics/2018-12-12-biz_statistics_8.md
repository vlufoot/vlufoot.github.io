---
layout : post
title : biz_statistics_One-sample tests of Hypothesis
categories : Data Science
tags : Basic statistics
---

## Terminology

- One-sample test
- Two-sample test : 두 모집단 간 비교
- Hypothesis : 가설
- Hypothesis test : 가설검정
- Null hypothesis : 귀무가설
- Alternative hypothesis : 대립가설 
- Critical value : 임계치 (두 가설을 나누는 곳)
- Significance level : 유의수준
- One-tailed test : 단측검정
- Two-tailed test : 양측검정

## Objective

- 가설검정의 이해
- 5단계 가설검정 프로세스
- Type1 오류와 Type2 오류
- 단측검정과 양측검정의 구별
- **p-value**의 이해
- 모집단의 평균에 대한 가설검정 수행
- 모비율에 대한 가설 검정을 수행

## 가설과 가설검정

저번시간에 추정에 대해서 배웠습니다. 이번에 가설검정에 대해 배울텐데요. 가설검정은 가설을 세우고 그 가설이 
유의수준 얼마에서 맞다 혹은 틀리다 라는 과정을 말합니다.

- 가설 : 검정의 대상이 되는 모집단의 모수에 대한 서술
- 가설검정 : 표본 추출과 확률적 이론을 바탕으로 가설의 타당성을 확인하는 과정


#### 가설검정 프로세스
1. 가설 수립
- 귀무가설(H0) : 일반적으로 기각될 것으로 예상된 가설
- 대립가설(H1) : 귀무가설이 기각될 때 받아들여지는 가설(내가 확인하고자 하는 영역)  

H0과 H1은 mutually exclusive / collectively exhaustive 관계.  
H0은 항상 참의 형태로 가설이 수립(같다 / 같거나 크다 등).
H1이 실제로 증명하고 하는 내용  
만약, H0이 기각되지 않더라도 이것은 귀무가설이 옳다는 뜻이라기 보단 기각되기에 충분한 증거가 없다로 해석해야 함.
  
그러나 H0이 기각되었다는 것은 H1이 옳다는 뜻으로 해석 할 수 있다.

2. 유의수준 선정
- Type 1 Error : 실제로 참인 귀무가설을 기각할 확률(검정의 유의수준)
- Type 2 Error : 실제로 거짓인데 기각되지 않을 확률

3. test statistics(검정 통계량) 선정
가설검정을 위하여 확률분포를 결정. 검정의 목적에 따라 z,t,f,x^2등 선정.

4. decision rule 선정 

5. 이제 샘플링 하고 어느 영역에 떨어지는지 확인 (rejected?)



## 모평균의 값에 대한 가설검정 

- H0 : 모평균 (= or >= or =<) Value
- H1 : 모평균 (!= or < or > ) Value  

평균이므로 z나 t분포의 검정 통계량을 사용.
다르다는 것이 h1이면 단측검정.  
가운데 95%를 h0한테 줌. 샘플링한 아이의 평균이 나머지 5%에 나오면 h0을 기각하고 h1 채택 가능.  

#### 예제

공장에서 하루 평균 200대 표준편차 16대의 의자를 만들도록 디자인을 했다.
근데 이번에 새로운 생산 방법을 도입 했습니다. 
그랬더니 주당 생산량 203.5 입니다 
유의수준은 0.01로 더 좋아진 것인지 가설검정을 해봅시다.

1. 가설 수립  
H0 : u = 200
H1 : u != 200

2. 유의수준 선정  
a = 0.01

3. test statistic 선정  
모집단의 표준편차를 알기때문에 Z분포

4. Decision rule  
양측검정( 0.005의 zvalue는 2.576 ). 
즉 -2.576~2.576사이에 나오면 H0의 구간 인 거임.

5. 확인
Z = (203.5 - 200) / (16 / sqrt(52) ) = 1.547 이 나옴.
그래서 H0을 기각할 수 없음. 즉 새로운 생산방법이 별 차이가 없네유..


#### 예제 2
cs부서에서 클레임 처리에 평균 60$의 비용이 든다. 원가절감 방법을 새로 도입해서 효과가 있는지 궁금했다.
저번달에 26개의 클레임 처리 비용을 알아왔다. 0.01의 수준으로 비용이 60$보다 낮아졌는지 확인해봐라.
샘플링한 데이터의 평균은 56.42 이며 표준편차는 10.04이다.

1. 가설 수립  
H0 : u >= 60
H1 : u < 60

2. 유의수준 선정  
a = 0.01

3. test statistic 선정  
모집단의 표준편차 모르니까 t분포.
n은 26이므로 자유도는 25.

4. Decision rule(critical value)  
t분포내에 자유도 25일때 0.01에 해당하는 구간은 -2.485.

5. 확인  
t = (56.42 - 60) / (10.04 / sqrt(26)) = -1.1818  
-2.485보다 작아야 기각할 수있는데 H0의 구간에 있으므로 비용이 줄었다고 말할 만한 충분한 증거가 없다.



## p-value

p-value는 귀무가설이 기각되지않을 기각치의 확률값을 나타내는 값.
내가 샘플링을해서 나온 검정통계량 값의 작은쪽이 p-value.
그러니까 그냥 p-value랑 유의수준을 비교하는 것만으로 귀무가설 기각이 가능함.
예를들어 pvalue가 0.03이 나오면 0.01의 유의수준에서는 기각할 수 없고 0.05의 유의수준에서는 기각이 가능한 것.
그럼 p-value를 알면 분포 그려볼 필요가 없는건가..? 유의수준 딱히 안정해도 pvalue만 보고 대략 판단 가능할듯.


## 비율에 대한 가설검정
비율을 계산한다는 것은 n이 일정이상이라는 것을 의미하는 것이기 때문에 표준정규분포 사용.

#### 예제
선거에서 80%이상의 지지를 받아야 승리할 수 있습니다. 2000명을 대상으로 조사했더니 1550명이 저를 지지한다고 합니다.
0.05의 유의수준으로 뽑힐 확률이 있을까요??

1. 가설 설정  

h0 : 뮤 >= 0.8
h1 : 뮤 < 0.8

2. 유의수준 설정
0.05

3. test statistic 선정

n= 2000, 뮤= 0.2 이므로 2000x0.2 / 2000x0.8 모두 5보다 크다.
그러면 표준정규분포 사용 가능

4. decision rule

0.05 수준에서 z값은 -1.64.
비율의 z를 계산해보니 -2.8이 나옴. h0을 기각하고 h1 선정.
즉 난 떨어질것이다..ㅠ.
p-value는 -0.00255인데 거의 100% 떨어진다는 소리임.
그냥 단순히 계산해서 1550/2000=77.5% 이기때문에 별로 차이 안나는 것처럼 보여도 실제로 통계적 계산을하면 
거의 100% 떨어진다고 주장할 수 있다는 것. 특히 n값이 매우 크기때문에 정확한 결과가 나온 것.



## 포장 기계는 제대로 작동하고 있을까?(분산에 관심을 가져야 하는 이유)

10kg의 쌀포대에 대해서 고객 불만을 줄이기 위한 프로젝트 진행.
표본을 추출해서 모평균이 10kg인 가설검정을 실시함.
0.05의 유의수준에서 귀무가설은 기각되지 않았다.
그러면 문제가 없을까? 고객불만이 왜 쌓이고 있는것일까?  

평균은 10kg 인건 맞는데!! 9kg~11kg가 들어간 녀석도 존재함. 그래서 9kg받은 애들의 고객 불만이 쌓이는 상황.
그래서 기업에서는 9.5kg이하는 고객 불만이 들어오고 10.5kg 이상은 비용이 많이 드므로 허용치를 정함(tolerance).
분포가 뾰족~~ 해질수록 limit안에 최대한 많은 애들이 들어옴(생산관리에서 6시그마가 여기서 나옴/ 평균 +- 6시그마만큼이 우리 관리내에 들어옴)



## 분산에 대한 가설검정

- 공정관리에 있어서 최초의 허용치가 S0^2가 유지 되고 있는지 현재의 S^2에 대한 관리는 매우 중요. 
H0 : S^2 = S0^2  
H1 : S^2 > S0^2  
이럴때 카이스퀘어 분포를 사용

- 비슷하게 A기계와 B기계의 분산을 비교할 수 있음. 둘의 분산이 유의하게 다른가?  
H0 : SA^2 = SB^2  
H1 : SA2 != SB^2  
이럴때 F분포를 사용  


## Chi-square distribution
쌀포대의 기준 V=0.0016 인데, 12개 표본추출해봤더니 V= 0.0025 였다.
분산은 유의한 수준으로 증가하였는가? n=12이니까 d.f=11.

```
X^2 = (11*0.0025)/0.0016 = 17.2  
자유도가 11인 카이자승 함수의 P-VALUE는 0.102  
쫌 크네?? 특히 생산공정인데 0.1이면 기각 못함. 분산값이 달라진게 없는거임.
```













## REFERENCES 
경영통계 / 유태종 교수님








