# Nanami Takahashi

### 自身が制作したポートフォリオWebサイトです。<br>自身の習得スキル等を記載したプロフィール、大学での活動から現在までの職務経歴を閲覧でき、過去に作成した技術記事や開発メモもご覧いただけます。

<img src='front/assets/image/site-page.jpg'>

## URL 
https://nt-myapp.firebaseapp.com

## 使用言語

- Nuxt.js 2.15.8
- Vue.js 2.6.14
- Node.js 14.15.1
- Vuetify 2.6.1

## 構築手順
<span style="color:red;">※前提としてNode.jsとnpmをインストールしておく必要があるためNode.jsとnpmをインストールする手順を同時に記載する。インストール済の場合は該当インストール手順をスキップし「プロジェクト構築手順」から手順を進める。</span>

### Node.jsのインストール手順
1. 下記URLにアクセスしOSに合う最新のNode.jsをインストールする。<br>
	https://nodejs.org/ja/download/
2. インストールが完了したら任意のターミナルにて下記コマンドを実行し、Node.jsがインストールされていることを確認する。バージョンが表示されたらNode.jsのインストール完了となる。
```
$ node -v
```

### npm,yarnのインストール手順
1. ターミナルを開き下記のコマンドを実行し、npmをインストールする。
```
$ sudo npm install -g npm
```
2. 下記コマンドを叩きnpmが正常にインストールされていることを確認する。
```
$ npm -v
```
3. 下記のコマンドを実行し、yarnをインストールする。
```
$ npm install -g yarn
```
4. 下記コマンドを叩きnpmが正常にインストールされていることを確認する。
```
$ yarn -v
```

### プロジェクト構築手順
1. ターミナルを開き、プロジェクトを配置する箇所まで移動し、下記コマンドを実行しGitHubからクローンする。
```
$ cd {プロジェクト配置箇所}
$ git clone https://github.com/N1112/myapp.git
```
2. 下記コマンドを実行し指定箇所まで移動し、必要なnpmパッケージをインストールする。
```
$ cd front
$ npm install
$ yarn
```
3. 下記コマンドを実行しサービスを起動する。
```
$ npm run dev
```
4. ブラウザにてhttp://172.21.27.135:3333/ を開き画面が確認できたら構築完了となる。

<img src='front/assets/image/site-page.jpg'>