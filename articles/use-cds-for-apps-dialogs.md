---
title: ガイド プロセスで Common Data Service ダイアログを使用する (非推奨) | MicrosoftDocs
description: ダイアログは、プロセスからユーザーに指示するためにステップバイステップのスクリプトを使用することによって、情報を収集および処理する同期または対話型のプロセスです。
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.topic: article
ms.service: flow
ms.assetid: d17f8ae2-854b-4f67-a115-5a03d4f0b8ce
caps.latest.revision: 25
author: msftman
ms.author: deonhe
manager: kvivek
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 69b8d448a3bb2636f4804fe75645467ca6bd081d
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3298420"
---
# <a name="use-common-data-service-dialogs-for-guided-processes-deprecated"></a>ガイド プロセスで Common Data Service ダイアログを使用する (非推奨)


[ダイアログは非推奨となっています](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#dialogs-are-deprecated)。 ダイアログを業務プロセス フローまたはキャンバス アプリに置き換える必要があります。 詳細: [ダイアログから業務プロセス フローまたはキャンバス アプリへの置き換え](replace-dialogs.md) 

Common Data Service のダイアログは、手順ごとのスクリプトによってユーザーをプロセスに誘導することで情報の収集と処理を行う、同期したプロセスまたは対話型のプロセスです。 たとえば、サービス担当者向けにサポート案件の解決やエスカレーションをガイドするダイアログを作成できます。 また、営業案件の見込み評価や潜在顧客の採点などの営業プロセスを標準化するダイアログを作成することもできます。

## <a name="differences-between-workflows-and-dialogs"></a>ワークフローとダイアログの違い

次の表に、Common Data Service のワークフローとダイアログの違いに関する情報を示します。  


| ワークフロー     |    ダイアログ      |
|---------------|--------------|
|                                                                                                  ユーザーが開始することも、自動化することもできます。                                                                                                   |                                                                                          ユーザーが開始する必要があります。                                                                                          |
|                                  非同期プロセスまたはリアルタイム プロセスで、完了まで実行するためにユーザー入力は必要ありません。 非同期プロセスはバックグラウンドで実行され、一方、リアルタイム プロセスをすばやく実行されます。                                   | リアルタイム プロセスでは、完了まで実行するためにユーザー入力が必要です。 これらのプロセスを実行すると、ウィザード風のインターフェイスが表示されるので、プロセスを実行するために適切な選択を行うことができます。 |
|                                                    非同期実行するワークフローの実行に関する詳細を保存するエンティティは `AsyncOperation`で、一方 `Process` はリアルタイム ワークフローで使用されます。                                                     |                                                       ダイアログの実行によって生成される情報を保存するエンティティは、`ProcessSession` エンティティです。                                                       |
|                  ワークフローに対するトリガーがサポートされています。 サポートされるトリガーの一覧については、[プロセスでサポートされている種類、トリガー、エンティティ](/dynamics365/customer-engagement/developer/supported-types-triggers-entities-actions-processes)に関するページを参照してください。                   |                                                                                   ダイアログに対するトリガーはサポートされていません。                                                                                    |
  
### <a name="see-also"></a>関連項目
[ダイアログを業務プロセス フローまたはキャンバス アプリに置き換える](replace-dialogs.md)
