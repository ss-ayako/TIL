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
```
-- 商品ごとに商品のid、売れた個数を取得してください
SELECT item_id,count(*)
FROM sales_records
GROUP BY item_id
;
```
```
-- 売れた数が多い上位5商品のidと個数を取得してください
SELECT item_id,count(*)
FROM sales_records
GROUP BY item_id
ORDER BY count(*) DESC
LIMIT 5
;
```
```
-- 売れた数が多い上位5商品のIDと名前、個数を取得してください
SELECT items.id,items.name,count(*)
FROM items
JOIN sales_records
ON sales_records.item_id = items.id
GROUP BY items.id
ORDER BY count(*) DESC
;
```
```
-- このサイトの総売上と総利益を取得してください
SELECT SUM(price) AS "総売上",SUM(price - cost) AS "総利益"
FROM items
JOIN sales_records
ON sales_records.item_id = items.id
;
```
```
-- 日ごとの販売個数とその日付を取得してください
SELECT purchased_at,COUNT(*) AS "販売個数"
FROM sales_records
GROUP BY purchased_at
ORDER BY purchased_at ASC;
```
```
-- 日ごとの売上額とその日付を取得してください
SELECT purchased_at,SUM(price) AS "売上額"
FROM sales_records
JOIN items
ON items.id=sales_records.item_id
GROUP BY  purchased_at
;
```
```
-- 10個以上購入したユーザーIDとユーザー名、購入した商品の数を取得してください
SELECT users.id,users.name,COUNT(*) AS "購入数"
FROM users
JOIN sales_records
ON users.id = sales_records.user_id
GROUP BY users.id
HAVING 10 <= COUNT(*)
;
```
