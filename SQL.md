# データベースを扱うための言語  
データベース テキストや数値などのデータを保存するためのツール  
表のことを「テーブル」  
縦の列のことを「カラム」  
横の行のことを「レコード」  
必要に応じて複数のテーブルを作成することが可能  
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

WHEREを用いて、数値データを条件に取得
```
SELECT *
FROM purchases
WHERE purchased_at = '2017-07-01';
```

# データ型
テキストデータ,数値データ、日付データ  
「テキストデータ,日付データ」はダブルクォーテーションまたはシングルクォーテーションで囲む必要がある  
  
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
