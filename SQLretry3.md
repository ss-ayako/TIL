```
SELECT goals
FROM players
WHERE name ="ウィル";
```
```
SELECT *
FROM players
WHERE goals > 14;
```
***
# サブクエリ  
```
SELECT name
FROM players
WHERE goals > (
  -- この下にウィルの得点数を取得するクエリを書いてください
  SELECT goals
  FROM players
  WHERE name ="ウィル"
)
;
```
```
SELECT name,goals
FROM players
WHERE goals > (
  SELECT AVG(goals)            
  FROM players            
);
```
```
--ASを使って、取得したカラム名を"身長180cm以上の選手"としてください
SELECT name AS "身長180cm以上の選手"
FROM players
WHERE height >= 180;
```
