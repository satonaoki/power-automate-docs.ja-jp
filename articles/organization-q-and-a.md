---
title: 組織における Flow サインアップの Q&A | Microsoft Docs
description: Office 365 テナントにおける Flow のライセンス、管理、およびユーザー サインアップに関してよくある質問と回答
services: ''
suite: flow
documentationcenter: na
author: stepsic-microsoft-com
manager: erikre
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/05/2016
ms.author: stepsic
search.app:
- Flow
- Powerplatform
search.audienceType:
- admin
ms.openlocfilehash: f1e3ab59ad135b47b79466e1bd4d7fec73139955
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3297584"
---
# <a name="flow-in-your-organization-qa"></a>組織における Flow の Q & A

このトピックでは、組織のユーザーが Flow を使用する方法と、管理者が Flow サービスを制御する方法について説明します。

## <a name="signing-up-for-flow"></a>Flow にサインアップする
### <a name="what-is-power-automate"></a>Power Automate とは何ですか?
Power Automate は、個人やチームを支援するパブリック クラウド サービスです。お気に入りのアプリとサービスの間のワークフローを自動化し、同期、通知の受信、データ収集などを行うことができます。 

### <a name="how-do-people-sign-up-for-flow"></a>Flow にサインアップするにはどうすればよいですか?
個人が Web ポータルから Flow にサインアップするには、2 つの方法があります。

