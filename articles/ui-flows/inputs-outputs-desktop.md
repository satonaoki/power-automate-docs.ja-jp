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
ms.date: 03/24/2020
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: fd4200c98df4a60318b5d95ab590d4ec59e6bef3
ms.sourcegitcommit: bba5bd4ae3879b6bf1521d8ed636374fe09709e7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3298794"
---
# <a name="use-inputs-and-outputs-in-desktop-ui-flows"></a>デスクトップ UI フローで入力と出力を使用する

入力を使用すると、データベースやサポートされている任意のコネクタなどの外部ソースからの情報を、UI フローで自動化されるレガシ ソフトウェアに渡すことができます。

たとえば、SharePoint リストの顧客情報を、従来の会計ソフトウェアへの入力のソースとして使用できます。

## <a name="define-inputs-in-the-ui-flows-wizard"></a>UI フロー ウィザードで入力を定義する

1. **[新しい入力]** を選択します。

   ![新規を選択](../media/inputs-outputs-desktop/select-new.png)

1. 入力に名前、サンプル データ、説明を追加します。

    - サンプル データは、記録またはテスト時に使用されます。

    - 説明は、作成した入力を区別するのに役立ちます。

   ![入力フィールド](../media/inputs-outputs-desktop/input-fields.png)

1.  入力を作成したら、[次へ] をクリックすると、それらを記録で使用できるようになります。

>[!TIP]
>**CRTL+ALT+L** キーの組み合わせを使用すると、UI フローで使用されているアプリケーションとの間で渡すことができるテキストを挿入できます。 このキーの組み合わせは、機密性の高いテキスト、静的テキスト、出力テキスト、および入力テキストに対して機能します。 

## <a name="use-inputs-to-pass-information-to-the-application"></a>入力を使用してアプリケーションに情報を渡す

1. 記録中に、**[入力の使用]** を選択すると、アプリで入力を使用できます。

1. 一覧では、次の 3 つのオプションから選択できます。

    - **[入力フィールドの設定]** ステップで定義した入力のいずれかを選択する。

    - 以前に定義した出力を使用する (「出力」セクションを参照)。 これは、同じ UI フロー内の異なるアプリケーション間で情報を渡す場合に便利です。

    - 記録時に新しい入力を作成する。 これは **[入力フィールドの設定]** ステップに戻ると見つかります。

   ![入力の種類の選択](../media/inputs-outputs-desktop/select-input-type.png)

1. 入力を使用する場所を選択します。 定義したサンプル値が自動的に使用されます。 次の例では、"Hello world" は入力名 "My input" のサンプル値で、Microsoft Word 内のページに追加されます。  
    
    ![入力の場所の選択](../media/inputs-outputs-desktop/select-location-for-input.png)

1. Power Automate の **ステップの記録と編集** で、入力を使用するアクションを展開して、選択されているものを表示します。

   ![アクションの展開](../media/inputs-outputs-desktop/expand-actions.png)

1. UI フローをトリガーするときに、入力値を任意に変更できます。

## <a name="use-outputs-to-extract-information-from-the-app"></a>出力を使用してアプリから情報を抽出する

出力を使用すると、UI フローで自動化されるレガシ ソフトウェアからの情報を、データベースや[サポートされている任意のコネクタ](https://flow.microsoft.com/connectors/)などの外部宛先に渡すことができます。

たとえば、従来の会計ソフトウェアの顧客情報を抽出して、SharePoint リストに追加することができます。

出力は、UI フローを記録するときにのみ作成できます。

1. 記録中に、**[出力の取得]** を選択します。

   ![出力の取得](../media/inputs-outputs-desktop/get-output.png)

1. **[テキストの選択]** を選択します。

   ![テキストの選択](../media/inputs-outputs-desktop/select-text.png)

1. ユーザー インターフェイス要素を選択して、出力用のテキストを取得します。 テキスト値は自動的にキャプチャされます。

   <!-- ![Get element output](../media/inputs-outputs-desktop/get-element-output.png) -->

   ![UI 要素の選択](../media/inputs-outputs-desktop/select-ui-element.png)

1. 出力の名前と説明を指定します。

   ![名前と説明の指定](../media/inputs-outputs-desktop/name-description.png)

1. **保存**を選択します。 

これで、出力がウィザードの専用領域で使用できるようになりました。

   ![出力を利用可能](../media/inputs-outputs-desktop/output-available.png)

各出力には次のものがあります。

-  記録中に定義された出力名。
-  説明: このフィールドは、記録中に多くの出力を定義し、それらを後続の処理で簡単に識別できるようにする場合に非常に便利です。
-  アクション名: UI フローで出力が定義されているアクション。

## <a name="delete-an-output-from-a-ui-flow"></a>UI フローから出力を削除する

出力が不要になった場合は、関連付けられているアクションに移動し、動的な値で出力名を削除することで、出力を削除します。

## <a name="test-your-ui-flow"></a>UI フローをテストする

UI フローをテストすることで、変更と適切な再生動作を検証できます。

1. (省略可能) 入力フィールドに新しい値を入力します。 
    
    ![新しいテスト値](../media/inputs-outputs-desktop/new-test-value.png)

1. **[今すぐテスト]** をクリックして、自動化されているレガシ ソフトウェアを確認します。 記録したステップが UI フロー オートメーションによって再生されます。 **再生中は、デバイスを操作しないでください。**

1. 再生が完了すると、UI フローの実行状態が表示されます。

    - アクションごとに、関連付けられている入力と共に、テストが正常に機能したことを示す状態インジケーター。

    - このテスト用に取得した出力の値。

    - エラーが発生した場合は、エラーが発生したときのスクリーンショットに、問題の原因となったステップが表示されます。

   ![正常な実行](../media/inputs-outputs-desktop/successful-run.png)

## <a name="learn-more"></a>詳細はこちら

- [Web UI フローのトリガー](run-ui-flow.md)方法について学習します。



