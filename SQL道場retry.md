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
