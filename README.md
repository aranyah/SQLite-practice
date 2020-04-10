# SQLite-practice
# Introduction to SQLite by analyzing data from Codecademy
# Assignment A

SELECT * FROM transaction_data LIMIT 10;

SELECT full_name, email FROM transaction_data WHERE zip = 20252;

SELECT full_name, email FROM transaction_data WHERE full_name = 'Art Vandelay' OR full_name LIKE '% der %';

SELECT ip_address, email FROM transaction_data WHERE ip_address LIKE '10.%';

SELECT email FROM transaction_data WHERE email LIKE '%temp_email.com';

SELECT * FROM transaction_data WHERE ip_address LIKE '120.%' AND full_name LIKE 'John%';

# Assignment B

SELECT DISTINCT year FROM population_years;

SELECT * FROM population_years;

SELECT population FROM population_years WHERE country = 'Gabon' ORDER BY population DESC limit 1;

SELECT country FROM population_years WHERE year = 2005 ORDER BY population limit 10;

SELECT DISTINCT country FROM population_years WHERE population > 100 AND year = 2010;

SELECT count(*) FROM (SELECT distinct country FROM population_years) WHERE country LIKE '%Islands%';

SELECT (population - (SELECT population FROM population_years WHERE country = 'Indonesia' AND year = 2000)) FROM population_years where country = 'Indonesia' and year = 2010;
