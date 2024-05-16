```<?php
class Menu {
  public $name;
  
  public function hello() {

    echo '私は'.$this->name.'です'; // '私は○○です'とecho,○○には$thisを用いてnameプロパティ
    //$thisはメソッドが呼ばれた時に、そのメソッドを呼び出しているインスタンスに置き換えられる
  }
}

$curry = new Menu();
$pasta = new Menu();
$curry->name = 'CURRY';
$pasta->name = 'PASTA';
$curry->hello();
echo '<br>';
$pasta->hello();

?>
```
***
```
<?php
class Menu {
  public $name;
  
  // コンストラクタを定義してください
  public function __construct(){  // コンストラクタを定義
    echo '１つのメニューが作られました';
  }
  
  public function hello() {
    echo '私は'.$this->name.'です';
  }
}

$curry = new Menu();//生成したインスタンスを変数$curry に代入,上に記述したコンストラクタが実行される
echo '<br>';
$pasta = new Menu();//生成したインスタンスを変数$pasta に代入,上に記述したコンストラクタが実行される
echo '<br>';
$curry->name = 'CURRY';// $curryのnameプロパティに'CURRY'を代入
$pasta->name = 'PASTA';// $curryのnameプロパティに'PASTA'を代入
$curry->hello();// $curryに対してhelloメソッドを呼び出し
echo '<br>';
$pasta->hello();// $pastaに対してhelloメソッドを呼び出し

?>
```
***
```
<?php
class Menu {
  public $name;
  
  public function __construct($name) {
    $this->name = $name;
  }
  
  public function hello() {
    echo '私は'.$this->name.'です';
  }
}

$curry = new Menu('CURRY');//Menu クラスの新しいインスタンスが生成。$curry という変数には、新しく生成された Menu クラスのインスタンスが代入。'CURRY' はコンストラクタに渡され、$name プロパティが 'CURRY' に設定.
$pasta = new Menu('PASTA');

?>


<p><?php echo $curry->name ?></p> //<p>タグの中で、$curryのnameプロパティを表示-->


<p><?php echo $pasta->name ?></p> //<p>タグの中で、$pastaのnameプロパティを表示-->
```
***
phpコードが埋め込まれている例  
```<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Embedded in HTML</title>
</head>
<body>

    <h1><?php echo "Hello, World!"; ?></h1>

</body>
</html>
```
HTML内にPHPコードを埋め込む場合、PHPコードが実行される位置に<?phpと?>で挟まれたタグが必要  
***
```
// 配列の中に上記の4つのインスタンスを順に入れて、変数$menusに代入してください
$menus=array($juice,$coffee,$curry,$pasta);
```
***
```
<!-- 配列$menusの要素を変数$menuとするforeach文を書いてください -->
     <?php foreach ($menus as $menu):?> 
     <h3><?php echo $menu->name ?></h3>
     <?php endforeach ?>
```
***
コードが長くなったら分ける  
```
<?php require_once('menu.php');
?>
// menu.phpを読み込み
```
読み込んだファイルで定義されているクラスや変数を、require_onceを記述したファイル内で使うことができる  
***
画像を表示するには、htmlタグにPHPを埋め込んで画像を表示  
echoをしないとphpの処理の結果が出力  
```
<img src="<?php echo $menu->image?>">
```  
  
Menuクラスに、・$price・$imageというプロパティを定義  
コンストラクタでプロパティの値をセットできるように,引数に$price, $imageを追加  
```
<?php
class Menu {
  public $name;
  // $priceというプロパティを定義してください
  public $price;
  // $imageというプロパティを定義してください
   public $image;
  
  // コンストラクタの引数に$price, $imageを追加してください
  public function __construct($name, $price, $image) {
    $this->name = $name;
    $this->price = $price;
    $this->image = $image;
   }
}
?>
```  
  
