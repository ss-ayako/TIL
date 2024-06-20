```
-- purchasesテーブルから、nameカラムのデータを取得してください

SELECT name
FROM purchases;
```
```
-- purchasesテーブルから、priceカラムのデータを取得してください
SELECT price
FROM purchases;
```
```
-- purchasesテーブルから、「nameカラム」と「priceカラム」のデータを取得してください
SELECT name,price
FROM purchases;
```
```
-- purchasesテーブルから、全てのカラムのデータを取得してください
SELECT *
FROM purchases;
```
```
-- 「FROM purchases」のあとにコードを追加し、categoryカラムが「食費」であるデータを取得してください

SELECT *
FROM purchases
WHERE category = "食費";
```
```
-- 「FROM purchases」のあとにコードを追加し、priceカラムが「1000」のデータを取得してください

SELECT *
FROM purchases
WHERE price = 1000;
```
```
-- 「FROM purchases」のあとにコードを追加し、purchased_atカラムが「2017-07-01」のデータを取得してください

SELECT *
FROM purchases
WHERE purchased_at = "2017-07-01";
```
```
-- 「FROM purchases」のあとにコードを追加し、purchased_atカラムが「2017-08-01以前」のデータを取得してください

SELECT *
FROM purchases
WHERE purchased_at <= "2017-08-01";
```
```
-- 「FROM purchases」のあとにコードを追加し、priceカラムが「1000以上」のデータを取得してください

SELECT *
FROM purchases
WHERE price >=1000;
```
```
-- 「FROM purchases」のあとにコードを追加し、nameカラムが「プリン」を含むデータを取得してください

SELECT *
FROM purchases
WHERE name LIKE "%プリン%";
```
```
-- 「FROM purchases」のあとにコードを追加し、nameカラムが「プリン」で始まるデータを取得してください

SELECT *
FROM purchases
WHERE name LIKE "プリン%";
```
```
-- 「FROM purchases」のあとにコードを追加し、nameカラムが「プリン」で終わるデータを取得してください

SELECT *
FROM purchases
WHERE name LIKE "%プリン";
```
```
-- 「FROM purchases」のあとにコードを追加し、character_nameカラムが「にんじゃわんこ」でないデータを取得してください

SELECT *
FROM purchases
WHERE NOT character_name = "にんじゃわんこ";　//NOT　ではないもの
```
SQLで文字列の部分一致をチェックするためには、LIKE 演算子を使用する必要がある  
```
-- 「FROM purchases」のあとにコードを追加し、nameカラムが「プリン」を含まないデータを取得してください

SELECT *
FROM purchases
WHERE NOT name LIKE "%プリン%"
```
```
-- 「FROM purchases」のあとにコードを追加し、priceカラムがNULLであるデータを取得してください

SELECT *
FROM purchases
WHERE price IS NULL;
```
