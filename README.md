<details>
<summary>20221126</summary>
<div markdown="1">

SQL 
<dr>   
* WITH RECURSIVE
<dr>
~~~
:memo:
<dr>
WITH RECURSIVE 테이블명 AS(
               SELECT 초기값 AS 컬럼별명1 ← 초기값 설정하는 쿼리
               UNION ALL
               SELECT 컬럼별명1 계산식 FROM 테이블명 WHERE 제어문 ← 루프돌때 값 설정
) 
~~~
<dr>

- 반복문이라고 생각하면 이해하기 쉬움

</div>
</details>






