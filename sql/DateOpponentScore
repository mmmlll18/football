Даты встреч команды, её противник и счёт
```
SELECT
    m.date,
    t_self.name  AS team_name,
    t_opp.name   AS opponent_name,
    m.home_score,
    m.guest_score
FROM match AS m
JOIN team_match AS tm_self
    ON tm_self.match_id = m.match_id
JOIN team AS t_self
    ON t_self.team_id = tm_self.team_id
JOIN team_match AS tm_opp
    ON tm_opp.match_id = m.match_id
   AND tm_opp.team_id <> tm_self.team_id
JOIN team AS t_opp
    ON t_opp.team_id = tm_opp.team_id
WHERE t_self.name = 'НПО «Зуев-Павлова»'
AND m.status = 'played'
ORDER BY m.date;
```
<img width="447" height="69" alt="Снимок экрана 2025-12-17 в 20 23 54" src="https://github.com/user-attachments/assets/5383f47b-8414-4a45-afd7-d2e0e2bc7450" />
