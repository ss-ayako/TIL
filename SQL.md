# データベースを扱うための言語  
# SQL
データベース テキストや数値などのデータを保存するためのツール  
表のことを「テーブル」  
縦の列のことを「カラム」  
横の行のことを「レコード」  
必要に応じて複数のテーブルを作成することが可能 
***
***
# クエリ  
データベースに送る命令  
# SELECT データベースから、データを取得  
SELECT カラム名  
# FROM どのテーブルのカラムか  
FROM テーブル名  
クエリの終わりにはセミコロン  


```
-- purchasesテーブルから、priceカラムのデータを取得してください

SELECT price
FROM purchases;
```
***
複数のカラムからデータを取得　　
SELECT カラム名、カラム名  
```
SELECT name,price
FROM purchases;
```

全カラムのデータを取得する場合は「＊」の記号
```
SELECT * 
FROM purchases;
```
***
WHEREを用いて、数値データを条件に取得
```
SELECT *
FROM purchases
WHERE purchased_at = '2017-07-01';
```
***
# データ型
テキストデータ,数値データ、日付データ  
「テキストデータ,日付データ」はダブルクォーテーションまたはシングルクォーテーションで囲む必要がある  
***
# LIKE演算子 
「指定したカラムが〇〇を含む（〇〇のような）レコード」という条件  
```
WHERE name LIKE 文字列;
```

# ワイルドカード  
どんな文字列にも一致することを指す記号  
```
WHERE name LIKE "%文字列%";
```
# 前方一致  
「〇〇%」とした場合、「〇〇」以降はどんな文字列にも一致
「〇〇」で始まる文字列を検索する  
```
WHERE name LIKE "文字列%";
```
# 後方一致 
「%〇〇」とした場合、「〇〇」より前はどんな文字列にも一致  
「〇〇」で終わる文字列を検索する  
```
WHERE name LIKE "%文字列";
```
# NOT演算子  
「〇〇を含まないデータ」や「〇〇に一致しないデータ」のような条件  
```
WHERE NOT name LIKE "%文字列%";
WHERE NOT price > 1000;

//character_nameカラムが「にんじゃわんこ」でないデータを取得してください

SELECT *
FROM purchases
WHERE NOT character_name = "にんじゃわんこ";

//nameカラムが「プリン」を含まないデータを取得してください

SELECT *
FROM purchases
WHERE NOT name LIKE "%プリン%";  
```
# NULL  
中身が何かわからない  
なんのデータも保存されていない  
# NULLのデータを取得  
```
WHERE price IS NULL;
```
# NULLではないデータを取得  
```
WHERE price IS NOT NULL;
```
「IS NOT NULL」も「IS NULL」と同様に、「カラム名 IS NOT NULL」のようにして使う  
# NOT演算子  
「〇〇を含まないデータ」や「〇〇に一致しないデータ」  
```
WHERE NOT price > 1000;        //1000より大きい
WHERE NOT name LIKE "%プリン%";  //プリンを含まない
WHERE NOT character_name = "にんじゃわんこ";　　//にんじゃわんこではない
```
# AND演算子  
WHEREに複数の条件を指定することができる  
「WHERE 条件１ AND 条件２」 条件１と条件２を共に満たすデータを検索  
```
WHERE category = "食費"
AND character_name = "ひつじ仙人";
```
categoryカラムが「食費」かつcharacter_nameカラムが「ひつじ仙人」であるデータ  

# OR演算子  
「WHERE 条件１ OR 条件２」 条件１または条件２のどちらかを満たすデータを検索 
```
WHERE category = "食費"
OR character_name = "にんじゃわんこ";
```
categoryカラムが「食費」またはcharacter_nameカラムが「にんじゃわんこ」であるデータ  
# ORDER BY  
SQLでは「昇順」は「ASC」、「降順」は「DESC」と指定  
ORDER BY 「並べ替えたいカラム名」 「並べ方」  
```
ORDER BY price DESC;
```
priceカラムを基準に降順に  
***
# LIMIT  
「最大で何件取得するか」を指定  
LIMIT  データの件数;  

「ORDER BY」は「WHERE」と併用することが可能  
```
SELECT *
FROM purchases
LIMIT 5;
```
# DISTINCT
検索結果から重複するデータを除く  
DISTINCT(カラム名)  

# SELECTで取得するカラムに使用することで、重複を省いたデータを取得  
```
SELECT DISTINCT(name)
FROM purchases;
```
purchasesテーブルからnameカラムの重複したデータを省いて取得  

# 四則演算「足す(+)、引く(-)、かける(*)、割る(/)」  
priceカラムに1.08をかけ、消費税を含んだ値を取得  
```
SELECT name,price*1.08
FROM purchases;
```
# 集計関数  
数値データの合計、平均などを求めてくれるもの  
# SUM関数  
 SUM(カラム名)
 SELECTで取得するカラムに用いることで、集計結果を取得することができる  
```
SELECT SUM(price)
FROM purchases;
```
 character_nameが「にんじゃわんこ」であるpriceカラムのデータの合計を取得してください
```
SELECT SUM (price)
FROM purchases
WHERE character_name="にんじゃわんこ"
;
```
# AVG関数  
数値の平均を計算する  
AVG(カラム名)  
SELECTで取得するカラムに使用することで、計算結果を取得することができる  
```
SELECT AVG(price)
FROM purchases;


AVG関数はWHEREと併用することができる  
SELECT AVG(price)
FROM purchases
WHERE character_name="にんじゃわんこ"
;
```

# COUNT関数
指定したカラムのデータの合計数を計算  
COUNT( カラム名 )  
COUNT関数でカラム名を指定した場合、nullになっているデータの数は計算されない  
nullの数も含めてデータの数を計算したい場合は、COUNT関数で * (全てのカラム)を指定  

```
SELECT COUNT (*)
FROM purchases;
```
nullの数を含めてデータの数を数えられる  


 character_nameが「にんじゃわんこ」であるデータの数を取得してください

```
SELECT COUNT (*)
FROM purchases
WHERE character_name = "にんじゃわんこ"
;
```
# MAX、MIN関数  
保存されているデータの中で最大・最小のものを検索する集計関数  
```
SELECT MAX(カラム名）
FROM purchases;
```

```
-- character_nameが「にんじゃわんこ」であるレコードの中で、
-- もっとも大きいpriceカラムの値を取得してください

SELECT MAX(price)
FROM purchases
WHERE character_name = "にんじゃわんこ"
;
```
# GROUP BY  
グループ化  
GROUP BY カラム名  
GROUP BYを用いる場合、SELECTで使えるのは、GROUP BYに指定しているカラム名と、集計関数のみ  
```
purchased_atごとのお金を使った数を取得してください  
COUNT関数を使って、グループごとにデータの数とpurchased_atを取得  
SELECT COUNT(price),purchased_at
FROM purchases
GROUP BY purchased_at
;
```
複数カラムのGROUP BYの書き方  
GROUP BY カラム名,カラム名  
# HAVING
グループ化したデータを更に絞り込みたい
GROUP BY カラム名  
HAVING 条件  
条件を満たすグループを取得  
検索、グループ化、関数、HAVING  
WHEREはグループ化される前のテーブル全体を検索対象    
HAVINGはGROUP BYによってグループ化されたデータを検索対象  
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
