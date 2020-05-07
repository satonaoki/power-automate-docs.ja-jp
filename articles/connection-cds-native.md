---
title: Common Data Service (現在の環境) コネクタを使用して自動化されたフローを作成する | Microsoft Docs
description: Common Data Service (現在の環境) コネクタと Power Automate を使用してワークフローを作成する
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
ms.openlocfilehash: 96b97fe3e6090a2810c0fa0e1dfae2d4b890da62
ms.sourcegitcommit: e58c8e6954c8e666497a66dc945fdc16c7c845a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/02/2020
ms.locfileid: "82728541"
---
# <a name="create-an-automated-flow-by-using-common-data-service-current-environment"></a>Common Data Service (現在の環境) を使用して自動化されたフローを作成する

>[!IMPORTANT]
>Common Data Service に接続するために使用できるコネクタが 3 つあります。 この記事では、Common Data Service に接続する場合に推奨される [Common Data Service (現在の環境) コネクタ](./connection-cds.md)について説明します。 また、[Common Data Service コネクタ](./connection-cds.md)と [Dynamics 365 コネクタ](https://docs.microsoft.com/connectors/dynamicscrmonline/)は、推奨コネクタを使用できない場合に使用できます。


Common Data Service (現在の環境) コネクタを使用するには、[ソリューション対応のフローを作成](./overview-solution-flows.md)する必要があります。 

作成したフローは、Common Data Service レコードが作成、更新、または削除されたときにトリガーできます。

さらに、Common Data Service 内のレコードに対して、作成、更新、取得、削除のアクションを実行できます。

## <a name="initiate-a-flow-with-common-data-service-current-environment"></a>Common Data Service (現在の環境) を使ったフローを開始する

**[When a record is created, updated or deleted]\(レコードが作成、更新、または削除されたとき\)** トリガーを使用して、フローを開始します。

   ![トリガーの選択](./media/cds-connector-native/native-trigger.png)

トリガーを選択したら、次の構成を行う必要があります。

- トリガーの条件。
- エンティティの名前。
- トリガーのスコープ。

### <a name="trigger-condition"></a>トリガーの条件

次の条件のいずれかを追加して、フローがトリガーされるタイミングを正確に決定できます。

   ![トリガーの選択](./media/cds-connector-native/trigger-conditions.png)

### <a name="the-entity-name"></a>エンティティ名

利用可能な多数のエンティティのいずれかを選択して、トリガーが動作するエンティティを示します。

   ![トリガーの選択](./media/cds-connector-native/entity-names.png)

### <a name="scope"></a>スコープ

スコープを使用して、誰 (自分、部署内の誰か、または組織内のユーザー) がレコードを作成したときにフローが実行されるかを決定します。

![スコープの選択](./media/cds-connector-native/scopes.png)

各スコープの詳細を次に示します。

|スコープ|トリガーのタイミング|
| --- | --- |
|部署|自分の部署が所有しているレコードに対して、アクションが実行される|
|組織|組織内またはデータベース内の任意のユーザーによってアクションが実行される|
|部署配下|自分の部署または配下の部署が所有しているレコードに対して、アクションが実行される|
|ユーザー|自分が所有しているレコードに対して、アクションが実行される|


レコードが更新されたときに実行されるトリガーには、フィルター処理の属性も使用できます。 これにより、定義されているいずれかの属性が更新されたときにのみフローが実行されることが確実になります。

> [!IMPORTANT]
> フィルター属性を使用して、フローが不必要に実行されることを防ぎます。

このフローは、フローのユーザーが所有している連絡先の姓または名が更新されたときにトリガーされます。

![フィルター属性](./media/cds-connector-native/filtering-attributes.png)

## <a name="trigger-privileges"></a>トリガーの権限

レコードに対する作成、更新、または削除に基づいてトリガーされるフローを作成するユーザーには、**コールバック登録**エンティティに対する作成、読み取り、書き込み、削除のユーザー レベル権限が必要です。 さらに、定義されたスコープによっては、ユーザーは同じエンティティに対して少なくともそのレベルの読み取りを必要とする場合があります。  環境のセキュリティの[詳細については、こちらを参照してください](https://docs.microsoft.com/power-platform/admin/database-security)。

## <a name="write-data-into-common-data-service"></a>Common Data Service にデータを書き込む

Common Data Service にデータを書き込むには、次のいずれかのアクションを使用します。

![フィルター属性](./media/cds-connector-native/actions.png)

次に示すフローの例では、部署 (**スコープ**) 内の誰かが**アカウント**を**作成**するたびに、その名前と年間収益の通知が送信されます。

> ![フォローアップ タスク](./media/cds-connector-native/example-flow.png)

## <a name="advanced-concepts"></a>高度な概念

### <a name="write-data-into-customer-owner-and-regarding-fields"></a>顧客、所有者、関連の各フィールドにデータを書き込む

顧客、所有者、関連の各フィールドにデータを書き込むには、2 つのフィールドを設定する必要があります。

| フィールドのカテゴリ | 設定の例 |
| --- | --- |
| 関連 | 関連 = レコードの ID (アカウント ID など) と一覧から選択した関連の種類。 |
| 顧客 | レコードの ID と一覧から選択した顧客の種類を表します。 |
| 所有者 | システム ユーザーまたはチームの ID と、一覧から選択した顧客の種類を表します。 |

### <a name="enable-upsert-behavior"></a>upsert 動作を有効にする

**レコードを更新する**アクションを利用して、レコードが既に存在する場合はレコードを更新し、存在しない場合は新しいレコードを作成する upsert アクションを提供できます。 upsert を呼び出すには、エンティティと GUID キーを指定します。 指定した種類とキーを持つレコードが存在する場合は、更新が発生します。 それ以外の場合、指定したキーを持つレコードが作成されます。

### <a name="trigger-behavior"></a>トリガー動作

レコードの更新時に登録されているトリガーがある場合、フローは特定のレコードへの*コミットされた*更新のたびに実行されます。 フローはサービスによって非同期的に呼び出され、呼び出しが発生した時点で取得されたペイロードを含みます。

> [!NOTE]
> 数秒以内に発生する 2 つの更新がある場合、最新バージョンのコンテンツを使用してフローが複数回トリガーされる可能性があります。

ご使用の環境内にシステム ジョブのバックログがある場合、フローの実行が遅延することがあります。 この遅延が発生した場合、フローは、フローを開始するシステム ジョブが実行されたときにトリガーされます。



