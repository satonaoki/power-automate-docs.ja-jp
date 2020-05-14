---
title: Common Data Service | Microsoft Docs
description: Common Data Service で、データのインポート、データのエクスポート、または承認を行うフローを作成します。
services: ''
suite: flow
documentationcenter: na
author: stepsic-microsoft-com
manager: kvivek
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/27/2020
ms.author: stepsic
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 7138d8f0aefc06799f5023204126e1a95494ba20
ms.sourcegitcommit: e58c8e6954c8e666497a66dc945fdc16c7c845a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/02/2020
ms.locfileid: "3331061"
---
# <a name="create-a-flow-that-uses-common-data-service"></a>Common Data Service を使用するフローを作成する

[Common Data Service](https://powerapps.microsoft.com/tutorials/data-platform-intro/) を使用するフローを作成することにより、ビジネス データの統合ビューで運用効率を向上させます。 組織の適切な標準ビジネス エンティティ (販売、購買、顧客サービス、生産性など) から成る、このセキュリティで保護されたビジネス データベースをデプロイします。 組織データを 1 つ以上の [カスタム エンティティ](https://powerapps.microsoft.com/tutorials/data-platform-create-entity/) に格納します。このエンティティには、Microsoft Excel や Salesforce などの外部データ ソースに比べて、いくつかの利点があります。

たとえば、Power Automate 内の Common Data Service をこれらの重要な方法で活用します：

* データのインポート、データのエクスポート、データに基づくアクションの実行 (通知の送信など) を行うフローを作成します。 この方法は完全な同期サービスではないことに注意してください。単に各エンティティに基づいてデータを内外に移動できるだけです。
  
    詳細な手順については、このトピックの後半にある手順を参照してください。
* [電子メールを介した承認ループを作成する](wait-for-approvals.md)代わりに、承認状態をエンティティに格納するフローを作成し、ユーザーが項目を承認または却下できるカスタム アプリをビルドします。
  
    詳細な手順については、[Common Data Service を使用した承認ループの作成](common-data-model-approve.md) を参照してください。

**前提条件**

* [Power Automate](https://flow.microsoft.com) と [Power Apps](https://make.powerapps.com) に登録します。
  
    問題が発生した場合は、所有するアカウントの種類が [Power Automate](sign-up-sign-in.md)  と [Power Apps](https://powerapps.microsoft.com/tutorials/signup-for-powerapps/) で対応しているかどうか、および組織が登録をブロックしていないことを確認してください。
* 今までに Common Data Service を使用したことがない場合は、 [powerapps.com](https://web.powerapps.com/#/entities) の **エンティティ** タブを開き、**自分のデータベースを作成する** をクリックまたはタップします。

## <a name="sign-in-to-your-environment"></a>環境へのサインイン
1. [Power Automate](https://flow.microsoft.com) ポータルを開き、右上隅の **サインイン** をクリックまたはタップします。
   
    **注**: **[サインイン]** ボタンを表示するには、左上のメニューを開く必要がある場合があります。
   
    ![サインイン](./media/common-data-model-intro/signin-flow.png)
2. 右上のメニューで、powerapps.com でデータベースを作成した環境を選択します。
   
    **注**: 同じ環境を選択しなかった場合は、エンティティが表示されません。
   
    ![環境の選択](./media/common-data-model-intro/select-environment.png)

## <a name="open-a-template"></a>テンプレートを開く
1. 画面上部の **[テンプレートの検索]** ボックスに、「**common**」と入力するか貼り付けて、Enter キーを押します。
   
    ![テンプレートの検索](./media/common-data-model-intro/template-search.png)
2. テンプレートの一覧で、目的のソースから目的のエンティティ (または "*オブジェクト*") にデータをインポートするテンプレートをクリックまたはタップします。
   
    たとえば、連絡先情報を Dynamics 365 から Common Data Service にコピーするテンプレートをクリックまたはタップします。
   
    ![テンプレートを選択する](./media/common-data-model-intro/choose-template.png)
3. **[このテンプレートを使用]** をクリックまたはタップします。
   
    ![テンプレートの使用](./media/common-data-model-intro/use-template.png)
4. Power Automate から Dynamics 365 への接続を作成していない場合は、 **サインイン** をクリックまたはタップし、資格情報の入力を促すメッセージが表示されたら入力します。
   
    ![Dynamics 365 へのサインイン](./media/common-data-model-intro/dynamics-signin.png)
5. **[続行]** をクリックまたはタップします。
   
    ![アカウントの確認](./media/common-data-model-intro/confirm-accounts.png)

## <a name="build-your-flow"></a>フローを構築する
1. 最初のカードでは、フローをトリガーするイベントを指定します。
   
    たとえば、Dynamics 365 のインスタンスから Common Data Service に新しい連絡先をコピーするフローを作成しようとしているとします。 **[When a record is created (レコードが作成されたとき)]** で、下向き矢印をクリックまたはタップし、表示された一覧のオプションをクリックまたはタップすることで、インスタンスを指定します。
   
    ![Dynamics 365 のインスタンスの指定](./media/common-data-model-intro/specify-instance.png)
2. (省略可能) 画面上部で、作成しているフローに別の名前を指定します。
   
    **注**: ブラウザー ウィンドウが最大化されていない場合、UI の表示が若干異なることがあります。
   
    ![フローの名前の指定](./media/common-data-model-intro/name-flow.png)
3. **[フローの作成]** をクリックまたはタップします。
   
    **注**: ブラウザー ウィンドウが最大化されていない場合、チェック マークだけが表示されることがあります。
   
    ![フローの作成](./media/common-data-model-intro/create-flow.png)

以上で、ソース システムにそのオブジェクトが作成されるたびに、オブジェクトが Common Data Service にインポートされます。 必要なことを実行するテンプレートが見つからない場合は、Common Data Service に基づいて動作するフローを[一から作成する](get-started-logic-flow.md)ことができます。

データベースでの変更に対してアクションを実行することができます。 たとえば、データが変更されるたびに通知メールを送信できます。

