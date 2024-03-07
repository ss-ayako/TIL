```<?php
class Menu {
  public $name;
  
  public function hello() {
    // '私は○○です'とechoしてください
    echo '私は'.$this->name.'です';// '私は○○です'とecho,○○には$thisを用いてnameプロパティ
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
