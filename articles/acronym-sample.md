---
title: アダプティブ カードの頭字語フォーム サンプル | Microsoft Docs
description: 頭字語を収集して Common Data Service に格納するアダプティブ カードを作成します。
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
ms.openlocfilehash: b1ecc0240dba1866ea3468647d06637397d73170
ms.sourcegitcommit: e3543e32e4e8e8163bef0565e27b657eabbdc741
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/10/2020
ms.locfileid: "75868298"
---
# <a name="acronyms-form-sample"></a>頭字語フォームのサンプル

**頭字語フォーム**サンプルは、頭字語を収集して、Common Data Service に格納するよう設計されたアダプティブ カード入力フォームです。 これらの頭字語は、この継続的なデータ収集によってどこからでも照会することができます。

![頭字語ロガー](media/adaptive-cards/acronym-logger.png)

*入力/出力とノート*

| 動的トークンの名前 | プレースホルダー テキスト                        | 注:              |
|--------------------|-----------------------------------------|---------------------|
| {acAcronym}        | 頭字語の省略形を入力します  | 応答の**出力** |
| {acDefinition}     | 上記の頭字語の定義を入力します | 応答の**出力** |

``` json
{
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "type": "AdaptiveCard",
    "version": "1.0",
    "body": [
        {
            "type": "TextBlock",
            "text": "Acronym Logger",
            "id": "Title",
            "spacing": "Medium",
            "horizontalAlignment": "Center",
            "size": "ExtraLarge",
            "weight": "Bolder",
            "color": "Accent"
        },
        {
            "type": "Container",
            "items": [
                {
                    "type": "TextBlock",
                    "text": "Acronym",
                    "wrap": true,
                    "spacing": "Medium"
                },
                {
                    "type": "Input.Text",
                    "id": "acAcronym",
                    "placeholder": "Enter the abbreviation for the acronym"
                },
                {
                    "type": "TextBlock",
                    "text": "Definition",
                    "wrap": true
                },
                {
                    "type": "Input.Text",
                    "placeholder": "Enter a definition of the acronym above",
                    "id": "acDefinition",
                    "isMultiline": true
                }
            ]
        }
    ],
    "actions": [
        {
            "type": "Action.Submit",
            "title": "Submit",            "id": "btnSubmit"
        }
    ]
}

```