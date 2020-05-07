---
title: カスタム応答で承認フローを作成する | Microsoft Docs
description: カスタム応答で承認フローを作成します
services: ''
suite: flow
documentationcenter: na
author: msftman
manager: kvivek
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/04/2019
ms.author: deonhe
search.app:
- Flow
- Powerplatform
search.audienceType:
- maker
ms.openlocfilehash: dc2eaf9ac0ffc0edb10f5cb096ee98dad6aac55d
ms.sourcegitcommit: 9cca2a2fca8371ab883b12011c1c4485ceb9c761
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2020
ms.locfileid: "82200472"
---
# <a name="create-custom-response-options-for-approval-flows"></a>承認フローのカスタム応答オプションを作成する


たとえば、従業員が経費報告書を SharePoint にアップロードするたびに承認要が送信され、承認者が承認、要詳細情報、却下の 3 つのオプションのいずれかで応答できるようにするものとします。


## <a name="prerequisites"></a>前提条件

- Power Automate アカウント。
- 従業員が経費報告書を入力するための SharePoint リスト。

## <a name="create-approval-flow"></a>承認フローを作成する
1. [Power Automate](https://flow.microsoft.com) にサインインします。
1. 左側のナビゲーション バーで **[マイ フロー]** を選択します。
1. **[新規]**  >  **[自動—一から作成]** を選択します。

    ![[一から作成] オプション](media/create-approval-response-options/create-approval-response-options.png)

1. 開いた画面の **[フロー名]** にフローの名前を指定します。 
  
1. **[フローのトリガーを選択してください]** で **SharePoint** を検索し、トリガーの一覧から **[項目が作成されたとき]** を選択して、 **[作成]** を選択します。

   ![[一から作成] を選択する](media/create-approval-response-options/create-from-blank.png)

1. SharePoint の **[サイトのアドレス]** と **[リスト名]** を指定します。 

   >[!TIP]
   >**[サイトのアドレス]** にテキストを入力する前に、 **[サイトのアドレス]** フィールドから **[カスタム値の入力]** を選択します。

1. **[新しいステップ]** を選択し、 **[承認]** を検索して、 **[開始して承認を待機]** を選択します。

1. **[開始して承認を待機]** カードで、 **[承認の種類]** 一覧を選択します。

1. **[カスタム応答 – 1 つの応答を待機]** を選択します。

    ![Approval type (承認の種類)](media/create-approval-response-options/select-approval-type.png)

    次に、承認者が従業員の経費の承認要求に応答するときに使用するカスタム応答を作成します。


1. **[Response options Item]\(応答オプション項目\)** ボックスに「**承認**」と入力し、 **[新しい項目の追加]** を選択します。 

    ![カスタム応答 1](media/create-approval-response-options/enter-response-1.png)

1. **[Response options Item]\(応答オプション項目\)** ボックスに「**却下**」と入力し、 **[新しい項目の追加]** を選択します。

1. **[Response options Item]\(応答オプション項目\)** ボックスに「**詳細な情報が必要**」と入力します。

    ![カスタム応答 3](media/create-approval-response-options/enter-response-3.png)   
    

1. **[タイトル]** 、 **[割り当て先]** (承認者のメール アドレス)、 **[詳細]** (承認要求に含める詳細) を入力します。

    次に例を示します。

    ![カスタム応答の詳細](media/create-approval-response-options/enter-title-assigned-to-details.png)


カスタム応答を作成したので、承認者からの応答に応じて、フロー内で異なる処理を行います。


## <a name="use-approval-responses"></a>承認応答を使用する 

要求に対する応答が**承認**の場合は、会計部門にメールを送信し、経費に対して従業員に払い戻しするように依頼します。 

応答が**却下**の場合は、従業員にメールを送信し、要求が却下されたことを知らせます。

最後に、承認者からの応答が**詳細な情報が必要**の場合は、従業員により多くの情報を提供するよう依頼する電子メールを送信します。

フローでこれらのいずれかを実行するには、[**条件**](add-condition.md)または**スイッチ** アクションをフローに追加し、動的コンテンツ ピッカーから承認要求の **[結果]** フィールドを選択します。 値が承認、詳細な情報が必要、却下かどうかを確認します。

## <a name="respond-to-approval-requests-with-a-custom-response"></a>カスタム応答で承認要求に応答する

承認者は、電子メールで承認要求を受け取ります。 要求は、Power Automate の承認センターにも表示されます。 

![承認要求メール](media/create-approval-response-options/approval-request-email.png)

## <a name="learn-more"></a>詳細情報
- [単一承認者フロー](modern-approvals.md)を作成する
- [シーケンシャル承認者フロー](sequential-modern-approvals.md)を作成する
