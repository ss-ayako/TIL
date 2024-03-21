# コールバック関数  引数として渡される関数
```
const printWanko = () => {
  console.log("にんじゃわんこ");
};

const printHitsuji = () => {
  console.log("ひつじ仙人");
};

const call = (callback) => {
  console.log("コールバック関数を呼び出します。");
  callback();
};

// 引数をprintHitsujiに書き換えて出力を確認しましょう
call(printHitsuji);
```
他の関数に引数として渡される関数をコールバック関数という  
JavaScriptでは引数に関数を渡すことができる
関数名の後ろに()をつけると呼び出される  
()をつけなければ関数そのものを指す  
```
const printWanko = () => {
  console.log("にんじゃわんこ");
};

// 関数callにcallbackという名前の引数を追加してください
const call = (callback) => {
  console.log("コールバック関数を呼び出します。");
  // 引数に渡したcallbackを呼び出してください
  callback();
};

// 関数printWankoを引数に渡して関数callを実行してください
call(printWanko);
```
事前に定義した関数をコールバック関数として渡した,関数を直接引数の中で定義することもできる  
```
const printWanko = () => {
  console.log("にんじゃわんこ");
};

const call = (callback) => {
  console.log("コールバック関数を呼び出します。");
  callback();
};

call(printWanko);

// 引数で関数を定義して渡してください
call(() => {
  console.log("ひつじ仙人");
});
```
