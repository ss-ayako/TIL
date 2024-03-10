個々のインスタンスがもつデータ（プロパティ）ではなく、クラスがもつデータをクラスプロパティ 「static」を用いて定義  
クラスプロパティにアクセスする場合は「クラス名::$クラスプロパティ名」のように「::」（コロン「:」２つ）を用いる 
```
// $countというpublicなクラスプロパティを、初期値を数値の4として定義してください
  public static $count = 4;

// menu.phpを読み込んでください
require_once('menu.php');

<!-- Menuクラスのクラスプロパティ$countを表示してください -->
    <h3>メニュー<?php echo Menu::$count?>品</h3>
```
***
インスタンスが生成されるたびにコントラスタが呼び出されるので・・・  
$countの初期値を0として、  
コンストラクタ内でクラスプロパティ$countの値に1を足すことで、  
生成されたインスタンスの数（メニュー数）を数えることができる  
***
クラス内でクラスプロパティにアクセスする際は「self」という特殊な変数を使う  
selfは、クラスの中で使うとそのクラス自身のことを指し示し、  
「self::$クラスプロパティ名」のように使う（$の位置に気をつけてください）  
***
$countのアクセス権をprivateに  
クラスの外から$countにアクセスできなくなるので$countのゲッターを定義  
$countのゲッターのように、個々のインスタンスのデータに関係ない処理を行いたい時には「クラスメソッド」を使う  
クラスメソッドは「static」を用いて定義、「クラス名::クラスメソッド名」  
***
```
// クラスプロパティ$countのアクセス権をprivateに、初期値を数値の0にしてください
  private static $count = 0;

// クラスプロパティcountの値に1を足してください
    self ::$count++;

// getCountというクラスメソッドを追加してください
  public static function getCount(){
     return self::$count;
  }

<!-- Menuクラスに対してgetCountメソッドを呼び出して、クラスプロパティ$countを表示してください -->
    <h3>メニュー<?php echo Menu::getCount() ?>品</h3>
```
***
すでに定義されているクラスのプロパティやメソッドを別のクラスに引き継ぐことを「継承」  
引き継がれる元のクラスを「親クラス」、継承してできる新しいクラスを「子クラス」と呼ぶ  
継承を用いて新しく子クラスを定義するとき「extends」を用いて「class 子クラス名 extends 親クラス名」と記述する  
子クラスにメソッドが定義されている場合にはそのメソッドが、定義されていない場合には親クラスのメソッドが呼び出し  
***
```
<?php 
require_once('menu.php');

class Drink extends Menu { //ここでクラスの継承を表しています。Drink クラスが Menu クラスを継承している
  // $typeというprivateなプロパティを定義してください
  private $type;
  
  // getTypeメソッドを定義してください
  public function getType() {
    return $this->type;
  }
  // setTypeメソッドを定義してください
 public function setType($type) {
    $this->type = $type;
  } 
  
}

?>
```
***