インスタンス生成時にpriceプロパティとimageプロパティをセット  
```
<?php
require_once('menu.php');

// それぞれpriceとimageを追加してください
$juice = new Menu('JUICE',600,'https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/php/juice.png');
$coffee = new Menu('COFFEE',500,'https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/php/coffee.png');
$curry = new Menu('CURRY',900,'https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/php/curry.png');
$pasta = new Menu('PASTA',1200,'https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/php/pasta.png');

$menus = array($juice, $coffee, $curry, $pasta);
?>
```
***
```
<?php
class Menu {
  public $name;
  public $price;
  public $image;
  //プロパティの定義
  
  public function __construct($name, $price, $image) {
    //__construct は新しいインスタンスが作成される際に呼び出し
    $this->name = $name;
    $this->price = $price;
    $this->image = $image;
  }
  //Menu クラスのインスタンスを生成する際に、
  //名前 ($name)、価格 ($price)、画像 ($image) を指定して初期化
  //$this は現在のインスタンスを指す。
  //これにより、新しく生成されるインスタンスの name, price, image プロパティが、
  //コンストラクタのパラメータで指定された値で初期化
  
  // getTaxIncludedPriceメソッドを定義してください
   public function getTaxIncludedPrice() {
     return floor($this->price * 1.08);
     //だからここも、$priceではなく$this->$price
   }
  //$price だけでは変数として解釈され、クラス内のプロパティ price として認識されない。
  //そのため、$this->price としてクラスのプロパティにアクセス。
}
?>


//$menuのgetTaxIncludedPriceメソッドの戻り値を表示してください -->
<p class="price">¥<?php echo $menu->getTaxIncludedPrice() ?>（税込）</p>

```
***
```
floor関数を使うと、小数点以下を切り捨てた値が得られます。
echo floor(1.5);
// 結果=> 1

priceプロパティに1.08を掛けたものを、小数点以下を切り捨てて、戻り値とするには以下のようにします。
return floor(priceプロパティ * 1.08);
```
***
パソコンの回路などはパソコンの内部に隠されており、ユーザーはキーボードなどの限られた部分しか操作することができない。  
回路を隠す（カプセル化をする）と回路に触れてパソコンを壊してしまう危険を回避できる。  
プログラミングでもこのような「カプセル化」という仕組みがある。  
自分がクラスを作る際には、他の人がそのクラスを使いやすいように、  
その人に使ってほしい機能（料金を取得する機能）は公開し、クラスの外で使ってほしくない機能（料金を直接変更する機能）は隠す。  
使える機能を制限することで他の人はどの機能を使えばいいかが分かりやすく、また、安全にクラスを利用することができる。  
***
```
<?php
class Menu {
  // name, price, imageプロパティのアクセス権をprivateにしてください
  private $name;  // 変更前 public $name;
  private $price; // 変更前 public $price;
  private $image; // 変更前 public $image;
  
  public function __construct($name, $price, $image) {
    $this->name = $name;
    $this->price = $price;
    $this->image = $image;
  }
  //プロパティのアクセス権をprivateにすると
  //プロパティの値をクラスの外から取り出すことができない。
  //プロパティの値を返すだけのメソッドを定義する。
  
  //プロパティの値を返すだけのメソッドを特に「ゲッター」
  //ゲッターは「getプロパティ名」のように命名
  
  // getNameメソッドを定義してください
  public function getName() {
    return $this->name;
  }
  
  // getImageメソッドを定義してください
  public function getImage() {
    return $this->image;
  }
  
  public function getTaxIncludedPrice() {
    return floor($this->price * 1.08);
  }
  
}
?>



//imageプロパティのゲッターを用いて以下を書き換えてください -->
          <img src="<?php echo $menu->getImage(); ?>" class="menu-item-image">
//nameプロパティのゲッターを用いて以下を書き換えてください -->
          <h3 class="menu-item-name"><?php echo $menu->getName(); ?></h3>
```
***
プロパティのアクセス権をprivateにするとプロパティの値をクラスの外から変更できない。  
そこで、プロパティの値を変更するメソッドを定義  
ロパティの値を変更するメソッドを特に「セッター」  
セッターは「setプロパティ名」のように命名  
***
```
<?php
class Menu {
  private $name;
  private $price;
  private $image;


  // 1.$orderCountというプロパティを定義してください。ただし、初期値を数値の0としてください。
  private $orderCount = 0; 
  
  public function __construct($name, $price, $image) {
    $this->name = $name;
    $this->price = $price;
    $this->image = $image;
  }
  
  public function getName() {
    return $this->name;
  }
  
  public function getImage() {
    return $this->image;
  }
  
  // 2.getOrderCountメソッドを定義してください
  public function getOrderCount() {
    return $this->orderCount;
  }
  
  // 3.setOrderCountメソッドを定義してください
   public function setOrderCount($orderCount) {
    $this->orderCount = $orderCount;
  }
  
  public function getTaxIncludedPrice() {
    return floor($this->price * 1.08);
  }
  
}
?>


// $juiceに対して数値の2を引数としてsetOrderCountメソッドを呼び出してください
$juice->setOrderCount(2);

// $menuのゲッターを用いてorderCountプロパティを表示してください -->
  <p>注文数: <?php echo $menu->getOrderCount() ?></p>
```
***
```
<?php require_once('data.php') ?>

<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Café Progate</title>
  <link rel="stylesheet" type="text/css" href="stylesheet.css">
  <link href='https://fonts.googleapis.com/css?family=Pacifico|Lato' rel='stylesheet' type='text/css'>
</head>
<body>
  <div class="menu-wrapper container">
    <h1 class="logo">Café Progate</h1>
    
    <!-- ここに<form>の開始タグを書いてください -->
**<form method="post" action="confirm.php">**
     <!-- ・<form>タグを作成してください。
・action属性をconfirm.phpに指定してください。
・method属性をpostに指定してください。
・閉じタグをコメントで指定してある場所に書いてください。 -->

      <div class="menu-items">
        <?php foreach ($menus as $menu): ?>
          <div class="menu-item">
            <img src="<?php echo $menu->getImage() ?>" class="menu-item-image">
            <h3 class="menu-item-name"><?php echo $menu->getName() ?></h3>
            <p class="price">¥<?php echo $menu->getTaxIncludedPrice() ?>（税込）</p>
            
            <!-- <input>タグを用いて入力ボックスを作成してください  -->
<input type ="text" name ="<?php echo $menu->getName() ?>" value =0>個数入れる入力ボックス
             <!--foreach文の中で、
・<input>タグを作成してください。
・type属性に「text」を指定してください。
・value属性に0をいれてください。
・name属性に、$menuのゲッターを用いてnameプロパティを表示してください。-->
メニューごとに数量を入力するための <input> タグ、名前属性はメニューの名前に対応しています。
            
            <span>個</span>
          </div>
        <?php endforeach ?>
      </div>
      <!-- <input>タグを用いて送信ボタンを作成してください  -->
**<input type ="submit" value ="注文する">**
      <!--foreach文の外で、
・<input>タグを作成してください。
・type属性に「submit」を指定してください。
・value属性に注文するを指定してください。-->

    <!-- ここで<form>の閉じタグを書いてください -->
    </form>
  </div>
</body>
</html>
```
***
```
<!-- ここでdata.phpを読み込んでください  -->
<?php require_once('data.php') ?>

<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Progate</title>
  <link rel="stylesheet" type="text/css" href="stylesheet.css">
  <link href='https://fonts.googleapis.com/css?family=Pacifico|Lato' rel='stylesheet' type='text/css'>
</head>
<body>
  <div class="order-wrapper">
    <h2>注文内容確認</h2>
    <?php foreach ($menus as $menu): ?>
      <!-- 変数$orderCountに$_POSTで受け取った値を代入してください -->
      <?php $orderCount = $_POST[$menu->getName()] ?>nameってあるけど個数。ここで定義したものを
      <p class="order-amount">
        <!-- ここに、$menuのゲッターを用いてnameプロパティを表示してください -->
        <?php echo $menu->getName() ?>
        x
        <!-- ここに、$orderCountを表示してください -->
        <?php echo $orderCount ?>ここで呼び出し
        個
      </p>
    <?php endforeach ?>
  </div>
</body>
</html>
```
***
```
// getTotalPriceメソッドを定義してください
  public function getTotalPrice() {
    return $this->getTaxIncludedPrice()*$this->orderCount;
  }


<?php require_once('data.php') ?>

<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Progate</title>
  <link rel="stylesheet" type="text/css" href="stylesheet.css">
  <link href='https://fonts.googleapis.com/css?family=Pacifico|Lato' rel='stylesheet' type='text/css'>
</head>
<body>
  <div class="order-wrapper">
    <h2>注文内容確認</h2>
    <?php foreach ($menus as $menu): ?>
      <?php 
        $orderCount = $_POST[$menu->getName()];
        // $menuに対して、$orderCountを引数としてsetOrderCountメソッドを呼び出してください
        $menu->setOrderCount($orderCount);
        
      ?>
      <p class="order-amount">
        <?php echo $menu->getName() ?>
        x
        <?php echo $orderCount ?>
        個
      </p>
      <!-- $menuに対してgetTotalPriceメソッドを呼び出して、金額を表示してください -->
      <p class="order-price"><?php echo $menu->getTotalPrice()?>円</p>
    <?php endforeach ?>
  </div>
</body>
</html>
```
<?php require_once('data.php') ?>

