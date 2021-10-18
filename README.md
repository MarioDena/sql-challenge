# Employee Database: A Mystery in Two Parts

![SQL](https://process.fs.teachablecdn.com/ADNupMnWyR7kCWRvm76Laz/resize=width:705/https://www.filepicker.io/api/file/RL4kFbu1SMiCIeLAtWX3)

## Challenge Instructions

This project utilizes Data Engineering and Data Analysis to build a SQL database of employees of a corporation called Pewlett Hackard from the 1980s and 1990s. There are six CSV files holding the data of employees. The SQL tables were designed and the data in the CSVs were successfully imported into a SQL database.

## Data Engineering

- Inspect the CSVs and sketch out an ERD of the tables. The [QuickDBD](https://www.quickdatabasediagrams.com/) was used in this project. Use the information from ERD to create a table schema for each of the six CSV files and specify data types, primary keys, foreign keys, and other constraints.

  - For the primary keys check to see if the column is unique, otherwise create a [composite key](https://en.wikipedia.org/wiki/Compound_key), which takes two primary keys in order to uniquely identify a row
  - Be sure to create tables in the correct order to handle foreign keys
  <p align="center">
    <img src="https://github.com/Jiuhe2020/sql-challenge/blob/master/EmployeeSQL/employee_ERD.png" height="75%" width="75%">
  </p>

- Import each CSV file into the corresponding SQL table and make sure to import the data in the same order that the tables were created

## Data Analysis

- List the following details of each employee: employee number, last name, first name, sex, and salary
- List first name, last name, and hire date for employees who were hired in 1986
- List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name
- List the department of each employee with the following information: employee number, last name, first name, and department name
- List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B"
- List all employees in the Sales department, including their employee number, last name, first name, and department name
- List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name
- In descending order, list the frequency count of employee last names, i.e., how many employees share each last name

## BONUS

A visualization of the data was generated by taking the following steps:

- Import the SQL database into Pandas (use the code below to get started)

```python
from sqlalchemy import create_engine
engine = create_engine('postgresql://localhost:5432/<your_db_name>')
connection = engine.connect()
```

- Create a histogram to visualize the most common salary ranges for employees
<p align="center">
  <img src="https://github.com/Jiuhe2020/sql-challenge/blob/master/images/BonusHistogram.png" height="75%" width="75%">
</p>

- Create a bar chart of average salary by title
<p align="center">
  <img src="https://github.com/Jiuhe2020/sql-challenge/blob/master/images/BonusBarChart.png" height="75%" width="75%">
</p>

## List of Content requiered

1. employee_ERD.png: an image file of the ERD
2. employee_schema.sql: a .sql file of the table schemata
3. employee_query.sql: a .sql file of the queries
4. employee.ipynb: a Jupyter Notebook of the bonus analysis
