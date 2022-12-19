WEBSITE: https://metabase.qa.studio
DATABASE: qastudio
LOGIN: student@qa.studio
PASSWORD: iloveqa1


-- Print the first and last name of all employees aged > 24 years in Moscow
SELECT name, surname 
FROM staff 
WHERE age > 24 AND address='Moscow';

-- Print the first and last name of all employees sorted from junior to senior
SELECT name, surname, age 
FROM staff 
ORDER BY age;

-- Print the age of all employees with the profession qa_engineer
SELECT age 
FROM staff 
JOIN positions ON positions.id=staff.position_id 
WHERE position_name='qa_engineer';

-- Print the first and last name of all frontend_dev with a line limit of 20
SELECT name, surname 
FROM staff 
JOIN positions ON positions.id=staff.position_id 
WHERE position_name='frontend_dev' LIMIT 20;

-- How many employees does the company have in total in Moscow?
SELECT COUNT(id) 
FROM staff 
WHERE address='Moscow';

-- What is the salary of each employee. In the resulting table, you need to display two columns — name and salary
SELECT name, salary 
FROM staff 
JOIN positions ON positions.id=staff.position_id;

-- What is the total salary of all employees who work in Moscow?
SELECT SUM(salary) 
FROM positions 
JOIN staff ON staff.position_id=positions.id 
WHERE address='Moscow';

-- Output a list of unique cities where there are employees.
SELECT DISTINCT address 
FROM staff;

-- Print a list of unique cities with the letter k in the name.
SELECT DISTINCT address 
FROM staff 
WHERE address LIKE '%k%';

-- Print the names of positions with salaries between 1500 and 2200
SELECT position_name, salary 
FROM positions 
WHERE salary BETWEEN 1500 AND 2200;

-- Print the First and Last Name of each employee along with their Position. 
-- Important: there are two positions where no one works. 
-- We need to get them too.
SELECT name, surname, position_name 
FROM staff 
RIGHT JOIN positions ON positions.id=staff.position_id;

-- Output which computer Anastasia Morozova has
SELECT computer_name 
FROM computers 
JOIN positions ON positions.computer_id=computers.id 
JOIN staff ON staff.position_id=positions.id 
WHERE staff.name='anastasia' AND staff.surname='morozova';

-- Output the salary amounts, broken down by city.
SELECT address, SUM(salary) 
FROM staff 
JOIN positions ON positions.id=staff.position_id 
GROUP BY staff.address;