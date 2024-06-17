# ngrok installマニュアル(Windows版)
## １．はじめに

このページでは、「Windows」ユーザがngrokをインストールするための方法を学びます。

※そもそもngrokって・・・？？

- 簡単に説明すると、ローカルPC上で稼働しているネットワーク（TCP）サービスを外部公開できるサービスである。

参考：https://speakerdeck.com/gishi_yama/mild-web-sap06

## ２．準備

以下のURLからngrokのアカウントをサインアップしてください。

-> https://dashboard.ngrok.com/login

URLに飛ぶと、画像のような画面になるため、「***Sign up for free!***」をクリックする。

<img width="250" src="https://github.com/122yuuki/SA_install/blob/main/SA_file/image_1-1.png">  

次の画面に移動し、必要事項を入力して「***Sign up***」をクリックすることで、サインアップが完了する。

※メールアドレスは任意ではあるが、学校のアカウントを使用することをおすすめします。

<img width="250" src="https://github.com/122yuuki/SA_install/blob/main/SA_file/image_1-2.png">

入力が完了すると、画像のような画面が出るが「***Skip***」をクリック。

<img width="250" src="https://github.com/122yuuki/SA_install/blob/main/SA_file/image_1-3.png">

次の画面の「***got it***」をクリック。

突如アンケートのようなものがでるが、何も変更させずに「***continue***」をクリック。

正常にサインアップが完了すると、画像のようなダッシュボード画面が表示される。

<img src="https://github.com/122yuuki/SA_install/blob/main/SA_file/image_1-5.png">

## ３．authtokenについて

サインアップが完了したときに表示される画面を操作する。

ngrokのインストールはspring-boot側で行うため、インストール方法は割愛する。

1．メニューバーの「***Your AuthTokens***」をクリックする。

2．画像のように、トークンについての情報が表示される。もし画像のような情報が表示されていなければ、新たにトークンを作成するとよい。

3．様々な情報が書かれているが、「***your authtoken***」があなたのトークンである。

4．コピーできるため、コピーしておく。コピーしたIDは今後使用するため、記録しておく。

<img src="https://github.com/122yuuki/SA_install/blob/main/SA_file/image_token.png">


## ４．domainについて

１．メニューバーの「***Domains***」をクリックすると、画像のような画面になる。

２．「***+ Create Domain***」をクリックし、ドメインを作成する。

３．ドメインがされたら、ドメインの詳細情報が書かてれいる部分をクリックすると、右側に別のタブが表示される。

４．「***Domain***」がコピーできるようになっているため、コピーをする。

5．コピーしたものは今後使用するため、記録しておくように。

<img src="https://github.com/122yuuki/SA_install/blob/main/SA_file/image_domain.png">

## 補足

メニューバーの「***Usage***」から、ngrokの使用状況や制限について確認することができる。

> [!caution]
> 無償版のngrokを利用しているが、1つのアカウントにつき1ヶ月あたりの使用量は決まっているため、注意するようにしてください。

<img src="https://github.com/122yuuki/SA_install/blob/main/SA_file/image35.png">
