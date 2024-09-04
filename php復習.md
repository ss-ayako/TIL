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

    $x = 99 * 99;
    $y = 77 * 77;

    // ここにif文を書いていきましょう
    if($x>9800){
      echo "変数xは9800より大きいです。";
    }
    if($y>6000){
      echo "変数yは6000より大きいです。";
    }
    
  ?>

</body>
</html>
```
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
    // $ageという変数に自分の年齢を代入してください
    $age = 38;
    if($age>30){
      echo "あなたは30歳以上です。";
    }else{
      echo "あなたは30歳未満です。";
    }
    
  ?>

</body>
</html>
```
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
  
    $x = 1071;
    
    // 以下にif-elseif-else文を書いてください
    if($x % 3 == 0&&$x % 7 == 0){
      echo "xは3の倍数かつ7の倍数です。";
    }elseif($x % 3 == 0){
      echo "xは3の倍数ですが7の倍数ではありません。";
    }elseif($x % 7 == 0){
      echo "xは7の倍数ですが3の倍数ではありません。";
    }else{
      echo"xは7の倍数でも3の倍数でもありません。";
    }
    
  ?>

</body>
</html>
```
- if, elseifによる分岐が多く複雑な場合、switch文で書き換えるとシンプルで読みやすいコードに
- caseブロックの最後にはbreak命令を指定します。
- break命令は現在のブロックから脱出するための命令です。
- break命令がないと、後ろに続くcaseブロックが続けて実行されてしまいます。
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

    // 変数$numを定義し、好きな数字を代入してください
    $num = 9;
  
    // 変数$remainderを定義し、変数$numを3で割った時の余りを代入してください
    $remainder = $num % 3;
 
    // switch文を用いてください
    switch($remainder){
      case 0:
        echo "大吉です。";
        break;
      case 1:
        echo "中吉です。";
        break;
      case 2:
        echo "小吉です。";
        break; 
      default:
        echo "凶です。";
        break; 
    }
  
  ?>

</body>
</html>
```
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

    // この下にfor文を書いてください
    for($i=1;$i<=1000;$i++) {
      if ($i>=501){
      break;
      }
      echo $i;
      echo'<br>';
    }
    
  ?>

</body>
</html>
```
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

    $str = 'progate';

    // strlenを用いて$strの長さをechoしてください
    echo strlen($str);
    
    echo '<br>';
    
    $array = array('HTML', 'CSS', 'PHP');

    // countを用いて$arrayの要素数をechoしてください
    echo count($array);
    
    echo '<br>';
    
    // randを用いて10から15までのランダムな数字をechoしてください
    echo rand(10,15);
    
  ?>

</body>
</html>
```
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

    // 関数helloを定義してください
    function hello(){
      echo "Hello, world!";
    }
    
    // 関数helloを呼び出してください
    hello();
    
    echo '<br>';
    // 関数printRectangleAreaを定義してください
     function printRectangleArea($height,$width){
      echo $height*$width;
    }
    
    // 引数を(5, 10)としてprintRectangleAreaを呼び出してください
    printRectangleArea(5,10);
    
  ?>

