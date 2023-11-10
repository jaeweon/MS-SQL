# MS-SQL
 
### 특징
### 사용자 편의성이 뛰어나다.
### DBMS 툴인 "Microsoft SQL Server Management Studio"의 사용이 매우 편리하다.
### 멀티 레코드셋을 지원한다.
<br>
<br> 
 
# MS-SQL 저장 방식
![image](https://github.com/jaeweon/MS-SQL/assets/34277606/90190dc9-f042-4466-815d-4f8e61300378)

### 데이터베이스안에는 PAGE라고 하는 하나의 단위가 존재한다.
### 이 PAGE는 총 3가지 구성요소가 있다.
### HEADER : 시스템 정보(Page의 번호, 유형, 가용 크기)가 저장되어 있다.
### BODY : 실제 테이블안에 들어있는 데이터가 저장되는 공간이다.
### Row Offset Table : Body안에 저장되어 있는 데이터의 주소값을 저장하고 있다.
<br>
<br>

## Extent
### 64kb로 구성되어 있으며, Page의 집합체이다.
### 하나의 Extent안에 8개의 Page가 존재한다.
![image](https://github.com/jaeweon/MS-SQL/assets/34277606/644d2735-1519-44fb-b583-b63711fe9d70)
<br>
<br>



## 데이터저장 구조
![image](https://github.com/jaeweon/MS-SQL/assets/34277606/6d33e692-6e0b-4b10-89e1-f64914a473a3)
### 데이터베이스를 열어보면 MDF와 LDF라는 파일이 존재한다.
#### MDF파일은 데이터의 핵심 정보가 포함되어 있고, LDF에는 로그(트렌젝션 로그 등)이 저장되어 있다.
#### MDF파일안에 Extent라는 Page의 집합체가 있고, 이 페이지 안에 Body영역에 우리가 다루는 데이터가 저장되어 있는 구조이다.
<br>
<br>

# Table 크기(용량) 구하기
![image](https://github.com/jaeweon/MS-SQL/assets/34277606/9575cf0f-9971-40d5-9b96-66e2ddbd1b9e)

## 첫 번째 결과 값
#### 학생 테이블에 39개의 데이터가 저장되어 있으며 총 2개의 Page가 할당 되었다.
#### 한개의 Page는 8kb의 용량을 차지하므로, 이 Table의 크기는 16kb이다.
<br>
<br>

## 두 번째 결과 값
#### 학생 테이블에 201개의 데이터가 저장되어 있으며 총 4개의 Page가 할당 되었다.
#### 한개의 Page는 8kb의 용량을 차지하므로, 이 Table의 크기는 32kb이다.

