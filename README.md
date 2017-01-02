# JPA-toturial
책 자바 ORM 표준 JPA 프로그래밍 따라하기

#### H2 데이터베이스 사용 
- embedded mode(JVM 메모리 안에서 실행)
- server mode : 압축푼 곳 bin/h2.sh
- http://localhost:8082


- JPA Annotation Package : javax.persistence


###persistence.xml 에서 설정 정보 관리
* persistence-unit 에서 데이터베이스 당 하나의 영속성 유닛을 등록

* javax.persistence.jdbc.driver JDBC 드라이버
* javax.persistence.jdbc.user 접속 아이디
* javax.persistence.jdbc.password 접속 비밀번호
* javax.persistence.jdbc.url 접속 URL

* hibernate.dialect : DB 방언 설정
* hibernate.show_sql : 하이버네이트가 실행한 쿼리 출력
* hibernate.format_sql : 하이버네이트가 실행한 쿼리를 보기좋게 정렬
* hibernate.use_sql_comment : 쿼리 출력할 때, 주석도 함께 출력
* hibernate.id.new_generator_mappings : JPA 표준에 맞춘 새로운 키 생성 전략 사용

###JPQL
- 엔티티 객체를 대상으로 쿼리한다.
- 데이터베이스 테이블을 전혀 알지 못한다.
- SQL과 달리 대소문자 구분

```
select m from Member m
```
from Member 에서 Member 는 회원 엔티티 객체를 말하는 것


##데이터베이스 스키마 자동생성
###hibernate.hbm2ddl.auto 속성
* create : 기존 테이믈 삭제, 새로 생성(drop + create)
* create-drop : create 속성에 추가로 종료할 때, 생선한 DDL을 제거(+drop)
* update : 데이터베이스 테이블과 엔티티 매핑정보를 비교해서 변경 사항만 수정
* validate : 테이블과 엔티티 매핑정보를 비교해서 차이가 있으면 경고를 남기고, 애플리케이션을 실행하지않는다.
이 설정은 DDL을 수정하지 않는다.

* none : 자동 생성 기능을 사용하지 않으려면, auto 속성 자체를 삭제하거나, 유효하지 않은 갑을 준다.(none 도 유효하지 않은 값)
