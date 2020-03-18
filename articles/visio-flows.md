---
title: Microsoft Visio でフローを設計する | Microsoft Docs
description: Visio に関する組織の専門知識を活用し、フローを作成するための出発点として一般的なモデルを構築します。
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
ms.date: 08/25/2019
ms.author: deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 1df42c58cb02f8d62e016b071b3ce556b06a0efe
ms.sourcegitcommit: 84fb0547e79567efa19d7c16857176f7f1b53934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "79195890"
---
# <a name="design-flows-in-microsoft-visio"></a>Microsoft Visio でフローを設計する


Power Automate デザイナーは、ロジックのあらゆる細部を構成できる多機能ツールです。 しかしながら、フローの構築を始める前にフロー ロジックをスケッチすることがあります。 その際、Power Automate 内から直接、Microsoft Visio を使用します。

>[!TIP]
> さまざまなプロセスで一般的なモデルが共有されますが、組織全体で細かな違いがあります。 Visio を利用してマスター ワークフローを作成することで、組織内で時間を節約できます。マスター ワークフローはその後、他のユーザーが特別なパラメーターで調整します。

## <a name="prerequisites"></a>前提条件

- Power Automate アカウント。
- Microsoft Visio デスクトップ アプリ (英語版)。
- Microsoft Visio の使用に関する専門知識。

## <a name="design-a-workflow-in-visio"></a>Visio でワークフローを設計する

1. [Power Automate](https://flow.microsoft.com) にサインインします。
1. 左側パネルから **[テンプレート]** を選択します。

     ![左側パネルからテンプレートを選択します。](./media/visio-flows/templates-from-left-panel.png)

1. 一覧から **[Visio]** を選択します。

     ![Visio テンプレートにフィルターを適用する](./media/visio-flows/select-visio.png) 

1. 表示された **Visio** テンプレートの一覧から **[Flow の基本的な BPMN 図]** テンプレートを選択します。

     ![Visio テンプレートを選択する](./media/visio-flows/visio-templates.png) 

     >[!IMPORTANT]
     >Visio からは、インターネットから入手したファイルはお使いのデバイスに害を与えるおそれがあることが警告されます。 問題なければ、警告メッセージ上の **[はい]** を選択します。

     ![インターネットから入手したファイルに関する警告に注意](./media/visio-flows/visio-warning.png)

1. Visio デザイナーが起動します。

     ![Visio デザイナーの外観](./media/visio-flows/visio-designer.png)


1. BPMN 基本図形を使用し、[ワークフローを設計します](https://support.office.com/article/design-a-microsoft-flow-in-visio-35f0c9a9-912b-486d-88f7-4fc68013ad1a)。

   ![BPMN 基本図形](./media/visio-flows/bpmn-basic-shapes.png)

## <a name="prepare-to-export-your-workflow-to-power-automate"></a>Power Automate にワークフローをエクスポートする準備をする

Power Automate にエクスポートできるように次の手順でワークフローを準備します。

1. **[プロセス]** タブを選択します。
1. アイコンの **[Power Automate]** グループから **[エクスポートの準備]** を選択します。

   ![[エクスポートの準備] アイコンを選択する](./media/visio-flows/prepare-export-icon.png)
   
   **[エクスポートの準備]** グループが開きます。

   ![[エクスポートの準備] グループ](./media/visio-flows/prepare-export-group.png)

1. **[エクスポートの準備]** グループの **[Flow のマッピング]** タブで、BPMN 図を Power Automate にマッピングします。 

1. **[エクスポートの準備]** グループの **[トリガーとアクション]** タブで、各図形を選択したら、Power Automate でその図形を表わすトリガーまたはアクションを選択することで、BPMN 図を Power Automate のトリガーとアクションにマッピングします。

**[エクスポートの準備]** コントロールに問題が残っていなければ、ワークフローはいつでもエクスポートできます。

![問題なし](./media/visio-flows/prepare-export-no-issues.png) 

## <a name="export-your-workflow"></a>ワークフローをエクスポートする
1. **[Flow にエクスポート]** ボタンを選択し、ワークフロー図を Power Automate にエクスポートします。
1. フローに名前を付け、 **[フローの作成]** ボタンを選択します。
   
   ![フローを作成する](./media/visio-flows/export-create-flow.png)

1. これに似たような成功レポートが表示されるはずです。

    ![成功](./media/visio-flows/export-create-flow-success.png)

これで、他のあらゆるフローと同様に、Power Automate デザイナーからフローを実行したり、編集したりできます。

>[!TIP]
> Visio の共有機能とコメント機能を利用して複数の関係者と共同作業すれば、ワークフローが短期間で完成します。

## <a name="learn-more"></a>詳細情報

- [Power Automate の概要](getting-started.md) 
- [複数ステップのフローの作成](multi-step-logic-flow.md)
- [Microsoft Visio でフローを設計する](https://support.office.com/article/design-a-microsoft-flow-in-visio-35f0c9a9-912b-486d-88f7-4fc68013ad1a)

     
