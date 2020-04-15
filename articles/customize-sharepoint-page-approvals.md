---
title: Power Automate による SharePoint ページの承認の管理 | Microsoft Docs
description: Power Automate を使用して SharePoint ページの承認を管理する方法について説明します。
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
ms.date: 04/06/2020
ms.author: deonhe
ms.openlocfilehash: 5fa6c10245c5fbc974ae96dd926c8e5b193aaab4
ms.sourcegitcommit: c43c98cc777780d42d15e287233c040771a6e147
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2020
ms.locfileid: "80801514"
---
# <a name="manage-sharepoint-page-approvals-with-power-automate"></a>Power Automate による SharePoint ページの承認の管理


SharePoint サイト管理者は、Power Automate を使用して、新規または更新されたサイト ページが発行される前に承認を求めるようにすることができます。

この記事では、フローを使用してサイトへの変更が公開される前に承認されるように求めるように、SharePoint サイトの構成方法を学習します。

## <a name="configure-sharepoint-for-page-approvals"></a>ページの承認用に SharePoint を構成する

### <a name="prerequisites"></a>前提条件 

この記事のアクティビティを実行するには、SharePoint サイトの管理者である必要があります。

1. サイト管理者として SharePoint にサインインします。
1. ナビゲーション バーから **[ページ]** を選択します。

    ![ページの承認フローの選択](media/customize-sharepoint-page-approvals/pages.png)

1. **[自動化]**  >  **[Power Automate]**  >  **[ページの承認フローの構成]** を選択します。
    
    ![ページの承認フローの選択](media/customize-sharepoint-page-approvals/select-page-approval-flow.png)

1. **[フローの作成]** を選択します。

1. 場合によっては、この Power Automate テンプレートで使用されるサービスにサインインする必要があります。

1. **[続行]** を選択します。

1. **フロー名**を指定し、 **[承認者]** ボックスに少なくとも 1 つの名前を入力して、 **[作成]** を選択します。
    
    ![ページの承認フローの選択](media/customize-sharepoint-page-approvals/flow-name-approvers-create.png)

これだけです。 これで、ページが追加または変更されるたびに、フローにリストされている**承認者**に承認要求が送信されます。

ページの承認フローは他のフローと同様で、 **[マイ フロー]** タブに一覧表示されます。

![ページの承認フローの選択](media/customize-sharepoint-page-approvals/page-approval-flow-success.png)

## <a name="submit-a-page-for-approval"></a>承認のためにページを送信する

ページの承認フローを作成したので、ページを追加または変更した人すべてが次の操作を行う必要があります。

 - サイトに (新しいページを追加するなどの) 変更を加え、変更を保存します。

     ![承認のためにページを送信する](media/customize-sharepoint-page-approvals/create-new-page.png)
     
 - だれかが変更を承認するのを待ちます。
    
    ![承認のためにページを送信する](media/customize-sharepoint-page-approvals/wait-for-approval.png)
    
## <a name="approve-a-page"></a>ページを承認する

承認者は、ページの承認要求があるたびにメールを受信します。 要求はメールで直接承認することも (メール クライアントでアクション可能メッセージがサポートされている場合)、メールからページを開いて確認してから SharePoint でページを承認することもできます。

## <a name="customize-page-approval-flows"></a>ページの承認フローをカスタマイズする

ページの承認ではバックグラウンドで Power Automate が使用されるため、サイト所有者がページの承認フローを使用して、フロー内の任意のカスタム ビジネス ロジックを変更および追加できます。 フローを変更するには、サイト所有者が **[フロー]** 選択し、ページ ライブラリで **[フローの表示]** を選択してページの承認フローを見つけることができます。

## <a name="learn-more"></a>詳細情報

- [ページの承認フロー](https://support.office.com/article/page-approval-flow-a8b2e689-d4a1-4639-8028-333c0ece30d9)
- [ページの承認を構成する](https://support.office.com/article/configure-page-approval-14ce6976-a0a7-427b-b4ab-d28d344a5222)
