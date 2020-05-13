---
title: Apply to each アクションを使用して項目の配列をループ処理する | Microsoft Docs
description: Power Automate を使って項目の配列をループ処理し、複数の条件を調べ、それらの条件に基づいてアクションを実行します。
services: ''
suite: flow
documentationcenter: na
author: msftman
manager: anneta
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2020
ms.author: deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: fcd99ea786c03eeac6ceabdf9a97886a8bbee022
ms.sourcegitcommit: 8714786a5b632dfd60099871629cf369a31c4125
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2020
ms.locfileid: "82896033"
---
# <a name="use-the-apply-to-each-action-in-power-automate-to-process-a-list-of-items-periodically"></a>Power Automate の Apply to each アクションを使用して項目の一覧を定期的に処理する

受信トレイに新しいメールが到着したときなど、多くのトリガーはイベントに基づいてフローをすぐに開始できます。 このようなトリガーは便利ですが、定義されているスケジュールでデータ ソースを照会し、データ ソース内の項目のプロパティに基づいて特定のアクションを行うようなフローを実行したいこともあります。 そのような処理のために、スケジュール (1 日 1 回など) に従ってフローを開始し、**Apply to each** などのループ アクションを使って項目の一覧を処理することができます。 たとえば、**Apply to each** を使うと、データベースのレコードや、Microsoft SharePoint の項目の一覧を更新できます。

このチュートリアルでは、15 分ごとに実行して以下の処理を行うフローを作成します。

1. Office 365 Outlook 受信トレイにある最新の未読メッセージを 10 件取得します。
2. 10 件の各メッセージを調べて、件名に**meet now** (会議の開始) が含まれるかどうかを確認します。
3. 上司からのメールかどうか、または高重要度で送信されたかどうかを確認します。
4. 件名に**meet now** (会議の開始) が含まれる、上司からのメールまたは高重要度で送信されたメールについて、プッシュ通知を送信し、既読としてマークします。

次の図は、作成するフローの詳細を示しています。

![作成するフローの概要](./media/apply-to-each/foreach-flow-visio.png)

## <a name="prerequisites"></a>前提条件
このチュートリアルの手順を正しく実行するための要件を次に示します。

