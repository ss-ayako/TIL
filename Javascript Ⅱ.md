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

「number += 1」は「number ++」のように省略して書ける   
「number -= 1」を「number --」と省略することができる  

```
// for文を用いて、1から100までの数字を出力してください
for(let number = 1; number <= 100; number ++){
  console.log(number);
}
```
***
```
// for文を完成させてください
for (let number = 1; number<=100 ;number+=1) {
  
  // if文を用いて、numberが3の倍数の時に「3の倍数です」、そうでないときは数字を出力してください
 if (number % 3 === 0) {
   console.log("3の倍数です");
 } else {
   console.log(number);
}
}
```
***
# 配列
複数の値をまとめて管理するには、配列
[値1, 値2, 値3] 
配列に入っているそれぞれの値のことを要素
```
// 定数animalsに、指定された配列を代入してください
const animals = ["dog","cat","sheep"];

// 定数animalsを出力して下さい
console.log(animals);
```
***

