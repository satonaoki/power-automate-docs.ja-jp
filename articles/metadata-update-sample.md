---
title: アダプティブ カード メタデータ更新カードのサンプル | Microsoft Docs
description: レコード、ファイル、またはトピックに関連するメタデータを使用して、Teams メンバーまたはチャネルに通知または更新します。
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
ms.date: 01/04/2020
ms.author: deonhe
ms.openlocfilehash: 902510ac5c2dd61fbcaae7c1dad771588e431873
ms.sourcegitcommit: e3543e32e4e8e8163bef0565e27b657eabbdc741
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/10/2020
ms.locfileid: "75868206"
---
# <a name="metadata-update-card-sample"></a>メタデータ更新カードのサンプル

**メタデータ更新**サンプルは、フローの作成者が、レコード、ファイル、またはトピックに関連するメタデータを使用して、Teams メンバーまたはチャネルに通知または更新できるように設計されたアダプティブ カードです。 このカードは、表示用のみのアダプティブ カードです。 ただし、"*応答を待機*" アクションのいずれかを使用して作成した場合、入力フィールドが追加されることがあります。

このカードは、次の 3 つのセクションで構成されます。

1. ヘッダー、サブヘッダー、および説明を含むトピック ヘッダー領域
1. 関連するレコード メタデータのファクト リスト領域
1.  データのテーブル配列をサポートする列セット

![メタデータのサンプル](media/adaptive-cards/metadata-sample.png) 


*入力/出力とノート*

| 動的トークンの名前 (入力) | プレースホルダー テキスト    | ノート                                     |
|-----------------------------|---------------------|--------------------------------------------|
| acHeader                    | {Header}            | 表示テキスト                               |
| acSubHeader                 | {SubHeader}         | 表示テキスト                               |
| acDescription               | ラテン語テキスト          | 表示テキスト                               |
| acFact1                     | {acFact1}           | 表示テキスト                               |
| acFact2                     | {acFact2}           | 表示テキスト                               |
| acFact3                     | {acFact3}           | 表示テキスト                               |
| acColumnSetHeader           | ヘッダー 1 から 3 | 表示テキスト <br>  列セット ヘッダーの表示テキスト                               |
| acColumnSet                 | 列 1 から 3 | 配列または列の値に置き換えます。       |


``` json
{
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "type": "AdaptiveCard",
    "version": "1.0",
    "body": [
        {
            "type": "TextBlock",
            "text": "Metadata Update Card",
            "weight": "bolder",
            "size": "large",
            "id": "acTitle"
        },
        {
            "type": "ColumnSet",
            "columns": [
                {
                    "type": "Column",
                    "width": "auto",
                    "items": [
                        {
                            "type": "TextBlock",
                            "text": "Sub Header Tag Line",
                            "weight": "Bolder",
                            "wrap": true,
                            "id": "acSubHeader"
                        }
                    ]
                }
            ]
        },
        {
            "type": "TextBlock",
            "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. In condimentum leo lorem, at facilisis augue hendrerit eget. Praesent ut malesuada ipsum. Vivamus semper faucibus felis quis sagittis. Nunc pellentesque metus at nunc gravida, vitae volutpat sapien vehicula. Nulla lorem nibh, porttitor vel semper ut, ornare nec erat.",
            "wrap": true,
            "id": "acDescriptionArea"
        },
        {
            "type": "FactSet",
            "facts": [
                {
                    "title": "Fact 1:",
                    "value": "{acFact1}"
                },
                {
                    "title": "Fact 2:",
                    "value": "{acFact2}"
                },
                {
                    "title": "Fact 3:",
                    "value": "{acFact3}"
                }
            ],
            "id": "acFactSet"
        },
        {
            "type": "Container",
            "spacing": "Large",
            "items": [
                {
                    "type": "ColumnSet",
                    "columns": [
                        {
                            "type": "Column",
                            "items": [
                                {
                                    "type": "TextBlock",
                                    "weight": "Bolder",
                                    "text": "HEADER 1"
                                }
                            ],
                            "width": "stretch"
                        },
                        {
                            "type": "Column",
                            "items": [
                                {
                                    "type": "TextBlock",
                                    "weight": "Bolder",
                                    "text": "HEADER 2"
                                }
                            ],
                            "width": "stretch"
                        },
                        {
                            "type": "Column",
                            "items": [
                                {
                                    "type": "TextBlock",
                                    "weight": "Bolder",
                                    "text": "HEADER 3"
                                }
                            ],
                            "width": "stretch"
                        }
                    ]
                }
            ],
            "bleed": true
        },
        {
            "type": "ColumnSet",
            "columns": [
                {
                    "type": "Column",
                    "items": [
                        {
                            "type": "TextBlock",
                            "text": "Column 1",
                            "wrap": true,
                            "id": "acCol1"
                        }
                    ],
                    "width": "stretch"
                },
                {
                    "type": "Column",
                    "items": [
                        {
                            "type": "TextBlock",
                            "text": "Column 2",
                            "wrap": true,
                            "id": "acCol2"
                        }
                    ],
                    "width": "stretch"
                },
                {
                    "type": "Column",
                    "items": [
                        {
                            "type": "TextBlock",
                            "text": "Column 3",
                            "wrap": true,
                            "id": "acCol4"
                        }
                    ],
                    "width": "stretch"
                }
            ],
            "$data": "acDataContext"
        }
    ],
    "bleed": true

}
```
