---
layout: post
title: "DS_1_Data"
excerpt_separator: "<!--more-->"
categories:
  - Data Science
tags:
  - Fundamental
---

## Data?
데이터는 세상에 대한 단순한 사실 입니다. 내가 돈이 많아서 강남에 가게를 하나 사려고 해요. 우리 집 앞에 괜찮아보이는데가 있길래 방문자 기록을 한번 봤어요.
10월 1일엔 1000명, 10월 2일엔 1300명, 하나하나가 데이터 입니다. 정보가 되기 위한 재료 라고 말할 수 있죠.
그 데이터를 특정의 목적을 갖고 일련의 처리과정을 거치면 INFORMATION이 됩니다. 월 평균 방문자는 1800명이고, 방문자 증가율이 250%라는 정보가 생겼어요.
KNOWLEDGE는 뭘까요? 그 동안 내가 투자했던 기록을 보니까 방문자 증가율이 200%가 넘은 가게들은 투자대비 수익률이 높았던 거에요.
그래서 아 이곳에 투자해야겠다는 지식을 도출 해냅니다.



| DATA        | Information                        |  Knowledge |
|-------------|------------------------------------|------------|
|세상에대한 단순한 **Fact**의 나열 | 데이터를 **특정한 맥락**을 갖고 일련의 처리과정을 거친 것 |   그 정보들의 **유의미한 패턴**을 파악해 얻은 노하우, 행동, 예측 |
|방문자 수 \ 10.1 : 1000, 10.31 : 2500   | 월 평균 방문자 : 1800 \ 방문자 증가율 : 250%| 방문자 증가율이 200%보다 높네 투자하자!|


## Data Science
- Gathering and massaging data to tell its **story**
- Turning data into **insight**
- 즉, 다양한 데이터로부터 지식과 인사이트를 추출하기 위해 일어나는 **과정**
- 효율적인 **Decision Making**을 하기 위해 함 

> “Data science will also revolutionize medicine, education, and other areas that are slated to become ‘evidence-based.’”  
> NYU’s Data Science and Statistics Working Group


데이터 사이언스는 방금 설명한 데이터라는 걸로부터 지식과 인사이트를 추출하기 위해 일어나는 과정을 말합니다.
과거에는 ‘직관’에 의해 의사결정 하는 경우가 많았습니다. 한 분야에 오래 있던 사람들은 경험이 축적 됩니다. 컴퓨터가 머신러닝에서 training data set을 학습하듯 사람도 계속해서 학습 하는 거죠. 그만큼 '직관'도 우연은 절대 아닙니다. 하지만 사람이라는 특성상 컨디션이나 망각 등 여러 요인에 의해 risk가 클 수 밖에 없습니다. 그래서 데이터 사이언스는 그 데이터들을 차곡차곡 잘 쌓아서 분석도 하고 '근거'를 갖고 의사결정도 하는거죠.  

예를 들어, A라는 직원은 자기가 30년 일한 결과 이 회사는 성장할 가능성이 크니까 인수해야된다고 주장 합니다. B라는 직원은 그 회사의 안정성,성장성 지표같은 여러 정보를 고려 했을 때 이 회사가 성장할 확률은 38%(오차범위 +-5)니까 투자를 보류하자는 의견을 냈어요. 의사결정자 입장이라면 B라는 직원이 더 타당해보이지 않을까요? 이런 현상이 의학, 교육 뿐 아니라 모든 분야에서 일어나고 있습니다.  
 
다른 예를 들어보죠. 항상 아침 9시 수업이 있습니다. 4년동안 등교한 경험으로는 광화문에서 8시 40분에 타면 지각할 확률이 높았고 8시 30분에 타면 앉아 올 확률이 높았습니다. 그게 제 몸에 체득 됐고 8시 30분까지 광화문에 도착하면 늦지 않겠다는 직관이 생겼습니다. 물론 알아도 항상 8시 40분에 타는건 변함이 없습니다. 분석 단계만큼 실행단계가 중요한 이유입니다. ANYWAY, 내가 등교 했던 4년간의 데이터를 하나하나 다 기록하고 분석해본다? 그게 바로 DATA SCIENCE라고 생각 합니다.  

데이터 사이언스나 빅 데이터가 2012년 정도 부터 언급량이 확 늘어나면서 완전히 새로운 분야라고 처음엔 생각이 들었습니다. 근데 그게 아니라 위에 말한 것들을 과거부터 했던 거고 단지 DATA가 BIGDATA가 된 것 뿐 입니다. BIGDATA가 뭔지는 다음장에서~!

