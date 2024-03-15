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
# インデックス番号
配列の要素にはそれぞれインデックス番号という番号がついている  
インデックス番号は、0から始まる  
```
const animals = ["dog", "cat", "sheep"];

// 配列の1つ目の要素を出力してください
console.log(animals[0]);

// 配列の3つ目の要素を出力してください
console.log(animals[2]);
```
***
# 定数
配列自体を再度代入することはできない、配列の要素を更新することはできる  
```
const animals = ["dog", "cat", "sheep"];

// 配列animalsの3つ目の要素を「rabbit」に更新してください
animals[2]="rabbit";

// 配列animalsの3つ目の要素をコンソールに表示して下さい
console.log(animals[2]);
----

const animals = ["dog", "cat", "sheep"];

// for文を用いて、配列の値を順にコンソールに出力してください
for(let i = 0;i <3;i++){
  console.log(animals[i]);
}
----

const animals = ["dog", "cat", "sheep", "rabbit", "monkey", "tiger", "bear", "elephant"];

// lengthを用いて配列の要素の数を出力してください
console.log(animals.length);

// lengthを用いて条件式を書き換えてください
for (let i = 0; i < animals.length; i++) {
  console.log(animals[i]);
}
```
# オブジェクト  
配列は複数の値を並べて管理するのに対し,  
オブジェクトはそれぞれの値にプロパティと呼ばれる名前をつけて管理  
オブジェクトは{}で囲む  
プロパティ名と値の間はコロン（ : ）で繋ぐ  
プロパティ間はコンマ（,）で区切る  

オブジェクトも定数に代入することができる  
```
「console.log(定数名)」とすると、オブジェクトがコンソールに出力される  
// 定数characterを定義し、指定されたオブジェクトを代入してください
const character={name:"にんじゃわんこ",age:14};

// characterの値を出力してください
console.log(character);
```
# オブジェクトの値更新
```
const character = {name: "にんじゃわんこ", age: 14};

// characterのnameの値を出力してください
console.log(character.name);

// characterのageの値を「20」に更新してください
character.age = 20;

// characterをコンソールに出力してください
console.log(character);
```
# オブジェクトを要素に持つ配列
配列の要素には、文字列や数値だけでなく、オブジェクトも使う  
コードが横に長くなることを防ぐために、要素ごとに改行する  


