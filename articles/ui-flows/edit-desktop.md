---
title: デスクトップ UI フローの編集方法を学習する | Microsoft Docs
description: デスクトップ UI フローの編集方法を学習します。
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
ms.openlocfilehash: 9c9da27098ca9114c0919d0fb6e70495f442a3c6
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74371712"
---
# <a name="edit-desktop-ui-flows"></a>デスクトップ UI フローの編集

[このトピックはプレリリース版のドキュメントであり、変更される可能性があります。]

[!INCLUDE [view-pending-approvals](../includes/cc-rebrand.md)]

デスクトップ UI フローを使うと、Windows デスクトップ アプリケーションを自動化できます。 発生する可能性のある問題、その問題の回避策、このプレビュー リリースではサポートされていないシナリオの詳細については、[既知の問題](create-desktop.md#known-issues-and-solutions)を参照してください。

## <a name="prerequisites"></a>前提条件
デスクトップ UI フロー。 編集するものがない場合は、[ここでデスクトップ UI フローを作成します](create-desktop.md#create-and-test-desktop-ui-flows)。

## <a name="edit-actions"></a>編集アクション

![編集アクション](../media/edit-desktop/edit-actions.png "編集アクション")

記録を編集するには、次のことを行います。

-   これをサポートするアクションの値を変更します。
-   ステップを削除します。
-   記録全体を削除します。
-   ドラッグ アンド ドロップを使用してアクションの順序を変更します。 記録の一貫性が損なわれる可能性があるため、この操作には注意してください。

高度なパラメーターを使用すると、次のことを変更できます。

-  アクションが実行された後の遅延。 たとえば、PT0S を PT1S に変更することによって、1 秒の遅延を追加できます。 これは、ターゲット アプリケーションの応答時間が遅く、UI フローの次のステップの前に完了しない場合に便利です。
-   ターゲット ユーザー インターフェイス要素の[セレクター](edit-desktop.md#set-the-selector)。

## <a name="add-a-recording"></a>記録の追加

UI フローを複数のセッションで記録する必要がある場合があります。 最初の記録が完了したら、次のように進めることができます。

1. [Power Automate](https://flow.microsoft.com) にサインインします。
1. **[マイ フロー]**  >  **[UI フロー (プレビュー)]** の順に選択します。
1. 編集する UI フローを選択します。
   ![](../media/edit-desktop/select-ui-flow.png)
1. **[編集]** を選択します。 
1. **[新しいステップ]** を選択します。

   ![新しいステップ](../media/edit-desktop/new-step.png "新しいステップ")

1. アクションの一覧から **[アプリの記録]** を選択します。

   ![アプリの記録](../media/edit-desktop/select-record-ui-actions.png "アプリの記録")

1. **[レコーダーの起動]** を選択します。

   ![[レコーダーの起動] の選択](../media/create-windows-ui-flow/select-launch-recorder.png "[レコーダーの起動] の選択")

   レコーダー コントロールが画面の上部に表示されます。

   ![レコーダー コントロール](../media/create-windows-ui-flow/recorder-control.png "レコーダー コントロール")

1. 記録するアプリを開始します。

     >[!TIP]
     >アプリのコントロールにマウスを置くと、各コントロールが青の枠線で強調表示されます。 コントロールを選択する前に、常に青の強調表示を待ちます。
     >
     >要素の周囲に青の強調表示が表示されない場合は、適切に記録されていない可能性があります。

1. レコーダー コントロールから **[記録]** を選択します。

1. 記録しているアプリのユーザー インターフェイスのステップを実行し、レコーダー コントロールの **[完了]** を選択します。
1. **[保存]** を選択し、UI フローをテストします。

## <a name="add-a-manual-action"></a>手動アクションの追加

少なくとも 1 つのアクションを使用してアプリケーションを記録したら、そのアプリケーションに対して次のアクションを手動で追加することができます。

| **アクション**          | **コメント**                                                       |
|---------------------|-------------------------------------------------------------------|
| アプリケーションの終了   |                                                                   |
| 右クリック         |                                                                   |
| キーの送信           | Ctrl + C などのキーとキーの組み合わせを送信します。                             |
| 左クリック          |                                                                   |
| テキストの取得            | ユーザー インターフェイス要素からテキストを読み取り、出力として使用します。 |
| テキストの入力          |                                                                   |
| 要素の有効/無効を取得 | ユーザー インターフェイス要素が有効になっているか、または無効になっているかを確認します。         |
| 要素のクリア       | 編集可能なユーザー インターフェイス要素の値をクリアします。             |
| 数秒待機する    | 次のステップに進む前に待機します。                           |

次の手順に従って手動アクションを追加します。

1. [Power Automate](https://flow.microsoft.com) にサインインします。
1. **[マイ フロー]**  >  **[UI フロー (プレビュー)]** の順に選択します。
1. 編集する UI フローを選択します。
   ![](../media/edit-desktop/select-ui-flow.png)
1. **[編集]** を選択します。 
1. 新しいステップを追加するステップを含む記録カードを選択します。
   カードが展開され、記録されたステップが表示されます。

   ![記録カードの選択](../media/edit-desktop/manual-select-recording-card.png)

1. 最後に記録されたステップのすぐ下にある記録カードの **[アクションの追加]** を選択します。
   このチュートリアルでは、前述の手動アクションの一覧が表示されます。 

1. 追加するアクションを選択します。 ここでは **[要素の有効/無効を取得]** を選択しましたが、シナリオに適した任意のアクションを選択できます。

   ![追加するアクションの選択.png](../media/edit-desktop/select-action-to-add.png)

アクションが追加されたら、アクションの詳細オプションで**セレクター**を設定する必要があります。

![アクションの詳細オプション](../media/edit-desktop/action-advanced-options.png "アクションの詳細オプション")

### <a name="set-the-selector"></a>セレクターの設定

セレクターは、再生中にアクションが実行されるユーザー インターフェイス要素を識別します。 可能であれば、同じユーザー インターフェイス要素を対象とする別のステップからこの情報をコピー/貼り付けすることをお勧めします。

セレクターの形式は次のとおりです。

```json
{  
   "type":"WinUIA",
   "parameters":{  
      "elementStack":[  

      ],
      "elementXPath":""
   }
}
```

セレクター要素の **elemementStack** と **elementXPath** の各フィールドにデータを指定する必要があります。

**elemementStack** の例は、次のようになります。

![要素スタック](../media/edit-desktop/elementstack.png "要素スタック")

[WinAppDriver UI Recorder](https://blogs.windows.com/windowsdeveloper/2018/06/20/introducing-winappdriver-ui-recorder/) を使用して **elementXPath** をキャプチャできます。

![WAD ツール](../media/edit-desktop/wad-tool.png "WAD ツール")

セレクターの **elementXPath** の結果を使用する前に、最初の要素 (/Window の前のすべて) を削除します。

UI フローをテストして、セレクターが正しく動作することを確認します。

## <a name="next-steps"></a>次のステップ

- 編集したばかりの [UI フローを実行する](run-ui-flow.md)方法について学習します。

- UI フローでさらに多くの操作を行う場合は、[入力と出力](inputs-outputs-web.md)パラメーターを使用して UI フローを試すこともできます。

