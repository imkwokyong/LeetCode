SELECT user_id, CASE WHEN
    COUNT(action) = 0 THEN 0.00
    ELSE ROUND(SUM(action = 'confirmed') / COUNT(action), 2)
    END AS confirmation_rate
FROM Signups AS s
LEFT JOIN Confirmations AS c
USING (user_id)
GROUP BY user_id
