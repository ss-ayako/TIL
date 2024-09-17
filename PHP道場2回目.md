- 出力するんだ！！
```
<?php
echo("Hello, PHP");
echo"<br>";
echo("10 + 7");
?>
```
- 文字と変数を連結
```
<?php
$name = 'Tom';
echo '変数$nameの値: '.$name;
echo '<br>';
echo '-----';
echo '<br>';

// この下にコードを書いてください
echo 'My name is '.$name;

?>
```
- 変数$priceには価格が、変数$taxRateには税率が代入されています。
- 変数$priceと$taxRateから税込価格を求めて、
- 税込価格は○○円ですと出力してください。
```
<?php
$price = 1000;
$taxRate = 0.08;
echo '変数$priceの値: '.$price;
echo '<br>';
echo '変数$taxRateの値: '.$taxRate;
echo '<br>';
echo '-----';
echo '<br>';

// この下にコードを書いてください
$Priceincludingtax = $price + $price * $taxRate;
echo '税込価格は'.$Priceincludingtax.'円です';

?>
```
