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
```
--ASを使って、取得したカラム名を"チームの合計得点"としてください
SELECT SUM(goals) AS "チームの合計得点"
FROM players
;
```
```
SELECT *
FROM countries
WHERE rank < (
SELECT rank 
FROM countries
WHERE name="日本"
)
;
```
# テーブル紐付け  
```
SELECT sum(goals),country_id
FROM players
GROUP BY country_id;
```
最初にテーブル結合、後からselect読み込まれるそんな順番
```
SELECT *
FROM players
--結合するテーブル名を追加してください
JOIN countries
--結合条件を追加してください
ON players.country_id=countries.id;
```
***
```
SELECT players.name,countries.name
FROM players
JOIN countries
ON players.country_id=countries.id;
```
```
SELECT countries.name,SUM(goals)
FROM players
JOIN countries

ON players.country_id=countries.id
GROUP BY countries.name;
```
