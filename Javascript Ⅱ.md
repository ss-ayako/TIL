# 繰り返し処理
while文  
whileとは「～の間」という意味の英語  
「条件式がtrueの間、{ }内の処理を繰り返す」  
{}の後にセミコロンは不要  
```
// 変数numberを定義してください
let number = 1;

// while文を作成してください
while(number <= 100){
  console.log(number);
  number += 1;
}
```
***
# 繰り返しFor文
while文以外にもfor文というものがある  
できることはwhile文と同じ  
while文に比べてシンプルに書くことができるのが特徴  
***
「number += 1」は「number ++」のように省略して書ける   
「number -= 1」を「number --」と省略することができる  

```
// for文を用いて、1から100までの数字を出力してください
for(let number = 1; number <= 100; number ++){
  console.log(number);
}
```
***
