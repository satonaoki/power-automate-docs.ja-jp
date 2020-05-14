---
title: Microsoft アカウント (MSA) で Power Automate GDPRデータ対象者削除要求をする | Microsoft Docs
description: Power Automate を使用して、Microsoft アカウント (MSA) で Power Automate GDPRデータ対象者の削除要求をする方法について説明します。
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
ms.date: 5/25/2018
search.app:
- Flow
- Powerplatform
search.audienceType:
- admin
ms.openlocfilehash: 48aafe66584e42f3011b135ff8dbdc5fec69737f
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3297958"
---
# <a name="respond-to-gdpr-data-subject-delete-requests"></a>GDPR データ主体の削除要求に応答する


個人データの削除による**忘れられる権利**は、GDPR での重要な保護です。 個人データの削除では、監査ログの情報を除く、すべての個人データが削除されます。

Power Automate では、ユーザーが自動化されたワークフローをビルドできます。 ユーザーが  Power Automate から個人データを削除するときに、ユーザーは個人データを確認し、その一部を削除するか、すべてを削除するかを決定します。

次の表では、自動的に削除される個人データと、Microsoft アカウント (MSA) ユーザーが確認して削除する必要があるデータを示します。

|MSA ユーザーが確認して削除する必要がある|自動的に削除済み|
|------|------|
|製品とサービス アクティビティ|実行履歴|
|フロー|アクティビティ フィード|
|つながり||

Power Automate では、ユーザーが自動的に削除されない個人データとリソースを検索、確認または変更できる以下のエクスペリエンスが提供されています。

## <a name="manage-delete-requests"></a>削除要求を管理する

以下の手順では、GDPR のセルフサービスの削除要求に対応する方法を説明します。

### <a name="delete-product-and-service-activity"></a>製品とサービス アクティビティを削除する

1. MSA で [Microsoft プライバシー ダッシュボード](https://account.microsoft.com/privacy/)にサインインします。
1. **[アクティビティの履歴]** リンクを選択します。

    ![アクティビティの履歴](./media/gdpr-dsr-export-msa/activityhistory.png)

1. Power Automate など、使用するさまざまな Microsoft アプリケーションとサービスのアクティビティの履歴を検索または参照できます。 **[削除]** を選択して、特定の製品またはサービス アクティビティ イベントを削除します。

    ![イベントを削除する](./media/gdpr-dsr-delete-msa/deleteevent.png)

1. 数分以内に、プライバシー ダッシュボードからその項目が削除されます。

### <a name="list-and-delete-flows"></a>フローを一覧して削除する

ユーザーは、次の手順を実行して、[Power Automate](https://flow.microsoft.com) からフローをリストアップして削除できます。

1. [Power Automate](https://flow.microsoft.com) にサインインし、**自分のフロー** を選びます。

1. 削除するフローの横にある **[...]** を選択して、**[削除]** を選択します。

    ![イベントを削除する](./media/gdpr-dsr-delete-msa/deleteflow.png)

### <a name="delete-connections"></a>接続を削除する

コネクタでは、接続を使用して、API および SaaS システムと通信します。 接続には、これらのシステムを作成するユーザーへの参照が含まれます。 ユーザーは、次の手順を実行して、いつでもこれらの参照を削除できます。

1. [Power Automate](https://flow.microsoft.com) にサインインし、歯車アイコンを選択して、**接続** を選択します。

    ![イベントを削除する](./media/gdpr-dsr-delete-msa/deleteconnections.png)

1. 削除する接続を選択して、**[...]**、**[削除]** の順に選択します。

    ![イベントを削除する](./media/gdpr-dsr-delete-msa/delete-connection.png)

1. 確認プロンプト上の **[削除]** アイコンを選択します。

    ![イベントを削除する](./media/gdpr-dsr-delete-msa/confirmdelete.png)

> [!NOTE]
> 他のフローで削除している接続を使用する場合は、新しい接続が必要とされることが通知されます。 それ以外の場合は、**[削除]** を選択して続行します。
>
>

## <a name="learn-more"></a>詳細はこちら

* [Power Automate](getting-started.md) の使用の開始
* Power Automate の [新機能](release-notes.md)
