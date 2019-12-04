---
title: Microsoft Teams でフローを作成および管理する方法を学習する | Microsoft Docs
description: フローを作成して管理することで、要求に応じてメッセージを投稿したり、ユーザーやチャンネルを @mention したり、応答オプションを使用してカードを投稿したりできます。
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
ms.date: 04/29/2019
ms.author: deonhe
ms.openlocfilehash: a2a9b5d5a6ed8305ed3e7c29717ef19978bae0a7
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74367066"
---
# <a name="power-automate-in-teams"></a>Teams での Power Automate
[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]

### <a name="prerequisites"></a>前提条件

1. Microsoft Teams にアクセスできること。
1. Power Automate へのアクセス。

## <a name="install-the-power-automate-app-in-teams"></a>Power Automate アプリを Teams にインストールする

Microsoft Teams に Power Automate アプリをインストールするには、次の手順に従います。

1. Microsoft Teams にサインインします。

1. Teams のナビゲーション バーの左下にある **[アプリ]** アイコンをタップします。

    ![アプリを選択](media/flows-teams/apps.png)

1. **[Flow]** アプリを選択します。 **[Flow]** が表示されない場合は、検索が必要になることがあります。

    ![[Flow] アプリを選択](media/flows-teams/select-flow-app.png)

1. **[インストール]** を選択します。

    ![[インストール] ボタン](media/flows-teams/select-install.png)

1. これで Power Automate がインストールされました。

    ![インストール済み](media/flows-teams/flow-installed.png)


## <a name="create-a-flow-in-teams"></a>Teams でフローを作成する

1. Microsoft Teams にサインインします。

1. ナビゲーション バーで **[さらに追加されたアプリ]** リンク (...) を選択してから、**[Flow]** アプリを選択します。

    ![追加されたアプリのアイコン](media/flows-teams/added-apps-icon.png)

1. それをまだ行っていない場合は、サインインしてアクセス許可を付与する必要があります。

    ![サインイン](media/flows-teams/grant-permissions-sign-in.png)


    次のタブに注目してください。

    ![Flow のランディング ページ](media/flows-teams/flow-landing-page.png)

    Name (名前)|目的
    ----|-----|
    会話|Flow ボットとやりとりします。
    フロー|フローを作成して管理します。
    承認|受信済みまたは送信済みの承認要求を一覧表示します。
    バージョン情報|Power Automate のバージョンおよびその他の情報を表示します。


    これで、Power Automate デザイナーで作成したすべてのフローが表示されます (存在する場合)。 

    また、Power Automate デザイナーで行う場合と同様に、カスタム テンプレートまたは空のテンプレートからフローを作成することもできます。 

## <a name="manage-approvals"></a>承認を管理する

Power Automate で行う場合と同様に、Microsoft Teams でも[承認](modern-approvals.md)を管理することができます。 承認を管理するには、次の手順に従います。

1. Microsoft Teams にサインインします。
1. **[承認]** タブを選択します。

    ![[承認] タブ](media/flows-teams/approvals-tab.png)

    次のサブタブが表示されます。

    タブ|目的
    ----|-----|
    受信済み|お客様が受信済みであり、お客様からのアクションを保留にしている承認要求を一覧表示します。
    送信済み|お客様が送信済みであり、他のお客様からのアクションを保留にしている承認要求を一覧表示します。
    履歴|受信済みまたは送信済みの承認要求を一覧表示します。
    承認フローを作成する|承認フローを作成します。

1. 詳細については、**[受信済み]** タブ、**[送信済み]** タブ、または **[履歴]** タブを選択します。

    ![[承認] タブ](media/flows-teams/approvals-tab-2.png)

1. 承認フローを作成するには、**[承認フローの作成]** を選択します。

    ![[承認] タブ](media/flows-teams/approvals-tab-3.png)

## <a name="use-the-bot-with-flows"></a>フローに対してボットを使用する

### <a name="list-and-launch-flows-with-the-bot"></a>ボットを使用してフローを一覧表示および起動する

> [!TIP]
> ボットを使用すると、スケジュールによってトリガーされるフロー、またはユーザーの入力なしで手動でトリガーされるフローを一覧表示し、実行することができます。

1. Microsoft Teams にサインインします。
1. ナビゲーション バーで **[さらに追加されたアプリ]** リンク (...) を選択してから、**[Flow]** アプリを選択します。

    ![追加されたアプリのアイコン](media/flows-teams/added-apps-icon.png)
    
1. **[会話]** タブを選択します。

    ![[会話] タブ](media/flows-teams/conversations-tab.png)

**[会話]** タブでは、ボットにコマンドを送信できます。ボットは、実行するように命令されたアクションを実行することで応答します。 たとえば、ご利用のフローを一覧表示し、インデックス 1 のフローを実行するには、次のコマンドを実行します。

- ```List flows``` - プレフィックスとしてインデックス番号が付けられたフローがボットによって一覧表示されます。
- ```Run flow 1``` - フロー番号 1 を実行します。 ここで、*1* は、実行するフローのインデックス番号です。

   ![ボットのコマンド](media/flows-teams/bot-commands.png)

### <a name="get-the-description-for-flows"></a>フローの説明を取得する

フローの一覧からインデックス 1 が付けられたフローの説明を取得するには、```describe flow 1``` を実行します。 ボットの応答は、次の画像のようになります。

   ![フローを説明する](media/flows-teams/bot-describe.png)

### <a name="get-the-list-of-commands-for-the-bot"></a>ボットのコマンドの一覧を取得する

ボットが処理するコマンドの一覧を取得するには、```learn more``` コマンドを使用してそれを要求します。 

ボットの応答は、次の画像のようになります。

![フローを説明する](media/flows-teams/bot-learn-more.png) 
