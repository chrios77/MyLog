# [DB] SQL(Structured Query Language)

![](https://velog.velcdn.com/images/chrios99/post/ce25c830-5e43-4ff7-969e-cf1096c0372a/image.png)

> 사진 출처 : https://namu.wiki/w/MySQL

### SQL이란?
SQL은 Structured Query Language의 약자로 '에스큐엘' 혹은 시퀄'이라고 부른다. 또한, RDBMS에서 사용하는 언어이다. 그러므로 RDBMS인 MySQL를 배우려면 SQL 학습은 필수이다.

SQL의 뜻는 '구조화된 질의 언어'이다.  'Structured'는 데이터가 테이블(표) 형태로 되어있다는 뜻이고, 'Query'는 사용자가 DBMS와 CRUD 등의 다양한 요청을 통해 의사소통을 할 수 있다는 뜻이며, 'Language'는 DBMS도 이해할 수 있고 사용자도 이해할 수 있는 언어가 사용된다는 뜻이다. 이를 정리해보면 SQL은 데이터베이스와 사용자 사이에 의사소통을 위한 요청을 작성할 때 사용하는 언어이다. 따라서 SQL를 사용하면 DBMS를 통해 데이터베이스라는 중요한 정보들을 입력, 관리하고 추출할 수 있다.

### SQL의 장점
그렇다면 SQL의 장점은 무엇일까?

'사람의 언어인 자연어와 비슷해 배우기 쉽다', '효율적이다'

전자의 이유는 SQL은 일반적인 영어 키워드를 사용하기 때문에 배우기가 매우 쉽다.

후자의 이유는 많다. 대표적으로 복잡한 데이터 처리 작업을 코드 몇 줄만으로 표현할 수 있기 때문이다.

### SQL의 종류
SQL의 종류로는 데이터 정의 언어, 데이터 조작 언어, 데이터 제어 언어가 있다. 각각 영어로 Data Definition Language(줄여서 DDL), Data Manipulation Language(줄여서 DML), Data Control Language(줄여서 DCL)이라고 부른다.

### 데이터 정의 언어(DDL)
DDL은 데이터베이스의 구조를 정의하는 명령어이다. 주요 명령어로는 CREATE, ALTER, DROP, TRUNCATE가 있다.

### 데이터 조작 언어(DML)
DML은 데이터를 추가/조회/변경/삭제하는 작업을 수행한다. 주요 명령어로는 INSERT, SELECT, UPDATE, DELETE이다.

### 데이터 제어 언어(DCL)
DCL은 권한제어, 트랜잭션 제어 작업을 수행한다. 주요 명령어로는 GRANT, REVOKE, COMMIT, ROLLBACK, SAVEPOINT가 있다.

### 데이터베이스에서 SQL를 받아들이는 방식
데이터베이스는 SQL를 띄워쓰기로 구별한다. 즉, 데이터베이스가 SQL을 판단하는 방법은 단어와 단어 사이의 띄어쓰기이다. 문장 맨앞에 위치한 단어의 첫번째 글자부터 차례대로 하나씩 읽으면서 사용자의 요청을 분석한다. 또한, 글자를 하나씩 읽다가 띄어쓰기가 나타나면 이전에 나온 글자들을 조합하여 입력된 언어를 파악한다.

> 참고 문헌:
1. 혼자 공부하는 SQL - https://m.hanbit.co.kr/store/books/book_view.html?p_code=B6846155853
2. https://www.oracle.com/kr/database/what-is-database/
3. https://365kim.tistory.com/102
4. https://velog.io/@ryuneng2/Database-%EA%B8%B0%EC%B4%88%EC%9A%A9%EC%96%B4-DBMS-SQL-RDBMS
5. https://www.icia.co.kr/community/board/view/2/1/89