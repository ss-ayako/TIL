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

heightカラムの値が180以上であるレコードから、データを取得してください。  
ただし、取得したnameカラムはASを使って"身長180cm以上の選手"に変更してください。  
```
SELECT name AS "身長180cm以上の選手"
FROM players
WHERE height >= 180;
```

goalsデータの合計を取得してください。  
ただし、取得したカラム名はASを使って"チームの合計得点"に変更してください  
```
SELECT SUM(goals) AS "チームの合計得点"
FROM players
WHERE goals;
```
***

サブクエリを使って、ランキングが"日本"より上位である国のデータを取得してください。  
```
SELECT *
FROM countries
WHERE rank < (
SELECT rank
FROM countries
WHERE name = "日本" 
)
;
```
***
テーブルを紐づけるために、外部キーと主キーを使う  
