---
title: ソリューション対応フローの概要| Microsoft Docs
description: ソリューション内にフローを作成する利点について説明します。
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
ms.openlocfilehash: 56b90ebdf7f3655763b7e40c60b985f06604c47b
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3298288"
---
# <a name="overview"></a>概要


[ソリューション](https://docs.microsoft.com/powerapps/maker/common-data-service/solutions-overview)でフローをホストすると、フローが移植可能になり、フローとそのすべてのコンポーネントを 1 つの環境から別の環境へ簡単に移動できるようになります。 典型的なユース ケースとしては、独立系ソフトウェア ベンダー (ISV) がサンドボックス環境内でフローを開発して、そのフローをテスト環境に移動する場合などが考えられます。 テストした後、ISV はこれらのフローを購入したクライアントに向けて運用環境にフローを移動します。 ソリューション内でフローを作成してからソリューションとそのコンテンツを移動すると、このプロセスははるかに簡単になります。

ソリューション内で作成するフローは、"*ソリューション対応*" フローと呼ばれます。 1 つのソリューションに複数のフローを追加できます。

> [!NOTE] 
> ソリューション対応ではないフロー (ソリューションで作成されたのではないフロー) をソリューションに移動することはできません。

## <a name="prerequisites"></a>前提条件

ソリューションとソリューション対応フローを作成するには、次のコンポーネントが必要です。

- [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
- バージョン 9.1.0.267 以上の環境

  バージョンを確認するには、[Power Automate 管理センター](https://admin.flow.microsoft.com) に移動して **環境** を選択し、目的の環境を選択してから **詳細** タブを選択します。

## <a name="create-a-solution"></a>ソリューションの作成

ソリューションを作成するには次の手順に従います。

1. [Power Automate](https://flow.microsoft.com) にサインインします。
1. ナビゲーション バーから **[ソリューション]** を選択します。

   ![](./media/overview-solution-flows/select-solutions-from-left-nav.png)

1. **[+ New solution]\(+ 新しいソリューション\)** を選択します。

   ![](./media/overview-solution-flows/select-new-solution.png)

1. 新しいソリューションに必要なすべての情報を指定します (**[表示名]**、**[発行者]**、**[バージョン]**、**[名前]** など)。 ソリューションの説明を入力することもお勧めします。

   ![](./media/overview-solution-flows/new-solution.png)

1. 上部にあるメニューから **[保存して閉じる]** を選択します。

   ![](./media/overview-solution-flows/save-and-close-solution.png)

   新しいソリューションは次の図のように表示されます。

   ![](./media/overview-solution-flows/new-solution-created.png)

   > [!TIP]
   > 新しいソリューションが表示されない場合は、**[ソリューション]** を選択してソリューションの一覧を更新します。

## <a name="learn-more"></a>詳細はこちら

- [ソリューションにフローを作成する](./create-flow-solution.md)
- [ソリューションのエクスポート](./export-flow-solution.md)
- [ソリューションのインポート](./import-flow-solution.md)
- [ソリューション対応フローを編集する](./edit-solution-aware-flow.md)
- [ソリューション対応フローを削除する](./remove-solution-aware-flow.md)
