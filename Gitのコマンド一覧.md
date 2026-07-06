
| コマンド                               | 操作                                |
| ---------------------------------- | --------------------------------- |
| pwd                                | カレントディレクトリを表示する                   |
| ls                                 | ファイル一覧を表示する                       |
| ls -a                              | 隠しファイルも含めて、ファイル一覧を表示              |
| git                                | オプションを付けていない状態で実行する場合、簡易ヘルプが表示    |
| git --version                      | バージョンを表示                          |
| git config --global user.name " "  | 名前の登録                             |
| git config --global user.email " " | メールの登録                            |
| git config --list                  | 登録情報確認                            |
| cd                                 | ディレクトリの指定                         |
| git init                           | .gitの隠しディレクトリに記録される               |
| git status                         | リポジトリやステージングエリアの状態を確認する           |
| git add [File name]                | ステージングエリアに仮登録                     |
| git commit                         | ステージングエリアの内容をコミットをする              |
| :q!                                | コミットの中断(vim)                      |
| a/A                                | 現在のカーソル位置の右から入力する/現在の行の末尾に入力(vim) |
| ESC                                | コマンドモード(vim)                      |
| :wq                                | 保存して終了(vim)                       |
| u                                  | もとに戻す(vim)                        |
| git log                            | コミット履歴を確認する                       |
| git add .                          | ステージングエリアにまとめて仮登録                 |
| git commit -a                      | 仮登録とコミットを同時に実行する                  |
| git commit -m "commit message"     | コミットメッセージを同時に指定する                 |
| git log --oneline                  | コミットメッセージだけを表示する                  |
| git log -2                         | 指定した件数だけコミットログを表示する               |
| git status -s                      | ステータスをシンプルな形式で表示                  |
| git diff                           | ステージングとワーキングディレクトリを比較する           |
| git diff --cached                  | 最新コミットとステージングエリアを比較する             |
| git diff HEAD                      | 最新コミットとワーキングディレクトリを比較する           |
| git checkout readme.txt            | ワーキングディレクトリのファイルを前の状態に戻す          |
| git reset readme.txt               | ステージング上の特定ファイルをひとつ前の状態に戻す         |
| git revert HEAD                    | 最新のコミットを打ち消す                      |
| git branch                         | ブランチを確認する                         |
| git branch add_html                | ブランチを作る                           |
| git checkout add_html              | ブランチを切り替える                        |
| git checkout master                | ブランチをmasterに切り替える                 |
| git merge add_html                 | ブランチをmasterにマージする                 |
| git branch -d add_html             | ブランチの削除                           |
| git branch -b add_html2            | ブランチの追加と切り替え                      |
| git clone /tmp/project_A.git       | 共同リポジトリを複製する                      |
| git remote -v                      | 複製した共同リポジトリの情報を表示する               |
| git push origin master             | コミットを共同リポジトリに反映する                 |
| git pull /tmp/project_A.git        | 変更を取り込む                           |
