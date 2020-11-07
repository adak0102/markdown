set집합 관련 연산자

 :  SELECT문 2개 이상일때만 가능 

나오는만큼 포함. (UNIONALL)

중복 한번만 포함 .





- maria DB 연결 정보
- 점속 도메인명 : multi-bigdata.cljkqcsbb9ok.ap-northeast-2.rds.amazonaws.com
- 접속 도메인명, 내 계정 둘다 기억  

sql

릴레이셔널 데이터베이스 시스템에 테이블을 구해서 전처리를 시행 



##### 하이디 sql

- -- : 주석 

- 데이터베이스(table을)를 먼저 만들어놓고 시작해야함

- 작성은 내 edu05만 됨, 리딩은 다 

- table이 자동으로 만들어지지 않음/ 툴에따라 자동으로 만들어지는 것도 있음

- SQL 사용법 워드 참고

  - 새로운 데이터베이스 만들시

  > 캐릭터셋 지정
  >
  > 조합:utf8_general_ci 사용해야 한글이랑 특수문자 먹힘

  미리 db테이블 만들어놓고 저장

  db테이블 만들때 db에 저장할 csv파일의 컬럼개수,데이터타입 맞춰서 만들어야함

  컬럼 10개-10개, 타입(정수,실수)

  variablecharacter  크기도 적당히 맞춰주는게 좋음

  컬럼 값 NA인 애들: NULL허용 체크박스 체크해야함

- 도구-csv 파일 가져오기

  ​	필드 종결자 ; -> , 로 바꿔야함



- 책 쭉 읽음



R

>  maria_aws

> day10 

분석할 데이터셋을 mariadb에서 읽어옴

MySQL 라이브러리

rjava, rjdbc 가 널리알려진 방법 



jupyter

> maria_aws.ipynb