---
title: OneDrive for Business の起動パネルからフローを作成する |Microsoft Docs
description: OneDrive for Business の起動パネルからフローを作成します。
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
ms.date: 08/25/2019
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 7458b3cb08ca1ce3e29a9d0d29e1bec91d46f7ea
ms.sourcegitcommit: 84fb0547e79567efa19d7c16857176f7f1b53934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "79193199"
---
# <a name="create-flows-from-the-onedrive-for-business-launch-panel"></a>OneDrive for Business の起動パネルからフローを作成する


[SharePoint 内の Power Automate の起動パネル](https://flow.microsoft.com/blog/introducing-flow-launch-panel-in-sharepoint-lists-and-libraries/)と同様に、OneDrive for Business の特定のファイルに対してフローを実行できます。 

この機能により、フローを実行しているユーザーが独自の資格情報を使用できるようになります。これは、IT 部門によって作成されたフローに特に当てはまります。 

ユーザーは、**承認者**や**メッセージ**などのランタイムの入力に対するプロンプトも表示できます。これには、テキスト、ファイル、電子メール、ブール値、または数値を入力できます。

このチュートリアルでは、多くの [OneDrive for Business テンプレート](https://flow.microsoft.com/search/?q=OneDrive)の 1 つを使用して、要求元の上司によるファイルの承認を要求するシンプルなフローを作成します。

## <a name="create-a-flow-that-requests-manager-approval-for-a-file-in-onedrive-for-business"></a>OneDrive for Business のファイルに対して上司の承認を要求するフローを作成する

1. OneDrive for Business にサインインします。
1. フローを作成するファイルを検索して選択します。
1. **アクションの表示**リンク (3 つの点) を選択します。
1. **[フロー]**  >  **[フローの作成]** を選択します。

     ![フローの作成](./media/onedrive-launch-panel/create-flow.png) 

1. いずれかのテンプレートを選択します。

    この例では、 **[選択したファイルについて上司の承認を要求する]** テンプレートを選択します。

     >[!TIP]
     >サインインを要求するコネクタにサインインします。

1. **[続行]** を選択します。
1. テンプレートに必要な変更を加え、覚えやすい名前でフローを保存します。

## <a name="run-the-flow"></a>フローを実行する

1. OneDrive for Business にサインインします。
1. 上司の承認を要求するファイルを検索して選択します。
1. **アクションの表示**リンク (3 つの点) を選択します。
1. **[フロー]** を選択します。 先ほど作成したフローが表示されます。
1. 先ほど作成したフローを選択します。

     ![フローを実行する](./media/onedrive-launch-panel/run-flow.png)


>[!TIP]
>このチュートリアルでは、テンプレートからフローを作成する方法について示しますが、一からフローを作成して、Power Automate で使用可能な多くのコネクタを使用することもできます。

## <a name="learn-more"></a>詳細情報

- [Power Automate の概要](getting-started.md) 
- [複数ステップのフローの作成](multi-step-logic-flow.md)
