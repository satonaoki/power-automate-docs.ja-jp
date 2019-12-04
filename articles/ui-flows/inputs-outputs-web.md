---
title: Web UI フローで入力と出力を使用する | Microsoft Docs
description: Web UI フローで入力と出力を使用する。
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
ms.openlocfilehash: 38b6ba7f8fe3ab7a386229b6c9c5ccc300a147de
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74371413"
---
# <a name="use-inputs-and-outputs-in-web-ui-flows"></a>Web UI フローで入力と出力を使用する

[このトピックはプレリリース版のドキュメントであり、変更される可能性があります。]

[!INCLUDE [view-pending-approvals](../includes/cc-rebrand.md)]

## <a name="define-inputs-for-a-web-ui-flow"></a>Web UI フローの入力を定義する

UI フローの入力を使用すると、データベースや別の UI フローなどの外部ソースからの情報を、自動化するターゲット レガシ ソフトウェアに渡すことができます。

(通常は **store** コマンドを使用して行われる) 初期化の前に使用される (読み取られる) 変数はすべて、入力変数として自動的に処理され、 **[Web の UI フローの実行]** アクション カードに表示されます。

変数は文字列補間を通じて使用できます。たとえば、click コマンドの Target フィールドを "id=\${elementId}" に変更したり、 type コマンドの Value フィールドを "\${inputText}" に変更したりします。

次のスクリーンショットのコマンド **set window size** とコマンド **type** では、初期化されていない変数 \${Width}、\${Height}、\${search} が使用されています。 これらの変数は入力値になります。

![ウィンドウのサイズと種類を設定する](../media/inputs-outputs-web/f05cb445dad212aaf395b66ba969622c.png "ウィンドウのサイズと種類を設定する")

一部のコマンドでは変数を直接使用できます。たとえば、forEach コマンドの Target/Value フィールドは両方とも変数なので、"\${}" で囲む必要はありません。

変数名を直接取得するコマンドについては、[Selenium コマンド](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/) リファレンスを参照してください。

## <a name="define-outputs-for-a-web-ui-flow"></a>Web UI フローの出力を定義する

Selenium スクリプトで定義されている変数はすべて、自動的に出力値になります。 変数を宣言するには、次のコマンドを使用します。

[Store](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/#store)

[Store attribute](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/#store-attribute)

[Store json](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/#store-json)

[Store title](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/#store-title)

[store value](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/#store-value)

[Store window handle](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/#store-window-handle)

[Store xpath count](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/#store-xpath-count)

[Execute script](https://www.seleniumhq.org/selenium-ide/docs/en/api/commands/#execute-script) (スクリプトの最後に 'return' 構文を追加して、格納するオブジェクトを返します)。

## <a name="next-steps"></a>次のステップ

- [Web UI フローの作成](create-web.md)方法について学習します。
- [Web UI フローのトリガー](run-ui-flow.md)方法について学習します。

