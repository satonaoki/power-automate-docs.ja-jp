---
title: 詳細オプションと複数のアクションの追加 | Microsoft Docs
description: フローを拡張して、詳細オプションを追加し (たとえば、電子メールの優先度を高く設定し)、同じイベントに対して他のアクションを追加します。
services: ''
suite: flow
documentationcenter: na
author: stepsic-microsoft-com
manager: anneta
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/20/2017
ms.author: stepsic
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: fbc18e31b571149164b7316bdaa02d2840686995
ms.sourcegitcommit: 52e739e5d53464b80e572928f131890562fc0396
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74376335"
---
# <a name="add-multiple-actions-and-advanced-options-to-a-flow"></a>フローへの複数のアクションと詳細オプションの追加
[!INCLUDE [view-pending-approvals](includes/cc-rebrand.md)]
同じトリガーに対して 1 つ以上の詳細オプションと複数のアクションを追加して、フローをカスタマイズします。 たとえば、電子メール メッセージを高い優先度で送信する詳細オプションを追加します。 SharePoint リストに項目が追加されたときに電子メールを送信するほか、同じ情報を含むファイルを Dropbox に作成します。

## <a name="prerequisites"></a>前提条件
* [フローを作成する](get-started-logic-flow.md)

## <a name="add-another-action"></a>他のアクションの追加
この手順では、フローの途中にアクションを追加します。 このアクションでは、ファイルを Dropbox に保存し、アイテムをリストにアーカイブします。

1. [flow.microsoft.com](https://flow.microsoft.com) で、上部のナビゲーション バーの **[自分のフロー]** を選択します。
2. フローの一覧で、編集するフローを選択します。
3. **[新しいステップ]** を選択し、 **[アクションの追加]** を選択します。
   
    ![折りたたまれている追加](./media/multi-step-logic-flow/add-action.png)
4. 使用できるアクションの一覧で "**ファイルの作成**" を検索し、 **[Dropbox - ファイルの作成]** を選択します。
   
    ![ファイルの作成を検索する](./media/multi-step-logic-flow/create-file-search.png)
5. メッセージが表示されたら、Dropbox の資格情報を指定します。
6. **[フォルダーのパス]** ボックスの右側にあるフォルダー アイコンを選択します。
7. 検索して、新しいファイルを配置するフォルダーを選択します。
   
    ![ファイルの作成を検索する](./media/multi-step-logic-flow/create-file-folder.png)
8. 新しいファイルの名前を **[ファイル名]** ボックスに入力します。 ファイル名に ".txt" などの拡張機能を追加するようにしてください。 ここでは、ファイルの一意性を確保するためにファイルの名前に **TweetId** を使用します。 **TweetId** トークンを探すには、 **[もっと見る]** を選択する必要がある場合があります。
9. **[ファイルのコンテンツ]** ボックスに入力して、ファイルに含めるテキストを追加します。 また、 **[ファイルのコンテンツ]** ボックスにトークンを追加することもできます。
   
    ![ファイル名とコンテンツ](./media/multi-step-logic-flow/create-file-name-and-contents.png)
   
   > [!IMPORTANT]
   > ファイルに既存のファイル名 (選択したフォルダー内) に一致する名前を付けた場合、既存のファイルは上書きされます。
   > 
   > 
10. 画面の上部にあるメニューで **[フローの更新]** を選択します。
11. 指定したキーワードを含むツイートを送信します。
    
     ファイルが 1 分以内に Dropbox アカウントに作成されます。

## <a name="reorder-or-delete-an-action"></a>アクションの並べ替えまたは削除
* Dropbox にファイルが作成された後に電子メールを受信するには、電子メール アクションの上にあるタイトル バーをドラッグして、Dropbox アクションを移動します。 トリガー (**新しいツイートの投稿時**) と電子メール アクションの間の矢印の上で、Dropbox アクションを放します。 (カーソルはアクションが正しく配置されているかどうかを示します。)
  
  > [!NOTE]
  > ステップの出力を使用している場合、そのステップの前に、別のステップを移動することはできません。
  > 
  > 
  
    ![メニューの削除](./media/multi-step-logic-flow/draggingaction.png)
* アクションを削除するには、削除するアクションのタイトル バーの右端にある省略記号 ([...]) を選択し、 **[削除]** 、 **[OK]** の順に選択します。
  
    ![メニューの削除](./media/multi-step-logic-flow/deletemenu.png)
  
     **注:** フローの任意の場所からアクションの出力を使用している場合、そのアクションは削除できません。 先にフィールドからその出力を削除すると、アクションを削除できます。


## <a name="copy-and-paste-actions"></a>アクションのコピーと貼り付け

フローをデザインするときにアクションを複製する場合、コピーして貼り付けることができます。 たとえば、条件を構築しているときに、**はいの場合**と**いいえの場合**で同様のアクションが必要な場合、アクションを両方、一から作成するのではなく、一方で最初のアクションを構築してから、もう一方にコピーします。


### <a name="to-copy-an-action"></a>アクションをコピーするには
1. アクション メニュー (アクションの右上にある [...])を選択します。
1. **[クリップボードにコピー]** を選択します。 
1. アクションを実行する **[新しいステップ]** を選択します。 

     **[自分のクリップボード]** タブで、コピーしたすべてのアクションから選択できることに注意してください。
1. 貼り付ける項目を選択します。

## <a name="add-advanced-options"></a>詳細オプションの追加
**[電子メールの送信]** アクションが含まれるフローを開始します。

1. **[電子メールの送信]** カードの下部にある **[詳細オプションの表示]** を選択します。
   
     電子メールの送信に使用する詳細オプションが表示されます。
   
    ![SharePoint のトリガー](./media/multi-step-logic-flow/advanced.png)
2. 詳細オプションを非表示にするには、 **[重要度]** の一覧で **[高]** を選択して、 **[詳細オプションを表示しない]** を選択します。
3. 画面の上部にあるメニューで **[フローの更新]** を選択します。
   
     このステップでは変更が保存されます。

