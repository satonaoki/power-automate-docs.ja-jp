---
title: SharePoint アイテムのリマインダー フローを作成する | Microsoft Docs
description: SharePoint アイテムの期限が迫っていることを通知するフローを作成します。
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
ms.date: 04/30/2019
ms.author: deonhe
ms.openlocfilehash: 414c14b02b0543dc3992253192020b7453b9e2e0
ms.sourcegitcommit: 84fb0547e79567efa19d7c16857176f7f1b53934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "79192900"
---
# <a name="sharepoint-remind-me"></a>SharePoint の通知を受け取る


SharePoint のリストとライブラリを使用すると、カスタム メタデータ列を定義して日付を追跡できます。 Power Automate と SharePoint の統合により、SharePoint の DateTime 列に基づいて、リマインダー フローを簡単に作成できます。 リマインダー フローを使用すると、SharePoint のドキュメントまたはアイテムの日付より事前に指定した日数だけ前に、個人のメール アラートを受け取ります。

## <a name="prerequisites"></a>前提条件
- Microsoft SharePoint Online へのアクセス。
- DateTime 列が含まれる SharePoint リストまたはライブラリ。
- Power Automate へのアクセス。

## <a name="create-a-reminder-flow"></a>リマインダー フローを作成する

 1. 現在のビューに少なくとも 1 つの DateTime 列を含む [SharePoint リスト](https://support.office.com/article/Create-a-list-in-SharePoint-0D397414-D95F-41EB-ADDD-5E6EFF41B083)を作成します。 
 1. **[フロー]**  >  **[リマインダーを設定する]**  >  **[Date deactivated]** (これは、リマインダー対象の DateTime を含む列です) を選択します。

     ![リマインダー フローを選択する](media/create-sharepoint-reminder-flows/select-reminder-flow.png)

1. **[リマインダーを設定する]** カードで、 **[フロー名]** と、DateTime 列のエントリの何日前にリマインダー アラートを受け取るかを指定します。

    ![リマインダー フローの詳細を設定する](media/create-sharepoint-reminder-flows/set-reminder-details.png)

1. **[リマインダーを設定する]** カードで、 **[作成]** を選択します。

1. フローが作成されたことを示す次のメッセージが表示されます。

    ![作成されたリマインダー フロー](media/create-sharepoint-reminder-flows/success.png)
    

## <a name="confirm-reminders-received"></a>リマインダーの受信を確認する

前に作成した **[リマインダーを設定する]** のフローで指定した **[何日も前にあらかじめこれを通知する]** に基づいて、電子メールでリマインダーを受け取ります。 

## <a name="edit-your-flow"></a>フローを編集する

リマインダー フローは他のフローと同じなので、[Power Automate](https://flow.microsoft.com) を使用してアクセスしたり編集したりすることができます。

## <a name="learn-more"></a>詳細情報

- [Power Automate](https://flow.microsoft.com) の概要。
- SharePoint で[リマインダー フロー](https://support.office.com/article/set-a-reminder-flow-23c0e172-1fc1-4ac8-a9db-cd0b81d634d8)を設定する。


