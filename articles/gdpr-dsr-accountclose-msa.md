---
title: Microsoft アカウント (MSA) で Power Automate GDPRデータ対象者のアカウント削除要求をする | Microsoft Docs
description: Power Automate を使用して、Microsoft アカウント (MSA) で Power Automate GDPRデータ対象者のアカウント削除要求をする方法について説明します。
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
ms.openlocfilehash: 10f232e45a53cea30892f512b626246fec16deed
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3297826"
---
# <a name="responding-to-gdpr-data-subject-account-close-requests-for-power-automate"></a>Power Automate の GDPR データ対象者のアカウント削除要求に対応する


個人データの**忘れられる権利**は、GDPR での重要な保護です。 この権利には、監査ログの情報を除く、すべての個人データの削除が含まれます。 ユーザーが自分の Microsoft アカウント (MSA) を削除する場合、ユーザーの基になるデータも削除されます。

これらのリソースには、ユーザーが MSA を削除するときに自動的に削除される個人データが含まれます。

|個人データが含まれるリソース|
|------|
|製品とサービス アクティビティ|
|実行履歴|
|フロー|
|アクティビティ フィード|
|ユーザーの詳細|
|つながり|

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

    この 30 日の期間が終了すると、この MSA のすべての Power Automate のリソースを削除するプロセスが開始されます。

## <a name="learn-more"></a>詳細はこちら

* [Power Automate](getting-started.md) の使用の開始
* Power Automate の [新機能](release-notes.md)
