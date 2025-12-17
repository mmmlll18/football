ФИО и номера игроков, участвовавших во встрече
```
SELECT DISTINCT
    p.full_name,
    p.number
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
WHERE t.name =  'Каменск-Уральский металлургический завод'
  AND m.date = '2026-01-05'
ORDER BY p.full_name;
```
<img width="278" height="243" alt="Снимок экрана 2025-12-17 в 20 28 28" src="https://github.com/user-attachments/assets/e60a7119-1c4c-49e8-b34e-097e3313cc83" />
