```
body {
  font-family: "Avenir Next";
}

/* headerの背景色を#f7f2b4、高さを90pxにしてください */
 .header{
   background-color:#f7f2b4;
   height:90px;
 }

/* mainの背景色を#bdf7f1、高さを600pxにしてください */
 .main{
   background-color:#bdf7f1;
    height:600px;
 }

/* footerの背景色を#ceccf3、高さを270pxにしてください */
 .footer{
   background-color:#ceccf3;
    height:270px;
 }
```
```
body {
  font-family: "Avenir Next";
}

/* list-styleプロパティを用いて、<li>要素の黒点を取り除いてください */
.header-list{
  list-style: none;
}

.header {
  background-color: #f7f2b4;
  height: 90px;
}

.main {
  background-color: #bdf7f1;
  height: 600px;
}

.footer {
  background-color: #ceccf3;
  height: 270px;
}
```
```
body {
  font-family: "Avenir Next";
}

li {
  list-style: none;
  float: left;
  /* 上下のpaddingを33px、左右のpaddingを20pxにしてください */
  padding:33px 20px;
  
}

.header {
  background-color: #26d0c9;
  color: #fff;
  height: 90px;
}

.header-logo {
  float: left;
  font-size: 36px;
  /* 上下のpaddingを20px、左右のpaddingを40pxにしてください */
   padding:20px 40px;
  
}

.main {
  background-color: #bdf7f1;
  height: 600px;
}

.footer {
  background-color: #ceccf3;
  height: 270px;
}

```
```
body {
  font-family: "Avenir Next";
}

li {
  list-style: none;
  /* 以下の2行を削除してください */
  
}

.header {
  background-color: #26d0c9;
  color: #fff;
  height: 90px;
}

.header-logo {
  float: left;
  font-size: 36px;
  padding: 20px 40px;
}

/* header-listの中のli要素にのみ適用したいCSSを記述してください */
.header-list li{
  float: left;
  padding: 33px 20px;
}

.main {
  background-color: #bdf7f1;
  height: 600px;
}

.footer {
  background-color: #ceccf3;
  height: 270px;
}
```
```
body {
  font-family: "Avenir Next";
}

li {
  list-style: none;
}

.header {
  background-color: #26d0c9;
  color: #fff;
  height: 90px;
}

.header-logo {
  float: left;
  font-size: 36px;
  padding: 20px 40px;
}

.header-list li {
  float: left;
  padding: 33px 20px;
}

.main {
  background-color: #bdf7f1;
  height: 600px;
}

.footer {
  /* background-colorを#2f5167に変更してください */
  background-color: #2f5167;
  
  /* colorを#fffにしてください */
  color: #fff;
  
  /* heightを120pxに変更してください */
  height: 120px;
  /* 上下左右のpaddingを40pxにしてください */
  padding: 40px;
  
}

/* footer-logoのfont-sizeとfloatを指定してください */
.footer-logo{
   font-size:32px;
    float:left;
}

/* footer-listのfloatを指定してください */
.footer-list {
float:right;
}
/* footer-listの中のli要素のpadding-bottomを指定してください */
.footer-list li{
  padding-bottom:20px;
}
```
```
body {
  font-family: "Avenir Next";
}

li {
  list-style: none;
}

.header {
  background-color: #26d0c9;
  color: #fff;
  height: 90px;
}

.header-logo {
  float: left;
  font-size: 36px;
  padding: 20px 40px;
}

.header-list li {
  float: left;
  padding: 33px 20px;
}

.main {
  /* background-colorの指定を消してください */
  
  /* heightの指定を消してください */
  
  /* 上下のpaddingを100px、左右のpaddingを80pxにしてください */
  padding: 100px 80px;
  
}

/* copy-containerの中のh1のfont-sizeを指定してください */
.copy-container h1{
font-size:140px;
}
/* copy-containerの中のh2のfont-sizeを指定してください */
.copy-container h2{
  font-size:60px;
}
/* copy-containerの中のspanの色を指定してください */
.copy-container span{
  color:#ff4a4a;
}

.footer {
  background-color: #2f5167;
  color: #fff;
  height: 120px;
  padding: 40px;
}

.footer-logo {
  float: left;
  font-size: 32px;
}

.footer-list {
  float: right;
}

.footer-list li {
  padding-bottom: 20px;
}

```
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Progate</title>
    <link rel="stylesheet" href="stylesheet.css">
  </head>
  <body>
    <div class="header">
      <div class="header-logo">Progate</div>
      <div class="header-list">
        <ul>
          <li>プログラミングとは</li>
          <li>学べるレッスン</li>
          <li>お問い合わせ</li>
        </ul>
      </div>
    </div>

    <div class="main">
      <div class="copy-container">
        <h1>HELLO WORLD<span>.</span></h1>
        <h2>プログラミングの世界へようこそ</h2>
      </div>
      
      <div class="contents">
        <!-- <h3>要素を追加してください -->
        <h3>学べるレッスン</h3>
        
        <!-- <div>要素を追加し、「contents-item」というclassをつけてください -->
        <div class="contents-item">
          <img src="https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/html/study/html.svg">
          <p>HTML & CSS</p>
          </div>
        
        <!-- <div>要素を追加し、「contents-item」というclassをつけてください -->
         <div class="contents-item">
           <img src="https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/html/study/php.svg">
           <p>PHP</p>
           </div>
        
        <!-- <div>要素を追加し、「contents-item」というclassをつけてください -->
        <div class="contents-item">
          <img src="https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/html/study/ruby.svg">
        <p>Ruby</p>
        </div>
        
        <!-- <div>要素を追加し、「contents-item」というclassをつけてください -->
        <div class="contents-item">
          <img src="https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/html/study/swift.svg">
        <p>Swift</p>
        </div>
        
      </div>
      
      <div class="contact-form">
        
      </div>
    </div>

    <div class="footer">
      <div class="footer-logo">Progate</div>
      <div class="footer-list">
        <ul>
          <li>会社概要</li>
          <li>採用</li>
          <li>お問い合わせ</li>
        </ul>
      </div>
    </div>
  </body>
