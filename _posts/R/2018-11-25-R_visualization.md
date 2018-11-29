---
layout: post
title: "Visualization"
excerpt_separator: "<!--more-->"
categories:
  - Data Science
tags:
  - R
---

## 산점도
```r
ggplot(data=apart, aes(x=area_m2, y=price)) + geom_point()
# + xlim(0,100) + ylim(0,10000) 으로 x,y축 조정 가능
```

## 막대그래프 (집단간 차이)
```r
apart_t <- apart %>% group_by(gu) %>% 
  summarise(mean_price = mean(price)) %>% 
  head(10)

ggplot(data=apart_t, aes(x=gu, y=mean_price)) + geom_col()

ggplot(data=apart_t, aes(x=reorder(gu,-mean_price), y=mean_price)) + geom_col()  # 큰순으로 정렬

```

## 빈도 막대 그래프
```r
ggplot(data=apart, aes(x=gu)) + geom_bar()
```

## 시계열 그래프
```r
ggplot(data = economics, aes(x=date, y= unemploy)) + geom_line()
```


## REFERENCE
- Do it 쉽게 배우는 




