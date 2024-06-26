```
-- 重複するデータを除いたcharacter_nameカラムのデータを取得してください

SELECT DISTINCT(character_name)
FROM purchases;
```
```
-- 「SELECT name, price, 」に追加し、消費税を含んだpriceカラムのデータを取得してください

SELECT name, price, price*1.08
FROM purchases;
```
```
-- priceカラムのデータの合計を取得してください

SELECT SUM(price)
FROM purchases;
```
```
-- priceカラムのデータの合計を取得してください

SELECT SUM(price)
FROM purchases;
```
