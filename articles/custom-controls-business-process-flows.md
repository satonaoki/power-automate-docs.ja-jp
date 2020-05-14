---
title: ビジネス プロセス フローでカスタム コントロールを使用する | Microsoft Docs
description: ビジネス プロセス フローのステップでカスタム コントロールを使用する方法について説明します。
services: ''
suite: flow
documentationcenter: na
author: msftman
manager: kVivek
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 12/15/2019
ms.author: deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: cd312fea655dfc652cf92a440801da2fdb17ebe4
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3297034"
---
# <a name="use-custom-controls-in-business-process-flows"></a>ビジネス プロセス フローでカスタム コントロールを使用する

ビジネス プロセス フローでは、作業を行うためのガイド付きの方法が、ステージとステップという形式で提供されます。 ステージによって自分がプロセスのどの段階にいるかがわかります。一方、ステップは必要な結果につながるアクション項目です。 ビジネス プロセス内のステップは、 Common Data Service のフィールドにバインドされます。 フィールドの種類 (テキスト ボックス、ドロップダウンなど) の既定の視覚化だけでなく、カスタム コントロールを使用して、ビジネス プロセス フローのステップに高度な視覚化 (スライダー、放射状ノブ、LinkedIn コントロールなど) を追加し、ご自分のビジネス プロセスを使用するユーザーに魅力的なエクスペリエンスを提供することができます。

## <a name="adding-custom-controls-to-a-business-process"></a>ビジネス プロセスにカスタム コントロールを追加する

たとえば、[リードから営業案件への営業プロセス] の **[推定予算金額]** ステップに放射状ノブを追加し、**[意思決定者の特定]** ステップにフリップ スイッチを追加する必要があるとします。 

![概要](./media/custom-controls/overview.png)

ビジネス プロセス フローにカスタム コントロールを追加するには、次の手順を実行する必要があります。

1. 関連するエンティティ フォームでカスタム コントロールを構成します。
1. ビジネス プロセス フローのフォームを生成してエクスポートします。
1. 関連するエンティティ フォームから、カスタム コントロールの構成をビジネス プロセス フローのフォームにコピーします。
1. カスタマイズを Common Data Service にインポートします。

ビジネス プロセス フローのステップに[カスタム コントロールを追加する詳細なチュートリアル](https://powerusers.microsoft.com/t5/Power-Automate-Community-Blog/Preview-Custom-Controls-in-Business-Process-Flows/ba-p/263237)のこれらの手順を実行します。






