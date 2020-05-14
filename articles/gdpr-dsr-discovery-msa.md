---
title: Microsoft アカウント (MSA) で Power Automate GDPRデータ対象者の検出要求をする | Microsoft Docs
description: Power Automate を使用して、Microsoft アカウント (MSA) で Power Automate GDPRデータ対象者の検出要求をする方法について説明します。
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
ms.openlocfilehash: 5e1dc452bdbe7aa65700d159cf9365812dc50bfb
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3298002"
---
# <a name="respond-to-gdpr-data-subject-discovery-requests"></a>GDPR データ主体の検出要求に応答する 


DSR 要求への応答の最初の手順は、要求の主体である個人データを見つけることです。
Microsoft アカウント (MSA) での認証を行うユーザーの個人データを含む、Power Automate リソースの概要は次のとおりです。

|リソース|目的|
|-----|-----|
|実行履歴|過去 28 日間の各フローの実行履歴を示します。 このデータには、開始時刻、終了時刻、状態、および各フローの実行に対するすべての入力/出力情報が含まれています。 [フローの実行履歴](https://flow.microsoft.com/blog/download-history-recurrence/)に関する詳細。|
|アクティビティ フィード| 実行状態、エラー、通知など、各フローのアクティビティの要約を提供します。|
|フロー|[フロー](https://docs.microsoft.com/flow/get-started-logic-flow)に対するワークフロー ロジック。|
|つながり|コネクタによって使用され、API、システム、データベースなどに接続できます。 [接続](add-manage-connections.md)に関する詳細。|

