
# Oracle SQL


## insert 
      insert into 테이블 values(필드값,필드값)
## select 
      select 필드 
      from 테이블 
      join 테이블 on 조건
      where 조건 
      group by 필드 having 조건 
      order by 필드 [desc:내림차순,asc:오름차순]
## 서브쿼리 
      select 필드 from (서브쿼리)  : 서브쿼리 값이 여러개여도 가능함
      select (서브쿼리) from 테이블  : 서브쿼리 값이 1개 여야함 
      select 필드 from 테이블 where 필드 = (서브쿼리)  : 값이 1개 
      select 필드 from 테이블 where 필드 in (서브쿼리)  : 값이 여러개여도 상관없음
### 조인
      left join , right join , inner join
      left outer join, right outer join, inner outer join
### 필드 
      decode(필드명,값1,출력값,기본값)
      count(필드) { *을 넣어도됨 } 
      to_char(필드,'변하는 스타일') ex : to_char(1000,'9,999') => 1,000
      round(필드,몇번째 자리)  ex : round(1,21,1) => 1.3
      floor(필드,몇번째 자리)  round 랑 같음
      sum(필드)  
      avg(필드) 
### 시퀀스
      create sequence 시퀀스이름
      increment by 1 (증가값)
      start with 1 (초기값)
      (nextval 증가,currval 값보기 { nextval랑 같이  } )
## update 
      update 테이블 set 필드 = 변경값 
      where 조건 
## delete 
      delete from 테이블 
      where 조건
