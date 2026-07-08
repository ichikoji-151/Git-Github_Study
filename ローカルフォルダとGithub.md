参考記事：https://zenn.dev/divsawa/articles/20251012_teaching-github-gitinit
1. ローカルリポジトリを初期化 
   ```
   # ローカルリポジトリに移動(bashにドラッグアンドドロップでもできる)
   cd ~/Desktop/my-project
   
   # Gitの初期化
   git init
   
   #.gitが設置されているか確認
   ls -la
   ```
2. Githubでリモートリポジトリを作成
3. ローカルとリモートを接続
   ```
   # ローカルとリモートを接続(SSHの場合)
   git remote add origin git@github.com:ユーザー名/my-project.git
   
   # ローカルとリモートを接続(HTTPSの場合)
   git remote add origin https://github.com/ユーザー名/リポジトリ名.git
   ```
   >[!info] origin行こうにあるリンクはgithubでリモートリポジトリ制作時に「Quick setup~」に記載があるのでそれをコピー

```
# 接続中のリモートリポジトリを確認
git remote -v

# 正しく接続された場合の表記
origin git@github.com:ユーザー名/my-project.git(fetch)
origin git@github.com:ユーザー名/my-project.git(push)
```
4. ファイルをコミット
   ```
   # 変更内容をステージング
   git add .
   
   # コミット(メッセージを付けて記録)
   git commit -m "first commit"
   ```
   ```
   # ステージングとコミットを同時にする
   git commit -a -m "first commit"
   ```
5. pushでアップロード完了
   ```
   # リモートリポジトリへ変更を反映
   git push origin main
   ```  

# Githubにあるコマンドたち
```
echo "#" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:.git
git push -u origin main

git remote add origin git@github.com:.git
git branch -M main
git push -u origin main
```
上のやり方はだいぶ端折っているのでないコマンドもあるが大体あんな感じの流れになる

# SSH認証
筆者はSSHで初めて設定して躓いた。
SSH鍵なるものをつくらしいのだ(Claudeに聞いた)
1. 鍵の作成
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```
2. ssh-agentを起動して鍵を登録
   ```
   eval $(ssh-agent -s)
   ssh-add ~/ .ssh/id_ed15519
   ```
3. 公開鍵の中身を表示してコピー
   ```
   cat ~/.ssh/id_ed25519.pub
   # ssh-ed255199 AAAAと表示されるのでそれをコピー
   ```
4. Githubに登録
   右上アイコン→Settings→左メニューSSH and GPG keys→New SSH key→Titleの設定、Key欄に3でコピーした内容を貼り付け→Add SSH key
5. 接続確認
   ```
   ssh -T git@githun.com
   ```
