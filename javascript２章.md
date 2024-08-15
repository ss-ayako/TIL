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
