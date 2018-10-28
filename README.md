# generate-spec-boilerplate

## 本プロジェクトについて

以下のライブラリを用いて、ドキュメント作成を行うためのテンプレート
* [gitbook](https://www.gitbook.com/) / [Github](https://github.com/GitbookIO/gitbook)
* [textlint](https://textlint.github.io/) / [Github](https://github.com/textlint/textlint)

## Installation

    yarn install
    yarn install:gitbook

    または

    npm install
    npm run install:gitbook

`uml`のインストールで失敗した場合は、再度`install:gitbook`を再実行してください。

## Usage
**Build**

GitBookをbuildします。

    yarn build
    または
    npm run build

**Watch**

Gitbookをbuildかつwatchを行います。
次のコマンドを実行すると、ローカルサーバが起動してhttp://localhost:4000へアクセスすることでプレビューを確認できます。

    yarn start
    または
    npm start

