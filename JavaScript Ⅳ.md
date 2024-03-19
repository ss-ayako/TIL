# クラス 
設計図のようなもの  

オブジェクトは複数の値をプロパティという名前をつけて管理できるもの  
定数名.プロパティ名で取得  
ブジェクトの「値」の部分には、関数を用いることもできる  
プロパティの値として関数を記述。その関数を呼び出すには、「定数名.プロパティ名()」  
```
// 定数animalを定義してください
const animal = {name:"レオ",age:3,greet:() => {
    console.log("こんにちは");
  }
};

// animalのnameプロパティの値を出力してください
console.log(animal.name);

// animalのgreetプロパティの関数を実行してください
animal.greet();
```
クラスからオブジェクトを生成するには 「new クラス名()」  
クラスから生成したオブジェクトは インスタンス  
```
class Animal {
}

// Animalクラスのインスタンスを定数animalに代入してください
const animal = new Animal ();

// 定数animalの値を出力してください
console.log (animal);
```
# 設計図に設定を追加する  
コンストラクタ インスタンスを生成するときに実行したい処理や設定を追加するための機能  
クラスの中括弧 { } 内に 「constructor() { }」 と記述  
ここに書いた処理はインスタンスが生成された直後に実行  
インスタンスごとに毎回実行される
```
class Animal {
  // コンストラクタを追加してください
  constructor(){
  console.log("インスタンスを生成しました");
}
}
const animal = new Animal();
```
コンストラクタの中で「this.プロパティ名 = 値」
生成されたインスタンスにプロパティと値を追加することができる  
```
class Animal {
  constructor() {
    // nameの値に文字列「レオ」を代入してください
    this.name = "レオ";
    
    // ageの値に数値の「3」を代入してください
    this.age = 3;
  }
}

const animal = new Animal();

// 「名前: 〇〇」となるように出力してください
console.log(`名前：${animal.name}`);
// 「年齢: 〇〇」となるように出力してください
console.log(`年齢：${animal.age}`);



class Animal {
  // 引数に「name」と「age」を追加してください
  constructor(name,age) {
    // 「"レオ"」の代わりに引数nameの値を代入してください
    this.name = name;
    
    // 「3」の代わりに引数ageの値を代入してください
    this.age = age;
  }
}

// 引数に「"モカ"」と「8」を渡してください
const animal = new Animal("モカ",8);

console.log(`名前: ${animal.name}`);
console.log(`年齢: ${animal.age}`);
```
# メソッド  
インスタンスの「動作」のようなもの  
「名前」や「年齢」などの情報はプロパティで追加した  
メソッドは「挨拶をする」「値を計算する」などの処理のまとまりを表す  
そのメソッドを呼び出し、処理を実行「インスタンス.メソッド名()」  
```
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  
  // greetメソッドを追加してください
  greet(){
  console.log("こんにちは");
}
}
const animal = new Animal("レオ", 3);

console.log(`名前: ${animal.name}`);
console.log(`年齢: ${animal.age}`);

// animalに対してgreetメソッドを呼び出してください
animal.greet();
```
# メソッド内で値を使う
「this.プロパティ名」  
```
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  
  greet() {
    console.log("こんにちは");
  }
  
  // infoメソッドを追加してください
  info(){
    console.log(`名前は${this.name}です`);
     console.log(`${this.age}歳です`);
  }
  
}

const animal = new Animal("レオ", 3);
animal.greet();

// animalに対してinfoメソッドを呼び出してください
animal.info();
```
# メソッド内で他のメソッドを呼び出す  
メソッド内で 「this.メソッド名()」  
infoメソッドの中で、Animalクラスのgreetメソッドを呼び出し  
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
    // greetメソッドを呼び出してください
    this.greet();
    
    console.log(`名前は${this.name}です`);
    console.log(`${this.age}歳です`);
  }
}

const animal = new Animal("レオ", 3);
// 以下の1行を消してください

animal.info();
```
# クラスの継承  
すでにあるクラスをもとに、新しくクラスを作成する方法のこと  
「Animalクラス」を継承して「Dogクラス」を作成する  「class Dog extends Animal」  
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

class Dog extends Animal {
}

// 定数dogにDogクラスのインスタンスを代入してください
const dog = new Dog("レオ",4);

// dogに対してinfoメソッドを呼び出してください
dog.info();
```
継承して作成したクラスにも、これまでと同じようにメソッドを追加することができる  
子クラスで定義した独自のメソッドは、親クラスから呼び出すことはできない  
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

class Dog extends Animal {
  // getHumanAgeメソッドを追加してください
  getHumanAge(){
  return this.age*7;
  }

}

const dog = new Dog("レオ", 4);
dog.info();

// 定数humanAgeを定義し、定数dogに対してgetHumanAgeメソッドを呼び出した値を代入してください
const humanAge = dog.getHumanAge();

// 「人間年齢で〇〇歳です」と出力してください
console.log(`人間年齢で${humanAge}歳です`);
```
# オーバーライド  
親クラスと同じ名前のメソッドを子クラスに定義すると、子クラスのメソッドが優先  
子クラスのメソッドが親クラスのメソッドを上書き  
