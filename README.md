# Placemnt_drives_eligibilty_system
Mini SQL Basics Project for Placement Shortlisting 
i have created a mini university placemnt eligibilty system real world project which issues the problem faced by companies during placemnet drives a lot of data needs to be handeled and thus it is a very timetaking process so with help of mysql queries the work can get easier .
# manually filling data in excel sheet is a very difficult and problematic task for companies this project entirely focuses on handling each and every thing through database logics 
# Database Schema 
student_id(primary key)
rollno int 
name varchar(20) 
cgpa
backlog
# making a specific student data table which handles all the student data 
and then one table for company drives their requirement 
min_cgpa_needed 
backlogs default(0)

# Tools used 
Cross JOIN - Since there is no common coloumn between student and company so any type of join won't add any value to it so instead i have used cross join which will cross multiply no of values and create n no of rows which are needed 


Case Statement- after cross join will create all combination case statement places a role of flag here 
like case 
when s.cgpa>= c.min_cgpa_required and s.backlog<= c.max_backlog_allowed then 'eligible' else  ' not eligible'
end as  shortlisted_status
so making the task easier 
