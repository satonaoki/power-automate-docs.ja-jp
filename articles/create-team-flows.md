---
title: フローに他の所有者を追加し、チーム フローを作成する方法 | Microsoft Docs
description: Power Automate を使用すると、反復的なタスクを簡単に自動化できます。 ユーザーまたはグループを所有者として追加し、共同作業によりフローの設計および管理ができます。
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
ms.date: 11/15/2019
ms.author: deonhe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: b4479c2df6b8c7a1d5c269a8e0a48f15c1dda275
ms.sourcegitcommit: 5b1965a0c319c4294b7dc0c829120ed1f4f90444
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2020
ms.locfileid: "3299322"
---
# <a name="create-team-flows"></a>チーム フローを作成する

組織内の他のユーザーを所有者として追加することにより、チーム フローを作成します。 チーム フローのすべての所有者は、次の操作を実行できます。

* フローの履歴 (つまり各実行) を表示する。
* フローのプロパティを管理する (たとえば、フローの開始または停止、所有者の追加、接続用の資格情報の更新)。
* フローの定義を編集する (たとえば、アクションまたは条件の追加または削除)。
* 他の所有者を追加および削除する (ただし、フローの作成者以外とする)。
* フローを削除する。

チーム フローの作成者または所有者は、[Power Automate](https://flow.microsoft.com) の**チーム フロー** タブでそのリストを見つけることができます。

![[チームのフロー] タブ](./media/create-team-flows/addowner5.png)

> [!NOTE]
> 共有された接続は、それらが作成されたフローの中で**のみ**使うことができます。
> 
> 

所有者は、フローのサービスを使うことはできますが、別の所有者が作成した接続の資格情報を変更することはできません。

## <a name="prerequisites"></a>前提条件
チーム フローを作成するには、[有料の Power Automate プラン](https://flow.microsoft.com/pricing/) が必要です。 また、チーム フローの所有者を追加/削除するには、作成者または所有者である必要があります。

## <a name="create-a-team-flow"></a>チーム フローを作成する
チーム フローを作成するには、またはチーム フローに所有者を追加するには、次の手順に従います。

1. [Power Automate](https://flow.microsoft.com) にサインインし、**自分のフロー** を選びます。
2. 共有するフローに対して、**その他のコマンド** を選択し、**共有** を選択します。
   
    ![[チーム] アイコン](./media/create-team-flows/addowner1.png)
3. 所有者として追加するユーザーまたはグループの名前、メール アドレス、またはグループ名を入力します。
   
    ![ユーザーの検索](./media/create-team-flows/addowner2.png)
4. 表示される一覧で、所有者にするユーザーを選びます。
   
    ![ユーザーの選択](./media/create-team-flows/addowner3.png)
   
     選んだユーザーまたはグループが、フローの所有者になります。
   
    ![新しい所有者](./media/create-team-flows/addowner4.png)
   
     以上で&mdash;チーム フローが作成されました。

## <a name="add-a-list-as-a-co-owner"></a>共同所有者として一覧を追加する

SharePoint のリストを共有者としてフローに追加することで、リストへの編集アクセス権を持っている全員が自動的にフローへの編集アクセス権を得ることができます。 フローが共有されると、フローへのリンクを簡単に配布できます。

> [!TIP]
> フローが SharePoint に接続される場合はリストを使用し、それ以外の場合はグループを使用してください。
>

## <a name="remove-an-owner"></a>所有者を削除する

> [!IMPORTANT]
> Power Automate サービスにアクセスするために使用される資格情報を持つ所有者を削除する場合は、フローが正常に実行され続けるように、それらの接続の資格情報を更新する必要があります。
> 
> 

1. 共有するフローに対して、**その他のコマンド** を選択し、**共有** を選択します。
   
    ![ユーザー選択アイコン](./media/create-team-flows/addowner1.png)
2. 削除する所有者の **[削除]** アイコンを選びます。
   
    ![[削除] を選択](./media/create-team-flows/removeowner2.png)
3. 確認ダイアログ ボックスで、**[この所有者を削除する]** を選びます。
   
    ![削除の確認](./media/create-team-flows/removeowner3.png)
4. 以上で&mdash; 削除したユーザーまたはグループはフローの所有者として一覧に表示されなくなります。


## <a name="update-connection-owner"></a>接続の所有者の更新

既存の所有者を削除した場合、フロー内の接続の所有者を変更することが必要となる場合があります。 次の手順に従って、フローの所有者を切り替えます。

1. 左側パネルから **[データ]** を選択します。
1. **[接続]** を選択します。
1. 更新したい接続を検索し、選択します。
1. 選択した接続で **[...]** (その他のコマンド) を選択し、**[アカウントの切り替え]** を選択します。
1. 接続に別のアカウントを使用するための手順に従います。

## <a name="embedded-and-other-connections"></a>埋め込み接続とその他の接続

フローで使う接続は、2 つのカテゴリに分類されます。

* **埋め込み** &mdash; これらの接続はフローで使われます。
* **その他** &mdash; これらの接続はフローに対して定義されていますが、フロー内では使われていません。

フロー内で使われなくなった接続は **[その他]** の一覧に表示され、所有者が接続を再びフローに含めるまでそのままになります。

[接続の所有者を更新する](./create-team-flows.md#update-connection-owner)手順に従って、埋め込み接続を変更します。

接続の一覧は、フローのプロパティで所有者の一覧の下に表示されます。

![埋め込み接続](./media/create-team-flows/embeddedconnections.png)

