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
Python 사용!

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

### Computational Graph

- TensorFlow Mechanics
[tensorflow_1](/assets/tensorflow_1.PNG)
1. 그래프를 우선 만들어야함
2. sess.run으로 그래프를 실행시킴
3. 어떤값이 return 됨

1. Build Graph (tensors) using TensorFlow operations
```python
# 더하기 그래프 만들자
node1 = tf.constant(3.0, tf.float32)
node2 = tf.constant(4.0 ) # tf.float32로 암시적 인식
node3 = tf.add(node1, node2)
```
```python
# 그냥 실행하면 텐서에 대한 설명만 나옴..
print("node1:", node1, "node2:",node2)
print("node3:", node3)
```
2. Feed data and run graph(operation)  
**sess.run(op)**  
3. Update variables in the graph(and return values)
```python
# 아까 말했듯이 세션 만들어서 run해야함 그럼 결과가 나옵니다
sess=tf.Session()
print("sess.run(node1,node2):", sess.run([node1,node2]))
print("sess.run(node3):", sess.run(node3))
```


### References
모두의 딥러닝 / Sung Kim / Youtube
