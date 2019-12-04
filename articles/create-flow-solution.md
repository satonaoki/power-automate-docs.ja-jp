---
title: ソリューション対応フローを作成する方法に関する説明 | Microsoft Docs
description: ソリューション対応フローを作成する方法について説明します。
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
ms.date: 11/05/2018
ms.author: deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 7379cb966be58edfa75cd20c3ad70cf9fff2407a
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74362650"
---
# <a name="create-a-flow-in-a-solution"></a>ソリューションにフローを作成する
[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]

ソリューション内に作成するフローは、"*ソリューション対応*" フローと呼ばれます。 次の手順に従って、ソリューション対応フローを作成します。

## <a name="prerequisites"></a>前提条件

ソリューション対応フローを作成する前に、少なくとも 1 つのソリューションを用意する必要があります。

## <a name="create-the-flow"></a>フローを作成する 

1. [Power Automate](https://flow.microsoft.com) にサインインします。
1. ナビゲーション バーから **[ソリューション]** を選択します。

   ![](./media/create-flow-solution/select-solutions-from-left-nav.png)

1. 内部にフローを作成するソリューションを選択します。

   ![](./media/create-flow-solution/new-solution-created.png)

1. **[+ 新規]** を選択した後、**[フロー]** を選択します。

   ![](./media/create-flow-solution/select-new-flow.png)

   Power Automate が開きます。

1. 利用可能なコネクタとトリガーを使用して、フローを構築します。

   この例では、受信トレイにメールが届いたときに通知を送信する、単純なフローを作成します。
1. **[Office 365 Outlook]** を検索して選択します。
1. **[新しいメールが届いたとき]** トリガーを選択します。
1. **[+ 新しいステップ]** を選択します。
1. **[Send me a mobile notification]\(モバイル通知を受け取る\)** アクションを選択します。
1. **[Send me a mobile notification]\(モバイル通知を受け取る\)** ボックスの **[テキスト]** フィールドに、**[件名]** 動的トークンを追加します。
1. フローに名前を付けた後、フローを保存します。

   フローは次のようになります。

   ![](./media/create-flow-solution/new-email-notification-flow.png)
   
1. **[ソリューション]** を選択して、ソリューション内のフローを確認します。

   ![](./media/create-flow-solution/new-flow-inside-solution.png)

## <a name="learn-more"></a>詳細については、こちらをご覧ください

* [ソリューションを作成する](./overview-solution-flows.md)
* [ソリューションをエクスポートする](./export-flow-solution.md)
* [ソリューションをインポートする](./import-flow-solution.md)
* [ソリューション対応フローを編集する](./edit-solution-aware-flow.md)
* [ソリューション対応フローを削除する](./remove-solution-aware-flow.md)
