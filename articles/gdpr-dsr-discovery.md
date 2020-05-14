---
title: Power Automate GDPRデータ対象者の検出要求 | Microsoft Docs
description: Power Automate を使用して GDPRデータ対象者の検出要求に対応する方法を説明します。
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
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3297166"
---
# <a name="responding-to-gdpr-data-subject-discovery-requests-for-power-automate"></a>Power Automate の GDPRデータ対象者の検出要求に対応する


DSR への応答の最初のステップは、要求の主体である個人データを見つけることです。 この最初のステップは、DSR の要求を承諾または拒絶するための組織の要件を DSR が満たしているかどうかを判断するのに役立ちます。 たとえば、対象の個人データを探して確認した後で、要求に応えると、他のユーザーの権利や自由が損なわれる可能性があるため、要求は組織の要件を満たしていないものと判断する場合があります。

以下は、特定のユーザーの個人データを含む Power Automate リソースの種類一覧です。

|**個人データが含まれるリソース**|**目的**|
|-----|-----|
|システムによって生成されたログ|システムのイベントと履歴をキャプチャするテレメトリ。|
|実行履歴|過去 28 日間の各フローの実行の履歴。 このデータには、開始時刻、終了時刻、状態、およびフローのすべての入力/出力情報が含まれています。 [詳細情報](https://flow.microsoft.com/blog/download-history-recurrence/)|
|アクティビティ フィード| 実行状態、エラー、通知など、フロー アクティビティの要約を提供します。|
|ユーザー ジョブ|ユーザーには表示されない、フロー実行のためにユーザーに代わって実行されるシステム ジョブ。|
|フロー|フローに対して存在するワークフロー ロジック。 [詳細情報](https://docs.microsoft.com/flow/get-started-logic-flow)|
|フロー アクセス許可|フローは、他のユーザーと共有したり、他のユーザーに再割り当てしたりできます。 アクセス許可リストはすべてのフローに存在します。 [詳細情報](https://docs.microsoft.com/flow/frequently-asked-questions#can-i-share-the-flows-i-create)|
|ユーザーの詳細|ユーザーが見ることはできない、フローの実行をサポートする詳細情報。|
|つながり|コネクタによって使用され、API、システム、データベースなどへの接続に対応します。 [詳細情報](https://docs.microsoft.com/flow/add-manage-connections)|
|接続のアクセス許可|特定の接続のアクセス許可。 [詳細情報](https://docs.microsoft.com/flow/add-manage-connections)|
|カスタム コネクタ|カスタム システムまたはサードパーティ システムに接続できる、ユーザーが作成して公開したカスタム コネクタ。 [詳細情報](https://docs.microsoft.com/connectors/custom-connectors/)|
|カスタム コネクタのアクセス許可|カスタム コネクタのアクセス許可リスト。 [詳細情報](https://docs.microsoft.com/connectors/custom-connectors/share)|
|ゲートウェイ|ゲートウェイはオンプレミスのデータ サービスであり、ユーザーはそれをインストールすることで、Power Automate とクラウド内に存在しないデータ ソースの間でデータをすばやく安全に転送できます。 [詳細情報](https://docs.microsoft.com/flow/gateway-manage)|
|ゲートウェイのアクセス許可|ゲートウェイは、組織内のユーザーと共有することができます。 [詳細情報](https://go.microsoft.com/fwlink/?linkid=872249)|
