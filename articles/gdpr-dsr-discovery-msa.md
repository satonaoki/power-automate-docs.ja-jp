---
title: Power Automate での Microsoft アカウント (MSA) に対する GDPR データ主体の検出要求 | Microsoft Docs
description: Power Automate を使用して Microsoft アカウントに対する GDPR データ主体の検出要求に応答する方法を説明します。
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
ms.date: 5/16/2018
search.app:
- Flow
- Powerplatform
search.audienceType:
- admin
ms.openlocfilehash: 2830d08832bad330ec67717234f5a8cb0482d3a9
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74369044"
---
# <a name="respond-to-gdpr-data-subject-discovery-requests"></a>GDPR データ主体の検出要求に応答する 
[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]

DSR 要求への応答の最初の手順は、要求の主体である個人データを見つけることです。
Microsoft アカウント (MSA) での認証を行うユーザーの個人データを含む、Power Automate リソースの概要は次のとおりです。

|リソース|目的|
|-----|-----|
|実行履歴|過去 28 日間の各フローの実行履歴を示します。 このデータには、開始時刻、終了時刻、状態、および各フローの実行に対するすべての入力/出力情報が含まれています。 [フローの実行履歴](https://flow.microsoft.com/blog/download-history-recurrence/)に関する詳細。|
|アクティビティ フィード| 実行状態、エラー、通知など、各フローのアクティビティの要約を提供します。|
|フロー|[フロー](https://docs.microsoft.com/flow/get-started-logic-flow)に対するワークフロー ロジック。|
|接続|コネクタによって使用され、API、システム、データベースなどに接続できます。 [接続](add-manage-connections.md)に関する詳細。|

