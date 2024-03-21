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
