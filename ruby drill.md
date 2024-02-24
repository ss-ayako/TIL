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

 
