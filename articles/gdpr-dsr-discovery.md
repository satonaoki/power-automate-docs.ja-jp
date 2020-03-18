---
title: Power Automate での GDPR データ主体の検出要求 | Microsoft Docs
description: Power Automate を使用して GDPR データ主体の検出要求に応答する方法を説明します。
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
ms.date: 4/17/2018
search.app:
- Flow
- Powerplatform
search.audienceType:
- admin
ms.openlocfilehash: 05def202f2a0b0db8a6eebb067406c96221e7d1c
ms.sourcegitcommit: 84fb0547e79567efa19d7c16857176f7f1b53934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "79195545"
---
# <a name="responding-to-gdpr-data-subject-discovery-requests-for-power-automate"></a>Power Automate に対する GDPR データ主体の検出要求への応答


DSR への応答の最初のステップは、要求の主体である個人データを見つけることです。 この最初のステップは、DSR の要求を承諾または拒絶するための組織の要件を DSR が満たしているかどうかを判断するのに役立ちます。 たとえば、問題の個人データを見つけて確認した後、他のユーザーの権利または自由に悪影響を及ぼす可能性があるため要求が組織の要件を満たしていないと判断する可能性があります。

特定のユーザーの個人データを格納している Power Automate リソースの種類の概要を次に示します。

|**個人データが含まれるリソース**|**目的**|
|-----|-----|
|システム生成ログ|システムのイベントと履歴をキャプチャするテレメトリ。|
|実行履歴|過去 28 日間の各フローの実行の履歴。 このデータには、開始時刻、終了時刻、状態、およびフローのすべての入力/出力情報が含まれています。 [詳細情報](https://flow.microsoft.com/blog/download-history-recurrence/)|
|アクティビティ フィード| 実行状態、エラー、通知など、フロー アクティビティの要約を提供します。|
|ユーザー ジョブ|ユーザーには表示されない、フロー実行のためにユーザーに代わって実行されるシステム ジョブ。|
|フロー|フローに対して存在するワークフロー ロジック。 [詳細情報](https://docs.microsoft.com/flow/get-started-logic-flow)|
|フローのアクセス許可|フローは、他のユーザーと共有したり、他のユーザーに再割り当てしたりできます。 アクセス許可リストはすべてのフローに存在します。 [詳細情報](https://docs.microsoft.com/flow/frequently-asked-questions#can-i-share-the-flows-i-create)|
|ユーザーの詳細|ユーザーが見ることはできない、フローの実行をサポートする詳細情報。|
|接続|コネクタによって使用され、API、システム、データベースなどに接続できます。 [詳細情報](https://docs.microsoft.com/flow/add-manage-connections)|
|接続のアクセス許可|特定の接続のアクセス許可。 [詳細情報](https://docs.microsoft.com/flow/add-manage-connections)|
|カスタム コネクタ|カスタム システムまたはサードパーティ システムに接続できる、ユーザーが作成して公開したカスタム コネクタ。 [詳細情報](https://docs.microsoft.com/connectors/custom-connectors/)|
|カスタム コネクタのアクセス許可|カスタム コネクタのアクセス許可リスト。 [詳細情報](https://docs.microsoft.com/connectors/custom-connectors/share)|
|ゲートウェイ|ゲートウェイは、Power Automate とクラウド内にないデータ ソースの間ですばやく安全にデータを転送するためにユーザーがインストールできるオンプレミスのデータ サービスです。 [詳細情報](https://docs.microsoft.com/flow/gateway-manage)|
|ゲートウェイのアクセス許可|ゲートウェイは、組織内のユーザーと共有することができます。 [詳細情報](https://go.microsoft.com/fwlink/?linkid=872249)|
