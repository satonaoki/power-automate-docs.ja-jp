---
title: 潜在顧客の収集のサンプル | Microsoft Docs
description: 一連の製品に関心のある人物から潜在顧客を収集するためのアダプティブ カードを作成します。
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
ms.openlocfilehash: 6ec875a8a3bf682b7a3d9b44a0cc1d3624bf7a70
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3298200"
---
# <a name="lead-collection-sample"></a>潜在顧客の収集のサンプル

**潜在顧客の収集**のサンプルは、一連の製品に関心のある個人と連絡を取る可能性のある人物から、潜在顧客を収集するために設計されたアダプティブ カードの入力フォームです。 製品の選択肢は自由に変更できます。各選択肢には表示テキストと、誰かがカードを送信した後に出力される内部値を含めることができることを忘れないでください (サンプル コード ブロックに示すのと同じものを使用することもできます)。

![](media/adaptive-cards/lead-notification.png)

"*入力/出力と注:*"

| 動的トークンの名前    | プレースホルダー テキスト       | メモ​​                                                                                       |
|-----------------------|------------------------|--------------------------------------|
| 敬称                 |                        | テキストの表示                                                                                  |
| acInstructions        |                        | テキストの表示                                                                                  |
| acLeadFName           | {firstName}            | 応答の**出力**                                                                           |
| acLeadLName           | {lastName}             | 応答の**出力**                                                                           |
| acLeadEmail           | {emailAddress}         | 応答の**出力**                                                                           |
| acLeadPrimaryPhone    | {primaryPhone10digits} | 応答の**出力**                                                                           |
| acLeadProductInterest | {productInterests}     | 応答の**出力**  <br>複数選択値として (各選択はコンマで区切られます)。                                                                         |

``` json
{
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "type": "AdaptiveCard",
    "version": "1.0",
    "body": [
        {
            "type": "ColumnSet",
            "columns": [
                {
                    "type": "Column",
                    "width": 2,
                    "items": [
                        {
                            "type": "TextBlock",
                            "text": "Lead Notification",
                            "weight": "Bolder",
                            "id": "Title",
                            "size": "ExtraLarge"
                        },
                        {
                            "type": "TextBlock",
                            "text": "Please fill out a single form for each individual expressing interest in our products. ",
                            "isSubtle": true,
                            "wrap": true,
                            "id": "acInstructions",
                            "size": "Large"
                        }
                    ]
                }
            ]
        },
        {
            "type": "Container",
            "items": [
                {
                    "type": "TextBlock",
                    "text": "Potential Customer FIRST NAME",
                    "wrap": true,
                    "size": "Medium"
                }
            ]
        },
        {
            "type": "Input.Text",
            "id": "acLeadFName",
            "placeholder": "{firstName}"
        },
        {
            "type": "TextBlock",
            "text": "Potential Customer LAST NAME",
            "wrap": true
        },
        {
            "type": "Input.Text",
            "id": "acLeadLName",
            "placeholder": "{lastName}"
        },
        {
            "type": "TextBlock",
            "text": "Corporate email",
            "wrap": true
        },
        {
            "type": "Input.Text",
            "id": "acLeadEmail",
            "placeholder": "{emailAddress}",
            "style": "Email"
        },
        {
            "type": "TextBlock",
            "text": "Business Phone Number"
        },
        {
            "type": "Input.Text",
            "id": "acLeadPrimaryPhone",
            "placeholder": "{primaryPhone10digits}",
            "style": "Tel"
        },
        {
            "type": "RichTextBlock",
            "inlines": [
                {
                    "type": "TextRun",
                    "text": "{productInterests}"
                }
            ]
        },
        {
            "type": "Input.ChoiceSet",
            "placeholder": "Placeholder text",
            "choices": [
                {
                    "title": "Office 365",
                    "value": "Office 365"
                },
                {
                    "title": "Dynamics 365",
                    "value": "Dynamics 365"
                },
                {
                    "title": "Azure Services",
                    "value": "Azure Services"
                },
                {
                    "title": "Power Platform",
                    "value": "Power Platform"
                }
            ],
            "style": "expanded",
            "id": "acLeadProductInterest",
            "isMultiSelect": true
        }
    ],
    "actions": [
        {
            "type": "Action.Submit",
            "title": "Submit"
        }
    ]
}
```


