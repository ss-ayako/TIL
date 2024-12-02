```
class PostsController < ApplicationController
  def index
    @posts = Post.all
  end
  
  # showアクションを追加してください
  def show
  end
end
```
「localhost:3000」にアクセスしたときにトップページが表示されるようにしてください。  
ルーティング
```
Rails.application.routes.draw do
  get "/" => "home#top"

  # For details on the DSL available within this file, see http://guides.rubyonrails.org/routing.html
end
```
コントローラー
```
class HomeController < ApplicationController
  def top
  end
end
```
サービス紹介ページを追加しよう  
```
ルーティング
Rails.application.routes.draw do
  get "/" => "home#top"
  get "/about" => "home#about"
  # For details on the DSL available within this file, see http://guides.rubyonrails.org/routing.html
end
```
```
コントローラー
class HomeController < ApplicationController
  def top
  end
  def about
  end
end
```
```
ビュー
<div class="about-main">
  <h2>TweetAppとは</h2>
  <p>
    SNSサービスです。
    近況やつぶやきを投稿し、他のユーザーと楽しくコミュニケーションできます。
  </p>
  <img class="about-img" src="/tweets.png">
</div>
```
「localhost:3000」 (後ろに/○○がないURL) に対応するルーティングは、  
「get "/" => "コントローラ名#アクション名"」というように、URLに"/"を指定  
```
