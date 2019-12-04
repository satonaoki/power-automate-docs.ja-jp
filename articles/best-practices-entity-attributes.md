---
title: ビジネス プロセス フロー エンティティ属性使用時のベスト プラクティス | MicrosoftDocs
description: ビジネス フロー エンティティ属性使用時のベスト プラクティスについて説明します。
ms.custom: ''
ms.date: 04/23/2019
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Business Process Flows
helpviewer_keywords:
- flow
- process flow
- business process flow
- process
- workflow
author: msftman
ms.author: deonhe
manager: kvivek
ms.openlocfilehash: ffc9fef64a9eda74d8a834745204fd635125e0c2
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74357268"
---
# <a name="best-practices-in-using-business-process-flow-attributes"></a>ビジネス プロセス フロー属性使用時のベスト プラクティス
[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]


エンティティにおける従来のプロセス関連の属性は非推奨になっています。 ビジネス プロセス フロー エンティティで*アクティブ ステージ* (activestageid) 属性を使用するときのベスト プラクティスをいくつか紹介します。 

## <a name="reporting-on-the-active-stage-of-a-business-process-flow"></a>ビジネス プロセス フローのアクティブ ステージについて報告する

**リードから営業案件への営業プロセス**がオンになっているアクティブ ステージについて報告することで営業パイプラインが見えるようにすることを望んでいるとします。

以前は、ステージ別にビジネス プロセスについて報告するとき、ビジネス プロセス フローの関連エンティティごとにビューを定義し、*アクティブ ステージ* (activestageid) フィールドについて報告することがありました。

関連エンティティの *アクティブ ステージ* (activestageid) フィールドが非推奨になっているため、ビジネス プロセス フローは 2 とおりの方法で報告できます。

### <a name="option-1-views-and-charts-on-business-process-flow-entity-recommended"></a>選択肢 1: ビジネス プロセス フロー エンティティのビューとグラフ **(推奨)**

バージョン 9.0 以降では、ビジネス プロセス フローごとに、通常はビジネス プロセス フロート同じ名前で独自の Common Data Service エンティティが作成されます。 ビジネス プロセス フローについて報告するには、報告対象のビジネス プロセス フローのエンティティを選択し、前と同じようにビューとグラフを作成します。

今回の例では、次の手順で**リードから営業案件への営業プロセス**エンティティに移動します。
1. https://make.powerapps.com に移動します。
1. **[データ]** を選択します。
1. **[エンティティ]** を選択します。
1. フィルターを **[すべて]** に設定します。
1. **リードから営業案件への営業プロセス** エンティティを探して選択します。

   ![リードから営業案件への営業プロセス エンティティ](media/best-practices-entity-attributes/lead-opportunity-process.png)

ここで、他のあらゆるエンティティと同様にビューとグラフを定義できます。

![変換プロセス エンティティの詳細](media/best-practices-entity-attributes/lead-to-opportunity-sales-process-details.png)

この方法の利点は、単一のビューまたはグラフを使用し、複数のエンティティにまたがるビジネス プロセス フローについて報告できることです。

さらに、ビジネス プロセス フロー エンティティは Common Data Service の他のあらゆるカスタム エンティティと変わらないため、カスタム フィールドをエンティティに追加し、必要な追加情報を追跡記録できます。

### <a name="option-2-copy-active-stage-to-a-related-entity"></a>選択肢 2: アクティブ ステージを関連エンティティにコピーする

あるいは、関連エンティティに関する報告を続行するには、ビジネス プロセス フロー エンティティから関連 Common Data Service エンティティのカスタム フィールドに*アクティブ ステージ* (activestageid) フィールドをコピーするフローを作成します。

この手法を使用するとき、いくつかのことにご留意ください。

1.  1 つのエンティティで複数のビジネス プロセス フローを実行することができます。 この手法の場合、エンティティで実行されるビジネス プロセス フロー別のアクティブ ステージを 1 つのカスタム フィールドで格納することをお勧めします。 この手法では、報告の整合性が維持されます。

1.  関連エンティティが報告元であるため、複数のエンティティにまたがるビジネス プロセス フローについて報告する 1 つのビューを作成することはできません。

## <a name="using-the-active-stage-to-run-logic"></a>アクティブ ステージを使用してロジックを実行する

次のような場合、アクティブ ステージに基づいてロジックを実行することがあります。

### <a name="using-the-active-stage-to-run-client-side-logic"></a>アクティブ ステージを使用してクライアント側のロジックを実行する

ビジネス プロセスを使用するとき、自動化が望ましい作業がたくさんあります。 例:

-   フォームまたはビジネス プロセス フローに関して新しく利用できる情報に基づき、アクティブなビジネス プロセス フローを変更します。

-   手順またはフォーム フィールドにユーザーが入力した値に基づき、アクティブ ステージを次のステージか前のステージに移動します。

-   選択したステージに基づき、フォーム タブとフィールドの表示と非表示を切り替えます。

-   アクティブなビジネス プロセス フロー、アクティブ ステージ、選択されているステージ、アクティブ ステージの移動などのイベントに基づき、情報メッセージを表示し、計算を実行します。

> [!TIP]
> 以上のようなシナリオの場合、ビジネス プロセス フロー用としてサポートされている一連の[クライアント API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/clientapi/reference/formcontext-data-process) を使用してください。
>

### <a name="using-the-active-stage-to-run-server-side-logic"></a>アクティブ ステージを使用してサーバー側のロジックを実行する

ビジネス プロセス フローに基づく自動化をサーバー側で行う必要がある場合があります。 例:

-   **営業案件の営業プロセス**の**見込みありと評価する**ステージがアクティブな状態になって 15 日間以上経過した場合、ユーザーに電子メールを送信します。

-   **営業案件の営業プロセス**のアクティブ ステージが変化するたびに、そのプロセスに関連する一連のアクティビティを自動的に作成します。

-   終了のための通話アクティビティが完了したとき、**営業案件の営業プロセス**を自動的に完了します。

> [!TIP]
> ビジネス プロセス フローのエンティティに定義したクラシック Common Data Service ワークフローまたはフローを使用します。
> 

内部ソリューション レビューのアクティビティを作成する Common Data Service ワークフローを構築し、**営業案件の営業プロセス**の**提案**ステージで顧客をフォローアップするには:

1. **営業案件の営業プロセス** エンティティでフローを作成し、エンティティの**アクティブ ステージ** フィールドが変化するたびに実行するようにそれを設定します。 
1. **アクティブ ステージ** フィールドが**提案**になっていることを確認する条件を定義します。 
1. ソリューションの内部レビューのための予約と通話レコードと、ソリューションをレビューするための顧客コールをそれぞれ作成します。

   ![ステージ終了フォローアップ](media/best-practices-entity-attributes/close-stage-followup.png)
