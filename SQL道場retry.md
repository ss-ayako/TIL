```
-- ユーザーの年齢ごとの人数と、その年齢を取得してください
SELECT age,COUNT(*)
FROM users
GROUP BY age
;
```
```
-- 20歳未満の男性ユーザーの、全てのカラムの値を取得してください。
SELECT *
FROM users
WHERE age < 20 AND gender = 0
;
```
```
-- 全商品の名前を重複無く取得してください
SELECT DISTINCT(name)
FROM items;
```
```
-- 全商品の名前と値段を、値段が高い順に並べてください
SELECT name,price
FROM items
ORDER BY price DESC;
```
```
-- 名前の一部に「シャツ」を含む商品の、全てのカラムの値を取得してください
SELECT *
FROM items
WHERE name LIKE "%シャツ%"
;
```
```
-- 全商品の名前、値段、利益を取得してください
SELECT name,price,price - cost
FROM items
;
```
```
-- 全商品の利益の平均を取得してください
SELECT AVG(price - cost)
FROM items
;
```
```
-- 各商品あたりの利益が上位5件の商品の名前と利益を取得してください
SELECT name,price - cost
FROM items
ORDER BY  price DESC
LIMIT 5
;
```
```
-- 「グレーパーカー」より値段が高い商品の名前と値段を取得してください
SELECT name,price
FROM items
WHERE price >(
SELECT price
FROM items
WHERE name = "グレーパーカー")
;
```
```
-- 7000円以下で「グレーパーカー」より利益が高い商品を取得してください
SELECT name,price-cost
FROM items
WHERE price <= 7000 AND price-cost > (
SELECT price-cost
FROM items
WHERE name = "グレーパーカー")
;
```
