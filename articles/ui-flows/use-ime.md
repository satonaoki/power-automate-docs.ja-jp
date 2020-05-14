---
title: UI flows での IME (入力方式エディター) の使用 | Microsoft Docs
description: UI flows での IME (入力方式エディター) の使用について学習します。
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
ms.date: 02/25/2020
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 167f9321dba853e801102bed2ebe7e8902437d71
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3298486"
---
# <a name="use-input-method-editors-imes-in-ui-flows"></a>UI フローでの入力方式エディター (IME) の使用

**[静的テキストの追加]** 機能を使用すると、IME または通常のキーボードを使用して、任意の言語でご自分の UI flows のテキスト入力を記録できます。 **[静的テキストの追加]** は、ご自分の UI flow が実行されるたびにオートメーションで同じテキストを挿入する場合に使用します。 

>[!TIP]
>**[Text input]** \(テキスト入力\) は、ご自分の UI flows が実行されるたびに変わる動的なテキストを使用する場合に使用します。

## <a name="invoke-ime"></a>IME の起動

記録を開始し、静的テキスト入力を挿入する準備ができたら、次の手順を実行します。

1. 静的テキストを入力するコントロールを選択します。

   ![コントロールの選択](../media/use-ime/select-control.png)

1. レコーダーで **[入力の使用]** を選択し、**[静的テキストの追加]** を選択します。

   ![[静的テキストの追加] の選択](../media/use-ime/add-static-text.png)

   静的テキストを入力する入力ボックスが表示されます。 IME、英語、または任意のインターナショナル キーボードを使用できます。

   ![静的テキストの入力](../media/use-ime/enter-static-text.png)

1. テキストを入力します。

1. **[アプリに追加する]** を選択し、テキストを挿入するコントロールを選択します。 テキストがコントロールに挿入されて表示されます。 

   このテキストは、再生するコンピューターのキーボード レイアウトまたは IME が記録時に使用されたものとは異なる場合でも再生時に自動入力されます。

   ![再生テキスト](../media/use-ime/playback-text.png)

   >[!TIP]
   >Web デザイナーで、**[Insert text input]** \(テキスト入力の挿入\) アクションを展開して、テキストを確認または編集します。

   ![テキスト入力の挿入](../media/use-ime/insert-text-input.png)


## <a name="use-the-replay-keystroke-action"></a>キーボード操作の再生アクションの使用

**[静的テキストの追加]** オプションを使用せずにテキスト入力を記録した場合、各キーボード操作が記録され、時系列で再生されます。 これには、すべての英語またはインターナショナル キーボード レイアウトの CTRL、ALT、Windows などの特殊キーがすべて含まれます。

デザイナーでは、**[Replay keystroke]** \(キーボード操作の再生\) アクションの下の[仮想キー](https://docs.microsoft.com/windows/win32/inputdev/virtual-key-codes)形式で記録情報を確認および編集できます。 

![仮想キー](../media/use-ime/virtual-key.png)


> [!NOTE]
> 以前のバージョンの UI flows レコーダーでは、**SendKeys** と **PostElement** 操作が使用されていました。 これらの操作は非推奨になります。 新機能を利用できるようにするには、UI flows レコーダーを最新バージョンにアップグレードして、スクリプトを再記録することをお勧めします。

## <a name="troubleshooting-tips"></a>トラブルシューティングのヒント

1. **[Replay keystroke]** \(キーボード操作の再生\) モードでキーボード操作を記録するには、記録時のコンピューターと同じキーボードが再生するコンピューターでも使用されている必要があります。これは、キーボードが異なる場合、同じキーボード操作の再生順で異なる値が入力される場合があるためです。

1. **[入力の使用]** は、テキスト型のコントロールに対してのみ使用できます。 現在 **[入力の使用]** では、コンボ ボックス、ドロップダウン、リスト ビューなど、他の種類のコントロールにはテキストを入力できません。

## <a name="next-steps"></a>次のステップ

- [UI フローの設定](setup.md)方法について学習します。 
- ワークフローを自動化するために使用できる[さまざまな種類のフロー](..\getting-started.md#types-of-flows)の詳細について学習する。


