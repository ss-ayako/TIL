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
