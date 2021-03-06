---
title: Microsoft Teams におけるフローの作成と管理の概要 | Microsoft Docs
description: フローを作成して管理することで、要求に応じてメッセージの投稿、ユーザーやチャンネルへの @mention 、応答オプションを使用したカードの投稿ができます。
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
ms.openlocfilehash: 1fbd0c6b1f6a7cd453f6c1a336f5ce450e236c5e
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3296836"
---
# <a name="power-automate-in-teams"></a>Teams の Power Automate


### <a name="prerequisites"></a>前提条件

1. Microsoft Teams へのアクセス。
1. Power Automate へのアクセス。

## <a name="install-the-power-automate-app-in-teams"></a>Teams で Power Automate アプリをインストールする

この手順に従って Microsoft Teams に Power Automate アプリをインストールします。

1. Microsoft Teams にサインインします。

1. Teams のナビゲーション バーの左下にある **[アプリ]** アイコンをタップします。

    ![アプリを選択](media/flows-teams/apps.png)

1. **[Flow]** アプリを選択します。 **[Flow]** が表示されない場合は、検索が必要になることがあります。

    ![[Flow] アプリを選択](media/flows-teams/select-flow-app.png)

1. **インストール**を選択します。

    ![[インストール] ボタン](media/flows-teams/select-install.png)

1. Power Automate がインストールされました。

    ![インストール完了](media/flows-teams/flow-installed.png)


## <a name="create-a-flow-in-teams"></a>Teams でフローを作成する

1. Microsoft Teams にサインインします。

1. ナビゲーション バーで **[さらに追加されたアプリ]** リンク (...) を選択してから、**[Flow]** アプリを選択します。

    ![追加されたアプリのアイコン](media/flows-teams/added-apps-icon.png)

1. それをまだ行っていない場合は、サインインしてアクセス許可を付与する必要があります。

    ![サインイン](media/flows-teams/grant-permissions-sign-in.png)


    次のタブに注目してください。

    ![Flow のランディング ページ](media/flows-teams/flow-landing-page.png)

    件名|目的
    ----|-----|
    会話|Flow ボットとやりとりします。
    フロー|フローを作成して管理します。
    承認|受信済みまたは送信済みの承認要求を一覧表示します。
    バージョン情報|Power Automate のバージョンおよびその他の情報を表示します。


    以上で、Power Automate のデザイナーで作成したすべてのフローが表示されます (存在する場合)。 

    また、 Power Automate デザイナーで行う場合と同様に、カスタム テンプレートまたは空のテンプレートからフローを作成することもできます。 

## <a name="manage-approvals"></a>承認を管理する

Power Automate と同様に、Microsoft Teams では [承認](modern-approvals.md) を管理できます。 承認を管理するには、次の手順に従います。

1. Microsoft Teams にサインインします。
1. **[承認]** タブを選択します。

    ![[承認] タブ](media/flows-teams/approvals-tab.png)

    次のサブタブが表示されます。

    タブ​​|目的
    ----|-----|
    受け取り済み|お客様が受信済みであり、お客様からのアクションを保留にしている承認要求を一覧表示します。
    送信日時|お客様が送信済みであり、他のお客様からのアクションを保留にしている承認要求を一覧表示します。
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
