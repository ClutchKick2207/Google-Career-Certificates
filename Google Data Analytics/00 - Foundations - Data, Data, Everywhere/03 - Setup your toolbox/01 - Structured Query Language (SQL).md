## Where is this course?
- [Google Career Certificates - Data Analytics](https://grow.google/certificates/data-analytics/#?modal_active=none)

## My Notes
> My notes for this overall course will be laid out by module in the course, and have subheadings in order to differentiate between different topics/videos that are presented in the courses. I'll add in any extra notes/resources that I use where necessary, and hope it will be helpful for anyone looking!

## SQL Guide - Getting Started
- **SQL Guide**
	- **Capitalization, indentation, and semicolons**
		- You can write your SQL queries in all lowercase and don’t have to worry about extra spaces between words. 
		- Use capitalization and indentation can help you read the information more easily. Keep your queries neat, and they will be easier to review or troubleshoot if you need to check them later on.
		- ![[Pasted image 20231116114836.png]]
		- Notice that the SQL statement shown above has a semicolon at the end.
	- **WHERE conditions**
		- In the query shown above, the **SELECT** clause identifies the column you want to pull data from by name, **field1**, and the **FROM** clause identifies the table where the column is located by name, **table**. Finally, the **WHERE** clause narrows your query so that the database returns only the data with an exact value match or the data that matches a certain condition that you want to satisfy.
	- **Comments**
		- Some tables aren’t designed with descriptive enough naming conventions. In the example, **field1** was the column for a customer’s last name, but you wouldn’t know it by the name. A better name would have been something such as **last_name**. In these cases, you can place comments alongside your SQL to help you remember what the name represents. Comments are text placed between certain characters, **/*** and ***/**, or after two dashes (**--**) as shown below. 
		- ![Image of SQL statements with comments shown between /* and */ and after --](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/k4wKMVuhQ6iMCjFbodOopA_eabf1858723e4c43a78ba734f9e40ff1_Screenshot-2021-04-30-10.53.40-AM.png?expiry=1700265600000&hmac=nmNmRb9-1FbUHyEedCJRFBt0UEK3ctBpzjidqu_FrpU)
		- ![[Pasted image 20231116115019.png]]
		- ![[Pasted image 20231116115042.png]]
	- **Aliases**
		- You can also make it easier on yourself by assigning a new name or **alias** to the column or table names to make them easier to work with (and avoid the need for comments). This is done with a SQL AS clause. In the example below, the alias **last_name** has been assigned to **field1** and the alias **customers** assigned to **table.** These aliases are good for the duration of the query only. An alias doesn’t change the actual name of a column or table in the database.
		- ![[Pasted image 20231116115108.png]]
	- **SQL to Work**
		- You want to pull all the columns: **empID**, **firstName**, **lastName**, **jobCode**, and **salary**. Because you know the database isn’t that big, instead of entering each column name in the **SELECT** clause, you use **SELECT ***.  This will select all the columns from the Employee table in the **FROM** clause.
			- ![[Pasted image 20231116115127.png]]
		- Now, you can get more specific about the data you want from the Employee table. If you want all the data about employees working in the **SFI** job code, you can use a **WHERE** clause to filter out the data based on this additional requirement.
			- ![[Pasted image 20231116115137.png]]
		- ![[Screenshot 2023-11-16 at 11.51.52 am.png]]
		- Suppose you notice a large salary range for the **SFI** job code. You might like to flag all employees in all departments with lower salaries for your manager. Because interns are also included in the table and they have salaries less than $30,000, you want to make sure your results give you only the full time employees with salaries that are $30,000 or less. In other words, you want to exclude interns with the **INT** job code who also earn less than $30,000. The **AND** clause enables you to test for both conditions.
			- ![[Pasted image 20231116115210.png]]
			- The resulting data from the SQL query might look like the following (interns with the job code **INT** aren't returned):
				- ![[Screenshot 2023-11-16 at 11.52.20 am.png]]
	- **SQL Resources**
		- https://www.w3schools.com/sql/default.asp
		- https://www.sqltutorial.org/sql-cheat-sheet/

