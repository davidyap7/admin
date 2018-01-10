---



copyright:

  years: 2015, 2017
lastupdated: "2017-12-07"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} への登録

{{site.data.keyword.Bluemix}} アカウントに登録するには、[{{site.data.keyword.Bluemix_notm}} ホーム・ページ](https://console.bluemix.net/)に移動して、**「フリー・アカウントの作成」**を選択します。既存の IBM ID を使用するか、新規 IBM ID を作成するか、フェデレーテッド ID を使用することができます。フェデレーテッド ID は、IBM に登録済みの会社ドメイン内の ID で、これにより、ドメインとユーザーの資格情報を使用して IBM Web アプリケーションにアクセスできます。
{:shortdesc}  

{: #federatedid}
お客様の会社が IBM への登録作業を完了している場合にのみ、フェデレーテッド ID で {{site.data.keyword.Bluemix_notm}} にアカウント登録できます。  会社のドメインを IBM に登録すると、会社の既存のユーザー資格情報で IBM の製品やサービスにログインできるようになります。 認証は、お客様の会社の ID プロバイダーによって処理されます。 フェデレーテッド ID で {{site.data.keyword.Bluemix_notm}} にログインすると、お客様の会社のログイン・ページを通じたログインを求められます。 会社または組織のドメインを IBM に登録するための申請、またはこのプロセスの詳細については、[IBMid Enterprise Federation Adoption Guide ![「外部リンク」アイコン](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window} を参照してください。 フェデレーテッド ID の登録を申請する際には、IBM のサポート役 (オファリング担当者やお客様担当者など) が必要です。

IBM では、この ID 連携のために Security Assertion Markup Language 2.0 (SAML 2.0) を利用しています。 SAML 2.0 は、セキュリティー・ドメイン間で認証データを交換するための標準版です。 これは XML ベースのプロトコルであり、アサーションが格納されたセキュリティー・トークンを使用して、組織の「ID プロバイダー」と「IBM Rely Party (RP)」 (サービス・プロバイダー) の間で情報を受け渡します。

| 登録方法 | 詳細 |    
|-----------------|---------|
|既存の IBM ID | IBM ID を既にお持ちの場合は、IBM の他の製品やサービスに使用する既存の資格情報で {{site.data.keyword.Bluemix_notm}} に登録します。 登録の際には、電話番号の入力が必要です。 |
|新しい IBM ID | IBM ID をまだお持ちではない場合は、その作成を選択できます。 IBM ID により、1 つのログイン・ユーザー名を、お客様が使用する IBM のすべての製品やサービス ({{site.data.keyword.Bluemix_notm}} を含む) に使用することが可能になります。 氏名や電話番号などの個人情報と、新しい資格情報のパスワードの入力が必要です。 IBM の他の製品やサービスを使用する際に、この IBM ID でログインできます。  |
|フェデレーテッド ID | お客様の会社が、そのドメインのユーザー資格情報を IBM に登録するための申請を完了している場合は、会社のログインに既に使用している資格情報で {{site.data.keyword.Bluemix_notm}} へのアカウント登録を行えます。 登録の際には、電話番号の入力が必要です。 |
{:caption="表 1. 登録方法" caption-side="top"}
