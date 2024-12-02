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
