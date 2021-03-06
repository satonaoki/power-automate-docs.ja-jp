---
title: Common Data Serviceで自動フローを作成する | Microsoft Docs
description: Common Data Service の接続と Power Automate を使用してワークフローを作成する
services: ''
suite: flow
documentationcenter: na
author: MSFTMAN
manager: KVIVEK
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/26/2020
ms.author: Deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 18719ac34d84298dd813b0241d00b652ae172ef6
ms.sourcegitcommit: e58c8e6954c8e666497a66dc945fdc16c7c845a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/02/2020
ms.locfileid: "3331085"
---
# <a name="create-an-automated-flow-by-using-common-data-service"></a>Common Data Service を使用して自動化されたフローを作成する

>[!IMPORTANT]
>Common Data Service に接続できるコネクタは 3 つ存在します。 推奨される [Common Data Service（現在の環境）コネクタ](./connection-cds-native.md) を使用してください。 この記事に記載している **Common Data Serviceコネクタ**、[Dynamics 365 Connector](https://docs.microsoft.com/connectors/dynamicscrmonline/) は、推奨コネクタが使用できない場合にご利用いただけます。


Common Data Service コネクタを使用すると、Common Data Service 内で作成、更新されるイベントによって開始するフローを作成できます。 さらに、Common Data Service 内のレコードに対して、作成、更新、取得、削除のアクションを実行できます。

## <a name="initiate-a-flow-from-common-data-service"></a>Common Data Service からフローを開始する

次のいずれかのトリガーを使用してフローを開始できます。

- レコードが選択されたとき
- レコードが作成されたとき
- レコードが削除されたとき
- レコードが更新されたとき


> [!div class="mx-imgBorder"]
> ![トリガーの選択](./media/cds-connector/Triggers.png)

選択したトリガーが環境の選択をする必要がある場合は、 `(Current)` を選択できます。これにより、Power Automate を実行する環境内のデータベースが常に使用されます。 フローが特定の環境におけるイベントに基づいて常にトリガーされるようにする場合は、その環境を選択します。

> [!div class="mx-imgBorder"]
> ![環境の選択](./media/cds-connector/Environments.png)

スコープを使用して、フローが実行されるのが、自分が新しいレコードを作成したときか、部署内のユーザーによって新しいレコードが作成されたときか、または組織内の任意のユーザーによって新しいレコードが作成されたときかを決定できます。

> [!div class="mx-imgBorder"]
> ![スコープの選択](./media/cds-connector/Scopes.png)

|Scope|トリガーのタイミング|
| --- | --- |
|部署 |自分の部署が所有しているレコードに対して、アクションが実行される|
|組織全体|組織内またはデータベース内の任意のユーザーによってアクションが実行される|
|部署配下|自分の部署または配下の部署が所有しているレコードに対して、アクションが実行される|
|ユーザー |自分が所有しているレコードに対して、アクションが実行される|

レコードが更新されたときに実行されるトリガーには、フィルター処理の属性も使用できます。 これにより、定義されているいずれかの属性が更新されたときにのみフローが実行されることが確実になります。

> [!IMPORTANT]
> フィルター属性を使用して、フローが不必要に実行されることを防ぎます。

このフローは、フローのユーザーが所有している連絡先の姓または名が更新されたときにトリガーされます。

> [!div class="mx-imgBorder"]
> ![フィルター属性](./media/cds-connector/FilterAttributes.png)

## <a name="trigger-privileges"></a>トリガーの権限

レコードに対する作成、更新、または削除に基づいてトリガーされるフローを作成するには、コールバック登録エンティティに対する作成、読み取り、書き込み、削除のユーザー レベル権限がユーザーに必要です。 さらに、定義されたスコープによっては、ユーザーは同じエンティティに対して少なくともそのレベルの読み取りを必要とする場合があります。  環境のセキュリティの[詳細については、こちらを参照してください](https://docs.microsoft.com/power-platform/admin/database-security)。

## <a name="write-data-into-common-data-service"></a>Common Data Service にデータを書き込む

Common Data Service にデータを書き込むには、次のいずれかのアクションを使用します：

- 新しいレコードを作成します
- レコードの更新

特定のユーザーが新しいアカウント レコードを作成したときのフォロー アップ タスクを作成する例を次に示します。  

> [!div class="mx-imgBorder"]
> ![フォローアップ タスク](./media/cds-connector/Regarding.png)

## <a name="advanced-concepts"></a>高度な概念

### <a name="write-data-into-customer-owner-and-regarding-fields"></a>顧客、所有者、関連の各フィールドにデータを書き込む

顧客、所有者、関連の各フィールドにデータを書き込むには、2 つのフィールドを設定する必要があります。

| フィールドのカテゴリ | 設定の例 |
| --- | --- |
| 関連 | 関連 = レコードの ID (アカウント ID など) と一覧から選択した関連の種類。 |
| 顧客 | レコードの ID と一覧から選択した顧客の種類を表します。 |
| 所有者  | システム ユーザーまたはチームの ID と、一覧から選択した顧客の種類を表します。 |

### <a name="enable-upsert-behavior"></a>upsert 動作を有効にする

**レコードを更新する**コマンドを利用して upsert アクションを指定することができます。これにより、レコードが既に存在する場合はレコードを更新するか、新しいレコードを作成します。 upsert を呼び出すには、エンティティと GUID キーを指定します。 指定した種類とキーを持つレコードが存在する場合は、更新が発生します。 それ以外の場合、指定したキーを持つレコードが作成されます。

### <a name="trigger-behavior"></a>トリガー動作

レコードの更新時に登録されているトリガーがある場合、フローは特定のレコードへの*コミットされた*更新のたびに実行されます。 フローはサービスによって非同期的に呼び出され、呼び出しが発生した時点で取得されたペイロードを含みます。

> [!NOTE]
> 数秒以内に発生する 2 つの更新がある場合には、バージョン管理された最新のコンテンツを使用してフローが複数回トリガーされる可能性があります。

ご使用の環境内にシステム ジョブのバックログがある場合、フローの実行が遅延することがあります。  この遅延が発生した場合、フローは、フローを呼び出すシステム ジョブが実行されたときにトリガーされます。

