***
# 変数
```
// 変数lengthを定義してください  
let length = 5;  

// 変数lengthの値を出力してください  
console.log(length);  

// 変数lengthを用いて、円の面積を出力してください  
console.log (length * length * 3 );  
```
***
変数は、一度代入した値を変更することもできる
一度値を代入した変数に、その後再び値を代入すると、上書きされる
「let」は必要なく 「変数名 = 新しい値」
***
```
let number = 7;
console.log(number);

// 変数numberの値に3を加えてください
number=number+3;

console.log(number);

// 変数numberの値を2で割ってください
number=number/2;

console.log(number);
```
***
# 定数
```
// 定数languageを定義してください
const language = "フランス語";

// 定数languageの値を出力してください
console.log (language);

// 定数languageを用いて、「〇〇を話せます」と出力してください
console.log (language+"を話せます");
```
***
文字列や定数の連結には、「+」記号  
ES6では「テンプレートリテラル」という連結方法がある、これで文字列の中に定数（変数）を埋め込むことができる  
文字列の中で「${定数}」とすることで、文字列の中に定数や変数を含めることができる  
この時、文字列全体をバッククォーテーション（`）で囲む必要がある  
***
```
const name = "にんじゃわんこ";
const age = 14;

// 「ぼくの名前は〇〇です」とコンソールに出力してください
console.log(`ぼくの名前は${name}です`);

// 「今は〇〇歳です」と出力してください
console.log(`今は${age}歳です`);
```
***
# 演算子 
「a == b」はaとbが等しければtrue、等しくなければfalse  
「a != b」はaとbが異なればtrue、等しくなければfalse  

厳密等価演算子  
「a === b」は厳密にaとbが等しければtrue、等しくなければfalse  
「a !== b」は厳密にaとbが異なればtrue、等しくなければfalse  
```
const password = "ninjawanko";

// passwordの値が"ninjawanko"の場合、「ログインに成功しました」と出力してください
if(password=="ninjawanko"){
  console.log("ログインに成功しました");
}



// passwordの値が"ninjawanko"でない場合、「パスワードが間違っています」と出力してください
if(password!=="ninjawanko"){
  console.log("パスワードが間違っています");
}
```
***
```
const age = 17;

// 条件式が成り立たない場合に「私は20歳未満です」と出力してください
if (age >= 20) {
  console.log("私は20歳以上です");
} else {
  console.log("私は20歳未満です");
}
```
***
# 条件分岐　
```
const age = 17;

// ageの値が10以上20未満のとき、「私は20歳未満ですが、10歳以上です」と出力してください
if (age >= 20) {
  console.log("私は20歳以上です");
} else if (age >= 10) {
  console.log("私は20歳未満ですが、10歳以上です");
} else {
  console.log("私は10歳未満です");
}
```
***
# かつ
「かつ」は「&&」  
「条件1 && 条件2」は「条件1かつ条件2」という意味.複数の条件がすべてtrueならtrue.  
```
const age = 24;

// 指定された条件のif文を作成してください
if(age>=20 && age<30){
  console.log("私は20代です");
}
```
***
# または
「または」は「||」  
「条件1 || 条件2」は「条件1または条件2」という意味.この場合は、複数の条件のうち1つでもtrueならtrue.  
***
# switch文
ある値によって処理を分岐する場合  
switch文の中にcaseを追加することで処理を分けることができる  
breakがないと、合致したcaseの処理を行った後、その次のcaseの処理も実行してしまう  
そのため、switch文を使うときにはbreakを忘れないようにする 
```
const n = 2;

switch (n) {
  case 1:
    console.log("大吉です");
    break;

  // nの値が2のcaseを追加してください
  case 2:
    console.log("吉です");
    break;
  
  
  // nの値が3のcaseを追加してください
  case 3:
    console.log("小吉です");
    break;  
}
```
caseのどれにも一致しなかった時、defaultのブロックが実行されます。defaultはif文のelseに似たようなもの  
if, elseifによる分岐が多く複雑な場合、switch文で書き換えるとシンプルで読みやすいコードにできる  
***
