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

