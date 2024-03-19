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
