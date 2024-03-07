-　変数
- 宣言いらない
- ```$name= 'My name is ○○';```
- ```echo $name;```
- ```改行はこれ echo '<br>'```
***
変数$nameを用いて、My name is ○○と出力してください。  
```<?php```  
```$name = 'Tom';```  
```echo '変数$nameの値: '.$name;```  
```echo '<br>';```  
```echo '-----';```  
```echo '<br>';```  

```// この下にコードを書いてください```  
```echo 'My name is '.$name;```  

```?>```  
- 「 .（ドット）」は 文字列 や 変数 を結合します。
***
- 文字列は、計算式の前後に「,」（カンマ）で繋げて表示しています。
- ```echo "アイスの税込価格は" , $ice_cream * $tax , "円です。<br>";```
- 文字列を指定する場合は「"」ダブルクォーテーション、または「'」シンブルクォーテーションで囲む
- 改行タグなどのHTMLタグを使用する場合も同じ
***
- if文
- if(条件式）{
- echo '成り立ったとき実行される'；
- }
- ifとelseでもしも　だったら、　そうでなければ文
- if　の条件がfaiseだったら、
- 変数定義
- if(変数==a){
- echo 'aだったらこの処理実行される’
- }else{
- echo 'この処理が実行される’；
- }
- elseのとこ条件式書かない！！！
***
``` <?php```   
``` for($i=1;$i<=100;$i++){```　　　　　1から100までの数字を1件ずつ   
 ```  if ($i % 3 == 0 && $i % 5 == 0){```　　　　　　その数が3でも5でも割り切れる場合、   
 ```  echo 'FizzBuzz';```   
 ```  }``` 
 ```  elseif ($i % 5 == 0){```　　　　　その数が5で割り切れる場合  
 ```    echo 'Buzz';```   
 ```  }```  
 ```  elseif ($i % 3 == 0){```　　　　　その数が3で割り切れる場合  
 ```    echo 'Fizz';```   
 ```  }```   
 ```  else{```   
 ```    echo $i;```それ以外の時は普通に表示   
 ```  }```   
 ```  echo'<br>';```改行入れる   
``` }```   
``` ?>```   
***
```php
<?php
$prices = array(1000, 650, 750, 800);
echo '$pricesの値: ';
foreach ($prices as $price) {
  echo $price.' ';
}
echo '<br>';
echo '-----';
echo '<br>';
```

1. **価格の配列の初期化:**
   ```php
   $prices = array(1000, 650, 750, 800);
   ```
   配列 `$prices` を初期化し、商品の価格を含んでいます。

2. **価格の表示:**
   ```php
   echo '$pricesの値: ';
   foreach ($prices as $price) {
     echo $price.' ';
   }
   ```
   `foreach` ループを使用して、価格の配列 `$prices` の各要素を取り出し、それをスペースで区切って表示します。表示結果は `$pricesの値: 1000 650 750 800` となります。

3. **区切り線の表示:**
   ```php
   echo '<br>';
   echo '-----';
   echo '<br>';
   ```
   区切り線として `-----` を表示し、その後に改行を挿入します。

```php
// この下にコードを書いてください
$totalprice = 0;
foreach($prices as $price){
 $totalprice += $price;}
echo "合計金額は".$totalprice."円です";
?>
```

4. **合計金額の計算と表示:**
   ```php
   $totalprice = 0;
   foreach($prices as $price){
     $totalprice += $price;
   }
   ```
   `foreach` ループを使用して、価格の配列 `$prices` の各要素を取り出し、それらを合計するための `$totalprice` 変数に加算します。

5. **結果の表示:**
   ```php
   echo "合計金額は".$totalprice."円です";
   ```
   最終的な合計金額が表示されます。この場合、`合計金額は3400円です` となります。
***
- テキストボックスを作る
- ```<form action =”送信先のurl”　method="ここはgetかpost">```
- アクション属性、メソッド属性を使って記述
- その下にフォームの内容記述（　’や”不要）
- ```</form>```閉じタグ忘れずに！
***
- ```<?php と ?>``` は、一種のお作法で、このように書くことで```「<?PHP」」``` から```「 ?>」 ```までの範囲がPHPである」と宣言
- htmlの中に記述するときなどに使用する
***

```php
<?php
$menus = array(
  array('name' => 'CURRY', 'price' => 900),
  array('name' => 'PASTA', 'price' => 1200),
  array('name' => 'COFFEE', 'price' => 600)
);
```

1. **配列の初期化:**
   ```php
   $menus = array(
     array('name' => 'CURRY', 'price' => 900),
     array('name' => 'PASTA', 'price' => 1200),
     array('name' => 'COFFEE', 'price' => 600)
   );
   ```
   配列 `$menus` を初期化し、3つの連想配列を要素として持ちます。各連想配列は `'name'` キーと `'price'` キーを持ち、それぞれメニュー名と価格を表しています。

```php
foreach ($menus as $menu) {
  echo $menu['name']."は".$menu['price']."円です";
  echo '<br>';
}
```

2. **`foreach` ループ:**
   ```php
   foreach ($menus as $menu) {
   ```
   `foreach` ループを使用して、`$menus` 配列の各要素を `$menu` として取り出します。`$menu` は各要素が持つ配列です。

3. **メニュー情報の表示:**
   ```php
   echo $menu['name']."は".$menu['price']."円です";
   ```
   各メニューの情報を表示します。`$menu['name']` はメニュー名、`$menu['price']` はメニューの価格です。例えば、"CURRYは900円です" といった形式で表示されます。

4. **改行の追加:**
   ```php
   echo '<br>';
   ```
   各メニューの情報を表示した後に改行を挿入します。

```php
?>
```

5. **PHPコードの終了:**
   ```php
   ?>
   ```

***
提供されたコードには、`foreach` ループ内で合計金額を表示し続けてしまう問題があります。  
具体的には、各メニューの情報ごとに合計金額が表示されてしまいます。  
正しくは、`foreach` ループの終了後に一度だけ合計金額を表示するように修正する必要があります。  
以下は修正後のコードです。  

```php
<?php
$menus = array(
  array('name' => 'CURRY', 'price' => 900),
  array('name' => 'PASTA', 'price' => 1200),
  array('name' => 'COFFEE', 'price' => 600)
);

// この下にコードを書いてください
$totalprice = 0;

foreach ($menus as $menu) {
   $price = $menu['price'];
 
  echo $menu['name']."は".$menu['price']."円です";
  echo '<br>';
  
  $totalprice += $price;
}

echo "合計金額は".$totalprice."円です";
?>
```

修正点：
echo "合計金額は".$totalprice."円です";の後に}ではダメな理由。  
1. `echo "合計金額は".$totalprice."円です";` を `foreach` ループの外に移動し、
2. ループの終了後に一度だけ合計金額を表示しています。  
これにより、各メニューの情報が表示された後に一度だけ合計金額が正しく表示されるようになります。
***


