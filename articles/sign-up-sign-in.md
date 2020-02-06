---
title: サインアップおよびサインイン | Microsoft Docs
description: Power Automate にサインアップおよびサインインして、このプロセスに関する問題のトラブルシューティングを行います。
services: ''
suite: flow
documentationcenter: na
author: anjlic
manager: anneta
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/04/2017
ms.author: anjlic
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 5c70db242974e549d07161fa47e76ab7eaa7a924
ms.sourcegitcommit: 835b005284b9ae21ae1742a7d36b574ba3884bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2020
ms.locfileid: "74372701"
---
# <a name="sign-up-and-sign-in-for-power-automate"></a>Power Automate にサインアップおよびサインインする

[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]

<iframe width="560" height="315" src="https://www.youtube.com/embed/cRkmSZrctLc?list=PL8nfc9haGeb55I9wL9QnWyHp3ctU2_ThF" frameborder="0" allowfullscreen></iframe>

個人として、Power Automate の使用を開始するのは簡単です。 フローを作成する前に、任意の電子メール アドレスを使用してサインアップします。 そのアドレスでオンラインの Microsoft 製品を使用したことがない場合は、少し時間を取って登録する必要があります。

## <a name="sign-up-free"></a>無料でサインアップ
他のオンライン Microsoft 製品を使用したことがない場合、サインアップが必要になります。

1. [Flow.microsoft.com](https://flow.microsoft.com) で、右上隅の **[無料でサインアップ]** をクリックまたはタップします。
2. 電子メール アドレスを入力します。
3. 右矢印をクリックまたはタップします。

    ![サインアップ リンク](./media/sign-up-sign-in/signup.png)

## <a name="sign-in"></a>サインイン
仕事または個人で他のオンライン Microsoft 製品を使用したことがある場合、サインインするだけでかまいません。

1. [flow.microsoft.com](https://flow.microsoft.com) で、右上隅の **[サインイン]** をクリックまたはタップします。

    ![サインイン リンク](./media/sign-up-sign-in/signin.png)
2. 電子メール アドレスを入力します。
3. [サインイン] ページで、電子メール アドレスとパスワードを入力します。

## <a name="using-paid-features"></a>有料機能の使用
どなたでもサインアップして、Power Automate の無料プランをご利用いただけます。 所属する組織で Office 365 または Dynamics 365 を購入しているようであれば、Power Automate のその他の機能を使用できる可能性があります。 有料の機能を使用したい場合は、90 日間無料試用版を開始するか、Power Automate Plan 1 または Plan 2 をご購入いただくこともできます。 支払いの詳細については、[こちら](billing-questions.md)をご覧ください。

管理については、[組織の Q&A のフロー](organization-q-and-a.md)に関するページをご覧ください。

## <a name="troubleshooting"></a>トラブルシューティング
ほとんどの場合、このトピックの前述の簡単なプロセスに従って、Power Automate に登録できますが、 場合によっては、登録できないこともあります。この表では、サインアップできない場合の最も一般的な原因と、その回避策について説明します。


|                                                                                                                                                                                       症状/エラー メッセージ                                                                                                                                                                                        |                                                                                                                                                                              原因と回避策                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                                                       **Microsoft アカウントが作成されていない** <br> サインアップ中に電子メール アドレスを入力した後、次のようなメッセージが届きます。<br><br> *その Microsoft アカウントは存在しません。別のアカウントを入力するか、新しいアカウントを取得してください。*                                                                                       |                                              Microsoft アカウントが作成されていない電子メール アドレスでサインアップしました。 そのページの **[今すぐサインアップ]** リンクを選択すると、お使いの電子メール アドレスに対応する新しい Microsoft アカウントを作成できます。 既存の電子メール アドレスを使用して Microsoft アカウントを作成できます。                                               |
|                                                  **.gov または .mil の電子メール アドレス**<br>サインアップ中に次のようなメッセージが表示されます。<br><br>*Power Automate unavailable:Power Automate is not available for users with .gov or .mil email addresses at this time. (Power Automate を利用できません。.gov または .mil のメール アドレスを持つユーザーは、現在のところ、Power Automate を利用できません。)Use another work email address or check back later. (他の勤務先の電子メール アドレスを使用するか、後でもう一度ご確認ください。)*                                                  |                                                                                            現在、.gov または .mil のアドレスで Power Automate にサインアップすることはできません。 その代わり、 *\@outlook.com* アドレスなど、任意の Microsoft アカウント電子メール アドレスを使ってサインインできます。                                                                                             |
| **セルフサービス サインアップが無効になっている**<br><br>サインアップ中に次のようなメッセージが表示されます。<br>"*We can't finish signing you up. (サインアップを完了できません。)Your IT department has turned off signup for Power Automate. (IT 部門によって Power Automate のサインアップが無効になっています。)Contact them to complete signup. (IT 部門に連絡して、サインアップを完了させてください。)* " <br>または<br> "*We can't finish signing you up. (サインアップを完了できません。)It looks like Microsoft Power Automate isn't currently available for your work or school. (現在、Microsoft Power Automate は職場または学校で使用できなくなっている可能性があります。)* |                                                                                        **[サインイン]** ではなく **[サインアップ]** を選択しました。 ホーム ページ上部の **[サインイン]** を選択すると、Power Automate にアクセスできるようになります。                                                                                        |
|                                                   **電子メール アドレスが Office 365 ID ではない**<br><br>サインアップ中に次のようなメッセージが表示されます。<br>*We can't find you at contoso.com. (contoso.com で見つかりません。)Do you use a different ID at work or school? (勤務先または学校の別の ID を使用しますか?)Try signing in with that, and if it doesn't work, contact your IT department. (その ID でサインインしようとして、うまくいかない場合は、IT 部門に問い合わせください。)*                                                    | ユーザーの組織では ID を使用して、Office 365 やその他の Microsoft サービスにサインインしていますが、その ID がユーザーの電子メール アドレスと異なります。 たとえば、電子メール アドレスが Nancy.Smith@contoso.com で、ID が nancys@contoso.com である場合もあります。 サインアップを完了するには、Office 365 やその他の Microsoft サービスにサインインするために組織が割り当てた ID を使用します。 |

## <a name="next-steps"></a>次の手順
* [テンプレートの使用を開始します](get-started-logic-template.md)。テンプレートは、設定済みの事前に構築されたフローです。
* 既にプロセスが決まっており、そのプロセスに合ったテンプレートが見つからない場合は、[ゼロからフローを作成](get-started-logic-flow.md)してください。

