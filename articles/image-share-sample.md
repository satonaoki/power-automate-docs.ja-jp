---
title: 写真共有のための画像共有サンプル | Microsoft Docs
description: アダプティブ カードを共有して写真を作成する方法を説明します。
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
ms.openlocfilehash: 0d310eb96a69f66b8f45718554f36ba8b2a51989
ms.sourcegitcommit: e3543e32e4e8e8163bef0565e27b657eabbdc741
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/10/2020
ms.locfileid: "75868735"
---
# <a name="image-share-sample"></a>画像共有のサンプル 

**画像共有フォーム** サンプルは、SharePoint に投稿された写真を共有するために設計されたアダプティブ カードであり、プロセスを完了するための依存関係になる場合もあります (検査、コンプライアンス、監査に関連するプロセスなど)。 これは、表示専用のアダプティブ カードです。

![表示専用のアダプティブ カード](media/adaptive-cards/image-share.png)

*入力/出力とノート*

| 動的トークンの名前 (入力) | プレースホルダー テキスト   | ノート                                              |
|-----------------------------|--------------------|-----------------------------------------------------|
| acphotoTitle                | {acphotoTitle}     | 表示テキスト                                        |
| acTimestamp                 | {acTimestamp]      | 表示日/時刻                                   |
| acImageThumbnail            | {acImageThumbnail} | 表示する画像 <br>有効な URL に置き換える必要があります|
| acAltText                   | {acAltText}        | アクセシビリティの代替テキスト                      |

``` json
{
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "type": "AdaptiveCard",
    "version": "1.0",
    "body": [
        {
            "type": "TextBlock",
            "text": "{acphotoTitle}",
            "id": "Title",
            "size": "Large"
        },
        {
            "type": "TextBlock",
            "text": "{acTimestamp}",
            "size": "Medium",
            "weight": "Lighter"
        },
        {
            "type": "Image",
            "altText": "{acAltText}",
            "url": "{acImageThumbnail}"
        }
    ],
    "spacing": "None"
}
```


