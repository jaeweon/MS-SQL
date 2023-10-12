# MS-SQL

### 특징
### 사용자 편의성이 뛰어나다.
### DBMS 툴인 "Microsoft SQL Server Management Studio"의 사용이 매우 편리하다.
### 멀티 레코드셋을 지원한다.

# MS-SQL 저장 방식
![image](https://github.com/jaeweon/MS-SQL/assets/34277606/90190dc9-f042-4466-815d-4f8e61300378)

### 데이터베이스안에는 PAGE라고 하는 하나의 단위가 존재한다.
### 이 PAGE는 총 3가지 구성요소가 있다.
### HEADER : 시스템 정보(Page의 번호, 유형, 가용 크기)가 저장되어 있다.
### BODY : 실제 테이블안에 들어있는 데이터가 저장되는 공간이다.
### Row Offset Table : Body안에 저장되어 있는 데이터의 주소값을 저장하고 있다.


![image](https://github.com/jaeweon/MS-SQL/assets/34277606/644d2735-1519-44fb-b583-b63711fe9d70)

## Extent
### 64kb로 구성되어 있으며, Page의 집합체이다.
### 하나의 Extent안에 8개의 Page가 존재한다.
