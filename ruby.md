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
```
<header>
      <div class="header-logo">
        <%= link_to("TweetApp", "/") %>
      </div>
      <ul class="header-menus">
        <li>
          <%= link_to("TweetAppとは", "/about") %>
        </li>
      </ul>
    </header>
    
    <h1>Home#top</h1>
<p>Find me in app/views/home/top.html.erb</p>
<div class="main top-main">
  <div class="top-message">
    <h2>つぶやきで、世界はつながる</h2>
    <p>今の気持ちをつぶやいてみよう！</p>
  </div>
</div>
```
```
ビュー
<div class="main posts-show">
  <div class="container">
    <div class="posts-show-item">
      <p>
        <%= @post.content %>
      </p>
      <div class="post-time">
        <%= @post.created_at %>
      </div>
    </div>
  </div>
</div>
```
```
ルーティング
Rails.application.routes.draw do
  get "posts/index" => "posts#index"
  get "posts/:id" => "posts#show"

  get "/" => "home#top"
  get "about" => "home#about"
end
```
一覧にリンク
```
<div class="main posts-index">
  <div class="container">
    <% @posts.each do |post| %>
      <div class="posts-index-item">
         <%= link_to(post.content, "/posts/#{post.id}") %>
      </div>
    <% end %>
  </div>
</div>
```
```
コントローラー
class PostsController < ApplicationController
 def index
    @posts = Post.all.order(created_at: :desc)
  end
  def show            
   @post = Post.find_by(id: params[:id])            
 end
end
```
