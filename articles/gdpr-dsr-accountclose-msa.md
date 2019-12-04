---
title: Power Automate での Microsoft アカウント (MSA) に対する GDPR データ主体のアカウントの削除要求 | Microsoft Docs
description: Power Automate を使用して、Microsoft アカウントに対する GDPR データ主体のアカウントの削除要求に応答する方法について説明します。
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
ms.openlocfilehash: 277765754683a6690b186a5f592517482b32666f
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74366376"
---
# <a name="responding-to-gdpr-data-subject-account-close-requests-for-power-automate"></a>Power Automate に対する GDPR データ主体のアカウントの削除要求への応答
[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]

個人データの**忘れられる権利**は、GDPR での重要な保護です。 この権利には、監査ログの情報を除く、すべての個人データの削除が含まれます。 ユーザーが自分の Microsoft アカウント (MSA) を削除する場合、ユーザーの基になるデータも削除されます。

これらのリソースには、ユーザーが MSA を削除するときに自動的に削除される個人データが含まれます。

|個人データが含まれるリソース|
|------|
|製品とサービス アクティビティ|
|実行履歴|
|フロー|
|アクティビティ フィード|
|ユーザーの詳細|
|接続|

## <a name="account-close-requests"></a>アカウントの削除要求

これらの手順では、GDPR のセルフサービスのアカウント削除要求に対応する方法を説明します。

1. Microsoft アカウントを使用して [Microsoft アカウントの削除ポータル](https://go.microsoft.com/fwlink/?LinkId=523898)にサインインし、**[次へ]** を選択します。

    > [!NOTE]
    > 既存のサブスクリプションをキャンセルするか、サブスクライブしている可能性がある既存のサービスからデータをエクスポートすることが通知されます。
    >
    >

    ![サブスクリプションの取り消し](./media/gdpr-dsr-delete-msa/accountclose.png)

1. MSA の削除による影響を理解していることを確認し、**[アカウントを削除する]** を選択します。

    アカウントが 30 日以内に削除されることを示す通知が表示されます。 この 30 日の期間中であれば、いつでもこのアカウントを再開することができます。

    ![削除されるアカウント](./media/gdpr-dsr-delete-msa/accountclosed.png)

    この 30 日の期間が終了すると、この MSA のすべての Power Automate リソースを削除するプロセスが開始されます。

## <a name="learn-more"></a>詳細については、こちらをご覧ください

* [Power Automate](getting-started.md) の概要
* Power Automate での[新機能](release-notes.md)を確認する
