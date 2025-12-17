Результативность данного игрока в данной встрече
```
SELECT
    p.full_name,
    t.name      AS team_name,
    m.date,
    pm.goal_scored
FROM match AS m
JOIN team_match AS tm
    ON tm.match_id = m.match_id
JOIN team AS t
    ON t.team_id = tm.team_id
JOIN player_match AS pm
    ON pm.match_id = m.match_id
   AND pm.team_id  = t.team_id
JOIN player AS p
    ON p.player_id = pm.player_id
WHERE t.name = 'Первый завод'
  AND m.date = '2026-06-14'
  AND p.full_name = 'Ладимир Александрович Маслов';
```
<img width="423" height="41" alt="Снимок экрана 2025-12-17 в 20 45 48" src="https://github.com/user-attachments/assets/15114e25-7eef-4cc0-9a33-fef718cf6380" />