### Data Scientist
![datascientist](/assets/datascientist.jpg)
- computing skills : 데이터는 대부분 디지털 형태로 존재하므로 가공, 분석, 시각화 하는데 컴퓨터의 역할이 절대적입니다. 데이터를 용이하게 다룰수 있게 해주는 도구라고 생각하는게 좋습니다.
- domain knowledge : 내가 식당 매출을 높이기 위해 데이터 과학을 도입하려고 할 경우 식당을 운영해본 경험이 있어야 도움이 됩니다. (데이터 사이언스는 팀 스포츠이며 보통 팀 내에 도메인 전문가 확보가 필수 입니다.)
- statistics & machine learning : 기존 데이터를 다루고 문제를 해결하는 다양한 기법들은 통계학자들의 영역이였습니다. 특히 대용량 데이터를 바탕으로 각종 예측 모델을 만드는 것은 기계학습 및 데이터 마이닝으로 많이 연구 중입니다.  

저는 아직 한낱 경영학과가 베이스인 학부생인데요. 처음엔 기술에만 매몰되곤 했습니다. 물론 기술도 매우매우 중요하지만 데이터 사이언스의 본질인 문제 해결에 초점을 맞춰서 실질적인 결과물들을 내는 공부를 하는 것을 추천드립니다!
여기저기서 주워 듣고 구직 사이트를 돌아본 결과 현재 국내에서는 크게 Data Engineer과 Data Analyst로 나눠서 뽑는 것 같습니다. 엔지니어는 빅데이터를 위한 플랫폼들을 설계, 구축, 관리하고 데이터들을 잘 수집, 관리, 유지 하구요. 애널리스트는 클라이언트의 요구에 맞춰 데이터들을 잘 분석하고 인사이트를 뽑아내어 잘 표현해내야하는 직무에 가까운 것 같습니다. Data Scientist는 알고리즘 성능 자체의 향상같은 조금 더 연구자의 느낌이 강하구요.


## 사례
- Mark Drangsholt's Personal Data
![personaldata](/assets/personaldata.PNG)
마크는 중년에 접어들면서 비만, 콜레스테롤 수치 등 이상 징후를 느끼고 개인의 데이터를 직접 수집하여 분석하기로 합니다. 매일 몸무게, 체지방 측정하여 한번에 한가지 씩 식생활 개선하여 10개월 후 20대의 몸무게로 회복하는데 성공 합니다. 그러던 중 2013년 특정 단어 기억하는데 어려움 느끼게 됩니다. 의사들도 원인 발견 실패하죠. 그는 유전자 검사를 통해 지방 소화력에 취약하며 치매의 위험을 증가시키는 유전자 가지고 있다는 것 파악하게 됩니다. 인지능력 테스트를 통해 자신의 언어능력이 떨어지고 있다는 것 또한 발견하죠. 그는 포화지방이 낮은 음식으로 식단을 바꾸고, 콜레스테롤 수치를 낮추는 스태틴이라는 약물 복용하며 매달 데이터를 측정하고 분석합니다. 그 결과 병을 회복하는 놀라운 경험을 하게 되죠.

- John Snow's Cholera map(19th century)
![personaldata](/assets/johnsnow.png)
1854년 의사인 존 스노우는 지도 위에 콜레라가 발병한 집들과 환자 수를 표시하는 간단한 시각화로 그 문제가 식수원 펌프에 있다는 것을 발견 합니다. 그 당시 나쁜 공기가 원인이라며 원인을 알 수 없었던 콜레라의 미스테리가 풀리는 순간 입니다.   


훌륭한 데이터 사이언스의 사례들은 주어진 현상의 본질을 포착할 수 있는 데이터를 수집하고, 단순한 분석 및 시각화를 통해 데이터에서 유용한 패턴을 찾아냈습니다. 그 패턴을 실제로 옮겨 중요한 사회 문제 혹은 자신의 삶의 문제를 해결하는 바탕으로 삼았는데요. 이들의 업적과 성취에는 어떤 고급 통계나 프로그래밍 기술도 필요하지 않았습니다.(물론 중요함..)

## 그럼 나는 뭘 해야 하는거죠...?
1. 문제정의
2. 스몰 데이터여도 충분
3. 대부분 엑셀로  가능
4. 대부분 기본 통계 기법으로 해결 가능
내 주변의 문제를 해결해보자. => 대다수의 데이터 분석은 테이블놀이  
중요한 것은 문제 정의 입니다. 무턱대고 데이터부터 모으기 시작하면 안됩니다. 문제정의를 잘 해야 어떤 데이터를 얼마나 모아서 무엇을 할지 결정할 수 있습니다.


## 실습
- 내가 오늘 만들어낸 데이터에는 뭐가 있을까? 거기서 어떤 가치를 찾아낼 수 있을까? ( 나의 이동경로, 교통카드, 검색기록, 카카오톡, 쇼핑, 데이트, 진료, 어떤 자리에 앉았는지 )
- [최규민님의 정자역에 내리는 사람 예측하기](https://www.slideshare.net/ssuser2fe594/2107-80754131)
- 자신의 문제를 해결하기 위해 직접 데이터를 모아보고 엑셀로 분석해보는 것이 데이터 사이언스의 시작이라고 생각합니다. 저도 제 데이터로 Toy Project 실행 예정!!



### References
데이터사이언스개론 / 이명호 교수님  
위키피디아  
헬로데이터과학 / 김진영 
