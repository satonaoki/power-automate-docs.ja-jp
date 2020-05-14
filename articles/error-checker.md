---
title: Power Automate でフロー チェッカーを使用してエラーの特定と修正をする | Microsoftドキュメント
description: Power Automate でフロー チェッカーを使用して簡単にエラーの特定と修正をする。
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
ms.date: 10/05/2019
ms.author: deonhe
search.app:
- Flow
- Powerplatform
search.audienceType:
- flowmaker
ms.openlocfilehash: 2f1dd4beffdcf31a1070928195dbd3895e479e3d
ms.sourcegitcommit: 9cca2a2fca8371ab883b12011c1c4485ceb9c761
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2020
ms.locfileid: "3299454"
---
# <a name="find-and-fix-errors-with-flow-checker"></a>フロー チェッカーを使用してエラーの特定と修正をする


Power Automate のフロー チェッカーを使用すると、フローを設計する際にベスト プラクティスに確実に従うことができるので、フローの品質のレベルが上がります。 このチェッカーを実行すると、"使用するフローの実装のどの領域でパフォーマンスまたは信頼性のリスクが生じるか" といった質問に対する分析情報を得ることができます。

チェッカーでは、識別した各問題について、フロー内の特定の出現箇所が示され、お客様はその箇所について改善を検討する必要があります。 さらに、それらの改善を実装する方法については、以下の詳細なガイダンスに従ってください。

このチェッカーは常にアクティブであり、デザイナーのコマンド バーに表示されます。 ご利用のフロー内で 1 つまたは複数のエラー、潜在的なエラー、または警告を検出すると、このチェッカーでは赤色のドットが表示されます。

![フロー チェッカー](media/checker/checker-in-designer.png "フロー チェッカー")


## <a name="view-errors-or-warnings-in-the-checker"></a>チェッカーでエラーまたは警告を表示する

フローのデザイン中に、**フロー チェッカー** ボタンを選択すると、チェッカーが起動して、エラーと警告が表示されます。 

エラーまたは警告がある場合は、フローを保存するときにもチェッカーが自動的に開かれます。  チェッカーが開かれると、ご利用のフロー内のすべてのエラーと警告が表示されます。 各セクションでは、エラーまたは警告が発生するアクションがチェッカーによって呼び出されます。 

## <a name="learn-to-fix-errors-and-warnings"></a>エラーと警告の修正について

各セクションを展開すると、エラーまたは警告を修正する方法の詳細が表示されます。

![チェッカーの詳細](media/checker/checker-detail.png "チェッカーの詳細")

## <a name="learn-more"></a>詳細はこちら

[Power Automate の概要](getting-started.md)



