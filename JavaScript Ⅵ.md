# 配列を操作するメソッド  
# pushメソッド 配列の最後に新しい要素を追加するメソッド  
push()の中に追加したい要素を入力  
```
// pushメソッドを使って配列charactersに、文字列「とりずきん」を追加してください
characters.push("とりずきん");
```
# forEachメソッド 配列の中の要素を1つずつ取り出して、全ての要素に繰り返し同じ処理  
forEachメソッドの引数には、学習Ⅲで学んだアロー関数が入ってる  
配列内の要素が1つずつ順番にアロー関数の引数に代入され、処理が繰り返し実行  
配列.forEach((引数）
```
const characters = ["にんじゃわんこ", "ベイビーわんこ", "ひつじ仙人", "とりずきん"];

// forEachメソッドを使って、配列charactersの中身をすべて出力してください
characters.forEach ( (character)=> {console.log(character);} );
```
配列charactersの要素が1つずつ順番に  
引数characterに代入され、  
処理内に書いてあるconsole.log(character)が繰り返し実行  
引数に入っている関数はコールバック関数と呼ぶ　 (character)=> {console.log(character);} 

長くなるので見やすく{
で改行する　こんな風に
```
const characters = ["にんじゃわんこ", "ベイビーわんこ", "ひつじ仙人", "とりずきん"];

// forEachメソッドを使って、配列charactersの中身をすべて出力してください
characters.forEach ( (character)=> {
  console.log(character);
} );
```
# findメソッド 条件式に合う1つ目の要素を配列の中から取り出すメソッド  
配列numbersの要素が1つずつ引数numberに代入されて処理  
コールバック関数の中は { return 条件 }   
条件に合う要素が戻り値  
条件に合う要素が見つかった時に終了.条件に合う最初の1つの要素のみ  
```
const numbers = [1, 3, 5, 7, 9];

// findメソッドを使って配列numbersから3の倍数を見つけ、定数foundNumberに代入してください
const foundNumber = numbers.find((number) => {
  return number%3===0;
});

// foundNumberを出力してください
console.log(foundNumber);


const characters = [  // オブジェクトの配列characters

  {id: 1, name: "にんじゃわんこ", age: 6},
  {id: 2, name: "ベイビーわんこ", age: 2},
  {id: 3, name: "ひつじ仙人", age: 100},
  {id: 4, name: "とりずきん", age: 21}
];

// 定数charactersからidが3のオブジェクトを見つけ、定数foundCharacterに代入してください
const foundCharacter = characters.find((character) => { //定数foundCharacterに代入
  return character.id===3; //処理: character.idが3のときにtrueをreturn
});


// foundCharacterを出力してください
console.log(foundCharacter);
```
# filterメソッド 記述した条件に合う要素全てを取り出して新しい配列を作成するメソッド
配列の要素がオブジェクトの場合も使うことができる

```
const numbers = [1, 2, 3, 4];

// filterメソッドを使ってnumbersから偶数を取り出し、定数evenNumbersに代入してください
const evenNumbers = numbers.filter((number)=>{
  return number %2===0;
});

// evenNumbersを出力してください
console.log(evenNumbers);


const characters = [
  {id: 1, name:"にんじゃわんこ", age: 14},
  {id: 2, name:"ベイビーわんこ", age: 5},
  {id: 3, name:"ひつじ仙人", age: 100}
];

// charactersから20歳未満のキャラクターを取り出し、定数underTwentyに代入してください
const underTwenty = characters.filter((character)=>{
  return character.age<=20;
});

// underTwentyを出力してください
console.log(underTwenty);
```
# mapメソッド　配列内のすべての要素に処理を行い、その戻り値から新しい配列を作成するメソッド
