# bigquery_test
Business Analytics Assignment

SELECT Farm_proprietors_income FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
where 
Farm_proprietors_income <= 15000
LIMIT 1000

SELECT SUM(Percapita_unemployment_insurance_compensation) GeoName FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
LIMIT 1000

SELECT MIN(Percapita_income_maintenance_benefits), GeoName  FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
GROUP BY GeoName
LIMIT 1000

SELECT MAX(Proprietors_income), GeoName FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
GROUP BY GeoName
LIMIT 1000

SELECT GeoName, Wages_and_salaries FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
where
GeoName LIKE '%FL'
LIMIT 1000

SELECT GeoFIPS, GeoName, Unemployment_insurance FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
order by 
Unemployment_insurance desc 
LIMIT 1000

SELECT GeoName, GeoFIPS, avg(Nonfarm_proprietors_income), avg(Nonfarm_proprietors_employment) FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
GROUP BY 
GeoName, GeoFIPS
order by 
GeoFIPS
LIMIT 1000

SELECT GeoFIPS, GeoName, Wage_and_salary_employment  FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
where
Wage_and_salary_employment between 15000 and 30000
order by 
Wage_and_salary_employment
LIMIT 1000

SELECT GeoFIPS, GeoName, Percapita_personal_income FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
where
GeoName not LIKE '%FL'
LIMIT 1000

SELECT SUM(Earnings_per_job_avg) GeoName FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
LIMIT 1000







