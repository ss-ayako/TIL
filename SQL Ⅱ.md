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

