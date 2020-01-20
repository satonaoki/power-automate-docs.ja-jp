---
title: 応募者のフィードバックのサンプル | Microsoft Docs
description: このサンプルを使用して、仕事の応募者のフィードバックを収集するアダプティブ カードを作成します。
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
ms.openlocfilehash: 0d0157c4e0d392dd8493e5aeca4e97531c95213d
ms.sourcegitcommit: e3543e32e4e8e8163bef0565e27b657eabbdc741
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/10/2020
ms.locfileid: "75868160"
---
# <a name="candidate-feedback-sample"></a>応募者のフィードバックのサンプル

**応募者のフィードバック フォーム**のサンプルは、面接ループ中のフィードバックを収集するために設計されたアダプティブ カードの入力フォームです。 共有インスタント フロー ボタンと共にこれを使用して、面接ループ中に、チームの全員が応募者に対するフィードバックを提供できるようにすることをお勧めします。 データベースやその他の望ましいデータ ソースに応答を記録することで、これを拡張し、次のさらなる機会をサポートします。

-   その応募者との次のセッションの前にフォローアップ提案を確認することを容易にします。
-   すべての応答が記録された後の集計データの確認を容易にします。
-   プロセスの終了時に、採用/不採用の投票数を人事担当者に通知します

     ![応募者のフィードバック フォーム](media/adaptive-cards/candidate-form.png)

"*入力/出力と注*"

| 動的トークンの名前 | プレースホルダー テキスト | 注:              |
|--------------------|------------------|---------------------|
| {acFullName}       | {acFullName}     | 表示テキスト        |
| {acComments}       | {acComments}     | 表示テキスト        |
| {acDecision}       |                  | 応答の**出力** |
| {acFollowUp}       |                  | 応答の**出力** |

``` json
{
  "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
  "type": "AdaptiveCard",
  "version": "1.0",
  "body": [
    {
      "type": "TextBlock",
      "size": "Medium",
      "weight": "Bolder",      "id": "Title",
      "text": "CANDIDATE FEEDBACK FORM",
      "horizontalAlignment": "Left"
    },
    {
      "type": "Input.Text",
      "placeholder": "{acFullName}",
      "style": "text",
      "isMultiline": false,
      "maxLength": 75,
      "id": "acFullName"
    },
    {
      "type": "Input.Text",
      "placeholder": "{acComments}",
      "style": "text",
      "isMultiline": true,
      "maxLength": 200,
      "id": "acComments"
    },
    {
      "type": "TextBlock",
      "size": "Medium",
      "weight": "Bolder",
      "text": "Decision",
      "horizontalAlignment": "Left",
      "separator": true
    },
    {
      "type": "Input.ChoiceSet",
      "id": "acDecision",
      "value": "1",
      "choices": [
        {
          "title": "Hire",
          "value": "Hire"
        },
        {
          "title": "No Hire",
          "value": "No Hire"
        }
      ],
      "style": "expanded"
    },
    {
      "type": "TextBlock",
      "text": "Suggest follow-up discussion regarding:",
      "weight": "Bolder"
    },
    {
      "type": "Input.ChoiceSet",
      "id": "acFollowUp",
      "isMultiSelect": true,
      "value": "",
      "choices": [
        {
          "title": "Past experience in the topic area",
          "value": "Experience"
        },
        {
          "title": "Inclusive behaviors and work ethics",
          "value": "Inclusivity"
        },
        {
          "title": "Ability to work without supervision",
          "value": "Independent"
        }
      ]
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