```php
<?php
$menus = array(
  array('name' => 'CURRY', 'price' => 900),
  array('name' => 'PASTA', 'price' => 1200),
  array('name' => 'COFFEE', 'price' => 600)
);

// この下にコードを書いてください
$totalprice = 0;  // 合計金額を入れるための変数
$maxprice = 0;    // 暫定の最高価格を入れるための変数
$maxPriceMenuName = '';  // $maxPriceのものの名前を入れるための変数

foreach ($menus as $menu) {
   $price = $menu['price'];  // メニューの価格を取得
   $name = $menu['name'];    // メニューの名前を取得
   
  echo $name."は".$price."円です";  // メニュー名と価格の表示
  echo '<br>';  // 改行
  
  $totalprice += $price;  // 合計金額に価格を加算
  
  if ($price > $maxprice) {
    $maxprice = $price;
    $maxPriceMenuName = $name;
  }
}

echo "合計金額は".$totalprice."円です";  // 合計金額の表示
echo '<br>';  // 改行
echo $maxPriceMenuName."が最高価格で".$maxprice."円です";  // 最高価格の表示
?>
```

各行の解説：

1. **メニューの初期化:**
   ```php
   $menus = array(
     array('name' => 'CURRY', 'price' => 900),
     array('name' => 'PASTA', 'price' => 1200),
     array('name' => 'COFFEE', 'price' => 600)
   );
   ```
   メニューの情報を持つ連想配列 `$menus` を初期化します。

2. **変数の初期化:**
   ```php
   $totalprice = 0;
   $maxprice = 0;
   $maxPriceMenuName = '';
   ```
   合計金額、最高価格、最高価格のメニュー名を格納するための変数を初期化します。

3. **`foreach` ループ:**
   ```php
   foreach ($menus as $menu) {
   ```
   `foreach` ループを使用して各メニューの情報にアクセスします。

4. **各メニューの表示と合計金額の計算:**
   ```php
   $price = $menu['price'];
   $name = $menu['name'];

   echo $name."は".$price."円です";
   echo '<br>';

   $totalprice += $price;
   ```
   各メニューの名前と価格を表示し、合計金額を計算します。

5. **最高価格の更新:**
   ```php
   if ($price > $maxprice) {
     $maxprice = $price;
     $maxPriceMenuName = $name;
   }
   ```
   各メニューの価格が暫定の最高価格よりも高ければ、最高価格とそのメニュー名を更新します。

6. **最終的な合計金額と最高価格の表示:**
   ```php
   echo "合計金額は".$totalprice."円です";
   echo '<br>';
   echo $maxPriceMenuName."が最高価格で".$maxprice."円です";
   ```
   合計金額と最高価格を最終的に表示します。
***

 ```<?php
 ```class Menu {
  ```public $name; //Menuクラスに、$nameというプロパティを定義
 ```}
 ```$curry = new Menu();//生成したインスタンスを変数$curry に代入
 ```$pasta = new Menu();//生成したインスタンスを変数$pasta に代入
 ```$curry->name = 'CURRY';// $curryのnameプロパティに'CURRY'を代入
 ```$pasta->name = 'PASTA';// $curryのnameプロパティに'CURRY'を代入
 ```echo $curry->name;// $curryのnameプロパティをech
 ```echo '<br>';
 ```echo $pasta->name;// $pastaのnameプロパティをecho
 ```?>

***

 ```<?php
 ```class Menu {
 ```  public $name;//Menuクラスに、$nameというプロパティを定義
  
  ``` public function hello(){// helloメソッドを定義
  ``` echo '私はMenuクラスのインスタンスです'; //私はMenuクラスのインスタンスですとecho
 ```}
 ```}
 ```$curry = new Menu();
 ```$pasta = new Menu();
 ```$curry->name = 'CURRY';
 ```$pasta->name = 'PASTA';
 ```$curry->hello();// $curryに対してhelloメソッドを呼び出し

 ```echo '<br>';
 ```$pasta->hello();// $pastaに対してhelloメソッドを呼び出し

 ```?>

***
