$menu->getName()によってnameプロパティを表示している部分を、<a>タグで囲んで,  
メニューの名前部分をクリックしてうまくページが変わるように  
```
<!-- 以下の1行をaタグで囲んでください -->
 <a href='show.php'><?php echo $menu->getName() ?><a>
```
これでshow.phpへのリンクを作成  
どのメニューの名前をクリックしてもshow.phpに飛ぶけど、どのメニューがクリックされたかわからないので、
どのメニューの詳細を表示するべきかわからない。そこでshow.phpにどのメニューがクリックされたかの情報を渡す必要がある  
***
URLの末尾の「?」以降に「キー名=値」の形で簡単な情報をのせる。  
これをクエリ情報といい、クエリ情報を用いてリンク先のページに情報を渡す（送信する）ことができる  

```<a href="show.php?name=<?php echo $menu->getName() ?>">```

<a> タグ: ハイパーリンク。指定された URL に移動  
href="show.php?name=<?php echo $menu->getName() ?>": href 属性には、リンク先の URL が指定。動的なデータを含む URL を生成。  
show.php: リンク先のページのファイル名が show.php 。  
?name=<?php echo $menu->getName() ?>: クエリ文字列。? 以降にキーと値がセット. name キーに、$menu->getName() で得たメニューの名前が設定。  
<?php echo $menu->getName() ?>: 動的にメニューの名前を取得。リンク先のページで特定のメニューの詳細を表示する際、そのメニューの名前引き継ぐ。  
***
nameプロパティの値を用いて、配列$menusから特定のMenuインスタンスを取得するクラスメソッド（findByNameメソッド）を作成  

```// findByNameというクラスメソッドを定義してください
  public static function findByName($menus,$name){  //配列$menusと、検索するメニュー名 $name を受け取り
    foreach($menus as $menu)    //配列$menus の各要素が順番に $name に代入
    if($menu->getName()==$name){   //$menuのnameプロパティと引数の$nameを比較して、同じ値なら
      return $menu;   //その$menuをreturn
    }
  }


// Menuクラスに対してfindByNameというクラスメソッドを呼び出してください
$menu = Menu::findByName($menus,$menuName);
```
***
```
<?php
// Reviewクラスを定義してください
class Review {
private $menuName;//プロパティを定義
private $body;//プロパティを定義

public function __construct($menuName,$body) { //コンストラクタを定義
  $this->menuName = $menuName; //menuNameプロパティに引数の値をセット
  $this->body = $body; //bodyプロパティに引数の値をセット
}
public function getMenuName() { //menuNameプロパティのゲッター（getMenuName）を定義
  return $this->menuName;
}
public function getBody() { //menuNameプロパティのゲッター（getMenuName）を定義
  return $this->body;
}
}
?>
```
***
```
<?php
require_once('drink.php');
require_once('food.php');
// review.phpを読み込んでください
require_once('review.php');

$juice = new Drink('JUICE', 600, 'https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/php/juice.png', 'アイス');
$coffee = new Drink('COFFEE', 500, 'https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/php/coffee.png', 'ホット');
$curry = new Food('CURRY', 900, 'https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/php/curry.png', 3);
$pasta = new Food('PASTA', 1200, 'https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/php/pasta.png', 1);

$menus = array($juice, $coffee, $curry, $pasta);
//2つのReviewクラスのインスタンスを生成して、変数$review1, 変数$review2に代入
// 変数$review1にReviewクラスのインスタンスを代入してください
$review1 = new Review($juice->getName(),"果肉たっぷりのオレンジジュースです！");
//$review1
//1つ目の引数: $juiceのnameプロパティ（ゲッターで取得する）
//2つ目の引数: 果肉たっぷりのオレンジジュースです！
// 変数$review2にReviewクラスのインスタンスを代入してください
$review2 = new Review($curry->getName(),"具がゴロゴロしていてとてもおいしいです");
//・$review2
//1つ目の引数: $curryのnameプロパティ（ゲッターで取得する）
//2つ目の引数: 具がゴロゴロしていてとてもおいしいです

// 変数$reviewsに$review1と$review2を要素とする配列を代入してください
$reviews = array($review1,$review2)

?>
```
***
```
<!-- foreach文を書いてください -->
        <?php foreach($reviews as $review): ?>
  　<h3><?php echo $review->getMenuName() ?></h3>
  　<!--<h3>タグを用意して、その中に$reviewのmenuNameプロパティを表示-->
  　<p><?php echo $review->getBody() ?></p>
  　<!--<p>タグを用意して、その中に$reviewのbodyプロパティを表示-->
<?php endforeach ?>
```
***
```
// getReviewsメソッドを定義してください
  public function getReviews($reviews) {  //getReviewsメソッドを定義,引数を$reviewsとする
  $reviewsForMenu=array();  //変数$reviewsForMenuに空の配列を代入
  foreach($reviews as $review){  //$reviewsの要素を変数$reviewとするforeach文
  if($review->getMenuName()==$this->name){//$reviewのmenuNameプロパティと、インスタンス自身($this)のnameプロパティを比較
  $reviewsForMenu[]=$review;  //trueであるなら、$reviewsForMenuに$reviewを追加
  }
  }
  return $reviewsForMenu;  //foreach文が終了した後、$reviewsForMenuをreturn
  }


// $menuに対して$reviewsを引数としてgetReviewsメソッドを呼び出して、戻り値を変数$menuReviewsに代入してください
$menuReviews=$menu->getReviews($reviews)
  ```
***
```
コンストラクタを定義するには、以下のようにします。
 public function __construct(引数) {
  $this->プロパティ = 引数;
 }
```
***
```
<?php
// Userクラスを定義してください
class User {
  private $name; //privateなプロパティを定義
  private $gender; //privateなプロパティを定義
  
  public function __construct($name, $gender) {    //コンストラクタを定義
    $this->name = $name;
    $this->gender = $gender;
    //引数を$name, $genderとする
    //nameプロパティとgenderプロパティに引数の値をセットする
  }

  //クラス内のプロパティの値を外部から取得するためゲッター定義する
  public function getName() { //nameプロパティのゲッター（getName）を定義
 return $this->name;
 }
  public function getGender() { //genderプロパティのゲッター（getGender）を定義
 return $this->gender;
 }
}
?>
```
