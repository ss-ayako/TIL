***
# サブクエリ  
サブクエリを使えば1個のクエリでデータ取得ができる  
( )で囲むことで、サブクエリを使用  
()内にセミコロン（;）は不要  
サブクエリを含むクエリの場合、サブクエリが実行された後、外側にあるクエリが実行 

サブクエリを使って、ウィルより得点数の多い選手名を調べましょう。  
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

平均得点数より得点数が多い選手名を調べましょう。  
```
SELECT name,goals
FROM players
WHERE goals >(
SELECT AVG(goals)
FROM players
);
```
# AS  
カラム名などに別名を定義  
「カラム名 AS "名前"」  
