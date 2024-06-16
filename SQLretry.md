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
