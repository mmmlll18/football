Отчёт по стадиону (кол-во матчей, победы хозяев/гостей)
```
SELECT
    COUNT(*) AS total_matches,
    SUM(CASE WHEN m.home_score > m.guest_score THEN 1 ELSE 0 END) AS home_wins,
    SUM(CASE WHEN m.home_score < m.guest_score THEN 1 ELSE 0 END) AS guest_wins
FROM match AS m
WHERE m.stadium_id =  2
  AND m.status = 'played';
```
<img width="235" height="45" alt="Снимок экрана 2025-12-17 в 16 34 37" src="https://github.com/user-attachments/assets/34c6d584-cc9a-4979-9fe8-2529c3a809d0" />
