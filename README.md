# TexCompileTest

Automatic tex compile via CircleCI

## About

push及びpull requestされる度にCircleCIがtexドキュメントを勝手にビルドし, エラーチェック及びpdfを生成してくれます.

日本語用にチューンナップされています.

## How to use

1. 必要ファイルのコピー

    1. あなたのドキュメント用のリポジトリを作成します.

    1. 以下のファイルを本リポジトリからコピーし, 配置します.
        - .circleci/config.yml
        - .gitignore
        - latexmkrc

1. CircleCIとの連携

    1. [CircleCIのページ](https://circleci.com/)に行き, ログインします.
    
    1. 左側リストの「Add projects」から先程作成したリポジトリを見つけ, 「Set up project」を押します.
    
    1. 連携後はpushする度にJobが走ります. Successした場合, Artifactsタブから成果物を見ることができます.
    ![2018-12-08](https://user-images.githubusercontent.com/20468497/49687225-90788c00-fb43-11e8-9479-dbcff8b6e4e0.png)

1. Overleafとの連携(additional)

    1. [Overleafのページ](https://ja.overleaf.com/project)に行きログインします.
    
    1. 「アカウント」→「アカウントの設定」から設定ページに飛び, Githubアカウントを連携させます.
    
    1. [先程のページ](https://ja.overleaf.com/project)に戻り「新規プロジェクト」を押すと「Githubからインポート」という項目があります.
    こちらを押してリポジトリを選ぶことでインポートが可能です.
    
    1. インポート後は編集画面の「メニュー」→「同期」→「Github」からpush及びpullが可能です. (branchが選択できるかどうかは未確認)
    
