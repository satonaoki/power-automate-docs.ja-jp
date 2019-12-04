---
title: 他のフローから UI フローを実行する | Microsoft Docs
description: 他のフローから UI フローを実行する
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
ms.date: 11/04/2019
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: d0d5380e1ade6d1d11d557f38e7fc5db6616d1d9
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74370953"
---
# <a name="run-ui-flows"></a>UI フローの実行

[このトピックはプレリリース版のドキュメントであり、変更される可能性があります。]

[!INCLUDE [view-pending-approvals](../includes/cc-rebrand.md)]

UI フローを作成してテストした後は、イベント、スケジュール、またはボタンから実行できます。 これを可能にするには、UI フローを [自動化されたフロー](../get-started-logic-flow.md)、[ボタン フロー](../introduction-to-button-flows.md)、[スケジュールされたフロー](../run-scheduled-tasks.md)、または[ビジネス プロセス フロー](../business-process-flows-overview.md)に追加します。

## <a name="prerequisites"></a>前提条件

- Power Automate によって UI フローがトリガーされるようにするには、ご使用のデバイスに[オンプレミス データ ゲートウェイ](https://go.microsoft.com/fwlink/?LinkID=820580&clcid=0x409)が必要です。
   
   このゲートウェイは、Power Automate とデバイス (UI フローが実行される場所) 間の、エンタープライズ レベルのセキュリティで保護された接続です。 Power Automate では、イベント、スケジュール、またはボタンから UI フローをトリガーできるように、このゲートウェイを使用してオンプレミスのデバイスにアクセスします。
- 職場または学校アカウント。 

   >[!IMPORTANT]
   >ゲートウェイの設定、Power Automate へのサインイン、Windows デバイスへのログインには、同じ職場または学校アカウントを使用する必要があります。
   

## <a name="run-your-ui-flow-from-an-event-button-schedule-or-business-process-flow"></a>イベント、ボタン、スケジュール、またはビジネス プロセス フローから UI フローを実行する

この例では、自動化されたフローを使用して、新しいメールが届いたときに、UI フローをトリガーします。

1. [Power Automate](https://flow.microsoft.com/) に移動します。
1. 左側のナビゲーション バーで **[マイ フロー]** を選択します。
1. **[新規]** を選択した後、 **[自動--一から作成]** を選択します。

   >[!TIP]
   >必要に応じて、他の種類のフローを選択できます。

1. **[フロー名]** ボックスでフローに名前を付けます。
1. "新しいメール" を検索し、トリガーの一覧から **[新しいメールが届いたとき (V3)]** を選択します。 
    
   ![トリガーの選択](../media/run-ui-flow/2d4ec17d239169a46905cef1829fa3a1.png "トリガーの選択")

1. **[作成]** を選択してから、 **[新しいステップ]** を選びます。

1. **UI フロー**を検索し、 **[アクション]** の一覧から **[デスクトップの UI フローの実行]** を選択します。 

   ![検索アクション](../media/run-ui-flow/search-action.png "検索アクション")

1. ゲートウェイ情報とデバイスの資格情報を指定します。 

   これは、デバイスごとに 1 回行う必要があります。

    - **接続名**: フロー接続するデバイスの名前を選択します。 ゲートウェイ名と異っていてもかまいません。
    - **ユーザー名**: ご使用のデバイスの職場または学校アカウントを指定します。
    - **認証の種類**: [Windows] を選択します。
    - **パスワード**: ご自分の職場または学校アカウントのパスワード。
    - **ゲートウェイ**: インストール時に作成したゲートウェイを選択します。

      ![接続の設定](../media/run-ui-flow/connection-settings.png "接続の設定")

      >[!TIP]
      >ゲートウェイが表示されない場合は、別の接続を選択する必要があるかもしれません。 これを行うには、 **[デスクトップの UI フローの実行 (プレビュー)]** カードの右上にある **[...]** を選択し、 **[自分の接続]** から使用する接続を選択します。

      ![新しい接続の選択](../media/run-ui-flow/select-new-connection.png "新しい接続の選択")

1. 以前に作成した UI フローを選択します。

   ![UI フローの選択](../media/run-ui-flow/select-ui-flow.png "UI フローの選択")

1. **[保存]** を選択して自動化されたフローを保存します。

1. フローをトリガーするメールを送信してフローをテストします。 記録したステップが UI フローで再生されます。 

![UI フローを呼び出す成功した実行](../media/run-ui-flow/successful-run.png "UI フローを呼び出す成功した実行")

>[!TIP]
>フローが実行されている間は、デバイスを操作しないでください。

## <a name="use-inputs-and-outputs"></a>入力と出力を使用する

UI フロー内で入力と出力を定義するときに、これらの入力と情報をやり取りすることができます。

1. UI フローをフローに追加すると、UI フローで定義された入力の一覧が表示されます。

   ![UI フローの入力](../media/run-ui-flow/inputs.png "UI フローの入力")

1. UI フローの各入力フィールドには、フローの前のステップの値を設定できます。 これを行うには、入力フィールドを選択し、トークン ピッカーから入力を選択します。


1. また、UI フローからの出力を、フロー内で後で表示されるアクションの入力として使用することもできます。 これを行うには、入力フィールドを選択し、トークン ピッカーから入力を選択します。

## <a name="limitations-and-known-issues"></a>制限事項と既知の問題

- ゲートウェイ クラスターはサポートされていません。
- このリリースでは、US (QWERTY) 以外のキーボードはサポートされていないため、US (QWERTY) 以外のキーボードからのキー シーケンスが記録された入力ステップを再生すると、キー ストロークは US (QWERTY) になります。

## <a name="learn-more"></a>詳細については、こちらをご覧ください

 - [オンプレミス データ ゲートウェイ](https://docs.microsoft.com/data-integration/gateway/service-gateway-app)のインストール。
 - [オンプレミス データ ゲートウェイのアプリの使用](https://docs.microsoft.com/flow/gateway-manage)に関するドキュメント
 - オンプレミス データ ゲートウェイの[トラブルシューティング](https://docs.microsoft.com/data-integration/gateway/service-gateway-tshoot)。
