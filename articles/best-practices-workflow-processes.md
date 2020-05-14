---
title: ワークフロー プロセスの管理に関するベスト プラクティス | MicrosoftDocs
description: 推奨されるワークフローの使用方法について説明します
ms.custom: ''
ms.date: 06/27/2018
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
ms.assetid: 34e34c33-003a-494f-858c-3d34aacb308c
caps.latest.revision: 10
ms.author: matp
manager: kvivek
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: f3d02ca92b94752a8bbe6e3458fa8639de917dd8
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3297100"
---
# <a name="best-practices-for-workflow-processes"></a>ワークフロー プロセスに関するベスト プラクティス


このトピックは、ワークフロー プロセスの作成と管理のためのベスト プラクティスを紹介します。  
  
<a name="BKMK_AvoidInfiniteLoops"></a>   
## <a name="avoid-infinite-loops"></a>無限ループの回避  
 無限ループを開始する、ワークフローのロジックを作成する可能性があります。無限ループは、サーバーのリソースを消費し、パフォーマンスに影響を及ぼします。 無限ループが発生する可能性のある一般的な状態は、属性が更新されたときに開始し、ワークフローのロジックでその属性を更新するように構成されている、ワークフローがある場合です。 更新アクションがレコードを更新する同じワークフローをトリガーし、ワークフローを何回も反復して開始します。  
  
 作成するワークフローには、無限ループを検出して停止するためのロジックが含まれます。 ワークフロー プロセスが、短時間に特定のレコードに対して一定の回数を超えて実行されると、次のエラーでそのプロセスは失敗します。**このワークフロー ジョブは、それを開始したワークフローに無限ループが含まれるので取り消されます。ワークフロー ロジックを修正して、もう一度やり直してください**。 回数の上限値は 16 です。  
  
<a name="BKMK_UseWorkflowTemplates"></a>   
## <a name="use-workflow-templates"></a>ワークフロー テンプレートの使用  
 同様なワークフローが存在し、同じパターンに従ったワークフローをさらに作成する予定の場合、ワークフローをワークフロー テンプレートとして保存します。 このように、同様なワークフローを次回作成する必要があるときに、テンプレートを使用してワークフローを作成すれば、一からすべての条件とアクションを入力する必要がなくなります。  
  
 **プロセスの作成**ダイアログで、**既存テンプレートからのプロセスの新規作成 (一覧から選択)** を選択します。  
  
<a name="BKMK_UseChildWorkflows"></a>   
## <a name="use-child-workflows"></a>子ワークフローの使用  
 別のワークフローでまたは条件分岐で同じロジックを適用する場合、ロジックを子ワークフローと定義すると、各ワークフローまたは条件分岐でそのロジックを手動で複製する必要がなくなります。 これにより、ワークフローの維持が容易になります。 同じロジックを適用できる可能性のある多数のワークフローを調べる代わりに、1 つのワークフローを更新するだけで済みます。  
  
## <a name="automatically-delete-completed-workflow-jobs"></a>完了したワークフロー ジョブを自動的に削除する
バックグラウンド (非同期) のワークフローでは、ワークフロー定義で **[完了したワークフロー ジョブを自動的に削除する (ディスク容量の確保)]** オプションをオンにすることをお勧めします。 このチェック ボックスをオンにすると、領域を節約するために、システムで成功した実行のワークフロー ログを削除できます。 失敗したワークフロー実行のログは、トラブルシューティングのために常に保存されます。  

![ワークフロー ジョブの保持](media/workflow-job-retention.png)

<a name="BKMK_AutoDeleteCompletedWorkflowJobs"></a>   
## <a name="keep-logs-for-workflow-jobs-that-encountered-errors"></a>エラーが発生したワークフロー ジョブのログを保持する  
バックグラウンドで実行されない (同期の) ワークフローでは、ワークフロー定義で **[エラーが発生したワークフロー ジョブのログを保持する]** オプションをオンにすることをお勧めします。 このオプションをオンにすると、失敗したワークフロー実行のログをトラブルシューティングのために保存することができます。 成功した同期ワークフロー実行のログは、領域を節約するために常に削除されます。   

![失敗したワークフローのログを保持するオプション](media/keep-logs-for-workflows.png)

## <a name="limit-the-number-of-workflows-that-update-the-same-entity"></a>同じエンティティを更新するワークフローの数を制限する
同じエンティティを更新する複数のワークフローを実行すると、リソース ロックの問題が発生する可能性があります。 各営業案件の更新プログラムが関連取引先企業に対して更新をトリガーしている状況で実行している複数のワークフローを考えてみてください。 これらのワークフローの複数のインスタンスが実行されて、同じアカウント レコードを同時に更新しようとすると、リソース ロックの問題が発生する可能性があります。 ワークフローのエラーが発生し、**SQL タイムアウト: リソース _リソース名_ のロックを取得できません** などのエラー メッセージが記録されます。 

  
<a name="BKMK_DocumentChangesUsingNotes"></a>   
## <a name="use-notes-to-keep-track-of-changes"></a>メモを使用して変更を追跡する  
 ワークフローを編集する際には、[メモ] タブを使用し、実行した内容とその理由を入力してください。 これにより、その変更について他のユーザーが理解できます。  
  
## <a name="next-steps"></a>次のステップ  
 [ワークフロー プロセスの概要](workflow-processes.md)   
 [ワークフロー プロセスの構成](configure-workflow-steps.md)   
 [ワークフロー プロセスの監視と管理](monitor-manage-processes.md)
   
