***
# サブクエリ  
サブクエリを使えば1個のクエリでデータ取得ができる  
( )で囲むことで、サブクエリを使用  
()内にセミコロン（;）は不要  
サブクエリを含むクエリの場合、サブクエリが実行された後、外側にあるクエリが実行 

サブクエリを使って、ウィルより得点数の多い選手名を調べましょう。  
***
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
***
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
countriesテーブルに主キー（id）はあったから、playersテーブルにだけ外部キー（country_id）を追加  
# JOIN  
紐付いたテーブル同士はJOINを使うことで合体させることができる  
ONで条件を指定  
結合条件は、「ON テーブル名.カラム名 = テーブル名.カラム名」で指定  
JOINを含んだクエリでは、はじめにJOINが実行。その次に、結合されたテーブルに対してSELECTが実行.  

JOINを使い、playersテーブルにcountriesテーブル を結合してデータを取得してください。  
ONを使い、playersテーブルのcountry_idとcountriesテーブルのidを紐づけてください。  
```
SELECT *
FROM players
--結合するテーブル名を追加してください
JOIN countries
--結合条件を追加してください
ON players.country_id=countries.id;
```
複数のテーブルに同じカラム名が存在するときは、「テーブル名.カラム名」で指定しなければならない  
SQLは、取得するテーブルを形成してから検索を行うので、FROM・JOINが先に行われる  

```
JOINを使い、playersテーブルにcountriesテーブル を結合して、下記のデータを取得してください。  
①countriesテーブルのnameカラム  
②goalsカラムの合計  
ただし、 GROUP BYを使って、countries.nameごとにグループ化してください。

SELECT countries.name,SUM(goals)
FROM players
JOIN countries
ON players.country_id = countries.id
GROUP BY countries.name;
```

***
JOINを使った結合は、FROMで指定したテーブルを基準に実行される  
ただし、外部キーがNULLのレコードは、実行結果に表示されない
***
```
JOINを使い、playersテーブルにteamsテーブルを結合して、データを取得

SELECT *
FROM players
JOIN teams
ON players.previous_team_id=teams.id;
```

```
JOINを使い、playersテーブルにteamsテーブルを結合して、下記のデータを取得してください。  
① playersテーブルのnameカラム  
② teamsテーブルのnameカラム  
ただし、①は選手名②は前年所属していたチームにカラム名を変更してください。  
SELECT players.name AS "選手名",teams.name AS "前年所属していたチーム"

FROM players
JOIN teams
ON players.previous_team_id=teams.id;
```
***
# LEFT JOIN  
FROMで指定したテーブルのレコードを全て取得  
```
LEFT JOINを使い、playersテーブルにteamsテーブルを結合して、データを取得

SELECT *
FROM players
LEFT JOIN teams
ON players.previous_team_id = teams.id;
```

```
LEFT JOINを使い、playersテーブルにteamsテーブルを結合して、下記のデータを取得してください。  
① playersテーブルのnameカラム  
② teamsテーブルのnameカラム  
ただし、①は選手名②は前年所属していたチームにカラム名を変更してください。  

SELECT players.name AS "選手名",teams.name AS "前年所属していたチーム"
FROM players
LEFT JOIN teams
ON players.previous_team_id = teams.id;
```
JOINは1つのクエリで、複数回使用できる  
JOINを複数回使用しても、FROMは1度だけ書けば大丈夫  
JOIN  
ON  
LEFT JOIN  
ON  
***
