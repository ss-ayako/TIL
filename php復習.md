```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Progate</title>
  <link rel="stylesheet" type="text/css" href="stylesheet.css">
</head>
<body>

  <?php

    $x = 5;
    $y = 2;
    $a = 8;
    $b = 4;
    
  ?>

  <!-- この下で$xの計算をしていきましょう -->
  <?php
    $x = $x + 10;
    echo $x;
  ?>

  <br>

  <!-- この下で$yの計算をしていきましょう -->
  <?php
    $y = $y * 5;
    echo $y;
    
  ?>

  <br>

  <!-- この下で$aの計算をしていきましょう -->
  <?php
    $a = $a + 1;
    echo $a;
    
  ?>

  <br>
  
  <!-- この下で$bの計算をしていきましょう -->
  <?php
    $b = $b - 1;
    echo $b;
    
    
  ?>

</body>
</html>
```
- 「.=」を用いると変数と文字列の連結を省略して書くことが出来ます。
- ダブルクォーテーションで文字列を囲んだ場合、中の変数を{}で囲むとその部分が変数に入っている値で置き換えられます(変数展開)。
- シングルクォーテーションで文字列を囲んだ場合は変数展開されず、変数が{}で囲まれていてもそのまま文字列としてみなされます。
```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Progate</title>
  <link rel="stylesheet" type="text/css" href="stylesheet.css">
</head>
<body>

  <?php
    $name = 'にんじゃわんこ';
    // 'こんにちは！'という文字列と$nameを連結してechoしてください
    echo "こんにちは！{$name}";
    
  ?>

</body>
</html>
```
