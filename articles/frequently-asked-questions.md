---
title: よく寄せられる質問 | Microsoft Docs
description: Power Automate に関するいくつかの一般的な質問に回答します
services: ''
suite: flow
documentationcenter: na
author: stepsic-microsoft-com
manager: kvivek
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/07/2020
ms.author: stepsic
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 99a666c80cb1e6994b774f6b269d657a62996548
ms.sourcegitcommit: 27ee91452be26cf5c96397c39f9f5b8bede14cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/08/2020
ms.locfileid: "3299014"
---
# <a name="frequently-asked-questions"></a>よくあるご質問

## <a name="audience-and-strategy"></a>対象ユーザーと戦略
### <a name="what-is-power-automate"></a>Power Automate とは何ですか?
Power Automate はクラウドベースのサービスであり、基幹業務ユーザーは、アプリケーションやサービスにおいて時間のかかる業務タスクやプロセスを自動化するワークフローを構築できます。

### <a name="who-is-the-intended-audience-for-power-automate"></a>Power Automate はどのようなユーザーが対象ですか？
Power Automate には 2 つの異なるオーディエンスがあります：

* IT とパートナーシップを組み、ビジネス ソリューションの責任をビジネス自体につなげる企業組織内の基幹業務 “シチズン インテグレーター”。
* IT や統合の専門家たちが、Azure Logic Apps などのより高度な統合ツールに専門知識を活用できるよう、基幹業務パートナーには独自のソリューションを構築できる力を与えたい IT の意思決定者。

