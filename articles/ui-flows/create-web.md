---
title: Web サイトの UI フローを作成する方法 | Microsoft Docs
description: UI フローを使用して Web アプリを自動化する方法について説明します。
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
ms.date: 02/28/2020
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 90951e4244ef7caa75bedc522d1bb032e070dbef
ms.sourcegitcommit: 26cda5060446812f3725ccd4fe435839088f50fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "78244262"
---
# <a name="create-and-test-your-web-ui-flows"></a>Web UI フローの作成とテスト

[このトピックはプレリリース版のドキュメントであり、変更される可能性があります。]

[!INCLUDE [view-pending-approvals](../includes/cc-rebrand.md)]

シンプルな Web UI フローを作成するには、次の手順に従います。

## <a name="create-a-web-ui-flow"></a>Web UI フローの作成

1. [次期バージョンの Microsoft Edge](https://www.microsoftedgeinsider.com/) または Google Chrome を開き、[Power Automate](https://flow.microsoft.com/) に移動します。

1. 必要に応じて職場または学校アカウントでサインインします。

1. **[マイ フロー]**  >  **[UI フロー (プレビュー)]**  >  **[新規]** を選択します。

   ![新しい UI フローの作成](../media/create-windows-ui-flow/create-new.png "新しい UI フローの作成")

1. **[Web アプリ]**  >  **[次へ]** を選択します。
    
   ![Web アプリの選択](../media/create-web-ui-flow/select-web-app.png "Web アプリの選択")

1. **[フロー名]** フィールドに UI フローの名前を入力します。

1. 自動化する Web サイトの URL を **[ベース URL]** フィールドに入力し、 **[レコーダーの起動]** を選択します。

   ![名前と URL の指定](../media/create-web-ui-flow/give-a-name.png "名前と URL の指定") 

   Selenium IDE が起動します。

   >[!TIP] 
   >ヒント:同じタブ内で、複数の HTTP または HTTPS Web サイト間でアクションを記録できます。  

1. Selenium IDE で、画面の右上にある赤色の **[REC]** ボタンを選択してレコーダーを起動します。

   前の手順で選択した URL が開きます。

   ![[Rec] の選択](../media/create-web-ui-flow/select-rec.png "[Rec] の選択")

1.  Web サイト上で記録する操作を実行します。 
    
    >[!TIP]
    >右下に記録の状態が表示されます。

    ![記録の状態](../media/create-web-ui-flow/recording-status.png "記録の状態")

1.  記録が終了したら、Selenium IDE の右上隅にある赤い **[停止]** ボタンを選択します。

    ![[停止] ボタン](../media/create-web-ui-flow/stop-button.png "[停止] ボタン" )

1. 画面の左上にある **[Run current test]\(現在のテストを実行\)** ボタンを選択して、先ほど作成した UI フローを表示します。

    ![現在のテストを実行](../media/create-web-ui-flow/run-test.png "現在のテストを実行")

   >[!TIP]
   >ステップ間の待機時間を設定して、テストのローカル再生速度を遅くすることができます。 この設定はテストのみを目的としており、UI フローが展開されても影響はありません。  
  
1. Selenium IDE の右上にある **[プロジェクトの保存]** ボタンを選択します。 これにより、プロジェクトが閉じ、アップロードされます。

Web UI フローを作成したので、それを他のフローで使用できます。

## <a name="limitations-and-known-issues-for-web-ui-flows"></a>Web UI フローの制限事項と既知の問題

>[!WARNING]
>**Selenium IDE のパスワードはプレーンテキストで格納されます。**  


**新しいバージョンをインストールした後、UI flows で Windows アプリケーションは記録または再生されなくなります。**

[最新バージョン](https://go.microsoft.com/fwlink/?linkid=2102613&clcid=0x409)を使用していることを確認します。

**再生用の一時ユーザー プロファイル**

Selenium IDE の記録は現在のユーザーのプロファイルで実行されますが、再生は一時ユーザー プロファイルを使用して行われます。 つまり、認証を必要とする Web サイトで、記録セッション中は資格情報を要求されない可能性がありますが、再生時に認証手順が必要になります。 

これに対処するには、ユーザーはスクリプトを手動で編集して、ログイン プロセスに必要なコマンドを挿入する必要があります。

**その他の制限事項**

-   Web 記録セッション中のデスクトップ アプリケーションの記録。 Web アプリケーションとデスクトップ アプリケーションの両方を自動化する必要がある場合は、種類ごとに個別の UI フローを作成し、それらを 1 つのフロー内で組み合わせることができます。

-   多要素認証 (MFA) はサポートされていません。MFA を必要としないテナントを使用してください。

-   次の Selenium IDE コマンドはサポートされていません:Run、AnswerOnNextPrompt、ChooseCancelOnNextConfirmation、ChooseCancelOnNextPrompt、ChooseOkOnNextConfirmation、Debugger、ClickAt、DoubleClickAt、Echo、MouseOut、MouseUpAt、および MouseDownAt。

-   右クリックはサポートされていません 

-   Foreach コマンドを使用すると、追加の Web UI フロー入力が生成されます。 この問題を回避するには、追加のフィールドに任意の値を入力します。 再生には影響しません。

-   .side ファイルに複数のテスト プロジェクトが含まれている場合は、作成された最初のプロジェクトだけが実行されます。 

     >[!TIP]
     >Selenium IDE では、作成日ではなく名前によってテストが並べ替えられるため、作成された最初のテストが一覧で最初のテストにならない場合があることに注意してください。

-   Selenium IDE での直接再生は、意図したとおりに動作しない場合があります。 ただし、UI フロー インフラストラクチャによる実行時の再生は正常に動作します。

## <a name="next-steps"></a>次の手順

- [UI フロー](run-ui-flow.md)の実行方法について学習します。

- UI フローでさらに多くの操作を行う場合は、[入力と出力](inputs-outputs-web.md)パラメーターを使用して UI フローを試すこともできます。

 
