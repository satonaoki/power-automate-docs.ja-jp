---
title: ワークフローからのユーザー定義アクションの呼び出し | MicrosoftDocs
description: ワークフローからのユーザー定義アクションの呼び出し方法について説明する
ms.custom: ''
ms.date: 11/22/2018
ms.reviewer: ''
ms.service: flow
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 (online)
- Dynamics 365 Version 9.x
- Power Apps
author: Mattp123
ms.assetid: 1fd5d39e-3dc8-4d1a-8b4b-ccaa303f4bbb
caps.latest.revision: 12
ms.author: matp
manager: kvivek
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: a35523209e3db8444da71c0757db29fa21de08b3
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3297914"
---
# <a name="invoke-custom-actions-from-a-workflow"></a>ワークフローからのユーザー定義アクションの呼び出し


ワークフローには、ビジネス シナリオをサポートするさまざまな機能があります。 レコードに対する基本的なデータ操作アクション (作成、更新、削除など) をワークフローの中から呼び出すことによって、かなりのビジネス シナリオが解決されます。 ただし、ワークフローの機能と、ワークフロー内から直接呼び出すユーザー定義アクションの機能を組み合わせると、コードを記述することなく、まったく新しい一連のビジネス シナリオをアプリケーションに追加できます。  
  
 ユーザー定義アクションがワークフローから呼び出されたときのシナリオを検討しましょう。 特定の営業案件の割引が 20% を超えたときにマネージャーの承認を要求するカスタム アクションを呼び出します。  
  
<a name="action"></a>   
## <a name="example-create-a-custom-action-using-the-opportunity-entity"></a>例: 営業案件エンティティを利用してカスタム アクションを作成する
  
1. [ソリューション エクスプローラー](/powerapps/maker/model-driven-apps/advanced-navigation#solution-explorer)で、**[プロセス]** を選択します。  
  
2.  ナビゲーション バーで、**新規**を選択します。 プロセスに名前を付け、**アクション**カテゴリを選択します。  
  
 値引きの承認を要求するには、**承認プロセス**という名前のユーザー定義アクションを使用します。 新規メッセージを作成して管理者の承認を得るための要求を送信するために、入力パラメーター **SpecialNotes** と、**電子メールの送信**ステップを次のように追加しました。  
  
 ![ステップの追加 - 電子メールの送信](media/enable-custom-action-approval-proces-sadd-email.png "ステップの追加 - 電子メールの送信")  
  
 電子メール メッセージを構成するには、**プロパティの設定**を選択します。 フォームが開いたとき、**フォーム アシスタント**を使用して、スクリーン ショットに強調表示されているように、電子メールに特別な注記とその他の情報を追加します。 特別な注記を追加するには、メッセージ内の表示させる場所にカーソルを置いてから、**フォーム アシスタント**の**検索**の最初のドロップダウン リストで**引数**を選択し、2 番目のドロップダウン リストで **SpecialNotes** を選択した後、**OK** を選択します。  
  
 ![電子メールの設定](media/enable-custom-action-approval-process-setup-email.png "電子メールの設定")  
  
 ワークフローからアクションを呼び出すには、それを有効にする必要があります。 アクションをアクティブ化した後、**プロパティの表示**を選択して、プロパティを表示することができます。  
  
 ![カスタム アクションのアクティブ化 - 承認プロセス](media/enable-custom-action-approval-process-activate-action.png "カスタム アクションのアクティブ化 - 承認プロセス")  
  
<a name="workflow"></a>   
## <a name="invoke-a-custom-action-from-a-workflow"></a>ワークフローからカスタム アクションを呼び出す  
  
1. [ソリューション エクスプローラー](/powerapps/maker/model-driven-apps/advanced-navigation#solution-explorer)で、**[プロセス]** を選択します。   
  
2.  ナビゲーション バーで、**新規**を選択します。 プロセスに名前を付け、**ワークフロー**カテゴリを選択します。  
  
 20% を超える営業案件の値引きに対して管理者の承認が必要なときは、いつでも**承認プロセス**というユーザー定義アクションを呼び出すワークフローを作成しました。  
  
 ![ワークフローからアクション プロパティを設定する](media/enable-custom-action-from-workflow.png "ワークフローからアクション プロパティを設定する")  
  
 **プロパティの設定**を選択することによって、アクションの入力プロパティを設定できます。 特別な注記に、営業案件に関連付けられている取引先企業の名前を追加しました。 **フォーム アシスタント**の**検索**で、最初のドロップダウン リストで**取引先企業**を選択し、2 番目のドロップダウン リストで**取引先企業名**を選択してから、**OK** を選択します。 **対象**プロパティが必要であり、そのプロパティはシステムによって自動的に入力されます。 **対象**プロパティでの **{営業案件 (Opportunity)}** は呼び出し元ワークフローを実行されるのと同じ営業案件です。 あるいは、検索を利用し、ターゲット プロパティに固有の営業案件を選択できます。  
  
 ![ApprovalProcess アクションの入力パラメーターを設定する](media/enable-customaction-workflow-set-properties.png "ApprovalProcess アクションの入力パラメーターを設定する")  
  



