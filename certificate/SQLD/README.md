- ORDER BY ... DESC
- ORDER BY ... ASC

- ORDER BY ... ASC, ... DESC

  - -> 정렬 여러개 하고 싶을 때는 , 을 쓸 것

- WHERE ... != "..."
- LIMIT N, M
    - N 부터 M개 만큼
```
SELECT NAME
FROM 
    (SELECT NAME
        FROM ANIMAL_INS
        ORDER BY DATETIME)
WHERE ROWNUM=1;
---
SELECT A.NAME 
FROM (
    SELECT *
    FROM ANIMAL_INS
    ORDER BY DATETIME ASC
) A
WHERE ROWNUM <= 1;
---
SELECT  MAX(DATETIME) AS "시간" FROM ANIMAL_INS;
---
SELECT COUNT(*) FROM ANIMAL_INS;
---
SELECT COUNT(DISTINCT NAME) FROM ANIMAL_INS WHERE NAME != "NULL";
```
- 조건 처리 후에 컬럼 그룹화 후에 조건 처리
- SELECT 컬럼 FROM 테이블 WHERE 조건식 GROUP BY 그룹화할 컬럼 HAVING 조건식;
- ORDER BY가 존재하는 경우
- SELECT 컬럼 FROM 테이블 [WHERE 조건식]
GROUP BY 그룹화할 컬럼 [HAVING 조건식] ORDER BY 컬럼1 [, 컬럼2, 컬럼3 ...];
- SELECT IF(조건, 참일때, 거짓일때) AS 이름 FROM ~
- SELECT IFNULL(컬럼명, "대체할 값") AS 이름 FROM ~