</html>
```
```
body {
  font-family: "Avenir Next";
}

li {
  list-style: none;
}

.header {
  background-color: #26d0c9;
  color: #fff;
  height: 90px;
}

.header-logo {
  float: left;
  font-size: 36px;
  padding: 20px 40px;
}

.header-list li {
  float: left;
  padding: 33px 20px;
}

.main {
  padding: 100px 80px;
}

.copy-container h1 {
  font-size: 140px;
}

.copy-container h2 {
  font-size: 60px;
}

.copy-container span {
  color: #ff4a4a;
}

/* contentsのheightを500pxにしてください */
.contents {
height:500px;
}
/* section-titleのborder-bottomを指定してください */
.section-title{
  border-bottom:2px  solid #dee7ec;
}

/* contents-itemのfloatプロパティをleftにしてください */
.contents-item{
  float:left;
}

.footer {
  background-color: #2f5167;
  color: #fff;
  height: 120px;
  padding: 40px;
}

.footer-logo {
  float: left;
  font-size: 32px;
}

.footer-list {
  float: right;
}

.footer-list li {
  padding-bottom: 20px;
}
```
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Progate</title>
    <link rel="stylesheet" href="stylesheet.css">
  </head>
  <body>
    <div class="header">
      <div class="header-logo">Progate</div>
      <div class="header-list">
        <ul>
          <li>プログラミングとは</li>
          <li>学べるレッスン</li>
          <li>お問い合わせ</li>
        </ul>
      </div>
    </div>

    <div class="main">
      <div class="copy-container">
        <h1>HELLO WORLD<span>.</span></h1>
        <h2>プログラミングの世界へようこそ</h2>
      </div>
      
      <div class="contents">
        <h3 class="section-title">学べるレッスン</h3>
        <div class="contents-item">
          <img src="https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/html/study/html.svg">
          <p>HTML & CSS</p>
        </div>
        <div class="contents-item">
          <img src="https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/html/study/php.svg">
          <p>PHP</p>
        </div>
        <div class="contents-item">
          <img src="https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/html/study/ruby.svg">
          <p>Ruby</p>
        </div>
        <div class="contents-item">
          <img src="https://s3-ap-northeast-1.amazonaws.com/progate/shared/images/lesson/html/study/swift.svg">
          <p>Swift</p>
        </div>
      </div>
      
      <div class="contact-form">
        <h3 class="section-title">お問い合わせ</h3>
        <p>メールアドレス（必須）</p>
        <!-- <input>要素を追加してください -->
        <input>
        <p>お問い合わせ内容（必須）</p>
        <!-- <textarea>要素を追加してください -->
        <textarea></textarea>
        
        <p>※必須項目は必ずご入力ください</p>
        <!-- <input>要素を追加してください -->
        <input class="contact-submit" type ="submit" value="送信">
        
        
      </div>
    </div>

    <div class="footer">
      <div class="footer-logo">Progate</div>
      <div class="footer-list">
        <ul>
          <li>会社概要</li>
          <li>採用</li>
          <li>お問い合わせ</li>
        </ul>
      </div>
    </div>
  </body>
</html>
```