</body>
</html>
```
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

    // 関数getCircleAreaを定義してください
    function getCircleArea($radius){
      return $radius * $radius * 3;
    }
    
    // 関数getCircleAreaを呼び出して、戻り値を変数$circleAreaに代入してください
    $circleArea = getCircleArea(5);
    
    // $circleAreaをechoしてください
    echo $circleArea;
    
  ?>

</body>
</html>
```
```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Progate</title>
  <link rel="stylesheet" type="text/css" href="stylesheet.css">
</head>
<body>
  <div class="header">
    <div class="header-left">Progate</div>
    <div class="header-right">
      <ul>
        <li>会社概要</li>
        <li>採用</li>
        <li class="selected">お問い合わせ</li>
      </ul>
    </div>
  </div>

  <div class="main">
    <div class="contact-form">
      <div class="form-title">お問い合わせ</div>
      <form method="post" action="sent.php">
        <div class="form-item">名前</div>
        <!-- この下にinputタグを書いていきましょう -->
        <input type ="text" name ="name">
        
        <div class="form-item">内容</div>
        <!-- この下にtextareaタグを書いていきましょう -->
        <textarea name ="body"></textarea>
        
      </form>
    </div>
  </div>
  
  <div class="footer">
    <div class="footer-left">
      <ul>
        <li>会社概要</li>
        <li>採用</li>
        <li>お問い合わせ</li>
      </ul>
    </div>
    <div class="like-box">
      <iframe src="https://www.facebook.com/plugins/likebox.php?href=https%3A%2F%2Fwww.facebook.com%2Fpages%2FProgate%2F742679992421539&amp;show_faces=false" scrolling="no" frameborder="0" style="border:none; overflow:hidden; height:300px;" allowTransparency="true"></iframe>
    </div>
  </div>
</body>
</html>
```
```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Progate</title>
  <link rel="stylesheet" type="text/css" href="stylesheet.css">
</head>
<body>
  <div class="header">
    <div class="header-left">Progate</div>
    <div class="header-right">
      <ul>
        <li>会社概要</li>
        <li>採用</li>
        <li class="selected">お問い合わせ</li>
      </ul>
    </div>
  </div>

  <div class="main">
    <div class="thanks-message">お問い合わせいただきありがとうございます。</div>
    <div class="display-contact">

      <div class="form-title">入力内容</div>

      <div class="form-item">■ 名前</div>
      <!-- nameを受け取りechoしましょう -->
       <?php echo $_POST['name']; ?>
      <div class="form-item">■ 内容</div>
      <!-- bodyを受け取りechoしましょう -->
      <?php echo $_POST['body']; ?>
    </div>

  </div>

  <div class="footer">
    <div class="footer-left">
      <ul>
        <li>会社概要</li>
        <li>採用</li>
        <li>お問い合わせ</li>
      </ul>
    </div>
    <div class="like-box">
      <iframe src="https://www.facebook.com/plugins/likebox.php?href=https%3A%2F%2Fwww.facebook.com%2Fpages%2FProgate%2F742679992421539" scrolling="no" frameborder="0" style="border:none; overflow:hidden; height:300px;" allowTransparency="true"></iframe>
    </div>
  </div>
</body>
</html>
```
- phpだから＜？php？＞が必要だった、、、
```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Progate</title>
  <link rel="stylesheet" type="text/css" href="stylesheet.css">
</head>
<body>
  <div class="header">
    <div class="header-left">Progate</div>
    <div class="header-right">
      <ul>
        <li>会社概要</li>
        <li>採用</li>
        <li class="selected">お問い合わせ</li>
      </ul>
    </div>
  </div>

  <div class="main">
    <div class="contact-form">
      <div class="form-title">お問い合わせ</div>
      <form method="post" action="sent.php">
        <div class="form-item">名前</div>
        <input type="text" name="name">

        <div class="form-item">年齢</div>
        <!-- この下にselectタグを書いていきましょう -->
        <select name= "age">
          <option value = "未選択">選択してください</option>
          <option value = "20代">20代</option>
          <option value = "30代">30代</option>
        </select>
        
        <div class="form-item">内容</div>
        <textarea name="body"></textarea>

        <input type="submit" value="送信">
      </form>
    </div>
  </div>
  
  <div class="footer">
    <div class="footer-left">
      <ul>
        <li>会社概要</li>
        <li>採用</li>
        <li>お問い合わせ</li>
      </ul>
    </div>
    <div class="like-box">
      <iframe src="https://www.facebook.com/plugins/likebox.php?href=https%3A%2F%2Fwww.facebook.com%2Fpages%2FProgate%2F742679992421539&amp;show_faces=false" scrolling="no" frameborder="0" style="border:none; overflow:hidden; height:300px;" allowTransparency="true"></iframe>
    </div>
  </div>
</body>
</html>
```
