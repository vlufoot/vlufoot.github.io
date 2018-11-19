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
![tensorflow_1](/assets/tensorflow_1.PNG)
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


### Placeholder
상수로 넣지 말고 그래프만 미리 만들어 놓고 실행단계에서 값을 던져주기 위해 씀
```python
a = tf.placeholder(tf.float32)
b = tf.placeholder(tf.float32)
adder_node = a + b

# 값도 같이 넘겨주자
print(sess.run(adder_node, feed_dict = {a:3, b:4.5}))
# array로 여러개 넘겨줄 수 있음
print(sess.run(adder_node, feed_dict = {a:{1,3}, b:{4.5}}))
```
위에서 본 세 단계랑 똑같이 placeholder라는 노드를 만들고 sess.run에 데이터를 넘겨주면 return 받는것

### Tensor?
- Rank(차원) : Scalar(0), Vector(1), Matrix(2), 3-Tensor, .... n-Tensor
```python
s = 483   # RANK 0 (magnitude)
v = [1.1, 2.2, 3.3]  # RANK 1 (magnitude and direction)
m = [[1, 2, 3], [4,5,6]] # RANK 2 (table of numbers)
....
```
- Shape : 각각의 element에 몇 개가 들어 있니?
```
t = tf.constant([[[1, 1, 1], [2, 2, 2]], [[3, 3, 3], [4, 4, 4]]])
tf.shape(t)  # [2, 2, 3]
```

- Type : 대부분 float32 사용 / tf.float32



### References
모두의 딥러닝 / Sung Kim / Youtube
