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