* [Power Automate](https://flow.microsoft.com) を使うために登録されたアカウント。
* Office 365 Outlook アカウント。
* [Android](https://aka.ms/flowmobiledocsandroid)、[iOS](https://aka.ms/flowmobiledocsios)、または [Windows Phone](https://aka.ms/flowmobilewindows) 向けの Power Automate モバイル アプリ。
* Office 365 Outlook とプッシュ通知サービスへの接続。

## <a name="create-a-flow"></a>フローの作成
1. [Power Automate](https://flow.microsoft.com) にサインインします。
1. **[マイ フロー]** >  **[新規]** >  **[スケジュール—空白から作成]** の順に選択します。
1. **[予定フローを作成]** 画面で、 **[フロー名]** にフローの名前を指定します。 
1. 15 分ごとに実行するようにスケジュールを設定します。 
1. **[作成]** を選択します。 
   
    ![実行のスケジュール](./media/apply-to-each/foreach-3.png) 

1. **[+ 新しいステップ]** を選択し、検索ボックスに「**outlook**」と入力して、Microsoft Outlook に関連するすべてのコネクタとアクションを検索します。
1. **[メールを取得する (V3)]** アクションを選択します。
1. **[メールを取得する (V3)]** カードが開きます。 受信トレイ フォルダーの先頭から未読のメールを 10 件選ぶように、 **[メールを取得する (V3)]** カードを構成します。 添付ファイルはフローで使われないため含めません。
   
    ![電子メール カードの構成](./media/apply-to-each/foreach-5.png)
   
   > [!NOTE]
   > ここまでで、受信トレイからメールをいくつか取得する単純なフローができました。 これらのメールは配列で返されます。**Apply to each** アクションには配列が必要であり、これがまさに必要なことにあたります。

## <a name="add-actions-and-conditions"></a>アクションと条件を追加する
1. **[新しい手順]** >  **[ビルトイン]** >  **[Apply to each]** アクションの順に選択します。
1. **[Apply to each]** カードの **[以前の手順から出力を選択]** フィールドに **value** トークンを挿入します。 これにより、**Apply to each** アクションで使うメールの本文が取得されます。
   
    ![Body トークンの追加](./media/apply-to-each/foreach-7.png)
1. **[新しいステップ]** >  **[コントロール]** >  **[条件]** の順に選択します。
1. 各メールの件名で文字列 "meet now" を検索するように、 **[条件]** カードを構成します。
   
   * **[条件]** カードの最初のフィールドに **Subject** トークンを挿入します。
   * 演算子の一覧で **[次の値を含む]** を選択します。
   * 3 番目のフィールドに「**meet now**」と入力します。
     
     ![条件の構成](./media/apply-to-each/foreach-subject-condition.png)
1. **[はいの場合]** 分岐から **[アクションの追加]** >  **[条件]** を選択します。 **[条件 2]** カードが開きます。そのカードを次のように構成します。
   
   * 最初のフィールドに **Importance** トークンを挿入します。
   * 演算子の一覧で **[次の値に等しい]** を選択します。
   * 右側のフィールドに「**high**」と入力します。
     
     ![条件の追加](./media/apply-to-each/foreach-importance-condition.png)
1. **[はいの場合]** セクションの下で **[アクションの追加]** を選択します。     
   **[アクションを選択してください]** カードが開くので、検索条件 (**meet now** を含むメールが高重要度で送信された) が真の場合の動作を定義します。
1. **通知**を検索し、 **[Send me a mobile notification]** (モバイル通知を送信する) アクションを選択します。
   
    ![通知の検索と選択](./media/apply-to-each/foreach-10.png)
1. **[Send me a mobile notification]** (モバイル通知を送信する) カードで、メールの件名に "meet now" が含まれ、**Importance** (重要度) が**high** (高) の場合に送信されるプッシュ通知の詳細を指定します。
   
    ![通知の構成](./media/apply-to-each/foreach-11.png)

1. **[条件 2]** カードの **[いいえの場合]** 分岐に戻ります。
    
    * **[アクションの追加]** を選び、検索ボックスに「**上司を取得する**」と入力します。
    * 検索結果の一覧から **[上司の取得 (V2)]** アクションを選択します。
    * **To** トークンを **[上司の取得 (V2)]** カードの **[ユーザー (UPN)]** ボックスに入力します。
      
      ![上司を取得するアクションの追加と構成](./media/apply-to-each/foreach-get-manager.png)
1. **[いいえの場合]** 分岐から **[アクションの追加]** を選択します。
1. **[アクションの選択]** カードから **[条件]** を選択します。 **[条件 3]** カードが開きます。メール送信者のメール アドレス (From トークン) が上司のメール アドレス (Email トークン) と同じかどうかを調べるようにカードを構成します。
    
    * 最初のボックスに **From** トークンを挿入します。
    * 演算子の一覧で **[次の値を含む]** を選択します。
    * 一番右のボックスに **mail** トークンを入力します。
      
      ![検索条件の構成](./media/apply-to-each/foreach-condition3-card.png)
1. **[条件 3]** カードの **[はいの場合]** セクションの下で **[アクションの追加]** を選択します。
    
次に、検索条件 (メールが上司から送信された) が真の場合の動作を定義します。

1. **通知**を検索し、 **[Send me a mobile notification]** (モバイル通知を送信する) アクションを選択します。
    
     ![通知アクションの検索](./media/apply-to-each/foreach-10.png)
1. **[Send me a mobile notification 2]** (モバイル通知を送信する 2) カードで、メールが上司からのものである場合に送信されるプッシュ通知の詳細を指定して、 **[アクションの追加]** を選びます。
    
     ![通知カードの構成](./media/apply-to-each/foreach-boss-notification.png)
1. **[既読または未読にする (V2)]** アクションを追加します。
1. **[既読または未読にする (V2)]** カードに **Message Id** トークンを追加します。 **Message Id** トークンを探すには、 **[もっと見る]** を選ばなければならない場合があります。 **Message Id**は、開封済みとして指定するメッセージの ID です。
1. **[既読または未読にする (V2)]** カードの **[次のマークを付ける]** 一覧から **[既読]** を選択します。
    
     ![開封済みにするアクションの構成](./media/apply-to-each/foreach-mark-as-read2.png)
1. **[保存]** を選択してフローを保存します。

## <a name="run-the-flow"></a>フローを実行する
1. 件名に **meet now** が含まれる高重要度のメールを自分宛てに送信します (または、組織内のだれかにそのようなメールを送信してもらいます)。
1. メールが受信トレイにあり、未開封であることを確認します。
1. Power Automate にサインインして、 **[マイ フロー]** を選択します。
   
    フローの一覧が表示されます。 
    
1. 先ほど作成したフローを選択し、 **[実行]** を選択します。

   ![今すぐ実行](./media/apply-to-each/run-flow.png)

1. **[フローの実行]** ページを選択し、結果を表示するフロー実行を選択します。
   
    ![実行結果](./media/apply-to-each/foreach-run-3.png)

## <a name="view-results-of-the-run"></a>実行の結果を表示する
フローが正常に実行されたので、モバイル デバイスにプッシュ通知が送られてきているはずです。
   
> [!NOTE]
> プッシュ通知が届かない場合は、モバイル デバイスのデータ接続が動作していることを確認します。
 

