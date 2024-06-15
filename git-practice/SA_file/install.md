# ngrok installマニュアル(Windows版)
## １．はじめに

このページでは、「Windows」ユーザがngrokをインストールするための方法を学びます。

※そもそもngrokって・・・？？

- 簡単に説明すると、ローカルPC上で稼働しているネットワーク（TCP）サービスを外部公開できるサービスである。

参考：https://qiita.com/mininobu/items/b45dbc70faedf30f484e

## ２．準備

以下のURLからngrokのアカウントをサインアップしてください。

-> https://dashboard.ngrok.com/login?state=8auND9VLdlsYOyjzFQ5igYc6nAy2ylcAaeJrn5Oq_NRXewK2PcDZfDP9gFMguOshE3N3oiBTTgH7C5YKi1ryHRq7JyQaZPjlJpl7WjVQq_6Yk--2CoAjBNbaX_BXzc9Tmi_8Y-N2zRBYxwq-Bj228f-Qg2I%3D

URLに飛ぶと、画像のような画面になるため、「***Sign up for free!***」をクリックする。

<img width="250" src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_1-1.png">  

次の画面に移動し、必要事項を入力して「***Sign up***」をクリックすることで、サインアップが完了する。

※メールアドレスは任意ではあるが、学校のアカウントを使用することをおすすめします。

<img width="250" src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_1-2.png">

入力が完了すると、画像のような画面が出るが「***Skip***」をクリック。

<img width="250" src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_1-3.png">

次の画面の「***got it***」をクリック。

突如アンケートのようなものがでるが、何も変更させずに「***continue***」をクリック。

正常にサインアップが完了すると、画像のようなダッシュボード画面が表示される。

<img src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_1-5.png">

## ３．ngrokのインストール

サインアップが完了したときに表示される画面を操作する。

１．メニューバーの「***Setup & Installation***」をクリック。

２．「1 Connect」の中に「***Installation***」がある。そのなかの「***Download***」をクリックする。すると、ファイルがダウンロードできるようになっている。

３．「***Download for Windows(64-Bit)***」をクリックすることで、ファイルのダウンロードが開始される(数分で完了)。「***ngrok-v3-stable-windows-amd64***」のような名前のzipファイルがダウンロードされていることを確認する。

<img src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_2-1.png">

ダウンロードされたzipファイルを解凍し、ファイル内にある「***ngrok.exe***」をクリックし起動させる。

正常起動できると、コマンドプロンプトのような画面が表示される。

ngrokが起動できたら、以下の画像の赤枠のコマンドをコピーし、コピーしたコマンドをngrokでペーストする。

<img src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_2-2.png">

実行すると、
```
Authtoken saved to configuration file: 保存先
```
のようなメッセージが表示されることを確認する。

ngrokで、以下のコマンドを入力する。
```
ngrok http http://localhost:8080
```

実行すると、以下の画像のようになることを確認する。

<img src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_2-3.png">


## ４．URL固定方法

１．メニューバーの「***Domains***」をクリックすると、画像のような画面になる。

２．「***+ Create Domain***」をクリックし、ドメインを作成する。

３．ドメインがされたら、ドメインの詳細情報が書かてれいる部分をクリックすると、右側に別のタブが表示される。

４．「***Domain***」がコピーできるようになっているため、コピーをする。

<img src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_3-2.png">
<img src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_3-3.png">

ngrokで、以下のようにコマンドを入力する。
```
ngrok http --region=jp --domain=コピーしたドメイン 8080
```

実行すると、以下の画像のようになることを確認する。

<img src="https://github.com/122yuuki/git-practice/blob/master/SA_file/image_3-4.png">


## 補足

URLを固定しないときと固定したときの違いがあまりわからないと思う。

「***Forwarding***」に書かれているURLを比較してみてほしい。
```
ngrok http http://localhost:8080
```
で何回か実行してURLを確認したとき、```.ngrok-free.app```の前の数字が毎回異なっていることが確認できる。

一方で、ドメインを使用してポートをオンライン状態にしたときは、ドメインを使用しているので```.ngrok-free.app```の前の値が一定であることが確認できると思う。
