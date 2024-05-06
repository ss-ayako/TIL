***
# ファイルの作成  
「touch ファイル名」  
# ファイルの中身を表示  
「cat ファイル名」  
# ディレクトリを作成  
「mkdir ディレクトリ名」  
# ルートディレクトリ  
ルートディレクトリは「/」で表される、1番親のディレクトリ  
# カレントディレクトリを確認  
pwd
ルートディレクトリからカレントディレクトリまでの階層が全て表示 

pwdコマンドを用いて、カレントディレクトリを確認  
「languages」ディレクトリに移動して、pwdコマンドを用いて、カレントディレクトリを確認  
```
~ $ pwd
/home/progate
~ $ cd languages
languages $ pwd
/home/progate/languages
languages $
```
# ディレクトリの中身を表示  
ls  

lsコマンドを用いて、ディレクトリの中身を表示  
「languages」ディレクトリに移動して、lsコマンドを用いて、ディレクトリの中身を表示  
```
~ $ ls
about.txt     beginner.txt  html          languages
~ $ cd languages
languages $ ls
index.txt
languages $
```

# 1つ親のディレクトリ  
cd ..  

# ディレクトリを指定しないcdコマンド  
cd  
# ファイルを移動
「mv ファイル名 ディレクトリ名」で指定したディレクトリにファイルを移動  
# ディレクトリごと移動  
「mv ディレクトリ名 移動先のディレクトリ名」  

# lsで確認する 
# ファイル名変更  
ファイルやディレクトリの移動に使ったmvコマンドは、ファイル名を変更することにも使える  

cdコマンドを用いて、「html」ディレクトリまで移動  
「beginner.txt」ファイルを「dojo.txt」というファイル名に変更  

```
~ $ cd languages
languages $ cd html

html $ mv beginner.txt dojo.txt
html $ ls
```



