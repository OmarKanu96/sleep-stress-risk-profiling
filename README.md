# sleep-stress-risk-profiling

## Problem Staement 
Using a dataset of 15,000 individuals....

## Tools Used
- MySQL
- Tableau

## Key findings

## SQL Queries 
-- Q1
SELECT occupation, 
SELECT occupation, count(*) as total_users, sum(case when stress_level >= 7 or sleep_quality_score <= 4 THEN 1 ELSE 0 END) as high_risk_count, 
round(sum(case when stress_level >= 7 or sleep_quality_score <= 4 then 1 else 0 end) * 100.0 / count(*), 2) AS high_risk_percentage
FROM sleep_mobile_stress_dataset_15000
GROUP BY occupation
ORDER BY high_risk_percentage DESC
