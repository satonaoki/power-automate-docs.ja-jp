---
title: Power Automate 米国政府機関
description: Power Automate US Government サービスの説明、プラン、および制限事項について説明します
services: ''
suite: flow
author: msftman
ms.service: flow
ms.devlang: na
ms.topic: article
ms.date: 08/30/2019
ms.author: deonhe
search.app:
- Flow
- Powerplatform
search.audienceType:
- admin
ms.openlocfilehash: 78e90d05ba57cc73264a2914de06feb3be3dd640
ms.sourcegitcommit: 5b1965a0c319c4294b7dc0c829120ed1f4f90444
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2020
ms.locfileid: "82153373"
---
# <a name="power-automate-us-government"></a>Power Automate 米国政府機関


米国公共部門の進化し続けるユニークな要望に応じて、Microsoft は Power Automate US Government プランを作成しました。 このセクションでは、Power Automate US Government に固有の機能に関する概要を説明します。 この補助セクションと、Power Automate サービスの[概要](https://docs.microsoft.com/flow/getting-started)トピックをお読みになることをお勧めします。 短く表現するために、このサービスは一般に *Flow GCC* と呼ばれます。

Power Automate US Government サービスの説明は、一般的な Power Automate サービスの説明を基にして書かれています。 ここでは、2016 年 10 月からお客様に提供されている一般的な Power Automate オファリングと比較して、ユニークなコミットメントと差異が定義されています。

## <a name="about-power-automate-us-government-environments-and-plans"></a>Power Automate US Government の環境とプランについて

Power Automate US Government プランは月次サブスクリプションであり、無制限の数のユーザーにライセンスを付与することができます。

Power Automate の GCC 環境は、FedRAMP High や DoD DISA IL2 などの、クラウド サービス向けの連邦の要件に準拠しています。 また、これは刑事司法制度 (CJI データ型) の要件にも準拠しています。

Power Automate US Government を使う組織は、Power Automate の機能に加えて、次の固有の機能を利用できます。

- 組織の顧客コンテンツは、Power Automate の商用オファリングの顧客コンテンツから物理的に分離されます。

- 組織の顧客コンテンツは、米国内に格納されます。

- 組織の顧客コンテンツへのアクセスは、Microsoft の選ばれた職員に限定されます。

- Power Automate US Government は、米国公共部門の顧客が要求するすべての認証や認定に準拠します。

2019 年 9 月以降、対象となるお客様は、**GCC High** 環境に Power Automate US Government をデプロイできます。これにより、シングル サインオンおよび Microsoft Office 365 の GCC High デプロイとのシームレスな統合が可能になります。 

Microsoft では、DISA SRG IL4 コンプライアンス フレームワークに沿った要件を満たすプラットフォームと運用手順を設計しました。 米国国防総省契約顧客ベースや、現在 Office 365 GCC High を利用している他の連邦政府機関が、Power Automate US Government GCC High デプロイ オプションを使用することを想定しています。 このオプションを選択すると、パブリック Azure AD を利用する GCC とは対照的に、お客様は顧客 ID に Azure AD Government を利用できるようになり、それが必要になります。 米国国防総省契約顧客ベースの場合、Microsoft が運用するサービスでは、これらのお客様は、米国国防総省との契約による規定および要求に従って、ITAR コミットメントおよび DFARS 獲得規則を満たすことができます。

## <a name="customer-eligibility"></a>顧客の適格性

Power Automate US Government を利用できるのは、(1) 米国連邦、州、地方、部族、地域の政府機関、および (2) 政府の規制や要件の対象となるデータを扱い、これらの要件を満たすために Power Automate US Government の使用が適切であるようなその他の機関であり、適格性の検証を必要とします。 Microsoft の適格性の検証には、国際武器取引規則 (ITAR) の対象となるデータ、FBI の Criminal Justice Information Services (CJIS) ポリシーの対象となる法執行データ、または政府によって規制または制御されるその他のデータの取り扱いの確認が含まれます。 検証には、データの取り扱いに関する特定の要件を伴う政府機関の公的支援が必要となる場合があります。

Power Automate US Government の適格性についてご不明な点がある機関は、各自のアカウント チームに問い合わせてください。 Microsoft は、Power Automate US Government の顧客契約の更新時に、適格性を再検証します。

## <a name="power-automate-us-government-plans"></a>Power Automate US Government プラン

Power Automate US Government プランへのアクセスは、以下のセクションで示すオファリングに制限されます。各プランは月単位のサブスクリプションとして提供され、無制限の数のユーザーにライセンスを付与することができます。

- Power Automate/Power Apps プラン 1 US Government

- Power Automate/Power Apps プラン 2 US Government

- Power Automate と Power Apps の機能は、スタンドアロン プランだけでなく特定の Office 365 US Government および Dynamics 365 US Government プランにも含まれ、顧客は Power Automate と Power Apps の機能を使って Office 365 と Dynamics 365 を拡張およびカスタマイズできます。

> [!NOTE]
> ライセンスは、2019 年 4 月中旬から顧客テナントで利用できます。

これらのライセンスのグループ間の機能の違いに関する追加情報と詳細については、ここで詳しく説明されています:[Power Automate ライセンス情報](https://flow.microsoft.com/pricing/)。

Power Automate US Government は、ボリューム ライセンスおよびクラウド ソリューション プロバイダーの購入チャンネルを通じて取得できます。

## <a name="differences-between-customer-data-and-customer-content"></a>顧客データと顧客コンテンツの違い

オンライン サービス条件で定義されているように、顧客データとは、あらゆるテキスト、音声、動画、画像ファイルを含むすべてのデータと、顧客により、または顧客の代わりに、オンライン サービスの使用を通じて Microsoft に提供されるソフトウェアを意味します。

顧客コンテンツは、ユーザーが直接作成した顧客データの特定のサブセットを指します。たとえば、[Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) エンティティのエントリを通じてデータベースに格納されるコンテンツなどです (例: 連絡先情報)。 一般的に、コンテンツは機密情報と見なされ、通常のサービス運用では、暗号化せずにインターネットを介して送信されることはありません。

Power Automate による顧客データの保護方法について詳しくは、[Microsoft オンライン サービス セキュリティ センター](https://www.microsoft.com/trustcenter/cloudservices/business-application-platform/default.aspx)をご覧ください。

## <a name="data-segregation-for-government-community-cloud"></a>Government Community Cloud のデータ分離

Power Automate US Government の一部としてプロビジョニングされた場合、Power Automate サービスは、National Institute of Standards and Technology (NIST) Special Publication 800-145 に従って提供されます。

Microsoft では、Government Community Cloud (GCC) としてこのオファーを参照します。

Power Automate Government サービスでは、アプリケーション レイヤーでの顧客コンテンツの論理的な分離だけでなく、商用の Power Automate の顧客向けに使われるインフラストラクチャから分離されたインフラストラクチャを使うことで、顧客コンテンツ用にセカンダリ レイヤーの物理的な分離が組織に提供されます。 これには、Azure の Government Cloud 内の Azure サービスの使用が含まれます。 詳細については、「[Azure Government](https://azure.microsoft.com/global-infrastructure/government/)」をご覧ください。

## <a name="customer-content-located-within-the-united-states"></a>米国内にある顧客コンテンツ

Power Automate US Government は、物理的に米国内にあるデータセンターで運用され、物理的に米国内にあるデータセンターにのみ顧客コンテンツを格納して保存します。

## <a name="restricted-data-access-by-administrators"></a>管理者による制限付きのデータ アクセス

Microsoft 管理者による Power Automate US Government の顧客コンテンツへのアクセスは、米国市民である職員に制限されています。 これらの職員には、関連する政府基準に従って身元調査が実施されます。

Power Automate のサポートとサービスに関するエンジニアリング スタッフは、Power Automate US Government でホストされる顧客コンテンツに継続的にアクセスすることができません。 顧客コンテンツにアクセスできるようになる一時的なアクセス許可の昇格を要求したスタッフは、必ず最初に次の身元調査をパスする必要があります。

|Microsoft 職員の審査と身元調査 <sup>1</sup>| Description|
|---------------------------------------------------------------|-----------------------------------|
| 米国市民権| 米国市民権の確認 |
| 職歴調査| 7 年間の職歴の確認|
| 学歴の確認 | 最終学歴の確認|
| 社会保障番号 (SSN) の検索| 職員が指定した SSN が有効であることの確認|
| 犯罪歴の調査| 州、国、地方レベルおよび連邦レベルでの、重罪および軽犯罪に関する 7 年間の前科の調査|
| 外国資産管理局のリスト (OFAC)| 米国人が取引や金融取引に関与することを禁じられているグループの財務省のリストの確認|
| 産業安全保障局のリスト (BIS)| 輸出活動への関与を禁じられている個人および団体の米商務省のリストの確認|
| 国防貿易管理局の禁止対象リスト (DDTC) | 軍需産業に関する輸出活動への関与を禁じられている個人および団体の国務省のリストの確認|
| 指紋による調査| FBI のデータベースに対する指紋の身元調査|
| CJIS 身元審査| Microsoft CJIS IA プログラムに参加している各州内の州 CSA 指定機関による、連邦および州の犯罪歴の州裁定再調査 |

<sup>1</sup> Power Automate US Government (GCC) でホストされている顧客コンテンツへの一時的または永続的なアクセス権を持つ職員に対してのみ適用されます。

## <a name="certifications-and-accreditations"></a>認証と認定

Power Automate US Government は、高い影響レベルで Federal Risk and Authorization Management Program (FedRAMP) 認定をサポートするよう設計されています。 このプログラムは、DoD DISA IL2 との連携を示します。 FedRAMP の成果物は、FedRAMP への準拠を要求されている連邦の顧客が確認用に利用できます。 連邦政府機関は、Authority to Operate (ATO) を付与するための確認の裏付けとして、これらの成果物を調査できます。

> [!NOTE]
> 現在、Power Automate US Government サービスは FedRAMP の確認中ですが、正規の [3PAO](https://www.fedramp.gov/3pao-requirements-update/) により Security Assessment Report (SAR) を付与されています。

標準的な監査サイクルの一部として Microsoft が移行して FedRAMP 成果物を更新すると、それに応じてコンテンツが更新されます。

Power Automate US Government には、法執行機関向けの顧客の CJIS ポリシー要件をサポートするために設計された機能があります。 認証と認定について詳しくは、セキュリティ センターにある Power Automate US Government の製品ページをご覧ください。

Microsoft では、DISA SRG IL4 コンプライアンス フレームワークに沿った要件を満たすプラットフォームと運用手順を設計しました。 Microsoft は、米国国防総省契約顧客ベースや、現在 Microsoft Office 365 GCC High を利用している他の連邦政府機関が、Power Automate US Government GCC High デプロイ オプションを使用することを想定しています。このオプションを選択すると、パブリック Azure AD を利用する GCC とは対照的に、お客様は顧客 ID に Azure AD Government を利用できるようになり、それが必要になります。 米国国防総省契約顧客ベースの場合、Microsoft が運用するサービスでは、これらのお客様は、ITAR コミットメントおよび DFARS 獲得規則を満たすことができます。

## <a name="power-automate-us-government-and-other-microsoft-services"></a>Power Automate US Government とその他の Microsoft サービス

Power Automate US Government には、ユーザーが他の Microsoft エンタープライズ サービス内容 (Office 365 US Government、Dynamics 365 US Government、Power Apps US Government など) と接続したり統合したりできるようになる機能がいくつか含まれています。

Power Automate US Government は、Microsoft データセンター内で、マルチテナント、パブリック クラウド デプロイ モデルと一貫性のある方法で運用されています。ただし、Power Automate モバイル アプリケーション (利用可能な場合) を含む (ただし Web ユーザー クライアントに制限されるわけではありません) クライアント アプリケーションや、Power Automate US Government に接続する任意のサード パーティ製クライアント アプリケーションは、Power Automate US Government の認定境界に含まれません。 政府機関の顧客がそれらの管理を担当します。

Power Automate US Government では、顧客の管理と課金のために Office 365 の顧客管理者 UI を活用します。

Power Automate US Government は実際のリソース、情報フロー、データ管理を維持する一方で、Office 365 に依存して、管理コンソールを通じて顧客管理者に表示されるビジュアル スタイルを提供します。 FedRAMP ATO の継承のために、Power Automate US Government では、インフラストラクチャとプラットフォーム サービスそれぞれのために Azure (Azure for Government を含む) ATO を活用します。

Active Directory フェデレーション サービス (AD FS) 2.0 の使用を採用し、ポリシーを設定してユーザーがシングル サインオンを使ってサービスに接続できるようにする場合は、一時的にキャッシュされている顧客コンテンツがすべて米国内に配置されます。

## <a name="power-automate-us-government-and-third-party-services"></a>Power Automate US Government とサード パーティのサービス

Power Automate US Government には、[コネクタ](https://docs.microsoft.com/connectors/index)を使ってサード パーティのアプリケーションをサービスに統合する機能が用意されています。 これらのサード パーティ製のアプリケーションおよびサービスでは、Power Automate US Government インフラストラクチャの外部にあるサード パーティのシステム上で組織の顧客データの格納、送信、処理を行う場合があります。そのため、これらは Power Automate US Government のコンプライアンスおよびデータ保護のコミットメントの対象ではありません。

> [!TIP]
> ご自身の組織に対してこれらのサービスの適切な使用を評価する場合、サード パーティによって提供されるプライバシーとコンプライアンスのステートメントを確認してください。

## <a name="power-automate-us-government-and-azure-services"></a>Power Automate US Government と Azure サービス

Power Automate US Government サービスは、Microsoft Azure Government にデプロイされます。 Azure Active Directory (Azure AD) は Power Automate US Government の認定境界に含まれませんが、顧客のテナントと ID 機能のために、顧客の [Azure AD](https://azure.microsoft.com/services/active-directory/) テナントに依存します (認証、フェデレーション認証、ライセンスなど)。

ADFS を使用している組織のユーザーが Power Automate US Government にアクセスしようとすると、そのユーザーは組織の ADFS サーバー上でホストされているログイン ページにリダイレクトされます。

ユーザーは、その組織の ADFS サーバーに自分の資格情報を提供します。 組織の ADFS サーバーでは、組織の Active Directory インフラストラクチャを使用してその資格情報の認証を試みます。

認証が成功した場合は、組織の ADFS サーバーによって、ユーザーの ID とグループのメンバーシップに関する情報を含む SAML (Security Assertion Markup Language) チケットが発行されます。

顧客の ADFS サーバーによって、非対称キー ペアの片方を使ってこのチケットが署名され、その後暗号化された TLS を経由して Azure AD にチケットが送信されます。 Azure AD では、非対称キー ペアのもう片方を使って署名を検証し、その後チケットに基づくアクセス権を付与します。

Azure AD では、ユーザーの ID とグループのメンバーシップに関する情報は暗号化されたままです。 つまり、ユーザーを特定できる一部の情報のみが Azure AD に格納されます。

Azure SSP では、Azure AD のセキュリティ アーキテクチャの完全な詳細情報を検索し、実装を把握できます。

Azure AD のアカウント管理サービスは、Microsoft Global Foundation Services (GFS) によって管理されている物理サーバー上でホストされています。 これらのサーバーへのネットワーク アクセスは、GFS で管理されたネットワーク デバイスによって、Azure で設定された規則を使って制御されます。 ユーザーが Azure AD と直接対話することはありません。

## <a name="power-automate-us-government-service-urls"></a>Power Automate US Government サービス URL

次の表に示すように、Power Automate US Government 環境にアクセスするには、異なる URL のセットを使用します。 表には、使い慣れているお客様のために、コンテキスト参照のための商用 URL も含まれています。


商用バージョン | US Government バージョン
------ | --------
[https://flow.microsoft.com](https://flow.microsoft.com) | [https://gov.flow.microsoft.us (GCC)](https://gov.flow.microsoft.us) および [https://high.flow.microsoft.us (GCC High)](https://high.flow.microsoft.us)
[https://admin.flow.microsoft.com](https://admin.flow.microsoft.com) | [https://gov.admin.flow.microsoft.us (GCC)](https://gov.admin.flow.microsoft.us) および [https://high.admin.flow.microsoft.us (GCC High)](https://high.admin.flow.microsoft.us)
[https://flow.microsoft.com/connectors](https://flow.microsoft.com/connectors) | [https://gov.flow.microsoft.us/connectors (GCC)](https://gov.flow.microsoft.us/connectors) および [https://high.flow.microsoft.us/connectors (GCC High)](https://high.flow.microsoft.us/connectors)


ネットワーク制限を実装しているお客様については、エンド ユーザーのアクセス ポイントで次のドメインへのアクセスを利用できることを確認してください。

### <a name="gcc-customers"></a>GCC のお客様:
* .microsoft.us
* .azure-apihub.us
* .azure.us
* .usgovcloudapi.net
* .microsoftonline.com
* .microsoft.com
* .windows.net
* .azureedge.net
* .azure.net
* .crm9.dynamics.com

ユーザーおよび管理者がお客様のテナント内に作成できる Common Data Service インスタンスにアクセスできるようにするには、AzureCloud.usgovtexas および AzureCloud.usgovvirginia に対する [IP 範囲](https://www.microsoft.com/download/confirmation.aspx?id=57063)を参照してください。 

### <a name="gcc-high-customers"></a>GCC High のお客様:
* .microsoft.us
* .azure-apihub.us
* .azure.us
* .usgovcloudapi.net
* .microsoftonline.us
* .azureedge.net
* .azure.net
* .crm.microsoftdynamics.us

ユーザーおよび管理者がお客様のテナント内に作成できる Common Data Service インスタンスにアクセスできるようにするには、AzureCloud.usgovtexas および AzureCloud.usgovvirginia に対する [IP 範囲](https://www.microsoft.com/download/confirmation.aspx?id=57063)を参照してください。 


## <a name="connectivity-between-power-automate-us-government-and-public-azure-cloud-services"></a>Power Automate US Government とパブリック Azure Cloud Services 間の接続

Azure は複数のクラウドに分散されます。 既定では、テナントでクラウド固有のインスタンスに対するファイアウォール規則を開くことが許可されていますが、クラウド間ネットワークの場合は異なり、サービス間で通信するために特定のファイアウォール規則を開く必要があります。 Power Automate のお客様で、アクセスする必要がある Azure パブリック クラウドに既存の SQL インスタンスがある場合、次のデータセンターのために、Azure Government Cloud IP 空間に対する特定のファイアウォール ポートを SQL で開く必要があります。

- USGov バージニア州
- USGov テキサス

AzureCloud.usgovtexas と AzureCloud.usgovvirginia に注目しながら、[Azure IP 範囲とサービス タグ – US Government Cloud](https://www.microsoft.com/download/confirmation.aspx?id=57063) のドキュメントを参照してください。 また、これらが、エンドユーザーがサービス URL にアクセスするために必要な IP 範囲であることにも注意してください。

## <a name="on-premises-data-gateway-configuration"></a>オンプレミス データ ゲートウェイの構成

Power Automate 内に構築されたキャンバス アプリと、クラウド内にないデータ ソースの間ですばやく安全にデータを転送するために、[オンプレミス データ ゲートウェイ](https://docs.microsoft.com/flow/gateway-manage)をインストールします。 例には、オンプレミスの SQL Server データベースや、オンプレミスの SharePoint サイトが含まれています。

ご自分の組織 (テナント) が、PowerBI US Government 用に既にオンプレミス データ ゲートウェイを構成し、正常に接続している場合、その有効化のために組織が実行したプロセスによって、Power Automate のオンプレミスの接続を有効化することもできます。 ただし、テナントに接続できない場合は、"ホワイトリスト" プロセスの実行が必要になる場合があります。これによりテナントに対してこの機能を有効化します。 これが発生した場合は、サポート チケットを開いてご自身のニーズに対応することができます。 サポート チームは、確立したプロセスに従ってリクエストに対応します。

## <a name="power-automate-us-government-feature-limitations"></a>Power Automate US Government の機能制限

Flow US Government の顧客は、Flow の商用バージョンで使用できる機能の一部を使用できません。 Flow チームは、US Government の顧客がこれらの機能を使用できるように積極的な作業を行っており、これらの機能が使用可能になった時点でこの記事を更新します。

- Power Automate US Government フローを SharePoint リスト "*から*" トリガーする

- Power Automate US Government フローを Dynamics 365 GCC "*から*" トリガーする

- [AI Builder](https://docs.microsoft.com/ai-builder/) は、GCC および GCC High テナントではまだ利用できません。

- [承認](./modern-approvals.md)は、GCC および GCC High テナントではまだ利用できません。

- [利用状況分析](https://flow.microsoft.com/blog/admin-analytics/)

- [Power Automate モバイル アプリケーション](https://docs.microsoft.com/flow/mobile-manage-flows)

- [テンプレートの送信](https://docs.microsoft.com/flow/publish-a-template)

    > [!NOTE]
    > エンタープライズ データのガバナンスとデータ フローの問題に対処するために、GCC ではテンプレートの送信が無効です。

- [コネクタ](https://docs.microsoft.com/connectors/index) – (使用状況テレメトリに基づいて) Microsoft の商用サービスで使用されている最も人気のあるコネクタが公開されています。商用オファリングで利用できるコネクタがあるのにデプロイされていることを確認できない場合は、サポートにお問い合わせいただければ、リクエストを確認します。

- [Power BI](https://docs.microsoft.com/connectors/powerbi/) – 現在、Power Automate US Government では Power BI はサポートされていません。

- [Power Platform 管理センター](https://docs.microsoft.com/power-platform/admin/admin-documentation) – 管理センターを使って[サポート チケットを開く](https://docs.microsoft.com/power-platform/admin/get-help-support)ことができますが、現在 US Government テナントではその他の機能を使用できません。

### <a name="see-also"></a>関連項目

[Power Apps US Government](https://docs.microsoft.com/power-platform/admin/powerapps-us-government)
