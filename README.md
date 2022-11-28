<details>
<summary>20221126</summary>
<div markdown="1">

SQL 
<dr>   
* WITH RECURSIVE
<dr>
```
:memo:
<dr>
WITH RECURSIVE 테이블명 AS(
               SELECT 초기값 AS 컬럼별명1 ← 초기값 설정하는 쿼리
               <dr>
               UNION ALL
               <dr>  
               SELECT 컬럼별명1 계산식 FROM 테이블명 WHERE 제어문 ← 루프돌때 값 설정
) 
```
<dr>

- 반복문이라고 생각하면 이해하기 쉬움

</div>
</details>


<details>
<summary>20221127</summary>
<div markdown="1">
 * 프로젝트 정리하기
 * SQL 코테 풀기
</dr>
</div>
</details>


details>
<summary>20221128</summary>
<div markdown="1">
TensorFlow 기본 개념
<br>
1. What is Data Flow Graph?
<br>
Node : mathematical operations
Edge: data array
</br>
2. TensorFlow 실습
 
 1) installing TensorFlow
 ```python
 !pip install --upgrade tensorflow
 !pip install --upgrade tensorflow-gpu
 ```
  2) 그래프 만들기
  ```python
  # TF v1
  import TensorFlow as tf
  hello = tf.constant("Helllo, TensorFlow!")
  sess = tf.Session()
  print(sees.run(hello))
  ```
  :check: v1의 프로세스
  <br>
    1. 새로운 빈 계산 그래프를 만든다
    2. 이 계산을 그래프에 노드(텐서나 연산)를 추가한다
    <br>
    3. 그래프를 평가(실행)한다
    <br>
    - 새로운 세션을 시작<br>
    - 그래프 내 변수를 초기화<br>
    - 이 세션에서 계산 그래프 실행

  ```python
  # TF v2
  import TensorFlow as tf
  hello = tf.constant("Helllo, TensorFlow!")
  tf.print(hello)
  ```
  3) 입력 데이터를 모델에 주입
  TensorFlow v1 : `Placehloder 사용`
  ```python
  # 노드 만들기
a = tf.placeholder(tf.float32) 
b = tf.placeholder(tf.float32)
adder_node = a+b

print(sess.run(adder_node, feed_dict={a:3 ,b: 4.5})) # 7.5
print(sess.run(adder_node , feed_dict={a:[1,3] ,b:[2,4]})) # [3. 7.]
```
TensorFlow v2 : `사용자 함수`

```python
def adder(a,b):
    c=tf.add(a,b)
    return c

a=tf.constant(1)
b=tf.constant(2)
print(adder(a,b)) # tf.Tensor(3, shape=(), dtype=int32)

c=tf.constant([1,2])
d=tf.constant([3,4])
print(adder(c,d)) # tf.Tensor([4 6], shape=(2,), dtype=int32) 
```
3. Everything is Tensor
 <br>
    1. Rank : 차원
    2. Shape : 자료형
    3. Type : 형태
</div>
</details>