#### <a name="option-1"></a>オプション 1
[flow.microsoft.com](https://flow.microsoft.com) にアクセスし、**[無料でサインアップ]** を選択し、[admin.microsoft.com](https://admin.microsoft.com/Start?sku=flow_free) または [signup.live.com](https://signup.live.com) で Flow のサインアップ プロセスを完了することで、誰でもサインアップすることができます。

#### <a name="option-2"></a>オプション 2
[flow.microsoft.com](https://flow.microsoft.com) にアクセスし、**[サインイン]** を選択し、職場、学校、個人のメールでサインインし、Flow の使用条件に同意します。    

組織のユーザーがオプション 2 の方法で Flow にサインアップすると、そのユーザーには Power Automate の無料版ライセンスが自動的に割り当てられます。

詳しくは、「[Flow にサインアップする](sign-up-sign-in.md)」をご覧ください。

### <a name="what-is-the-power-automate-free-plan"></a>Power Automate 無料プラン の概要

Power Automate の 無料プランは、追跡目的でのみ使用されます。 これを有効化または無効化しても、フローを作成するユーザーの機能に影響はありません。 Power Automate の無料プランを無効にした場合、ユーザーがログインするともう一度これが有効になります。 これは想定どおりの動作です。

### <a name="can-i-block-another-person-from-signing-up-for-flow"></a>他のユーザーが Flow にサインアップすることを禁止できますか?
Power Automate は完全なパブリック クラウド サービスです。世界中のすべてのユーザーが Flow にサインアップし、Flow を使って日常のタスクを自動化できます。 Power Automate の使用に際して、Office 365 アカウントの作成や使用をする必要はありません。 このため、現時点では、他のユーザーが Flow を使うのを禁止するメカニズムはありません (世界中のすべてのユーザーがメール アドレスに関係なく使用できます)。

ただし、Power Automate に新規登録したユーザーが、組織内ではサポートしないことを選択した場合、そのユーザーが会社に費用を負担させることはできません。 個人が Power Automate に新規登録するとき、その関係は、Bing、Wunderlist、OneDrive、Outlook.com のような Microsoft の他のクラウド サービスと同様に、個人と Microsoft 間の関係になります。 Power Automate を個人で利用する場合は、組織がサービスの提供者として解釈されることは決してありません。

最後に、会社が Power Automate 内の組織専用データの使用を制限することを望んでいる場合は、データ消失防止 (DLP) ポリシーによりそれが可能になります。

### <a name="how-can-people-gain-access-to-the-paid-features-of-power-automate"></a>どうすれば Power Automate の有料機能にアクセスできますか？
個人が Power Automate の有料機能を利用するには、3 つの方法があります。

1. Flow Plan 1 または Flow Plan 2 の 90 日間無料評価版にサインアップする
2. Office 365 管理ポータルでユーザーに Flow ライセンスを割り当てる。
3. ユーザーに、Flow サービスを利用できる Office 365 プラン、または Dynamics 365 プランが割り当てられている。 Flow 機能を含む Office 365 プランまたは Dynamics 365 プランの一覧は [Flow の価格設定ページ](https://flow.microsoft.com/pricing/) でご覧いただけます。

### <a name="can-i-block-another-person-from-using-the-paid-features-of-flow"></a>他のユーザーが Flow の有料機能を使用することをブロックできますか?
個人は誰でも Power Automate  の有料機能を 90 日間無料で試すことができます。コストは発生しません。 ただし、Office 365 管理ポータルを利用すれば、組織内の永久有料ライセンスの割り当てを完全管理できます。

無料で提供されるものであり、必ずしも会社の推薦ではない、個人と Microsoft の直接関係である評価版に個人がサインアップします。

## <a name="administration-of-flow"></a>Flow の管理
### <a name="why-has-the-flow-icon-appeared-in-the-office-365-app-launcher"></a>Office 365 アプリ起動ツールに Flow アイコンが表示されているのはなぜですか？
8 月に発表されたように、Power Automate は Office 365 スイートの基本構成要素となりました。 この発表から 3 か月後、 Power Automate  は、すべての既存 の Office 365 でサービスとして有効になりました。 世界中のユーザーが Power Automate を利用できるようになったため、アプリ起動ツールに表示されています。

既定でアプリ起動ツールから Flow タイルを削除する方法については、次のセクションをご覧ください。

### <a name="how-do-i-remove-power-automate-from-the-app-launcher-for-my-organization"></a>組織のアプリ起動ツールから Power Automate を削除するにはどうすればよいですか？
あるユーザーに Flow Plan 1 または Flow Plan 2 のライセンスが割り当てられている場合、次の手順でそのユーザーの Flow ライセンスを削除できます。ライセンスを削除すれば、アプリ起動ツールから Flow アイコンが削除されます。

1. [Office 365 管理ポータル](https://portal.microsoftonline.com/) に移動します。
2. 左側のナビゲーション バーで**ユーザー**を選択し、**アクティブ ユーザー**を選択します。
3. ライセンスを削除したいユーザーを検索して、名前を選択します。
4. ユーザーの詳細ウィンドウで、**製品ライセンス** セクションの**編集**を選択します。
5. **Power Automate プラン 1** または **Power Automate プラン 2** という名称のライセンスを見つけて **オフ** に切り替え、**保存** を選択します。
   
   ![](./media/organization-q-and-a/remove-license.png)

Office 365 のプランや Dynamics 365 プランのライセンスでユーザーが Flow を利用できる場合、そのプランに含まれる追加機能へのアクセスを次の手順で無効にできます：

1. [Office 365 管理ポータル](https://portal.microsoftonline.com/) に移動します。
2. 左側のナビゲーション バーで**ユーザー**を選択し、**アクティブ ユーザー**を選択します。
3. アクセス権を削除したいユーザーを検索して、名前を選択します。
4. ユーザーの詳細ウィンドウで、**製品ライセンス** セクションの**編集**を選択します。
5. ユーザーの Office 365 または Dynamics 365 ライセンスを展開し、**Flow for Office 365** または**Flow for Dynamics 365** という名前のサービスへのアクセスを無効にし、**保存** を選択します。
   
   ![](./media/organization-q-and-a/remove-service-plan.png)

PowerShell を使ってライセンスを一括削除することもできます。 詳細な例については、[Office 365 PowerShell でユーザー アカウントからライセンスを削除する](https://technet.microsoft.com/library/dn771774.aspx) を参照してください。   最後に、ライセンス内でのサービス一括削除に関するより詳細なガイダンスは、[Office 365 PowerShell でサービスへのアクセスを無効にする](https://technet.microsoft.com/library/dn771769.aspx) にあります。

組織のユーザーに対して Flow のライセンスまたはサービスを削除すると、そのユーザーを対象に、次の場所から Flow アイコンが削除されます。

1. [Office.com](https://office.com)
   
   ![](./media/organization-q-and-a/office-home.png)
2. Office 365 アプリ起動ツール
   
   ![](./media/organization-q-and-a/office-waffle.png)

この場合、既定で Flow のタイルが削除されるだけです。 ユーザーは引き続き個人として Power Automate の使用を選択できます。

### <a name="why-did-10000-licenses-for-power-automate-show-up-in-my-office-365-tenant"></a>私の Office 365 テナントに、Power Automate のための 10,000 のライセンスが表示されました。
誰でも Power Automate プラン 1 または 2 を 90 日間試すことができます。そのような評価版ライセンスがご利用のテナントでの新しい Flow ユーザーの利用可能なキャパシティを表します。 これらのライセンスに関して料金は発生しません。 Office 365  管理ポータルに 10,000 の (評価版) ライセンスが表示される場合は、具体的に次の 2 つの理由が考えられます。

1. 2016 年 4 月から 2016 年 10 月までの間でテナント内の 1 名以上のユーザーが Flow に参加した場合、"Microsoft Power Appsと Logic flows" というラベルの付いた 10,000 のライセンスが表示されます
   
    ![](./media/organization-q-and-a/licenses2.png)
2. テナント内の 1 名以上のユーザーが [Power Appsにサインアップする方法](#how-do-people-sign-up-for-flow) セクションの試用サインアップ **オプション 1** で Flow プラン 2 評価版にサインアップした場合、"Microsoft Power Apps  & Flow" というラベルの付いた 10,000 ライセンスが表示されます
   
    ![](./media/organization-q-and-a/licenses1.png)

Office 365 管理ポータルから追加ライセンスをユーザーに自分で割り当てることができますが、それは Power Automate プラン 2 の評価版ライセンスであり、ユーザーに割り当ててから 90 日後に期限が切れることに注意してください。

### <a name="is-this-free-will-i-be-charged-for-these-licenses"></a>無料ですか?  ライセンスに料金はかかりますか。
明示的な同意なしでは、ユーザーが組織にコストを発生させることはありません。無料ライセンスと評価版ライセンスのいずれも、組織に何の料金も発生させません。 また、クォータの実行など、クォータは試用されません。

### <a name="i-removed-the-power-automate-free-license-and-users-can-still-access-flow"></a>Power Automate 無料ライセンスを削除しました。ユーザーは Flow に引き続きアクセスできますか？
Power Automate の 無料ライセンスは、追跡目的でのみ使用されます。 最初のセクションで説明したように、他のユーザーが個人として Power Automate の使用を禁止することはできません。 そのため、Power Automate の無料ライセンスは実際にはいかなる機能も付与、または削除することはありません。

### <a name="why-cant-i-see-all-flow-licenses-in-the-office-365-admin-portal"></a>Office 365 管理ポータルにすべての Flow ライセンスが表示されないのはなぜですか？
Power Automate  は、個人または組織の一員として利用できます。 組織レベルのライセンスは Office 365 ポータルに常に表示されます。 しかしながら、個人として試用版に新規登録した場合、Office 365 の管理対象外となるため、ポータルには表示されません。

### <a name="how-does-an-individual-find-out-what-plan-they-are-on"></a>個人のプランを確認する方法はありますか?
[https://flow.microsoft.com/pricing](https://flow.microsoft.com/pricing) の Flow 価格ページでご自分のプランをご確認いただけます。 現在利用しているプランまたは試用版が表示されます。

### <a name="will-power-automate-sign-up-impact-the-identities-in-my-organization"></a>Power Automate を新規登録すると組織の ID に影響を与えますか？
組織に Office 365 環境が既にあり、組織のすべてのユーザーが Office 365 のアカウントを持っている場合、ID 管理に影響はありません。

もし組織に既存の Office 365 環境があるものの、すべてのユーザーが Office 365 アカウントを持っていない場合、テナントにユーザーが作成され、ユーザーの職場または学校の電子メール アドレスに基づいてライセンスが割り当てられます。 これは、組織内のユーザーがサービスにサインアップする度に、その時点で管理しているユーザーの数が増えるということを意味します。

もし組織に電子メール ドメインと接続された Office 365 環境がない場合、ID を管理する方法に変更はありません。 ユーザーは新しいクラウド専用のユーザー ディレクトリに追加されることになります。管理者は、それらのユーザーをテナント管理者として引き継いで管理するかどうかを選ぶことができます。

### <a name="a-new-tenant-was-created-by-power-automate-how-do-i-manage-this"></a>新しいテナントが Power Automate で作成されましたが、どのように管理すればよいですか？
Power Automate によって作成された新規テナントが作成された場合は、次の手順を使用して、当該テナントを要求し、管理することができます：

1. 管理するテナント ドメインと一致する電子メール アドレス ドメインを使って Flow にサインアップすることで、テナントに参加します。 たとえば、Microsoft が contoso.com のテナントを作成した場合、@contoso.com で終わる電子メール アドレスを使ってテナントに参加します。
2. ドメインの所有権を確認することによって、管理コントロールを要求します。テナントに参加した後は、ドメインの所有権を確認することによって自分自身を管理者の役割に昇格させることができます。 これを行うには、次の手順に従います。    
   
   1. [https://admin.microsoft.com](https://admin.microsoft.com/Start?sku=flow_free) に移動します。
   2. 左上のアプリ起動ツール アイコンを選んで、[管理者] を選びます。
   3. **管理者になる**ページの指示を参照し、**はい、管理者になります**を選択します。  
      
       **注意**：このオプションが表示されない場合は、Office 365 の管理者が既に存在していることを意味します。

### <a name="if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-are-added-to"></a>複数のドメインを持っている場合、ユーザーが追加された Office 365 テナントを制御することはできますか?
もし何もしないなら、各ユーザーの電子メール ドメインおよびサブドメインに対してテナントが作成されます。

電子メール アドレスの拡張性にかかわらず、すべてのユーザーを同じテナントに入れたい場合:  

* 事前にターゲット テナントを作成するか、または既存のテナントを使用します。 そのテナントで統合したいすべての既存のドメインおよびサブドメインを追加します。 以後、電子メール アドレスの末尾がこれらのドメインとサブドメインに該当するすべてのユーザーは、サインアップ時に自動的に対象テナントに追加されます。

**重要**: いったん作成されたテナント間でユーザーを自動的に移動するための機構は用意されていません。 ドメインを 1 つの Office 365 テナントに追加することについては、[Office 365 にユーザーとドメインを追加する](https://support.office.com/article/Add-your-users-and-domain-to-Office-365-ffdb2216-330d-4d73-832b-3e31bcb5b2a7) を参照してください。

### <a name="how-can-i-restrict-my-users-ability-to-access-my-organizations-business-data"></a>ユーザーが組織のビジネス データにアクセスする機能を制限するにはどうすればよいですか?
以下に示すように、Power Automate を使用してビジネス データとビジネス以外のデータのデータ ゾーンを作成します。 このようなデータ損失防止ポリシーを導入すると、ビジネス データとビジネス以外のデータを組み合わせる Flow をユーザーは設計したり、実行したりできなくなります。 詳細については、[データ消失防止 (DLP) ポリシー](prevent-data-loss.md) を参照してください。

  ![](./media/organization-q-and-a/data-loss-prevention-policy.png)

