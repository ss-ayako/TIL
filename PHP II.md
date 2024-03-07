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
$curry->name = 'CURRY';
$pasta->name = 'PASTA';
$curry->hello();
echo '<br>';
$pasta->hello();

?>
```
***
