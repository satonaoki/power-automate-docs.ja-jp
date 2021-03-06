---
title: Web UI フローを編集する方法 | Microsoft Docs
description: Web UI フローを編集する方法について説明します。
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
ms.date: 11/04/2019
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 74c323f844c6bdc0f4cb1ad3d1a37977070a0a26
ms.sourcegitcommit: bba5bd4ae3879b6bf1521d8ed636374fe09709e7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3298750"
---
# <a name="edit-web-ui-flows"></a>Web UI フローの編集

Web UI フローでは、[Microsoft Edge (バージョン 80 以降) ](https://www.microsoft.com/edge/) または Google Chrome で実行されている Web サイトが自動化されます。 [Web UI フローを作成](create-web.md)した後で、それを編集する必要がある場合があります。 このドキュメントの手順に従って、Web UI フローを編集する方法を学習します。

## <a name="edit-in-selenium-ide"></a>Selenium IDE での編集

Selenium IDE を使用して、Web UI フローを編集します。

>[!NOTE]
>Selenium IDE での編集は、上級ユーザーと開発者を対象としています。

スクリプトの編集方法については、[Selenium のコマンド](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/)を参照してください。

Selenium IDE では、ユーザー インターフェイス要素をターゲットにするときに、さまざまなセレクターと既定値が提示されます。 提案されたセレクターが適切でない場合は、新しいセレクターを定義することもできます。 これは通常、Web サイトの HTML 構造が高度に動的である場合に発生します。

Selenium IDE で特定できるセレクターの例を次に示します。

![使用可能なセレクター](../media/edit-web/possible-selectors.png "使用可能なセレクター")

## <a name="accessing-a-property-of-an-object-variable-or-item-of-an-array-variable"></a>オブジェクト変数のプロパティまたは配列変数の項目へのアクセス **

この高度な機能を使用すると、\${foo.bar} のような構文を使用して、foo オブジェクトの bar プロパティにアクセスできます。 store コマンドの value プロパティとして foo を使用して、foo の bar プロパティに書き込むこともできます。 \${foo[0]} のような構文を使用して、foo 配列内のインデックス 0 の項目にアクセスすることもできます。

## <a name="next-steps"></a>次のステップ

- [Web UI フローの作成](create-web.md)
- [UI フローの実行](run-ui-flow.md)
