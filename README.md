# Overview
The purpose of this analysis was to combine data from multiple csv files that shared various data columns. We created comprehensive joined tables combining information pulled from the different tables using various SQL functions. Through these methods, we were able to determine the number of retiring employees by title and identify employees eligible to participate in Pewlett-Hackard's mentorship program. 

# Results
- Once we filter out the duplicate titles from our retirement_titles.csv table, we see that 90,399 employees fit the criteria for retirement at Pewlett-Hackard. 
<img width="731" alt="unique_titles_image" src="https://user-images.githubusercontent.com/82029390/120903290-5bb1f680-c613-11eb-92f1-2ce63cf6b89a.png">


-  Of the various employee titles, Senior Engineers are the greatest in count that are likely to retire, followed by Senior Staff and Engineers. 
<img width="252" alt="retiring_titles_image" src="https://user-images.githubusercontent.com/82029390/120903603-0a0a6b80-c615-11eb-82c6-a4f4b79c02f5.png">

- If we alter the code we used to retrieve our retiring_titles table, we can view how many employees are eligible for mentorship by their titles. 
<img width="217" alt="mentorship_by_title_image" src="https://user-images.githubusercontent.com/82029390/120903729-d8de6b00-c615-11eb-99ad-893791cb1f44.png">

- There are approximately 1,549 employees that are eligible for Pewlett-Hackard's mentorship program.

# Summary
Approximately 90k roles will need to be filled as these employees are ready to retire. We are able to view through our analyses how many of our silver tsunami employees belong to which departments and their corresponding titles. This provides us with a good insight as to which departments Pewlett-Hackard will need to reach out to in order to prepare them for iminent recruitment. There are only 1.5k employees that are eligible for the mentorship program and this is likely going to be an issue when 90k of our older employees retire. It is recommended that these 1.5k employees start training their current coworkers so as to increase their likelihood of being eligible for the mentorship program in order to prepare for the iminent hiring of new employees. 
As shown above, an additional code we can run to gain further insight to our data allows us to view how many employees are eligible for mentorship by their titles.

<img width="217" alt="mentorship_by_title_image" src="https://user-images.githubusercontent.com/82029390/120903729-d8de6b00-c615-11eb-99ad-893791cb1f44.png">

We can also join our retirements_titles table that contains our silver tsunami members info with our dept_emp table to add a dept_no column.

<img width="835" alt="silver_tsunami_depts_image" src="https://user-images.githubusercontent.com/82029390/120905184-5c03bf00-c61e-11eb-9bd5-bbf183d406ae.png">

I first had to add dept_no to the table by joining the tables through their shared emp_no column. Once this column is added(as shown above), we can generate a table that shows us how many employees that are likely to retire soon belong to which department numbers in descending order by the count function as used in our previous code. 

<img width="149" alt="silver_pic" src="https://user-images.githubusercontent.com/82029390/120905268-0976d280-c61f-11eb-9007-2598a5d78e17.png">


We could also add the actual department name by adding de.departments in the SELECT line upon making the table in line 280 of this code. This analysis gives us insight as to which departments will be exhibiting the greatest loss.
