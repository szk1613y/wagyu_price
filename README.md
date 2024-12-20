# Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？

- **リモートリポジトリ**
  - ネット上に配置して複数人で共有するためのリポジトリ。(個人開発用にも使えます)
  >例：Github、GitLab、BitBucket、AWS CodeCommit、Gogs等
- **ローカルリポジトリ**
  - 開発者一人ひとりが使用するために自分のPC上に配置するためのリポジトリ。


## プッシュとマージの違いは何でしょうか？

1. 変更内容の反映先
    - `Push`はローカルリポジトリの変更内容をリモートリポジトリへ反映
    - `marge`はローカルリポジトリ、またはリモートリポジトリ上でブランチに別のブランチの作業内容を取り込む
1. 
1. 

## コミットとプッシュの違い

#### commit
    ファイル追加や変更の履歴をリポジトリに記録すること
    尚、commit前に修正したファイルをaddする必要がある
#### Push
    commitで記録した内容をリモートリポジトリにアップする操作

## コミットのメッセージはどのように書いてあげるのが最適でしょうか？

##### > 履歴を見た際にそのコミットメッセージから「どんな変更を行なったのか」がわかるようなメッセージにする
---

## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？

###### ローカルでマージするフロー
  - コードレビューをする前にmasterに反映されるため、コードにバグがあっても気づかない可能性がでてくる。
  > 最終的には誰も気づかなかったバグがそのまま本番環境にアップされ、大変な事態になる可能性がある。
###### プルリクエストでマージするフロー
  - コードレビューをしてからマージするという手順を踏むことで、事前にバグを発見する事ができる。

## コンフリクトを起こしてしまった場合、どう対処すべきですか？

###### 以下の3通りの方法で変更を取り込む必要がある。
1. 先にマージされた変更内容を取り込む
1. 後にマージしようとしている変更内容を取り込む
1. どちらの変更内容も取り込む
>どれを選択するかに関しては状況によって異なるが、特に3の両方取り込む場合は注意が必要。
コンフリクト解決には自分以外の人が書いたソースコードの内容を把握する必要があるため、少しでも意図が読み取れない処理とぶつかってしまった場合は、そのソースコードを書いた人と相談しながら作業を進めるようにする。