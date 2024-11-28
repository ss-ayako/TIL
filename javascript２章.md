```
<script>
  var name = prompt("おなまえは？");
  var sippo = prompt("突然ですが問題です。パンダのしっぽは何色？");
  if(sippo =="白"){
    alert("正解。");
  } else {
    alert(name + "さん、残念。白でした！！");
  }
  var kuni = prompt("では、世界で一番大きい国は？");
  if(kuni =="ロシア"){
    alert("正解。");
  } else {
    alert(name + "さん、残念。ロシアでした！！");
  }
  var keisan = prompt("最後の問題です。7✖️8 =?");
  if(keisan =="56"){
    alert("正解。");
  } else {
    alert(name + "さん、残念。56でした！！");
  }
  if(sippo =="白"){
    if(kuni =="ロシア"){
      if(keisan =="56") {
        alert("全問正解おめでとう！！すごいよ" + name + "さん");
      }
    }
  }
</script>
```
```
<!DOCTYPE html>
<html>
  <head></head>
  <meta charset="UTF-8">
  <script>
    function kaibun(){

       // 入力された文字列を取得
        let source = document.getElementById("source").value;
        
        // 逆順の文字列を生成
        let reversed = "";
        for (let i = source.length - 1; i >= 0; i--) {
          reversed += source.charAt(i); // 1文字ずつ追加
        }
        
        // 結果を表示（逆順文字列のみ）
        document.getElementById("result").textContent = reversed;
    }
  </script>
  </head>
  <body>
    <input id ="source">
    <button onclick="kaibun()">回文</button>
    <p id="result"></p>
  </body>
</html>
```