<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Progate</title>
  <link rel="stylesheet" type="text/css" href="stylesheet.css">
  <link href='https://fonts.googleapis.com/css?family=Pacifico|Lato' rel='stylesheet' type='text/css'>
</head>
<body>
  <div class="order-wrapper">
    <h2>注文内容確認</h2>
    <!-- 変数$totalPaymentを定義し、数値の0を代入してください -->
    <?php $totalPayment=0?>
    
    <?php foreach ($menus as $menu): ?>
      <?php 
        $orderCount = $_POST[$menu->getName()];
        $menu->setOrderCount($orderCount);
        // $totalPaymentに、$menuのgetTotalPriceメソッドで得た値を足してください
        $totalPayment += $menu->getTotalPrice()
        //このコードは複数のメニューが存在する場合、各メニューの合計金額を計算し、その合計金額を $totalPayment に加算していくことで、最終的な注文の合計金額を得る
        
      ?>
      <p class="order-amount">
        <?php echo $menu->getName() ?>
        x
        <?php echo $orderCount ?>
        個
      </p>
      <p class="order-price"><?php echo $menu->getTotalPrice() ?>円</p>
    <?php endforeach ?>
    <!-- $totalPaymentを表示してください -->
    <h3>合計金額: <?php echo $totalPayment?>円</h3>
  </div>
</body>
</html>
***