### <a name="how-do-power-automate-and-logic-apps-relate-to-each-other"></a>Power Automate と Logic Apps は互いにどのように関連していますか？
Power Automate では、基幹業務ユーザーがワークフローを自動化する機能を提供します。 Logic Apps は、Power Automate の強力な機能のみならず、Azure Resource Manager および Azure Portal との統合、PowerShell と xPlat CLI、Visual Studio、より多くのコネクタなどの機能も提供する Azure サービスです。 [Logic Apps の詳細については、こちらを参照してください](https://azure.microsoft.com/services/app-service/logic/)。

### <a name="how-does-power-automate-fit-in-microsofts-overall-business-application-platform-strategy"></a>Power Automate は、マイクロソフトのビジネス アプリケーション プラットフォーム戦略全体でどのような役割を果たしますか？
Power Automate は、強力で適応性のあるビジネス アプリケーション プラットフォームの一部であり、Power Apps、Common Data Service、Dynamics 365、Office 365 が含まれています。 Microsoft のお客様、パートナー、および ISV パートナーは、機能的な役割を果たす、または特定の地域に特化した専用のソリューションを、このプラットフォームで、自身の企業や業界専用に構築できます。 ビジネス要件を最もよく理解している基幹業務ユーザーは、データおよびプロセスを簡単に、分析、構成および合理化できるようになります。 プロフェッショナルな開発者は、自動化、分析、アプリの基幹業務を簡単に拡張して、Functions、App Service および Logic Apps などの Azure サービスを活用できます。 API コネクタ、ゲートウェイ、Common Data Service を使用すると、クラウドまたはオンプレミスのいずれかで、既に使用中のサービスやデータから、より多くのデータを引き出すことができるようになります。

## <a name="functionality"></a>機能
### <a name="what-do-i-need-to-use-power-automate"></a>Power Automateを使用するには何が必要ですか？
Power Automate を使用するには、Web ブラウザーおよび電子メール アドレスのみが必要です。

### <a name="what-browsers-and-devices-can-i-use-with-power-automate"></a>Power Automate ではどのようなブラウザーとデバイスに対応していますか？

Power Automate は、すべての最新のデバイスおよびブラウザーで使用できます。

#### <a name="supported-devices"></a>サポートされるデバイス

Power Automate最新のデバイスで良好に動作します。 モバイル デバイスから Power Automate を管理する必要がある場合は、[iPhone](https://itunes.apple.com/app/microsoft-flow/id1094928825?ls=1&mt=8)、[Android](https://play.google.com/store/apps/details?id=com.microsoft.flow)、[Windows Phone](https://www.microsoft.com/p/microsoft-flow/9nkn0p5l9n84?rtc=1#activetab=pivot:overviewtab) で利用可能な Power Automate モバイル アプリをお試しください。

#### <a name="supported-browsers"></a>サポートされているブラウザー

オペレーティング システムと互換性のある最新のブラウザーを使用することをお勧めします。 次のブラウザーがサポートされています。

* Microsoft Edge
* Internet Explorer 11
* Safari
* Chrome
* Firefox

### <a name="which-email-addresses-are-supported"></a>メール アドレスとしてサポートされているのは、どのようなものですか。
Power Automate は、末尾が .gov と .mil 以外のすべてのメール アドレスに対応しています。  

### <a name="is-power-automate-available-on-premises"></a>オンプレミスでは Power Automate に対応していますか？
Power Automate は、パブリック クラウド上のみのサービスです。 ただし、オンプレミス データ ゲートウェイを通じてオンプレミス サービスに安全に接続できます。

### <a name="what-services-can-power-automate-connect-to"></a>どのようなサービスが Power Automate に接続できますか？
Power Automate は最初から 100 以上のデータ ソースに接続できるようになっており、それらは追加され続けています。 データ ソースとサービスの例をいくつか次に示します。

* SharePoint
* Dynamics 365
* OneDrive
* OneDrive for Business
* Google ドライブ
* Google シート
* Trello
* Twitter
* Box
* Facebook
* SalesForce.com
* Mailchimp
* 顧客 API

使用可能なすべてのコネクタの一覧は、[こちら](https://go.microsoft.com/fwlink/?LinkId=832211)を参照してください。

[オンプレミス データ ゲートウェイ](gateway-manage.md)を介して自社の IT インフラストラクチャ上のデータ ソースにアクセスできます。

### <a name="what-are-templates"></a>テンプレートとは何ですか。
テンプレートとは、よく使用される一般的なシナリオ用に事前に作成されたフローのことです。 このテンプレートを使用するのに必要なのは、テンプレート内のサービスにアクセスできることと、必要な設定を入力することだけです。

### <a name="what-data-sources-will-i-be-able-to-connect-to"></a>どのデータ ソースに接続できますか。
Office 365、Twitter、SharePoint、OneDrive、Dropbox、SQL Server など、Microsoft とサード パーティの 100 以上の標準的なサービスに接続することができます。 Salesforce や Common Data Service などのプレミアム サービスに接続することもできます。

### <a name="how-do-i-connect-to-a-rest-api-in-my-flow"></a>フローで REST API に接続する方法を教えてください。
[カスタム コネクタ](developer/register-custom-api.md)を作成することで、JSON を使用し、10 を超える認証方法のうち少なくとも 1 つをサポートしている任意の REST API に接続できます。

### <a name="how-do-i-connect-to-sql-server-and-other-on-premises-data-sources"></a>SQL Server やその他のオンプレミス データ ソースに接続する方法を教えてください。
[オンプレミスのデータ ゲートウェイ](gateway-manage.md)を使用すると、ローカル ネットワーク上のサービスに接続できます。

### <a name="can-i-share-the-flows-i-create"></a>作成したフローは共有できますか。
以下の方法のいずれかでフローを共有することができます。

* フローの所有者として、組織の同僚やグループを追加することができ、同僚やグループがフローを編集したり管理したりすることができるようなります。
* 手動で実行できるフローでは、組織の他のユーザーまたはグループにフローの実行のみを許可することができます。

### <a name="how-many-flows-can-i-have"></a>所有できるフローの数を教えてください。
Power Automate には最大で 50 のフローが付属しています。 さらに必要な場合は、リクエストすることが可能です。

### <a name="where-do-i-get-started-with-power-automate"></a>Power Automate はどこから始めればいいのでしょうか？
次のリソースから開始できます。

* [ブログ](https://flow.microsoft.com)
* [YouTube チャンネル](https://youtube.com/playlist?list=PL8nfc9haGeb55I9wL9QnWyHp3ctU2_ThF)
* [トピック](getting-started.md)
* [コミュニティ](https://powerusers.microsoft.com)

### <a name="what-operating-systems-does-the-mobile-app-for-power-automate-support"></a>Power Automate のモバイル アプリが対応しているする OS は何ですか？
Power Automate モバイル アプリは、[Android](https://aka.ms/flowmobiledocsandroid)、[iOS ](https://aka.ms/flowmobiledocsios)、[Windows Phone](https://aka.ms/flowmobilewindows) で利用可能です。

### <a name="can-flows-be-turned-off-or-disabled"></a>フローをオフまたは無効にすることはできますか。

はい。各フローにはオン/オフ スイッチがあり、フローで要求が処理されないようにすることができます。

フローがオンに戻ったときにどのように反応するかについては、次の表を確認してください。

トリガーの種類|内容
-------|--------
ポーリング (**繰り返し**トリガーなど)|フローが再度オンになったときに、未処理/保留中のイベントがすべて処理されます。 保留中の項目を処理しない場合は、フローを削除します。
webhook|フローが再度オンになったときに処理されるのは、フローがオンになってから生成される新しいイベントのみです。

### <a name="what-regions-and-languages-does-power-automate-support"></a>Power Automate はどの地域と言語に対応していますか？
Power Automate は、42 の言語、[6 つの地域](regions-overview.md) で使用できます。

### <a name="how-does-power-automate-compare-to-sharepoint-designer-2013"></a>Power Automate とSharePoint デザイナー 2013 の違いは何ですか？
Power Automate は、承認、ドキュメントの校閲、オンボード/オフボードなど、多くの一般的なビジネス シナリオに対応する SharePoint Designer の後継サービスです。 これは、今後 SharePoint で業務を自動化させる既定のツールとなります。

### <a name="how-does-power-automate-ensure-that-corporate-data-isnt-accidentally-released-to-social-media-services"></a>Power Automate では企業のデータが誤ってソーシャル メディア サービスに公開されないようにするためにどのような対策が講じられていますか？
管理者は[データ損失防止ポリシー](prevent-data-loss.md)  を作成して、承認されたサービスのみが Power Automate で使用できるようにすることができます。

### <a name="does-power-automate-support-service-accounts"></a>Power Automate はサービス アカウントに対応していますか？

サービス アカウントを使用してフローを作成できますが、サービス アカウントの資格情報が共有されている場合、この操作は推奨されません。

## <a name="licensing"></a>ライセンス
### <a name="will-power-automate-still-have-a-free-or-trial-option"></a>Power Automate には無料版または試用版のオプションはありますか？
はい。 ユーザー権限に制限のある無料版の使用または、Power Automate の 90 日間試用版に登録することができます。 試用期間中は、いつでもサブスクリプションをアクティブにできます。

### <a name="what-pricing-plans-do-you-offer"></a>どのような価格プランのオファーがありますか。
Power Automate には、無料と有料の両方のサービス レベルが用意されています。 [価格の詳細については、こちらをご覧ください](billing-questions.md)。

## <a name="learn-more"></a>詳細はこちら

* Power Automate の [ガイド付き学習ツアー](https://docs.microsoft.com/learn/paths/automate-process-using-flow) を見る
* [入門ガイド](getting-started.md) で Power Automate の基本を学ぶ
