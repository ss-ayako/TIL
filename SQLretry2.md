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
```
-- character_nameが「にんじゃわんこ」であるpriceカラムのデータの合計を取得してください

SELECT SUM(price)
FROM purchases
WHERE character_name = "にんじゃわんこ"
;
```
```
-- priceカラムの平均を取得してください

SELECT AVG(price)
FROM purchases;
```
```
-- character_nameが「にんじゃわんこ」であるpriceカラムのデータの平均を取得してください

SELECT AVG(price)
FROM purchases
WHERE character_name = "にんじゃわんこ"
;
```
