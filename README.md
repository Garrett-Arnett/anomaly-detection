## Codeup Curriculum Anomaly Detection

Project Goals

Codeup staff bring up some questions to the data science team in email regarding concerns of the curriculum's safety.

Our goal is to answer the quesions and identify users with abnormal activity through anomaly detection and data analysis.

## Questions:

* Which lesson appears to attract the most traffic consistently across cohorts (per program), which lessons are least accessed?

* Is there a cohort that referred to a lesson significantly more than other cohorts seemed to gloss over? 

* Are there students who, when active, hardly access the curriculum? If so, what information do you have about these students? 

* Is there any suspicious activity, such as users/machines/etc accessing the curriculum who shouldn’t be? Does it appear that any web-scraping is happening? Are there any suspicious IP addresses? 

* At some point in 2019, the ability for students and alumni to access both curriculums (web dev to ds, ds to web dev) should have been shut off. Do you see any evidence of that happening? Did it happen before?

* What topics are grads continuing to reference after graduation and into their jobs (for each program)? 

* Which lessons are least accessed? 

## Data Dictionary 

|Variable|	Value	|Meaning
|---|----|---|
|date	|datetime|	The date of log entry|
|time	|datetime	|The time of the day of log entry|
|path	|string|	The path the user is on|
|user id	|float	|The primary key of log table, indicating each user|
|ip|	string|	The user's ip address|
|cohort name	|string	|The name of user's cohort|
|slack|	string|	The name of the slack chanel that user belongs to|
|start date|	datetime|	The start date of the cohort|
|end date	|datetime	|The end date of the cohort|
|program id	|datetime	|This indicates which program is the user in|


## Findings and Takeaways

* Data Science cohorts access classification/overview the most. There are 100+ pages that were accessed only once. For example: "Introduction to Python", "Creating Charts", "Case Statements", "ML Methodologies Drawing", "Tidy Data", "git/cli", "mySQL Introduction", etc.

* Web Development cohorts access javascript-i the most. There are 400+ pages that were accessed only once. For example: "JavaScript Working with Variables", "Java-i", "HTML", "HTML-CSS Introduction", etc.

* For Full Stack PHP (Web Development) Program:

- cohort 1 looked at jquery much more than other cohorts

- cohort 17 looked at jquery and java-1/methods much more than other cohorts.
* For Full Stack Java (Web Development), Data Science, Front End Program: None of the cohorts looked at a lesson signifcantly more that another cohort just glanced at.

* 4 users hardly ever accessed the curriculum. All 4 users are from Full Stack Java (Web Development) Program. Their information are provided above.

* There are 29 users have suspicious activities, among those users we suspect 2 of them perform web-scrapping and 3 appear to be accessing curriculums that they shouldn't access.

* There is no suspicious IP address. But for those who have significant amount of IP addresses during their program, their IP address appear to be distributed accross the United States.

* 116 users have abnormal amount of log entry (page visit).

* For Data Science Program: There does not appear to be any access to the Web Dev paths before September 2019, and after December 2019. Which leads us to believe they did not have access during those time periods.

* For Web Development Program: There appears to be access to the Data Science paths after September 2019. Specifically, from July 2020 to April 2021.

* Most Visited Topics For Full Stack Java: HTML, JavaScript, CSS, Spring, and Java.

* Most Visited Topics For Full Stack PHP: JavaScript, spring, CSS, and Java.

* Most Visited Topics For Data Science: Anomaly Detection, mySQL, Classification, Feature Scaling, and AL-ML-DL.

* Most Visited Topics For Front End: HTML, CSS, Introduction to HTML-CSS.

* Web Development: there are 400+ pages that were accessed only once.

* Data Science: there are 100+ pages that were accessed only once.

* Many of the pages are introduction pages with no useful information.


## Re-Create

* 1. final_project.ipynb file from this git repo
* 2. wrangle.py file from this git repo
* 3. acs.csv from this git repo or mysql access



