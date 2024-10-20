***
1  
- シンボルを使ったキーの記述方法は、キーの後にコロン:をつけて定義
- hash = { キー: 値}
  
オブジェクト.keysで、ハッシュに含まれるキーを取得  
 hash = { one: 1, two: 2, three: 3 }  
 puts hash.keys  
 one  
 two  
 three  
 
オブジェクト.valuesで、ハッシュに含まれる値を取得  
hash = { one: 1, two: 2, three: 3 }  
puts hash.values  
1  
2  
3  
***
2  
配列の内部に、複数のユーザーの情報をハッシュとして持つ変数user_dataがあります  
user_data = [  
 {user: {profile: {name: 'George'}}},  
 {user: {profile: {name: 'Alice'}}},  
 {user: {profile: {name: 'Taro'}}},  
]  
user_dataを利用して、全てのユーザーの名前だけが出力されるようにRubyでコーディング  

user_data.each do |u|  
  puts u[:user][:profile][:name]  
end  

ハッシュから特定の値を取得する場合は、その値に対応するキーを指定  
以下の書き方で取得ができる  
ハッシュ[取得したい値のキー]  

二重ハッシュから特定の値を取得する場合,  
取得したい値のキーまで連続して指定すると取得できる 

今回取得したい値は、George, Alice, Taroという値  
よって、取得したい値に対応するキーはnameというキー  
そのため、nameというキーまで連続して指定すると、George, Alice, Taroという値を取得できる  
ハッシュ[:user][:profile][:name]  

今回は配列の中にハッシュが格納  
each文でハッシュの1つ1つを取り出した上で,ハッシュ[:user][:profile][:name]  
***
3  
国語が80点、英語が50点、数学が70点の場合のテストの平均点をターミナルに出力するプログラム  
変数を使って定義  
３教科の平均点は、◯点です。 

japanese_score = 80  
english_score = 50  
math_score = 70  

average_score = (japanese_score + english_score + math_score) / 3  

puts "3教科の平均点は、#{average_score}点です。"  
各教科の点数をそれぞれ変数として定義  
変数名はjapanese_score、japanese、kokugo_score、kokugo  

平均点に関しても変数を使うほうが望ましいです。変数を使わない場合は以下のようになります。


puts "3教科の平均点は、#{(japanese_score + english_score + math_score) / 3}点です。"  
これだとコードが読みにくく、(japanese_score + english_score + math_score) / 3が何を指しているのかを見ただけでは判断することが難しい  
そこで平均点も以下のように変数として定義  
average_score = (japanese_score + english_score + math_score) / 3  
平均点の出力の際には、文字列と数値の連結となる  
式展開かto_sメソッドを使う  
 
***
4  
class Article  

  def initialize(author, title, content)  
    @author = author  
    @title = title  
    @content = content  
  end  

end  

initialize  
インスタンス再生時に呼び出し  
