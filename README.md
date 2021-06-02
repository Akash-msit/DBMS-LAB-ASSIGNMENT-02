# DBMS-LAB-ASSIGNMENT-02
constraints
Create a table DRIVER_DETAILS with all the constraints as discussed in class. Insert a row that generates error for violating constraint and insert a second record that gets successfully inserted. Show both the outputs.

Input--
create table driver_detail(dname varchar2(45),daddr varchar2(45),dphno number(11),dlno varchar2(15),dgrade char(1),ddistance number(5),ddob date,ddoj date,constraint pk_dp_dn primary key(dname,dphno),constraint ck_dg check(dgrade in('A','B','C','D')));

Then Insert check constraint (dgrade) A --

Input-- 

insert into driver_detail(DNAME,DADDR,DPHNO,DLNO,DGRADE,DDISTANCE) values('Akash','Kgp','8537086332','MH0/12','B','200');

insert into driver_detail(DNAME,DADDR,DPHNO,DLNO,DGRADE,DDISTANCE) values('Souvik','Bankura','8537086332','MH0/12','A','200');

Output--
1 row(s) inserted.

Then Insert check constraint (dgrade) E --

Input - insert into driver_detail(DNAME,DADDR,DPHNO,DLNO,DGRADE,DDISTANCE) values('Priya','Kgp','8537086332','MH0/12','E','200');

output-
check constraint ck_dg violated...
