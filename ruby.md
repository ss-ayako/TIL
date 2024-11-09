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
