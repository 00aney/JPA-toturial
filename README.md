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
