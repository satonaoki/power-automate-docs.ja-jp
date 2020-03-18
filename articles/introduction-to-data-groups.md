---
title: Power Automate のデータグループ | Microsoft Docs
description: Microsoft Power Apps と Power Automate のデータ グループの概要
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
ms.date: 10/26/2016
ms.author: deonhe
search.app:
- Flow
- Powerplatform
search.audienceType:
- admin
ms.openlocfilehash: ca3271f7c61c6835c856bc363f64882802f1556f
ms.sourcegitcommit: 84fb0547e79567efa19d7c16857176f7f1b53934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "79195614"
---
# <a name="learn-all-about-data-groups"></a>データ グループについて詳しく学ぶ

## <a name="what-is-a-data-group"></a>データ グループとは
データ グループは、[データ損失防止 (DLP) ポリシー](prevent-data-loss.md)内のサービスを分類する簡単な方法です。 **[ビジネス データのみ]** グループおよび **[許可されたビジネス データなし]** グループの 2 つのデータ グループが使用可能です。 組織は、特定のデータ グループにどのサービスが配置されるかを自由に決定できます。 サービスを分類するのに良い方法は、組織への影響に基づいて、サービスをグループ内に配置する方法です。 既定では、すべてのサービスが **[許可されたビジネス データなし]** データ グループに配置されます。 DLP ポリシーのプロパティを管理センターから作成または変更する場合に、データ グループ内のサービスを管理します。

## <a name="how-data-is-shared-between-data-groups"></a>データ グループ間でデータを共有する方法
グループの異なるサービス間ではデータを共有できません。 たとえば、**Business data only** (ビジネス データのみ) グループに SharePoint と Salesforce を配置し、**No business data allowed** (ビジネス データ禁止) グループに Facebook と Twitter を配置した場合、SharePoint と Facebook の間でデータを移動させるフローを作成することはできません。 グループの異なるサービス間ではデータを共有することはできませんが、特定のグループ内のサービス間ではデータを共有できます。 そのため、前の例に戻ると、SharePoint と Salesforce は同じデータ グループに配置されたため、エンド ユーザーが作成したフローでは、SharePoint と Salesforce の間でデータを共有できます。 同様に、エンド ユーザーは Facebook と Twitter の間でデータを共有するフローや Power Apps を作成できます。 重要なポイントは、特定のグループ内にあるサービスはデータを共有でき、異なるグループ間のサービスはデータを共有できないということです。  

また、1 つのデータ グループを*既定の*グループとして指定する必要があります。 最初は、 **[許可されたビジネス データなし]** グループが *既定の* グループであり、すべてのサービスがこのデータ グループ内にあります。 監理者は既定のデータ グループを **Business data only** (ビジネス データのみ) グループに変更できます。 **注** フローに追加された新しいサービスは指定の *既定* グループに配置されます。 そのため、**No business data allowed** (ビジネス データ禁止) を既定のグループにすることが推奨されます。ビジネス データを新しいサービスと共有した場合の影響を組織が判断してから **Business data only** (ビジネス データのみ) グループにサービスを手動で追加します。

## <a name="add-services-to-a-data-group"></a>サービスをデータ グループに追加する
このチュートリアルでは、SharePoint と Salesforce をデータ損失防止 (DLP) ポリシーの **[ビジネス データのみ]** データ グループに追加します。 

1. DLP ポリシーの **[ビジネス データのみ]** グループ ボックス内にある **[+ 追加]** リンクを選択します。    
   ![イメージの追加](./media/introduction-to-data-groups/add-to-data-group-1.png)  
2. SharePoint と Salesforce を選択し、次に **[サービスの追加]** を選択してビジネス データのみのグループに両方を追加します。    
   ![[サービスの追加] のイメージ](./media/introduction-to-data-groups/add-to-data-group-2.png)  
3. 上部にあるメニューから **[ポリシーの保存]** を選択します。  
   ![[ポリシーの保存]](./media/introduction-to-data-groups/add-to-data-group-4.png) 
4. SharePoint と Salesforce の両方が、ビジネス データのみのグループにあることを確認します。  
   ![更新されたビジネス データのみのグループ](./media/introduction-to-data-groups/add-to-data-group-3.png)   

このチュートリアルでは、DLP ポリシーの **Business data only** (ビジネス データのみ) データ グループに SharePoint と Salesforce を追加しました。 DLP ポリシーの環境に属する人物が SharePoint または Salesforce と **No business data allowed** (ビジネス データ禁止) データ グループのサービスの間でデータを共有するアプリを作成した場合、そのアプリの実行は許可されません。

## <a name="remove-services-from-a-data-group"></a>データ グループからサービスを削除する
すべてのサービスは、使用可能なデータ グループのいずれかに含まれる必要があるため、サービスを特定のグループから削除する場合は、そのサービスを別のグループに追加してから、ポリシーを保存します。  

## <a name="change-the-default-data-group"></a>既定のデータ グループの変更
このチュートリアルでは、**No business data allowed** (ビジネス データ禁止) から **Business data only** (ビジネス データのみ) グループに既定のデータ グループを変更します。  

**重要** フローに追加された新しいサービスは指定の *既定* グループに配置されます。 このような理由から、**No business data allowed** (ビジネス データ禁止) を既定のグループにしておき、**Business data only** (ビジネス データのみ) グループにサービスを手動で追加する方法が推奨されます。

1. 既定のデータ グループとして指定するデータ グループの右上隅にある **[...]** を選択します。    
   ![既定のグループの変更](./media/introduction-to-data-groups/default-data-group-0.png)  
2. **[既定のグループとして設定]** を選択します。  
   ![既定のグループの変更](./media/introduction-to-data-groups/default-data-group-1.png)   
3. 上部にあるメニューから **[ポリシーの保存]** を選択します。  
   ![既定のグループを変更する](./media/introduction-to-data-groups/add-to-data-group-4.png) 
4. 選択したデータ グループが既定のデータグループとして指定されていることを確認してください。  
   ![既定のグループの変更](./media/introduction-to-data-groups/default-data-group-2.png)   

## <a name="next-steps"></a>次の手順
* [データ損失防止 (DLP) ポリシーに関する詳細](prevent-data-loss.md)
* [環境の詳細](environments-overview-admin.md)   

