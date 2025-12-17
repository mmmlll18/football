Стадионы, где проводились встречи
```
SELECT
    s.stadium_id,
    s.name,
    s.city,
    COUNT(m.match_id) AS games_played
FROM stadium AS s
JOIN match AS m
    ON m.stadium_id = s.stadium_id
WHERE m.status = 'played'
GROUP BY s.stadium_id, s.name, s.city
ORDER BY s.name;
```
<img width="387" height="113" alt="Снимок экрана 2025-12-17 в 16 37 57" src="https://github.com/user-attachments/assets/26e21fdf-e3b4-445d-acd5-918ec356ecd6" />
