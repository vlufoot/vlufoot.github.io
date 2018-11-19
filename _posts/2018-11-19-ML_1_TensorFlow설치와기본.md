---
layout: post
title: "ML_1_TensorFlow설치와기본"
excerpt_separator: "<!--more-->"
categories:
  - Data Science
tags:
  - Machine Learning
---
### TensorFlow?
TensorFlow is an open source software library for numerical computation using **data flow graphs**.
Python으로 작동함!

### Data Flow Graph가 뭐야..?

- 우선 Graph는 노드와 노드가 엣지로 연결된 자료구조
- Data Flow Graph에서 Nodes는 더하기나 곱하기같은 Mathematical Operations를 담당함
- Data Flow Graph에서 Edges는 multidimensional data arrays(=tensors)

### Installing
```
pip install --upgrade tensorflow
```

- 임포트, 버전확인하기
```python
import tensorflow as tf
tf.__version__
```

### Hello World!

```python
# 노드 만들기
hello = tf.constant("Hello, TensorFlow!")
# 노드를 실행하려면 session을 만들고 session.run을 해야함
sess = tf.Session()
print(sess.run(hello))
```




### References
모두의 딥러닝 / Sung Kim / Youtube
