Игроки, забивавшие мячи на этом стадионе, по командам
```
SELECT
    t.name        AS team_name,
    p.full_name   AS player_name,
    SUM(pm.goal_scored) AS goals
FROM match AS m
JOIN player_match AS pm
    ON pm.match_id = m.match_id
JOIN player AS p
    ON p.player_id = pm.player_id
JOIN team AS t
    ON t.team_id = pm.team_id
WHERE m.stadium_id =  2
  AND m.status = 'played'
  AND pm.goal_scored > 0
GROUP BY t.name, p.full_name
ORDER BY t.name, goals DESC;
```
<img width="363" height="246" alt="Снимок экрана 2025-12-17 в 16 36 58" src="https://github.com/user-attachments/assets/12883bb4-3fdb-4322-867a-16e6af898857" />
