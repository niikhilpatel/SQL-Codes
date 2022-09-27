create table branch
(
branch_name char(10) primary key,
branch_city char(20),
assets int
)
insert into branch values
('IDBP','BPL',200000)

select * from branch

create table customer
(
customer_name char(50),
customer_street varchar(100),
customer_city char(50)
)

insert into customer values
('Lucky','Ranjhi',5000)

select * from customer


create table customer2
(
customer_name char(50),
customer_street varchar(100),
customer_city char(50)
)

insert into customer values
('Rahul','Jaipur',200)

select * from customer


create table loan
(
loan_number int,
branch_name char(50),
amount int
)

insert into loan values
('','SBI',100000)

select * from loan


create table borrower
(
customer_name char(50),
loan_number int
)

insert into borrower values
('','')

select * from borrower




create table branch1
(
branch_name char(50),
branch_city char(50),
assets int
)

insert into branch1 values
('SBI','',100000)

select * from branch1

select customer_name
from loan inner join borrower
on loan.loan_number=borrower.loan_number
inner join branch1 on
loan.branch_name=branch1.branch_name
where branch_name='SBI'and
assets>100000
