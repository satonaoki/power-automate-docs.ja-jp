---
title: オンプレミス データ ゲートウェイについて | Microsoft Docs
description: Power Automate でオンプレミス データ ゲートウェイを表示してインストールします。
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
ms.date: 02/13/2020
ms.author: deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: f3600587897b9e64ecd76f85c8b9762e84bc7b94
ms.sourcegitcommit: dbba53a52e2c5b1c2965f6c608e586748d5baae0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2020
ms.locfileid: "77567003"
---
# <a name="manage-an-on-premises-data-gateway-in-power-automate"></a>Power Automate でオンプレミス データ ゲートウェイを管理する
[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]

オンプレミス データ ゲートウェイをインストールして管理すると、Power Automate を介してさまざまなクラウドベースのアプリをオンプレミスのデータやアプリと安全に統合できます。

ゲートウェイを使用すると、次の接続を介して、オンプレミス データに接続できます。

* Apache Impala
* 作成するカスタム コネクタ
* DB2
* ファイル システム
* Azure AD での http
* Informix
* MySQL
* Oracle Database
* PostgreSQL
* SharePoint
* SQL Server
* Teradata (プレビュー)

> [!IMPORTANT]
> Microsoft SharePoint データ ゲートウェイは、HTTP トラフィックと HTTPS トラフィックの両方をサポートするようになりました。

## <a name="prerequisites"></a>前提条件

* Power Automate への[サインアップ](sign-up-sign-in.md)で使用したユーザー名とパスワード。
* ゲートウェイの管理者アクセス許可。

  インストールするゲートウェイごとに、これらのアクセス許可が既定で与えられます。 また、別のゲートウェイの管理者がそのゲートウェイのこれらのアクセス許可を与えることができます。
* ゲートウェイをサポートするライセンス。 詳細については、[料金に関するページ](https://flow.microsoft.com/pricing/)の「Connectivity (接続)」セクションを参照してください。

> [!TIP]
> ゲートウェイとオンプレミスの接続は、[任意の環境](environments-overview-maker.md)で作成することができます。

## <a name="install-a-gateway"></a>ゲートウェイのインストール

ゲートウェイをインストールするには、「[オンプレミス データ ゲートウェイをインストールする](/data-integration/gateway/service-gateway-install)」に記載の手順に従います。 _オンプレミス データ ゲートウェイ (個人用モード)_ は Power BI にのみ使用できるため、ゲートウェイを標準モードでインストールします。

## <a name="view-your-gateways"></a>ゲートウェイを表示する

[Power Automate Web サイト](https://flow.microsoft.com)の右上隅にある歯車アイコンを選択して、 **[ゲートウェイ]** を選択します。

![管理対象のゲートウェイ][1]

> [!NOTE]
> ゲートウェイへのアクセス権限を作成した場合、または Power Apps でゲートウェイへのアクセス権限が付与されている場合、Power Automate の **[ゲートウェイ]** 一覧にそのゲートウェイが表示されます。

## <a name="cluster-your-gateways"></a>ゲートウェイをクラスター化する

[オンプレミス データ ゲートウェイ インストールの高可用性クラスター](/data-integration/gateway/service-gateway-high-availability-clusters)を作成することで、オンプレミスのデータ リソースにアクセスする際の単一障害点を回避することができます。

既定では、Power Automate では、クラスター内のプライマリ ゲートウェイが使用されます。 プライマリ ゲートウェイが使用できない場合、サービスはクラスター内の次のゲートウェイに切り替わります (以下同様)。

ゲートウェイ クラスターを設定したら、クラスター内のすべてのゲートウェイにトラフィックを分散させることができます。

ご利用のゲートウェイ間でトラフィックを分散するには、次の手順に従います。

1. 左側にあるナビゲーション バーで **[データ]** を選択します。
1. **[ゲートウェイ]** を選択します。
1. ご利用のゲートウェイのいずれかを選択します。
1. **[このクラスター内のすべてのアクティブなゲートウェイで要求を配布します]** を選択します。
1. **[適用]** を選択して変更を保存します。

詳細については、[ゲートウェイの概要](gateway-reference.md)に関するページを参照してください。

<!-- Image references -->
[1]: ./media/manage-gateway/view-gateways.png
