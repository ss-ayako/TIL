# ファイルの分割  
ファイルを分割したときにエラー  これは分割したことで、ファイル内に必要な値がなくなったことが理由  
***
# 他のファイルへ値を渡すexport（出力）
クラスの定義の後「export default クラス名」  
そのクラスをエクスポート（出力）し、他のファイルへ渡すことができる  
```
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log("こんにちは");
  }

  info() {
    this.greet();
    console.log(`名前は${this.name}です`);
    console.log(`${this.age}歳です`);
  }
}

// Animalクラスをエクスポートしてください
//他のファイルへ値を渡すexport
//クラス定義の後に記述　export default クラス名
export default Animal;
```
***
# 他のファイルで定義されているクラスを使用インポート（読込） 
使用するファイルの先頭で「import クラス名 from "./ファイル名"」  
```
// Animalクラスをインポートしてください
//他のファイルから読み込むimport
//使用するファイルの先頭で「import クラス名 from "./ファイル名"」
import Animal from "./animal"

class Dog extends Animal {
  constructor(name, age, breed) {
    super(name, age);
    this.breed = breed;
  }

  info() {
    this.greet();
    console.log(`名前は${this.name}です`);
    console.log(`犬種は${this.breed}です`);
    console.log(`${this.age}歳です`);
    const humanAge = this.getHumanAge();
    console.log(`人間年齢で${humanAge}歳です`);
  }

  getHumanAge() {
    return this.age * 7;
  }
}

// Dogクラスをエクスポートしてください
//他のファイルへ値を渡すexport
//クラス定義の後に記述　export default クラス名
export default Dog;
```
***
# 値のエクスポート  
文字列や数値や関数もエクスポート可能  
エクスポートする際は「export default 定数名;」  
インポートする際は「import 定数名 from "./ファイル名";」  
```
「script.js」から「dogData.js」にdogインスタンスを定義する部分を移動
// Dogクラスのインポートと定数dogを以下に張り付けてください
import Dog from "./dog";

const dog = new Dog("レオ", 4, "チワワ");

// 定数dogをエクスポートしてください
export default dog;
```
# デフォルトエクスポート  export default  
そのファイルがインポートされると自動的に「export default 値」の値がインポートされる  
そのためエクスポート時の値の名前と、インポート時の値の名前に違いがあっても問題ない  
デフォルトエクスポートの値を自動でインポートするため、値が1つのみ

# 「名前付きエクスポート」  
複数の値をエクスポートしたい場合
エクスポート 名前を{}で囲む defaultを書かない  
インポート 「import { 値の名前 } from "./ファイル名"」  

# 1つのファイルから複数のエクスポート  
エクスポート 「export { 名前1, 名前2 }」  
インポート 「import { 値の名前,値の名前 } from "./ファイル名"」  
```
import Dog from "./dog";

// 定数dog1, dog2を確認してください
const dog1 = new Dog("レオ", 4, "チワワ");
const dog2 = new Dog("ベン", 2, "プードル");

// 以下を書き換えて、定数dog1, dog2をエクスポートしてください
//1つのファイルから複数のエクスポート
export {dog1,dog2};


// 以下を書き換えて、定数dog1, dog2をインポートしてください
import { dog1, dog2 } from "./dogData";

// 定数dog1とdog2を出力するように左からコピーして書き換えてください
console.log("---------");
dog1.info();
console.log("---------");
dog2.info();
console.log("---------");
```
# 相対パス  
「./」 同じディレクトリ  
```
import { dog1, dog2 } from "./data/dogData";
```
「../」 1つ上の階層に戻る  
```
import Dog from "../class/dog";
```
# パッケージ
誰かが作った便利なプログラムがパッケージという形で公開されてる  
パッケージを自分のプログラムで使うためには、importを用いてパッケージをインポート  
# readline-sync
質問文が出力されると一旦処理が止まり、コンソールに値が入力されると、次の処理に進む  
入力された値は、定数や変数に代入することが出来る  
年齢のように整数を入力してほしい場合はquestionIntを用いる  
const 定数 = readline-sync.questionInt("年齢入れてください"）;  
あとは入力値を用いて、Dogのインスタンスを生成すれば完成  
```
// readline-syncをインポートしてください
import readlineSync from "readline-sync";

import Dog from "../class/dog";

const dog1 = new Dog("レオ", 4, "チワワ");

// readlineSync.questionを使って書き換えてください
const name = readlineSync.question("名前を入力してください: ");

// readlineSync.questionIntを使って書き換えてください
const age = readlineSync.questionInt("年齢を入力してください: ");

// readlineSync.questionを使って書き換えてください
const breed = readlineSync.question("犬種を入力してください: ");

const dog2 = new Dog(name, age, breed);

export { dog1, dog2 };
```
