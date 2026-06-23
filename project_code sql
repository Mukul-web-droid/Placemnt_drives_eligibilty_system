create database universityplacement;
use universityplacement;
create table student_data(
student_id int primary key  ,
name varchar(20) not null,
roll_no int,
branch varchar(20) not null,
cgpa decimal(3,2) not null,
backlog int  default(0),


constraint unique_roll unique(roll_no),
constraint check_cgpa_limit check(cgpa >=0.00 and cgpa<=10.00),
constraint  active_backlog check(backlog >=0)
);
create table company_drives(
company_id int primary key auto_increment,
companyname varchar(20),
min_cgpa_required decimal (3,2),
max_backlog_allowed  int default(0),
package_lpa decimal(4,2),
constraint check_package check(package_lpa>0)
);

insert into student_data(student_id,name,roll_no,branch,cgpa,backlog) values 
(101,'Avinesh Triphati',108,'CSE',7.11,0),
(102,'Priyanshu Bhatt',109,'CSE',7.22,1),
('103', 'Adam', 110,'AIML', 7.11, 1),
('104', 'Rohit Sharma',111, 'CSE', 6.85, 2),
('105', 'Priya Verma', 112,'DATA SCIENCE', 8.20, 0),
('106', 'Rahul Yadav', 113,'AIML', 5.50, 3),
('107', 'Sneha Gupta',114, 'CSE', 7.80, 0),
('108', 'Amit Patel', 115,'DATA SCIENCE', 6.40, 1),
('109', 'Anjali Mishra', 116,'AIML', 8.45, 0),
('110', 'Vikram Singh', 117,'CSE', 7.25, 0);
SELECT * FROM Student_data;
insert into company_drives(company_id,companyname,min_cgpa_required,max_backlog_allowed,package_lpa) values 
(1, 'Google', 8.50, 0, 45.50),
(2, 'Microsoft', 8.00, 0, 38.00),
(3, 'TCS ', 6.00, 0, 3.60),
(4, 'Infosys', 6.50, 0, 6.25),
(5, 'Cognizant', 7.00, 0, 4.50);
select * from company_drives;
Select 
s.name,
s.roll_no,
s.branch,
s.cgpa,
s.backlog,
c.companyname,
c.package_lpa,
case 
when s.cgpa>= c.min_cgpa_required and s.backlog<= c.max_backlog_allowed then 'eligible' else  ' not eligible'
end as  shortlisted_status
from student_data s
cross join company_drives c
order by s.roll_no asc, c.package_lpa desc;

