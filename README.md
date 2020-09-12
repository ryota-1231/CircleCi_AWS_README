# CircleCI ✖︎ AWSでCI/CDを体験しよう！！

![image](https://user-images.githubusercontent.com/66664167/92107539-ecf40280-ee20-11ea-8651-7261697f7995.png)


## はじめに
### CI/CDとは

CI/CDとは高度な継続的自動化と継続的監視をアプリケーション開発に取り組むこと、また、そのプロセスのこと

![image](https://user-images.githubusercontent.com/66664167/92073666-39264f00-edef-11ea-8e05-c9db7127b3e9.png)

<br>
<br>

### - 継続的インテグレーション　-

>継続的インテグレーションは、コードを共有リポジトリの master ブランチに常時頻繁に統合することを奨励する開発手法です。それぞれの機能を個別にビルドして、開発サイクルの最後に統合するのではなく、各開発者のコードが 1 日に何度も共有リポジトリに統合されます。
>すべての開発者が共有メインラインに毎日コミットします。コミットされるたびに、自動化されたビルドとテストがトリガーされます。ビルドやテストが失敗しても、数分以内にすばやく修復できます。
>チームの生産性、効率、満足度を向上させます。 問題をすばやく検出して解決できます。 より高品質で安定したプロダクトをリリースできます。
<br>
※　CircleCi公式ドキュメントより：https://circleci.com/docs/ja/2.0/about-circleci/#section=welcome
<br>

![image](https://user-images.githubusercontent.com/66664167/92101045-83232b00-ee17-11ea-89d9-38ee6caee2df.png)

<br>
※　技術評論社より：https://gihyo.jp/book/pickup/2015/0045
<br>

### - 継続的デリバリー -
>検証されたコードのリポジトリへのリリースを自動化します。継続的デリバリーの目標は、本番環境にデプロイできるコードベースを常に保持しておくことです。
継続的デリバリーでは、コード変更のマージから本番環境対応のビルドのデリバリーまで、すべてのステージでテストの自動化とコードリリースの自動化が実施されます。このプロセスの終了時には、運用チームはアプリケーションを本番環境にすばやく簡単にデプロイできます。
<br>

### - 継続的デプロイメント -
>成熟した CI/CD パイプラインの最終ステージは、継続的デプロイメントです。本番環境対応のビルドをコードリポジトリへ自動的にリリースする継続的デリバリーの延長として、継続的デプロイメントはアプリケーションを本番環境に自動的にリリースします。本番環境に移す前のパイプラインのステージでは手動でのチェックはないので、継続的デプロイメントは主に、入念に設計されたテスト自動化を活用します。
<br>
<br>

## なぜCI/CDなのか？
#### ・自動化テストの重要性の高まり<br>
これだけソフトウェアが普及していくと、品質に対する要求も高くなり、今まで手動でテストしていた分野でも積極的に自動化テストを取り入れるようになってきます。なぜならCI/CDを使うと、コードの変更が発生するたびに自動でテストが行われるので、テストの実行忘れや、環境依存のテストを失くすことでの品質を向上させることができるからです。

#### ・アジャイル開発のプラクティスの浸透と進化<br>
アジャイル開発で重要なことはスピードです。より小さな粒度の変更をいかに早くテスト／リリースしてフィードバックを得るかがアジャイル開発の成功の鍵となりますが、CI/CDを使うことでこれらを実現することができます。
<br>
<br>

## CI/CDツール選定
### Jenkins
![image](https://user-images.githubusercontent.com/66664167/92107197-5a536380-ee20-11ea-95b5-6488c0ecb79f.png)
#### メリット
- 拡張性が高い。プロジェクトに合わせてカスタマイズしやすい
- オンプレ上に構築するため、IPが固定される
- ドキュメントが豊富で調査しやすい

#### デメリット
サーバを用意する必要があるため、費用がかかる、準備に時間がかかる
本番を含めワークフローに組み込むため、導入は計画的に行う必要がある
保守・運用が必要なため管理を怠ると属人化しやすい


### TravisCI
![image](https://user-images.githubusercontent.com/66664167/92107394-a9999400-ee20-11ea-80af-30f183fb4802.png)
#### メリット
- Cloudであるため、サーバの管理・運用は不要になる
- Githubとの親和性高い
- ドキュメントが豊富で調査しやすい

#### デメリット
- コンテナにsshで入れないのでデバッグしにくい
- $129がかかるため、CIをはじめて導入する際には提案しにくい
- Cloudなのでビルドの度にIPが変わる


### CircleCI
![image](https://user-images.githubusercontent.com/66664167/92107539-ecf40280-ee20-11ea-8651-7261697f7995.png)

#### メリット
- Cloudであるため、サーバの管理・運用は不要
- 公式のサポートが手厚い
- ドキュメントが豊富で調査しやすい
- sshでコンテナに入れるので、デバッグしやすい
- 無料で使い始められる

#### デメリット
- Clouldなのでビルドの度に毎回IPが変わる
- GitHubまたはBitbucketとの連携が前提


## ★　今日やること　★
### 1.目的
------------------------------------整える-----------------------------------------
![image](https://user-images.githubusercontent.com/66664167/92490881-8447c400-f22c-11ea-9e32-5fdcdd313832.png)

### 2.今日のゴール



### 3.環境・言語



### 4.事前準備
- AWS アカウント作成
- AWS EC2インスタンの起動　[設定方法はこちら](https://github.com/miracleave-ltd/aws_ec2)
- Git インストール
- Docker　インストール
- docker-compose インストール
- GitHub アカウント作成


## .やってみよう！

### 1. リポジトリを作成
#### 1-1 GitHubにアクセスする
[こちらからリポジトリにアクセス](https://github.com/miracleave-ltd/meet-up_CI-CD)

#### 1-2 FORKする
![image](https://user-images.githubusercontent.com/66664167/92986631-54801100-f4f7-11ea-94f1-bc27cf0c8d77.png)

##### 「ユーザー名/meet-up_CI-CD」になっていることを確認する。（自分のリポジトリとして管理できる状態になる）
![image](https://user-images.githubusercontent.com/66664167/92986668-8b562700-f4f7-11ea-9a81-80b527403d6d.png)

#### 1-3 ローカルの任意の場所にクローンする
※ターミナル（コマンドプロンプト)を使用します。

##### 1-3-1 「Code」ボタンを押下して、リポジトリのURLをコピーする
![image](https://user-images.githubusercontent.com/66664167/92986964-6e225800-f4f9-11ea-9dbb-5daae9c512dd.png)

##### 1-3-2 ターミナルを使用して、任意の場所にクローンする

```
例：デスクトップに作成する場合
$ cd ~/Desktop
// 先ほどコピーしたURLを貼り付けて実行する
$ git clone https://github.com/[ユーザー名]/[リポジトリ名].git
```

※以降、こちらの手順書ではDesktopにリポジトリがある想定でコマンドのパスを表記します


### 2. 初期設定
Laravelのライブラリパッケージ等をdockerコンテナ内にインストールする

#### 2-1 コンテナを立ち上げる
```
~/Desktop/meet-up_CI-CD$ docker-compose up -d
```

#### 2-2 dockerコンテナに入る
```
~/Desktop/meet-up_CI-CD$ docker-compose exec app bash
```

#### 2-3 アプリの実行に必要なインストール・設定をする
```
~/Desktop/meet-up_CI-CD$ cd my-laravel-app && composer install && cp ../docker/laravel/.env .env && chmod 777 -R storage/ && php artisan key:generate && php artisan config:cache && php artisan migrate 
```

#### 2-4 コンテナを抜ける
```
~/Desktop/meet-up_CI-CD$ exit 
```

#### 2-5 コンテナを再起動する 
```
~/Desktop/meet-up_CI-CD$ docker-compose down && docker-compose up
```


### 3.EC2の設定
#### 3-1 EC2の設定をする
(https://github.com/miracleave-ltd/aws_ec2)
##### ※「インスタンスの詳細を設定する」という画面で【ユーザーデータ】という項目があるので、そこに下記のファイルの内容を設定する
```
#!/bin/bash
# Dockerをインストール
sudo yum update -y
sudo yum install -y docker
sudo service docker start
sudo chkconfig docker on
sudo usermod -a -G docker ec2-user
# docker-composeをインストール
sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
# gitインストール
sudo yum install -y git
```

#### 3-2 EC２に接続する
```
// EC2にログイン
$ ssh -i ~/.ssh/[pem key名] [ユーザー名]@[IP]<br>
```

#### 3-3 リポジトリをcloneする
```
// EC2インスタンス内で実行
$ git clone https://github.com/{ユーザー名}/{リポジトリ}.git
```

#### 3-4 コンテナを立ち上げる
```
// EC2インスタンス内で実行
$ cd meet-up_CI-CD<br>
$ docker-compose up -d<br>
```

#### 3-5 アプリの実行に必要なインストール・設定をする
```
// EC2インスタンス内で実行
$ docker-compose exec app bash
$ cd my-laravel-app && composer install && cp ../docker/laravel/.env .env && chmod 777 -R storage/ && php artisan key:generate && php artisan config:cache && php artisan migrate
```

#### 3-6 コンテナを抜け、再起動する
```
// EC2インスタンス内で実行
$ exit
$ docker-compose restart
```

### 4 CircleCIの設定
#### 4-1 ログインする
https://circleci.com/ja/vcs-authorize/

![image](https://user-images.githubusercontent.com/66664167/92234453-095d7100-eeed-11ea-8730-beb61574538a.png)


#### 4-2 該当プロジェクトの設定をする
##### 4-2-1 該当プロジェクトの「Set Up Project」を押下する
![image](https://user-images.githubusercontent.com/66664167/92300453-c6a3a380-ef95-11ea-8aee-ab2a4078691c.png)

##### 4-2-2 「Use Existing Config」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92300489-2ac66780-ef96-11ea-922c-d56902bea456.png)

##### 4-2-3 「Start Building」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92300523-7aa52e80-ef96-11ea-8856-8511d7febf14.png)

#### 4-3 EC2インスタンスと関連付ける
テストが開始される（各種設定前なのでFAILDになるが問題ありません）
##### 4-3-1 「Project Setting」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92300761-7417b680-ef98-11ea-9a75-a0ae99371953.png)

##### 4-3-2 メニューの「SSH Keys」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92300833-16379e80-ef99-11ea-87de-99bc615f8c53.png)

##### 4-3-3 ターミナルを開き、EC2インスタンスにログインして、SSH Keyをコピーする

> // EC2にログイン<br>
> $ ssh -i ~/.ssh/[pem key名] [ユーザー名]@[IP]<br>

> // SSH Keyが表示される<br>
> $ cat ~/.ssh/id_rsa

コピーする
![image](https://user-images.githubusercontent.com/66664167/92301975-2d7b8980-efa3-11ea-9ab9-461ff58fa09b.png)


##### 4-3-4 ページ下部の「Add SSH Keys」ボタンを押下すし、IPアドレスとコピーしたKeyを入力する
![image](https://user-images.githubusercontent.com/66664167/92301125-d58d5480-ef9b-11ea-9f27-ee3ce9b92fdc.png)
![image](https://user-images.githubusercontent.com/66664167/92302429-23f42080-efa7-11ea-8730-1d28548e33ef.png)

##### 入力した内容が表示されていることを確認する（Keyは変換されて表示されているため、実際の入力した内容と表示は異なります）
![image](https://user-images.githubusercontent.com/66664167/92482470-9de40e00-f222-11ea-8bcb-78bb6130ccd5.png)


#### 4-4 環境変数を設定する
##### 4-4-1 メニューの「Organization Settings」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92302693-0d4ec900-efa9-11ea-9f7f-e80315837035.png)

##### 4-4-2 メニューの「Contexts」を選択（初期画面）し、「Create Context」を押下する
![image](https://user-images.githubusercontent.com/66664167/92478693-7f2f4880-f21d-11ea-8415-d0338347fc9f.png)

##### 4-4-3 「Context Name」に任意の名前を入力し、「Create Context」を押下する（例：meet-up）
![image](https://user-images.githubusercontent.com/66664167/92479021-f95fcd00-f21d-11ea-9058-81509b3171a5.png)

##### 4-4-4 前画面に戻るので、入力した名前があるか確認し、該当のNameを押下する
![image](https://user-images.githubusercontent.com/66664167/92479460-87d44e80-f21e-11ea-947a-5a8ed7b8e1f9.png)

##### 4-4-5 「Add Environment Variables」を押下する
![image](https://user-images.githubusercontent.com/66664167/92479794-f6191100-f21e-11ea-8d4a-ade01ec2fd12.png)

##### 4-4-6 「Environment Variable Name」と「Value」にそれぞれ下記の通り入力し、 「Add Environment Variables」を押下する

① Environment Variable Name: USER_NAME<br>
　 Value: EC2インスタンスのユーザー名（例：ec2-user）
  
② Environment Variable Name: HOST_NAME<br>
　 Value: EC2インスタンスのIPアドレス

![image](https://user-images.githubusercontent.com/66664167/92480545-01b90780-f220-11ea-9379-feb90dc1c7c3.png)

###### 入力後の画面にてそれぞれName,Valueが入っていることを確認する
![image](https://user-images.githubusercontent.com/66664167/92481230-0205d280-f221-11ea-8325-9c25d2ba924f.png)

<br>

#### 設定完了！お疲れ様でした！
#### ここからいよいよCI/CD体験をしていきましょう！

<br>

### 5 ローカルで変更を加えてCI/CDの動作を確認する

#### 5-1 ローカルのクライアントソースで任意の場所を変更し、リポジトリにpushする。

##### 例：　ヘッダーのボタンをそれぞれ「登録」「一覧」から「登録ボタン」「一覧ボタン」に変更する。
##### Before
![image](https://user-images.githubusercontent.com/66664167/92484565-ccfb7f00-f224-11ea-9d07-dc6482b7fc82.png)

##### After
![image](https://user-images.githubusercontent.com/66664167/92484786-0df39380-f225-11ea-9a7f-6a22c5627b00.png)


##### 5-1-1 ソース変更後、変更をリポジトリにpushする。

> $ git add .<br>
> $ git commit -m "fix"<br>
> $ git push
 
##### 5-1-2 CircleCIを確認する

「Running」状態になっている
![image](https://user-images.githubusercontent.com/66664167/92486011-94f53b80-f226-11ea-901c-332e524ab23a.png)

時間が経つと「Success」になる
![image](https://user-images.githubusercontent.com/66664167/92486333-ed2c3d80-f226-11ea-88da-f35f6aabad27.png)


##### 5-1-3 CircleCIで「Success」後、ブラウザで確認する。
変更が反映されている！
![image](https://user-images.githubusercontent.com/66664167/92484786-0df39380-f225-11ea-9a7f-6a22c5627b00.png)


#### 5-2 テストが失敗した状態を体験する
##### 5-2-1 テストコードをテストが失敗するように編集する(例：あるURLにgetリクエストした際のレスポンススタッツで200が返ってくる想定の箇所で、500を設定する）

![image](https://user-images.githubusercontent.com/66664167/92488026-ff0ee000-f228-11ea-82b1-219101bdc322.png)


##### 5-2-2 ソース変更後、変更をリポジトリにpushする。

> $ git add .<br>
> $ git commit -m "fix"<br>
> $ git push


##### 5-2-3 CircleCIを確認する

「Faild」になる
![image](https://user-images.githubusercontent.com/66664167/92488378-6f1d6600-f229-11ea-94be-b955b8ced24e.png)

##### 5-2-4 「Faild」→「失敗箇所（今回は「build」）」を押下して、ログを確認する
![image](https://user-images.githubusercontent.com/66664167/92490179-a9880280-f22b-11ea-9328-d6d81766cfa6.png)











CI/CD パイプラインのさまざまなテストおよびリリースステージに合わせて自動化されたテストを作成する必要があるため、まとまった事前の投資も必要です。
