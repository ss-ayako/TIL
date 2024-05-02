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
