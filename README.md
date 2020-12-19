# TypeScript環境構築確認用

## 作成手順

1. プロジェクトの作成  
以下コマンドを実行しプロジェクトフォルダを作成する。
    ~~~
    mkdir [フォルダ名]
    ~~~
    作成したプロジェクトフォルダをカレントディレクトリにする。
    ~~~
    cd [フォルダ名]
    ~~~
    次に以下コマンドを実行しpackage.jsonを作成する。
    ~~~
    npm init --y
    ~~~
2. gitリポジトリを作成する  
    以下コマンドを実行しgitリポジトリを作成する。
    ~~~
    git init
    ~~~
    node_modulesをgit管理対象外にするため「.gitignore」を作成する。
    ~~~
    copy nul .gitignore
    ~~~
    作成した「.gitgnore」に以下を記入する。
    ~~~
    node_modules/
    ~~~

3. 必要なpackageのインストールをする。  
    ~~~
    npm install typescript ts-loader webpack webpack-cli webpack-dev-server
    ~~~
4. package.jsonのscriptに以下を追加する。
    ~~~
    "build": "webpack --mode=development",
    "start": "webpack serve --mode=development"
    ~~~
    
