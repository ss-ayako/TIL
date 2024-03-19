# ファイルの分割  
ファイルを分割したときにエラー  これは分割したことで、ファイル内に必要な値がなくなったことが理由  
***
Animalクラスを他のファイルでも使用できるように  
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
他のファイルで定義されているクラスを使用するにはインポート（読込）  
使用するファイルの先頭で「import クラス名 from "./ファイル名"」  
***
