表示させる
```
<?php
echo "Hello, PHP";
echo'<br>';
echo "10 + 7";
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
echo "My name is {$name}";

?>
```
- 変数$priceと$taxRateから税込価格を求めて、税込価格は○○円ですと出力してください。
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
$kakaku= $price + $price * $taxRate;
echo '税込価格は'.$kakaku.'円です';

?>
```
- 変数$moneyには所持金が代入されています。
- 次に所持金と求めた税込価格の比較結果に応じて、文字列を出力してみましょう。

-以下のように出力してください。
・所持金が税込価格より大きい場合、
商品を買うことができます

・両方の値が等しい場合、
商品を買うことができますが、所持金がなくなります

・所持金が税込価格より小さい場合、
商品を買うことができません

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
$kakaku = $price + $price * $taxRate;

if ($money>$kakaku){
  echo "商品を買うことができます";
}else if($money===$kakaku){
 echo "商品を買うことができますが、所持金がなくなります";
}else{
  echo "商品を買うことができません";
}
?>
```
- 「$i が 3 の倍数かつ 5 の倍数」の条件を最初にチェックしないと、正しく動作しません。
- このコードじゃダメ。
```
<?php
for($i=1;$i<=100;$i++){
  
  if($i % 3 == 0){
    echo 'Fizz';
    echo '<br>'; 
  }elseif($i % 5 == 0){
    echo 'Buzz';
    echo '<br>'; 
  }elseif($i % 3 == 0 && $i % 5 == 0){
    echo 'FizzBuzz';
    echo '<br>'; 
  }else{
   echo $i;
   echo '<br>'; 
  }
}
?>
```
- これが正解！！
```
<?php
for($i=1;$i<=100;$i++){
  
  if($i % 3 == 0 && $i % 5 == 0){
    echo 'FizzBuzz';
 
  }elseif($i % 5 == 0){
    echo 'Buzz';
  
  }elseif($i % 3 == 0){
    echo 'Fizz';
  
  }else{
   echo $i;
 
  }            
 echo '<br>';            
 }
?>
```
