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
```
<?php
$money = 2000;
$price = 1000;
$taxRate = 0.08;
echo '変数$moneyの値: '.$money;
echo '<br>';
echo '変数$priceの値: '.$price;
echo '<br>';
echo '変数$taxRateの値: '.$taxRate;
echo '<br>';
echo '-----';
echo '<br>';

// この下にコードを書いてください
$taxinprice = $price + $price * $taxRate;

if($taxinprice < $money){
  echo '商品を買うことができます';
}elseif($taxinprice == $money){
  echo '商品を買うことができますが、所持金がなくなります';
}else{
  echo '商品を買うことができません';
}
```
echo '<br>'; が for 文の中に書かれていますが、正確には各条件分岐 (if や elseif) の外に配置されています。  
これは、各ループの繰り返しが終わるたびに改行を行いたいからです。  
もし echo '<br>'; が for 文の外に置かれていたら、すべての数値や文字が改行なしで一続きに表示されてしまい、見やすさが損なわれます。  
```
<?php
for($i=1;$i<100;$i++){
  if($i % 5 ==0&&$i % 3 ==0){
    echo 'FizzBuzz';
  }elseif($i % 5 ==0){
    echo 'Buzz';
  }elseif($i % 3 ==0){
    echo 'Fizz';
  }else{
  echo $i;
}
  echo '<br>';
}
?>
```
```
<?php
$prices = array(1000, 650, 750, 800);
echo '$pricesの値: ';
foreach ($prices as $price) {
  echo $price.' ';
}
echo '<br>';
echo '-----';
echo '<br>';

// この下にコードを書いてください
$totalprice = 0;
foreach ($prices as $price) {
  $totalprice = $totalprice + $price;

}
echo '合計金額は'.$totalprice.'円です';
?>
```
```
<?php
$prices = array(1000, 650, 750, 800);
echo '$pricesの値: ';
foreach ($prices as $price) {
  echo $price.' ';
}
echo '<br>';
echo '-----';
echo '<br>';

// この下にコードを書いてください
$totalprice = 0;
$maxprice=0;
foreach ($prices as $price) {
  $totalprice = $totalprice + $price;
if($price>$maxprice){
$maxprice=$price;
}
}
echo '合計金額は'.$totalprice.'円です';
echo '<br>';
echo '最高価格は'.$maxprice.'円です';
?>
```
```
<?php
$menu = array('name' => 'CURRY', 'price' => 900);
echo '$menuの値: ';
// var_exportは変数の中身を見るための関数です
var_export($menu);
echo '<br>';
echo '-----';
echo '<br>';

// この下にコードを書いてください
echo $menu["name"].'は'.$menu["price"].'円です';

?>
```
