---
title: デスクトップ UI フローで入力と出力を使用する | Microsoft Docs
description: デスクトップ UI フローで入力と出力を使用する。
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
ms.openlocfilehash: 391e977343617497328ff231d4808a0c78ceb154
ms.sourcegitcommit: 835b005284b9ae21ae1742a7d36b574ba3884bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2020
ms.locfileid: "74371643"
---
# <a name="use-inputs-and-outputs-in-desktop-ui-flows"></a>デスクトップ UI フローで入力と出力を使用する

[このトピックはプレリリース版のドキュメントであり、変更される可能性があります。]

[!INCLUDE [view-pending-approvals](../includes/cc-rebrand.md)]

## <a name="define-inputs"></a>入力を定義する

入力を使用すると、データベースやサポートされている任意のコネクタなどの外部ソースからの情報を、UI フローで自動化されるレガシ ソフトウェアに渡すことができます。

たとえば、SharePoint リストの顧客情報を、レガシ会計ソフトウェアへの入力のソースとして使用できます。

### <a name="define-inputs-in-the-ui-flows-wizard"></a>UI フロー ウィザードで入力を定義する

1. [新しい入力] を選択します。

   ![](../media/inputs-outputs-desktop/2eb6313a0e966f1fbfc352445b89ee39.png)

1. 入力に名前、サンプル データ、説明を追加します。

    - サンプル データは、記録またはテスト時に使用されます。

    - 説明は、作成した入力を区別するのに役立ちます。

   ![](../media/inputs-outputs-desktop/e33d206bf2158228277a276261c49785.png)

1.  入力を作成したら、[次へ] をクリックすると、それらを記録で使用できるようになります。

### <a name="use-inputs-to-pass-information-to-the-application"></a>入力を使用してアプリケーションに情報を渡す

1. 記録中に、 **[入力の使用]** を選択すると、アプリで入力を使用できます。

1. 一覧では、次の 3 つのオプションから選択できます。

    - UI フローの **[入力フィールドの設定]** ステップで定義した入力のいずれかを選択する。

    - 以前に定義した出力を使用する (「出力」セクションを参照)。 これは、同じ UI フロー内の異なるアプリケーション間で情報を渡す場合に便利です。

    - 記録時に新しい入力を作成する。 これは UI フローの **[入力フィールドの設定]** ステップに戻ると見つかります。

   ![](../media/inputs-outputs-desktop/de36baa0f85d5a19304e1606de25aa3e.png)

1. 入力を使用する場所を選択します。 定義したサンプル値が自動的に使用されます。 次の例では、"Hello world" は入力名 "My input" のサンプル値で、Microsoft Word 内のページに追加されます。  
    
    ![](../media/inputs-outputs-desktop/d6b74dc86f38c51cf1daa0582ff0cc33.png)

1. Power Automate の**ステップの記録と編集**で、入力を使用するアクションを展開して、選択されているものを表示します。

   ![](../media/inputs-outputs-desktop/340aa71942b618431b0455b632f76f52.png)

1. UI フローをトリガーするときに、入力値を任意に変更できます。 詳細については、入力と出力の使用に関するページを参照してください。

## <a name="use-outputs-to-extract-information-from-the-app"></a>出力を使用してアプリから情報を抽出する

出力を使用すると、UI フローで自動化されるレガシ ソフトウェアからの情報を、データベースや[サポートされている任意のコネクタ](https://flow.microsoft.com/connectors/)などの外部宛先に渡すことができます。

たとえば、レガシ会計ソフトウェアの顧客情報を抽出して、SharePoint リストに追加することができます。

出力は、UI フローを記録するときにのみ作成できます。

1. 記録中に、レコーダーの [出力の取得] ボタンを選択します。

   ![](../media/inputs-outputs-desktop/13f8dfca19c0ed04ca2a0f87bf7055ea.png)

1. [テキストの選択] ボタンを選択します (これは現時点で使用可能な唯一の出力の種類です)。

   ![](../media/inputs-outputs-desktop/2845b73ee807a5be747c1dc494570ab7.png)

1. ユーザー インターフェイス要素をクリックして、出力用のテキストを選択します。 値は自動的にキャプチャされます。

   ![](../media/inputs-outputs-desktop/7df19b56aadcd0aef207c7372a04b3c6.png)

   ![](../media/inputs-outputs-desktop/af55a0bf39d805b154a783eff3de131b.png)

1. 出力の名前と説明を定義します。

   ![](../media/inputs-outputs-desktop/a083579ee011dfb76aa21fac116796a3.png)

1. **[保存]** を選択します。 

これで、ウィザードの専用領域で出力が使用できるようになりました。

   ![](../media/inputs-outputs-desktop/b9f396de0b5893c5a3152b592911f67a.png)

各出力には次のものがあります。

-  記録中に定義された出力名
-  説明:このフィールドは、記録中に多くの出力を定義し、それらを簡単に識別できるようにする場合に非常に便利です。
-  アクション名: UI フローで出力が定義されているアクション

## <a name="delete-an-output-from-a-ui-flow"></a>UI フローから出力を削除する

出力が不要になった場合は、関連付けられているアクションに戻り、動的な値で出力名を削除することで、出力を削除できます。

## <a name="test-your-ui-flow"></a>UI フローをテストする

UI フローをテストすることで、変更と適切な再生動作を検証できます。

1. (省略可能) 入力フィールドに新しい値を入力します。 
    
    ![](../media/inputs-outputs-desktop/0b4aef639c4ab30b93413e1e7a5e662d.png)

1. **[今すぐテスト]** をクリックして、自動化されているレガシ ソフトウェアを確認します。 記録したステップが UI フロー オートメーションによって再生されます。 **再生中は、デバイスを操作しないでください。**

1. 再生が完了すると、UI フローの実行状態が表示されます。

    - アクションごとに、テストが正常に実行されたことを示す状態と関連する入力。

    - このテスト用に取得した出力の値。

    - エラーが発生した場合は、エラーが発生したときのスクリーンショットで問題となったステップを確認できます。

   ![](../media/inputs-outputs-desktop/85056d7942d12a5408005f5b683d432b.png)

## <a name="learn-more"></a>詳細情報

- 作成した [UI フローをトリガーする](run-ui-flow.md)方法について学習します。

- UI フローでさらに多くの操作を行う場合は、[入力と出力](inputs-outputs-web.md)パラメーターを使用して UI フローを試すこともできます。


