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
```
body {
  margin: 0;
  font-family: "Hiragino Kaku Gothic ProN";
}

a {
  text-decoration: none;
}

/* containerクラスのCSSを指定してください */
.container{
  width:1170px;
  padding: 0 15px;
  margin: 0 auto;
}


/* top-wrapperクラスのCSSを指定してください */
.top-wrapper{
  padding:180px 0 100px 0;
  background-image:url(https://prog-8.com/images/html/advanced/top.png);
  background-size:cover;
  color:white;
}


```
```
body {
  margin: 0;
  font-family: "Hiragino Kaku Gothic ProN";
}

a {
  text-decoration: none;
}

.container {
  width: 1170px;
  padding: 0 15px;
  margin: 0 auto;
}

.top-wrapper {
  padding: 180px 0 100px 0;
  background-image: url(https://prog-8.com/images/html/advanced/top.png);
  background-size: cover;
  color: white;
}

/* top-wrapperの中の<h1>のCSSを指定してください */
.top-wrapper h1{
opacity:0.7;
font-size:45px;
letter-spacing:5px;
}

/* top-wrapperの中の<p>のCSSを指定してください */
.top-wrapper p{
  opacity:0.7;
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
    <header>
    </header>
    <div class="top-wrapper">
      <div class="container">
        <h1>LEARN TO CODE.</h1>
        <h1>LEARN TO BE CREATIVE.</h1>
        <p>Progateはオンラインプログラミング学習サービスです。</p>
        <p>初心者にもやさしいスライドとレッスンで、Webサービスを作りながらプログラミングを学んでいきましょう。</p>
        <!-- ここにコードを書いていきましょう -->
        <div class="btn-wrapper">
          <a href="#" class="btn signup">新規登録はこちら</a>
          <p>or sign up with</p>
          <a href="#" class="btn facebook">Facebookで登録</a>
          <a href="#" class="btn twitter">Twitterで登録</a>
        </div>
      </div>
    </div>
    <div class="lesson-wrapper">
    </div>
    <div class="message-wrapper">
    </div>
    <footer>
    </footer>
  </body>
</html>
```
```
body {
  margin: 0;
  font-family: "Hiragino Kaku Gothic ProN";
}

a {
  text-decoration: none;
}

.container {
  width: 1170px;
  padding: 0 15px;
  margin: 0 auto;
}

.top-wrapper {
  padding: 180px 0 100px 0;
  background-image: url(https://prog-8.com/images/html/advanced/top.png);
  background-size: cover;
  color: white;
}

.top-wrapper h1 {
  opacity: 0.7;
  font-size: 45px;
  letter-spacing: 5px;
}

.top-wrapper p {
  opacity: 0.7;
}

/* btnクラスのCSSを指定してください */
.btn {
  padding: 8px 24px;
  color: white;
  display: inline-block;
  opacity: 0.8;
}


/* signupクラスのCSSを指定してください */
.signup{
background-color: #239b76;
}



/* facebookクラスのCSSを指定してください */
.facebook{
background-color: #3b5998;
margin-right: 10px;
}


/* twitterクラスのCSSを指定してください */
.twitter{
background-color: #55acee;
}


/* btn-wrapperクラスのCSSを指定してください */
.btn-wrapper{
margin: 20px 0;
}


/* btn-wrapperクラスの中にある<p>のCSSを指定してください */
.btn-wrapper p{
margin:10px 0;
}

```
```
body {
  margin: 0;
  font-family: "Hiragino Kaku Gothic ProN";
}

a {
  text-decoration: none;
}

.container {
  width: 1170px;
  padding: 0 15px;
  margin: 0 auto;
}

.top-wrapper {
  padding: 180px 0 100px 0;
  background-image: url(https://prog-8.com/images/html/advanced/top.png);
  background-size: cover;
  color: white;
  /* text-alignをcenterに指定してください */
  text-align:center;
}

.top-wrapper h1 {
  opacity: 0.7;
  font-size: 45px;
  letter-spacing: 5px;
}

.top-wrapper p {
  opacity: 0.7;
}

.btn {
  padding: 8px 24px;
  color: white;
  display: inline-block;
  opacity: 0.8;
  /* border-radiusを4pxに指定してください */
  border-radius:4px;
}

/* btnクラスにhoverしたときのCSSを指定してください */
.btn:hover{
opacity: 1;
}

.signup {
  background-color: #239b76;
}

.facebook {
  background-color: #3b5998;
  margin-right: 10px;
}

.twitter {
  background-color: #55acee;
}

.btn-wrapper {
  margin: 20px 0;
}

.btn-wrapper p {
  margin: 10px 0;
}

```
```
body {
  margin: 0;
  font-family: "Hiragino Kaku Gothic ProN";
}

a {
  text-decoration: none;
}

.container {
  width: 1170px;
  padding: 0 15px;
  margin: 0 auto;
}

.top-wrapper {
  padding: 180px 0 100px 0;
  background-image: url(https://prog-8.com/images/html/advanced/top.png);
  background-size: cover;
  color: white;
  text-align: center;
}

.top-wrapper h1 {
  opacity: 0.7;
  font-size: 45px;
  letter-spacing: 5px;
}

.top-wrapper p {
  opacity: 0.7;
}

.btn-wrapper {
  margin: 20px 0;
}

.btn-wrapper p {
  margin: 10px 0;
}

.signup {
  background-color: #239b76;
}

.facebook {
  background-color: #3b5998;
  margin-right: 10px;
}

.twitter {
  background-color: #55acee;
}

.btn {
  padding: 8px 24px;
  color: white;
  display: inline-block;
  opacity: 0.8;
  border-radius: 4px;
}

.btn:hover {
  opacity: 1;
}

.fa {
  margin-right: 5px;
}

header {
  height: 65px;
  width: 100%;
  background-color: rgba(34, 49, 52, 0.9);
}

.logo {
  width: 124px;
  margin-top: 20px;
}

/* header-leftクラスのCSSを指定してください */
.header-left{
  float:left;
}


/* header-rightクラスのCSSを指定してください */
.header-right{
  float:right;
  background-color:rgba(255, 255, 255, 0.3);
}


/* header-rightクラスにhoverしたときのCSSを指定してください */
.header-right:hover {
  background-color:rgba(255, 255, 255, 0.5);
}

```
```
body {
  margin: 0;
  font-family: "Hiragino Kaku Gothic ProN";
}

a {
  text-decoration: none;
}

.container {
  width: 1170px;
  padding: 0 15px;
  margin: 0 auto;
}

.top-wrapper {
  padding: 180px 0 100px 0;
  background-image: url(https://prog-8.com/images/html/advanced/top.png);
  background-size: cover;
  color: white;
  text-align: center;
}

.top-wrapper h1 {
  opacity: 0.7;
  font-size: 45px;
  letter-spacing: 5px;
}

.top-wrapper p {
  opacity: 0.7;
}

.btn-wrapper {
  margin: 20px 0;
}

.btn-wrapper p {
  margin: 10px 0;
}

.signup {
  background-color: #239b76;
}

.facebook {
  background-color: #3b5998;
  margin-right: 10px;
}

.twitter {
  background-color: #55acee;
}

.btn {
  padding: 8px 24px;
  color: white;
  display: inline-block;
  opacity: 0.8;
  border-radius: 4px;
}

.btn:hover {
  opacity: 1;
}

.fa {
  margin-right: 5px;
}

header {
  height: 65px;
  width: 100%;
  background-color: rgba(34, 49, 52, 0.9);
}

.logo {
  width: 124px;
  margin-top: 20px;
}

.header-left {
  float: left;
}

.header-right {
  float: right;
  background-color: rgba(255, 255, 255, 0.3);
  transition: all 0.5s;
}

.header-right:hover {
  background-color: rgba(255, 255, 255, 0.5);
}

.header-right a {
  line-height: 65px;
  padding: 0 25px;
  color: white;
  display: block;
}

/* lesson-wrapperクラスのCSSを指定してください */
.lesson-wrapper{
  height:500px;
  padding-bottom:80px;
  background-color:#f7f7f7;
}


/* headingクラスのCSSを指定してください */
.heading{
  padding-top:60px;
  padding-bottom:30px;
  color:#5f5d60;
}


/* headingの中の<h2>のCSSを指定してください */
.heading h2{
  font-weight:normal;
}

```
文字に画像をかさねる
```
body {
  margin: 0;
  font-family: "Hiragino Kaku Gothic ProN";
}

a {
  text-decoration: none;
}

.container {
  width: 1170px;
  padding: 0 15px;
  margin: 0 auto;
}

.top-wrapper {
  padding: 180px 0 100px 0;
  background-image: url(https://prog-8.com/images/html/advanced/top.png);
  background-size: cover;
  color: white;
  text-align: center;
}

.top-wrapper h1 {
  opacity: 0.7;
  font-size: 45px;
  letter-spacing: 5px;
}

.top-wrapper p {
  opacity: 0.7;
}

.btn-wrapper {
  margin: 20px 0;
}

.btn-wrapper p {
  margin: 10px 0;
}

.signup {
  background-color: #239b76;
}

.facebook {
  background-color: #3b5998;
  margin-right: 10px;
}

.twitter {
  background-color: #55acee;
}

.btn {
  padding: 8px 24px;
  color: white;
  display: inline-block;
  opacity: 0.8;
  border-radius: 4px;
}

.btn:hover {
  opacity: 1;
}

.fa {
  margin-right: 5px;
}

header {
  height: 65px;
  width: 100%;
  background-color: rgba(34, 49, 52, 0.9);
}

.logo {
  width: 124px;
  margin-top: 20px;
}

.header-left {
  float: left;
}

.header-right {
  float: right;
  background-color: rgba(255, 255, 255, 0.3);
  transition: all 0.5s;
}

.header-right:hover {
  background-color: rgba(255, 255, 255, 0.5);
}

.header-right a {
  line-height: 65px;
  padding: 0 25px;
  color: white;
  display: block;
}

.lesson-wrapper {
  height: 500px;
  padding-bottom: 80px;
  background-color: #f7f7f7;
  /* text-alignをcenterに指定してください */
  text-align:center;
}

.heading {
  padding-top: 60px;
  padding-bottom: 30px;
  color: #5f5d60;
}

.heading h2 {
  font-weight: normal;
}

.lesson {
  float: left;
  width: 25%;
}

/* lesson-iconクラスのCSSを指定してください */
.lesson-icon{
  position:relative;
}


/* lesson-iconの中の<p>のCSSを指定してください */
.lesson-icon p{
  position:absolute;
  top:90px;
  width:100%;
  color:white;
}


/* txt-contentsクラスのCSSを指定してください */
.txt-contents{
  width:80%;
  display:inline-block;
  margin-top:20px;
  font-size:12px;
  color:#b3aeb5;
}


```
```
body {
  margin: 0;
  font-family: "Hiragino Kaku Gothic ProN";
}

a {
  text-decoration: none;
}

.container {
  width: 1170px;
  padding: 0 15px;
  margin: 0 auto;
}

.top-wrapper {
  padding: 180px 0 100px 0;
  background-image: url(https://prog-8.com/images/html/advanced/top.png);
  background-size: cover;
  color: white;
  text-align: center;
}

.top-wrapper h1 {
  opacity: 0.7;
  font-size: 45px;
  letter-spacing: 5px;
}

.top-wrapper p {
  opacity: 0.7;
}

.btn-wrapper {
  margin: 20px 0;
}

.btn-wrapper p {
  margin: 10px 0;
}

.signup {
  background-color: #239b76;
}

.facebook {
  background-color: #3b5998;
  margin-right: 10px;
}

.twitter {
  background-color: #55acee;
}

.btn {
  padding: 8px 24px;
  color: white;
  display: inline-block;
  opacity: 0.8;
  border-radius: 4px;
}

.btn:hover {
  opacity: 1;
}

.fa {
  margin-right: 5px;
}

header {
  height: 65px;
  width: 100%;
  background-color: rgba(34, 49, 52, 0.9);
}

.logo {
  width: 124px;
  margin-top: 20px;
}

.header-left {
  float: left;
}

.header-right {
  float: right;
  background-color: rgba(255, 255, 255, 0.3);
  transition: all 0.5s;
}

.header-right:hover {
  background-color: rgba(255, 255, 255, 0.5);
}

.header-right a {
  line-height: 65px;
  padding: 0 25px;
  color: white;
  display: block;
}

.lesson-wrapper {
  height: 500px;
  padding-bottom: 80px;
  background-color: #f7f7f7;
  text-align: center;
}

.heading {
  padding-top: 60px;
  padding-bottom: 30px;
  color: #5f5d60;
}

.heading h2 {
  font-weight: normal;
}

.lesson {
  float: left;
  width: 25%;
}

.lesson-icon {
  position: relative;
}

.lesson-icon p {
  position: absolute;
  top: 90px;
  width: 100%;
  color: white;
}

.txt-contents {
  width: 80%;
  display: inline-block;
  margin-top: 20px;
  font-size: 12px;
  color: #b3aeb5;
}

/* message-wrapperクラスのCSSを指定してください */
.message-wrapper{
  border-bottom:1px solid #eee;
  padding-bottom:80px;
  text-align:center;
}


.message {
  padding: 15px 40px;
  background-color: #5dca88;
  /* box-shadowをつけてください */
  box-shadow:0 7px #1a7940;
}

.heading h3 {
  font-weight: normal;
}
```
