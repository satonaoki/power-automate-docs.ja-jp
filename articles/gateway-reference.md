---
title: オンプレミス データ ゲートウェイ | Microsoft Docs
description: この記事は Power Automate のオンプレミス データ ゲートウェイの概要です。
services: ''
suite: flow
documentationcenter: na
author: MSFTMan
manager: KFile
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: conceptual
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/16/2019
ms.author: deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 46a661b8e4cae28be2c25e8b07269b2677ca5667
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74367940"
---
# <a name="what-is-an-on-premises-data-gateway"></a>オンプレミス データ ゲートウェイとは
[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]

オンプレミス データ ゲートウェイはブリッジとして機能し、オンプレミス データ (クラウド内に存在しないデータ) といくつかの Microsoft クラウド サービスとの間でデータをすばやく安全に転送できます。 そのようなクラウド サービスには、Power BI、Power Apps、Power Automate、Azure Analysis Services、Azure Logic Apps があります。 ゲートウェイを使用することにより、組織はオンプレミス ネットワーク上のデータベースやその他のデータソースを維持しながら、そのオンプレミス データをクラウド サービスで安全に使用することができます。

## <a name="how-the-gateway-works"></a>ゲートウェイのしくみ

![ゲートウェイの概要](media/gateway-reference/on-premises-data-gateway.png)

ゲートウェイのしくみの詳細については、「[オンプレミス データ ゲートウェイのアーキテクチャ](/data-integration/gateway/service-gateway-onprem-indepth)」を参照してください。

## <a name="types-of-gateways"></a>ゲートウェイの種類

ゲートウェイには次の 2 種類があり、それぞれ異なるシナリオで使用されます。

- **オンプレミス データ ゲートウェイ**の場合、複数のユーザーが複数のオンプレミスのデータ ソースに接続できます。 単一のゲートウェイ インストールで、サポートされているすべてのサービスでオンプレミス データゲートウェイを使用できます。 このゲートウェイは、複数のユーザーが複数のデータ ソースにアクセスする複雑なシナリオに適しています。

- **オンプレミス データ ゲートウェイ (個人用モード)** の場合、1 人のユーザーがソースに接続できます。他のユーザーとは共有できません。 オンプレミスのデータ ゲートウェイ (個人用モード) は、Power BI でのみ使用できます。 このゲートウェイは、レポートを作成するユーザーが 1 人だけであり、データ ソースを他のユーザーと共有する必要がないシナリオに適しています。

## <a name="use-a-gateway"></a>ゲートウェイの使用

ゲートウェイを使用するための 4 つの主要な手順があります。

1. ローカル コンピューターに[ゲートウェイをダウンロードしてインストール](/data-integration/gateway/service-gateway-install)します。
2. ご利用のファイアウォールやその他のネットワーク要件に基づいてゲートウェイを[構成](/data-integration/gateway/service-gateway-app)します。
3. 他のネットワーク要件も管理および操作できる[ゲートウェイ管理者を追加](/data-integration/gateway/service-gateway-manage)します。
4. エラーが発生した場合にゲートウェイの[トラブルシューティング](/data-integration/gateway/service-gateway-tshoot)を行います。

## <a name="next-steps"></a>次のステップ

- [オンプレミス データ ゲートウェイのインストール](/data-integration/gateway/service-gateway-install)
