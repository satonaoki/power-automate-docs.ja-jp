---
title: アダプティブ カードの日単位の天気予報サンプル | Microsoft Docs
description: Teams チャネルに毎日の天気の更新情報を投稿するためのアダプティブ カード作成用サンプル
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
ms.openlocfilehash: 8f7128104d3cb8aae361b6dd574822f503893e35
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3297078"
---
# <a name="daily-weather-report-sample"></a>日単位の天気予報のサンプル

**日単位の天気予報**サンプルは、Teams チャネルに日単位の天気の更新情報を投稿するための、MSN 天気予報で使用するために設計されたアダプティブ カードです。

![](media/adaptive-cards/weather.png)

*入力/出力とノート*

| 動的トークンの名前     | プレースホルダー テキスト | メモ​​                                                                         |
|------------------------|------------------|--------------------------------------------------------------------------------|
| {acCityState}          | テンプレートを参照     | テキストの表示 <br>  変数は、市区町村、都道府県、または郵便番号の値を保持するために使用できます。                                                                   |
| {acDailySummary}       | テンプレートを参照     | テキストの表示                                                                   |
| {acCurrentDateTime}    | テンプレートを参照     | テキストの表示                                                                   |
| {acUrlConditionsImage} | テンプレートを参照     | テキストの表示  <br> テンプレートのコメントを参照。有効な URL に置き換える必要があります。                                                                 |
| {acCurrentTemperature} | テンプレートを参照     | テキストの表示                                                                   |
| {actempHi}             | テンプレートを参照     | テキストの表示                                                                   |
| {actempLow}            | テンプレートを参照     | テキストの表示                                                                   |


``` json
{
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "type": "AdaptiveCard",
    "version": "1.0",
    "body": [
        {
            "type": "TextBlock",
            "text": "{acCity}, {acState}",
            "size": "Large",
            "isSubtle": true
        },
        {
            "type": "TextBlock",
            "text": "{acCurrentDateTime}",
            "spacing": "None"
        },
        {
            "type": "TextBlock",
            "text": "{acDailySummary}",
            "spacing": "None"
        },
        {
            "type": "ColumnSet",
            "columns": [
                {
                    "type": "Column",
                    "width": "auto",
                    "items": [
                        {
                            "type": "Image",
                            "url": "{acUrlConditionsImage}",
                            "size": "Large"
                        }
                    ]
                },
                {
                    "type": "Column",
                    "width": "auto",
                    "items": [
                        {
                            "type": "TextBlock",
                            "text": "{acCurrentTemperature}",
                            "size": "ExtraLarge",
                            "spacing": "None"
                        }
                    ]
                },
                {
                    "type": "Column",
                    "width": "stretch",
                    "items": [
                        {
                            "type": "TextBlock",
                            "text": "°F",
                            "weight": "Bolder",
                            "spacing": "Small"
                        }
                    ]
                },
                {
                    "type": "Column",
                    "width": "stretch",
                    "items": [
                        {
                            "type": "TextBlock",
                            "text": "Hi {actempHi}",
                            "horizontalAlignment": "Left"
                        },
                        {
                            "type": "TextBlock",
                            "text": "Lo {actempLow}",
                            "horizontalAlignment": "Left",
                            "spacing": "None"
                        }
                    ]
                }
            ]
        }
    ]
}
```
