```
<?php
echo('Hello, PHP');
echo '<br>';
echo('10 + 7');
?>
```
```
<?php
$name = 'Tom';
echo '変数$nameの値: '.$name;
echo '<br>';
echo '-----';
echo '<br>';

// この下にコードを書いてください
echo('My name is'.$name);

?>
```
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
$taxinprice = $price + $price * $taxRate;
echo('税込価格は'.$taxinprice.'円です');

?>
```
