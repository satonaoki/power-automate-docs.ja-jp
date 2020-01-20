---
title: アンケート ジェネレーターのサンプル | Microsoft Docs
description: Microsoft Teams に投票を送信するように設計されたアダプティブ カード入力フォーム。
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
ms.date: 01/01/2020
ms.author: deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: b19a5b58db4680786ade089731846f0f8000d164
ms.sourcegitcommit: e3543e32e4e8e8163bef0565e27b657eabbdc741
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/10/2020
ms.locfileid: "75868229"
---
# <a name="create-a-poll-sample"></a>アンケート作成サンプル

**アンケート作成**サンプルは、Microsoft Teams に投票を送信するように設計されたアダプティブ カード入力フォームです。 このカードの表示テキストを置き換えて、投票用にカスタマイズします。 このアダプティブ カードを使うと、カード コンシューマーの投票の値で提供された回答または投票数に応じて、さまざまなデシジョン パスを使用できます。

![投票サンプル](media/adaptive-cards/poll.png)

*入力/出力とノート*

| 動的トークンの名前 | プレースホルダー テキスト | 注:                                            |
|--------------------|------------------|---------------------------------------------------|
| タイトル              |                  | 表示テキスト                                      |
| acHeaderTagLine    |                  | 表示テキスト                                      |
| acHeader           |                  | 表示テキスト                                      |
| acPollQuestion     |                  | 表示テキスト                                      |
| acPollChoices      |                  | 応答の**出力**  <br> 単一選択 (ラジオ ボタン)|

``` json
{
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "type": "AdaptiveCard",
    "version": "1.0",
    "body": [
        {
            "type": "TextBlock",
            "text": "Poll Request",
            "id": "Title",
            "spacing": "Medium",
            "horizontalAlignment": "Center",
            "size": "ExtraLarge",
            "weight": "Bolder",
            "color": "Accent"
        },
        {
            "type": "TextBlock",
            "text": "Header Tagline Text",
            "id": "acHeaderTagLine",
            "separator": true
        },
        {
            "type": "TextBlock",
            "text": "Poll Header",
            "weight": "Bolder",
            "size": "ExtraLarge",
            "spacing": "None",
            "id": "acHeader"
        },
        {
            "type": "TextBlock",
            "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer vestibulum lorem eget neque sollicitudin, quis malesuada felis ultrices. ",
            "id": "acInstructions",
            "wrap": true
        },
        {
            "type": "TextBlock",
            "text": "Poll Question",
            "id": "acPollQuestion"
        },
        {
            "type": "Input.ChoiceSet",
            "placeholder": "Select from these choices",
            "choices": [
                {
                    "title": "Choice 1",
                    "value": "Choice 1"
                },
                {
                    "title": "Choice 2",
                    "value": "Choice 2"
                },
                {
                    "title": "Choice 3",
                    "value": "Choice 3"
                }
            ],
            "id": "acPollChoices",
            "style": "expanded"
        }
    ],
    "actions": [
        {
            "type": "Action.Submit",
            "title": "Submit",
            "id": "btnSubmit"
        }
    ]
}
```


