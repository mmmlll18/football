Цена билета на матч указанных команд
```
SELECT DISTINCT
    m.match_id,
    m.date,
    s.name  AS stadium_name,
    m.ticket_price
FROM match AS m
JOIN stadium AS s
    ON s.stadium_id = m.stadium_id
JOIN team_match AS tm1
    ON tm1.match_id = m.match_id
JOIN team AS t1
    ON t1.team_id = tm1.team_id
JOIN team_match AS tm2
    ON tm2.match_id = m.match_id
   AND tm2.team_id <> tm1.team_id
JOIN team AS t2
    ON t2.team_id = tm2.team_id
WHERE t1.name = 'Каменск-Уральский металлургический завод'
  AND t2.name = 'ОАО «Тетерин-Соболева»'
  AND m.date = '2026-01-05';
```
<img width="334" height="39" alt="Снимок экрана 2025-12-17 в 20 44 21" src="https://github.com/user-attachments/assets/75c29358-e3e8-4419-a284-7443686674fe" />
