## SQL Queries and Results

### Query 1: Policies nearing expiry

```sql
SELECT c.client_name, p.cover_type, p.end_date, p.annual_premium
FROM policy AS p
JOIN client AS c ON c.client_id = p.client_id
WHERE p.end_date BETWEEN CURRENT_DATE AND CURRENT_DATE + 30
ORDER BY p.end_date;
```

### Query 2: Policy count and premium by client

```sql
SELECT c.client_id, c.client_name, COUNT(p.policy_id) AS policy_count,
       SUM(p.annual_premium) AS total_annual_premium
FROM client AS c
LEFT JOIN policy AS p ON p.client_id = c.client_id
GROUP BY c.client_id, c.client_name
ORDER BY total_annual_premium DESC;
```
The result from the query above shows the policy count and total annual premium for each client ordered from highest to lowest.  The LEFT JOIN command keeps clients with no policies in the results.

## Performance and Indexing

The baseline plan used a sequential scan on the policy table and had an execution time of 0.683 ms. After creating idx_policy_end_date, the plan used a bitmap index scan followed by a bitmap heap scan on policy, and the execution time was 0.595 ms. This single-run reduction of 0.088 ms is a modest improvement, and timings may vary between runs. The plan still used a sequential scan on the small client table.

##Index Used

CREATE INDEX idx_policy_end_date ON policy (end_date);
