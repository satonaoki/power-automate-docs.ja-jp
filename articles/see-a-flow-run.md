---
title: フロー実行の確認 | Microsoft Docs
description: フローの段階ごとに入力と出力を表示し、予想どおりに動作していることを確認します。
services: ''
suite: flow
documentationcenter: na
author: MSFTMAN
manager: KVIVEK
ms.author: Deonhe
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/05/2018
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 5d38ee4df1e1edb16b86c402e77ce43ff659dc64
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74373575"
---
# <a name="watch-your-flows-in-action"></a>実行中のフローの確認
[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]

>[!VIDEO https://www.youtube.com/embed/3wPoUCGm7Yg]

フローが期待どおりに実行されることを確認するには、トリガーを実行し、その後、フロー内の各手順によって生成された入力と出力を確認します。

1. フローを作成または更新し、 **[フローの作成]** または **[フローの更新]** を選択した後、デザイナーは開いたままにします。

     たとえば、 **#azure** ハッシュタグが付いたツイートが投稿されるたびに電子メールを送信する[フローを作成](get-started-logic-flow.md)します。
1. フローの開始アクションを実行します。

    たとえば、 **#azure** ハッシュタグが含まれるツイートを送信します。

    開始アクションと以降の各ステップには、実行が成功したかどうかと、その所要時間が示されます。

    ![実行成功のイメージ](./media/see-a-flow-run/successful-flow-run.png)
1. トリガーまたはアクションを選択し、その入力と出力を確認します。

    ![カードが展開された実行成功のイメージ](./media/see-a-flow-run/successful-flow-expanded-cards.png)
1. **[フローの編集]** を選択して変更します。フローが期待どおりに動作している場合は、 **[完了]** を選択します。
