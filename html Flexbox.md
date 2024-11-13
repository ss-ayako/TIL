ならびむきを指定  
折り返しを指定  
***
display: flexは指定した要素の子要素を横並びに  
横並びにしたい要素の親要素にdisplay: flex  
***
親要素の幅に合わせて伸ばしたい要素にflex: autoを指定  
***
flex-wrap: wrapを指定すると、子要素のサイズに応じて折り返す  
折り返したい要素の親要素にflex-wrap: wrapを指定  
折り返したい要素自身には列数に応じたwidthを指定  
今回は2列にしたいのでwidth: 50%を指定  
***
```
.flex-list {
  display: flex;
  /* flex-wrapを指定してください */
  flex-wrap: wrap
  
}
.flex-list li {
  flex: auto;
  /* widthを50％に指定してください */
  width:50%;
  
}
```
画面幅を狭めた時に2列に折り返すように  
