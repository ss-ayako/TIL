```
class Main {
  public static void main(String[] args) {
    // 「4 + 2」と「6」を比較し、falseとなるようにしてください
    System.out.println(4 + 2 > 6);
    
    // 「4 + 2」と「6」を比較し、trueとなるようにしてください
    System.out.println(4 + 2 == 6);
    
  }
}
```
```
class Main {
  public static void main(String[] args) {
    // trueと出力されるようにしてください
    System.out.println(true);
    
    // falseと出力されるようにしてください
    System.out.println(false);
    
    // 「8 < 5」かつ「3 >= 2」の結果を出力してください
    System.out.println(8 < 5&&3 >= 2);
    
    // 「8 < 5」または「3 >= 2」の結果を出力してください
    System.out.println(8 < 5||3 >= 2);
    
    // 「8 < 5」でない、の結果を出力してください
    System.out.println(!(8 < 5));
    
  }
}
```
```
class Main {
  public static void main(String[] args) {
    int number = 12;
    
    // numberが20より小さいとき、どちらでもないときの条件分岐を追加してください
    if (number < 10) {
      System.out.println("10より小さい");
    }else if(number < 20){
      System.out.println("10以上、20より小さい");
    }else{
      System.out.println("20以上");
    }
    
  }
}
```
```
class Main {
  public static void main(String[] args) {
    int number = 10;
    
    // while文を用いて、numberが0より大きい場合に繰り返す、繰り返し処理を作ってください
    while(number>0){
    System.out.println(number);
    number++;
      
    }
  }
}
```
```
class Main {
  public static void main(String[] args) {
    // 変数namesに、配列を代入してください
    String [] names ={"にんじゃわんこ","ひつじ仙人","ベイビーわんこ"};
    
    // インデックス番号が0の要素を出力してください
    System.out.println(names[0]);
    
    // インデックス番号が2の要素を出力してください
    System.out.println(names[2]);
    
  }
}
```
