---
title: Power Automate のリージョンの概要 | Microsoft Docs
description: Power Automate のリージョンに関する質問と回答の概要
services: ''
suite: flow
documentationcenter: na
author: MSFTMan
manager: KVivek
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/07/2020
ms.author: deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: a87845247f57e58edf7170dc3e8da721db7d275e
ms.sourcegitcommit: 27ee91452be26cf5c96397c39f9f5b8bede14cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/08/2020
ms.locfileid: "80862517"
---
# <a name="faq-for-regions-in-power-automate"></a>Power Automate のリージョンに関する FAQ

このドキュメントでは、Power Automate についてよく寄せられる質問のリストを提供します。

## <a name="how-do-i-find-out-where-my-flow-is-deployed"></a>自分のフローがデプロイされる場所を確認する方法
フローは、[環境](environments-overview-admin.md)をホストする[リージョン](https://azure.microsoft.com/regions/)にデプロイされます。 たとえば、環境がヨーロッパ リージョンで作成されている場合、フローはヨーロッパのデータ センターに保存されます。

管理者は、Power Automate [管理センター](https://admin.flow.microsoft.com)にサインインすると、リージョンを識別できます。 **[環境]** タブには、既存のすべての環境とそのリージョンが一覧表示されます。

![環境を表示する](media/regions-overview/environments-list.png)

## <a name="what-regions-are-available"></a>どのリージョンを利用できますか。
* 米国
* ヨーロッパ
* アジア
* オーストラリア
* インド
* 日本
* カナダ
* 南アメリカ
* イギリス
* 米国政府向け (GCC)
* フランス

## <a name="what-features-are-specific-to-a-given-region"></a>リージョン固有の機能

環境は複数の異なるリージョンに作成でき、その地理的な場所にバインドされます。 環境にフローを作成すると、そのフローはその地理的な場所のデータセンターにデプロイされます。 これは、Common Data Model、フロー、接続、ゲートウェイ、アプリ、カスタム コネクタなど、その環境で作成するすべての項目に適用されます。

最適なパフォーマンスのためには、ユーザーに最も近いリージョンに環境を作成します。 たとえば、ユーザーがヨーロッパにいる場合は、ヨーロッパ リージョンに環境を作成します。 ユーザーが米国にいる場合は、米国リージョンに環境を作成します。

## <a name="region-mappings-for-power-automate-and-gateways"></a>Power Automate とゲートウェイのリージョン マッピング

ゲートウェイがインストールされているリージョンは、Power Automate リージョンにマップする必要があります。 地理的な境界間でのマップはサポートされていません。 

マッピング情報を次に示します。

Power Platform リージョン|ゲートウェイ リージョン
-----|-----
米国 (プレビューを含む)|米国中部、米国東部 2、米国東部、米国中北部、米国中南部、米国西部 2、米国中西部、米国西部
アジア|東アジア、東南アジア
オーストラリア|オーストラリア東部、オーストラリア南東部
カナダ|カナダ中部、カナダ東部
ヨーロッパ|北ヨーロッパ、西ヨーロッパ
フランス|フランス中部、フランス南部
インド|インド中部、インド南部、インド西部
日本|東日本、西日本
南アメリカ|ブラジル南部
イギリス|英国南部、英国西部

## <a name="is-power-automate-available-in-national-clouds"></a>Power Automate は各国のクラウドで使用できますか?
はい。 [詳細情報](./us-govt.md)

## <a name="what-outbound-ip-addresses-are-used-in-each-region"></a>各リージョンではどのような送信 IP アドレスが使われますか。
「[制限事項と構成](limits-and-config.md)」を参照してください。

