# 0801
sql
## ddl,dml,dcl
<pre>
    <code>
  select 필드 from 테이블 명;
  insert into 테이블 명 values(필드값1, ~~2);
  update 테이블명 set 컬럼 where 조건;
  delete from 테이블 명 where 조건;
  create table 테이블 명 (컬럼이름 ,길이, (not null));
  drop table 테이블명;
   alter table 테이블명 add 컬럼, drop 컬럼
  grant
  revoke
    </code>
  </pre>
  ## sql
<pre>
    <code>
  like '%값', '%값%', '%%값' 등등
  decode(컬럼이름,'컬럼값','바꿀값');
  group by 컬럼이름
  order by 컬럼(컬럼 값 desc or asc) desc = 내림차순 asc = 오름차순
  sum(*)
  max(*)
  min(*)
  avg(*)
  count(*)
  to_char(컬럼 이름, '바꿀값')
  in, not in (컬럼값) 
  between 15 and 20
  
    </code>
  </pre>
