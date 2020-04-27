---
title: データ損失防止 (DLP) ポリシーの概要 | Microsoft Docs
description: Power Automate のデータ損失防止ポリシーの概要。
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
ms.date: 04/26/2020
ms.author: deonhe
search.app:
- Flow
- Powerplatform
search.audienceType:
- admin
ms.openlocfilehash: 722cf0c0f56a67b46f7f20ae76c2e98a86121f69
ms.sourcegitcommit: e709e8c4a62df6fdb0ca06f3f8afb5c639c76632
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2020
ms.locfileid: "82159563"
---
# <a name="data-loss-prevention-dlp-policies"></a>データ損失防止 (DLP) ポリシー


このドキュメントでは、定義したコネクタ一覧で組織のデータを共有から保護するデータ損失防止ポリシーについて説明します。

## <a name="whats-a-data-loss-prevention-policy"></a>データ損失防止ポリシーとは

組織のデータは、その成功に不可欠です。 そのデータは、意思決定のために容易に利用できる必要がありますが、アクセスすべきではないユーザーと共有されることがないように保護する必要があります。 このデータを保護するため、Power Automate では、ビジネス データにアクセスして共有できるコンシューマー コネクタを定義するポリシーを作成して適用できます。 データの共有方法を定義するこれらのポリシーは、データ損失防止 (DLP) ポリシーと呼ばれます。

## <a name="why-create-a-dlp-policy"></a>DLP ポリシーを作成する理由

DLP ポリシーを作成して、ビジネス データにアクセスして共有できるコンシューマー コネクタを明確に定義します。 たとえば、Power Automate を使っている組織は、SharePoint のビジネス データが Twitter フィードに自動的に発行されることを望まない場合があります。 これを防ぐには、SharePoint データがツイートのソースとして使用されるのをブロックする DLP ポリシーを作成します。

## <a name="benefits-of-a-dlp-policy"></a>DLP ポリシーの利点

* 組織全体でデータが一貫した方法で管理されることを保証します。
* 重要なビジネス データが誤ってソーシャル メディア サイトなどのコネクタに発行されるのを防ぎます。

## <a name="managing-dlp-policies"></a>DLP ポリシーの管理

### <a name="prerequisites-for-managing-dlp-policies"></a>DLP ポリシー管理の前提条件

* 環境管理者またはテナント管理者としてのアクセス許可のいずれか。

    アクセス許可の詳細については、[環境に関する記事](environments-overview-admin.md)をご覧ください。


## <a name="create-a-dlp-policy"></a>DLP ポリシーを作成する

### <a name="prerequisites-for-creating-dlp-policies"></a>DLP ポリシー作成の前提条件

DLP ポリシーを作成するには、少なくとも 1 つの環境へのアクセス許可が必要です。

会社の SharePoint サイトのデータが Twitter に発行されるのを防ぐ DLP ポリシーを作成するには、次の手順のようにします。

1. [Power Automate 管理センター](https://admin.flow.microsoft.com) (管理センター) にサインインします。

1. [データ ポリシー] タブを選び、 **[新しいポリシー]** リンクを選びます。

    ![サインイン](./media/prevent-data-loss/create-policy-1.png)
1. **[データ グループ]** タブを選びます。

1. ページの上部にある **[データ ポリシー名]** ラベルに、DLP ポリシーの名前として「*Secure Data Access for Contoso*」と入力します。

    ![サインイン](./media/prevent-data-loss/create-policy-2.png)

1. **[環境]** タブで[環境](environments-overview-admin.md)を選びます。

    > [!NOTE]
    > 環境管理者は、1 つの環境のみに適用されるポリシーを作成できます。 テナント管理者は、環境の任意の組み合わせに適用されるポリシーを作成できます。
    >
    >

    ![環境の選択](./media/prevent-data-loss/create-policy-3.png)

1. **[データ グループ]** タブを選択します。

    ![データ ソースの選択](./media/prevent-data-loss/create-policy-4.png)

1. **[Business data only]\(ビジネス データのみ\)** グループ ボックスの内部にある **[追加]** リンクを選びます。

    ![追加の選択](./media/prevent-data-loss/create-policy-5.png)

1. **[コネクタの追加]** ページで、 **[SharePoint]** コネクタと **[Salesforce]** コネクタを選びます。

   ![コネクタの選択](./media/prevent-data-loss/create-policy-6.png)

1. **[コネクタの追加]** ボタンを選んで、ビジネス データを共有できるコネクタを追加します。

1. 画面右上隅の **[ポリシーの保存]** を選びます。

1. しばらくすると、新しい DLP ポリシーが [データ損失防止ポリシー] の一覧に表示されます。

    ![DLP リスト](./media/prevent-data-loss/create-policy-9.png)

1. **(省略可能)** 新しい DLP ポリシーが利用可能になったことを知らせる電子メールやその他の通信をチームに送信します。

以上で、SharePoint と Saleforce 間でのデータ共有をアプリに許可し、他のサービスとのデータ共有をブロックする DLP ポリシーが作成されました。

> [!NOTE]
> 1 つのデータ グループにサービスを追加すると、他のデータ グループからそのサービスが自動的に削除されます。 たとえば、Twitter が現在、**ビジネス データのみ**データ グループに読み込まれているとき、ビジネス データを Twitter と共有しない場合、Twitter サービスを**ビジネス データ禁止**データ グループに追加します。 ビジネス データのみデータ グループから Twitter が削除されます。
>
>

## <a name="data-sharing-violations"></a>データ共有の違反

これまでに説明したような DLP ポリシーを作成した場合、ユーザーが Salesforce (**ビジネス データのみ**のデータ グループ) と Twitter (**ビジネス データが許可されない**データ グループ) の間でデータを共有するフローを作成すると、データ損失防止ポリシーに一致しないためにフローが**中断**されることがユーザーに通知されます。

![フローの作成](./media/prevent-data-loss/10.png)

ユーザーから中断されたフローについての問い合わせがあった場合は、次のことを検討します。

1. この例では、SharePoint と Twitter の間でビジネス データを共有するビジネス上の正当な理由がある場合は、DLP ポリシーを編集できます。

1. DLP ポリシーに準拠するようにフローを編集するよう、ユーザーに依頼します。

1. これら 2 つのエンティティ間でのデータ共有について決定が下されるまでフローを中断した状態のままにするよう、ユーザーに求めます。

## <a name="find-a-dlp-policy"></a>DLP ポリシーを検索する

### <a name="admins"></a>管理者

管理者は、管理センターから検索機能を使用して、特定の DLP ポリシーを検索できます。

> [!NOTE]
> 管理者は、組織内のユーザーがフローを作成する前にポリシーを認識できるように、すべての DLP ポリシーを公開する必要があります。
>
>

### <a name="makers"></a>作成者

管理者権限はないが、組織の DLP ポリシーの詳細を知りたい場合は、管理者に問い合わせてください。 詳細については、[作成者環境に関する記事](environments-overview-maker.md)もご覧ください。

> [!NOTE]
> DLP ポリシーを編集または削除できるのは管理者だけです。
>
>

## <a name="edit-a-dlp-policy"></a>DLP ポリシーを編集する

1. [管理センター](https://admin.flow.microsoft.com)を起動します。

1. 起動した管理センターで、左側の **[データ ポリシー]** リンクを選択します。

    ![データ ポリシーの選択](./media/prevent-data-loss/2.png)

1. 既存の DLP ポリシーの一覧を検索し、編集するポリシーの横にある編集ボタンを選びます。

1. ポリシーに必要な変更を行います。 たとえば、グループ内の環境またはサービスを変更できます。

1. **[ポリシーの保存]** を選んで、変更を保存します。

> [!NOTE]
> 環境管理者は、テナント管理者によって作成された DLP ポリシーを見ることはできますが、編集することはできません。
>
>

## <a name="delete-a-dlp-policy"></a>DLP ポリシーを削除する

1. [管理センター](https://admin.flow.microsoft.com)を起動します。

1. 左側にある **[Data polices]\(データ ポリシー\)** タブを選びます。

    ![データ ポリシー タブの選択](./media/prevent-data-loss/2.png)

1. 既存の DLP ポリシーの一覧を検索し、削除するポリシーの横にある削除ボタンを選びます。

    ![削除ボタンの選択](./media/prevent-data-loss/3-delete.png)

1. **[削除]** ボタンを選択して、ポリシーを削除することを確認します。

    ![ポリシー削除の確認](./media/prevent-data-loss/4.png)

## <a name="dlp-policy-permissions"></a>DLP ポリシーのアクセス許可

DLP ポリシーの作成と変更は、テナントと環境の管理者だけが実行できます。 アクセス許可の詳細については、[環境](environments-overview-admin.md)に関する記事をご覧ください。


## <a name="custom-and-http-connectors"></a>カスタム コネクタと HTTP コネクタ

カスタム コネクタと HTTP コネクタは、Power Automate テンプレートまたは PowerShell のいずれかを使用して DLP に追加する必要があります。

> [!TIP]
> スキーマ バージョン 2018-11-01 からダウングレードすることはできません。 ポリシーから HTTP サポートを削除することはできません。 HTTP サポートを削除しようとする場合、DLP ポリシーが破損している可能性があります。 さらに、DLP ポリシーが HTTP コネクタをサポートするように更新された場合、これらの HTTP 機能を使用している現在のフローが停止される可能性があります。

ポリシーに追加できる HTTP コネクタは次のとおりです。

- HTTP (および HTTP + Swagger)
- HTTP Webhook
- HTTP 要求

## <a name="add-connectors-custom-and-http-connectors-with-templates"></a>テンプレートを使用してコネクタ (カスタム コネクタと HTTP コネクタ) を追加する

[テンプレート](https://flow.microsoft.com/galleries/public/templates/ae9683086770420e902c043e5ed4b363/)を使用してカスタム コネクタをポリシーに追加するには、ポリシー名、コネクタを追加するグループ、コネクタの名前、ID、種類を入力します。 フローを 1 回実行して、指定されたポリシーとグループにカスタム コネクタを追加します。

[テンプレート](https://flow.microsoft.com/galleries/public/templates/834eb1366aa54335a5f979014a9e0477/)を使用して既存のポリシーに HTTP コネクタを追加するには、追加するポリシーの名前を入力し、そのフローを実行します。

## <a name="add-custom-and-http-connectors-with-powershell"></a>PowerShell を使用してカスタム コネクタと HTTP コネクタを追加する

PowerShell を使用し、ポリシーにカスタム コネクタや HTTP コネクタのサポートを追加するには、最新の Power Apps PowerShell スクリプトを[ダウンロード](https://docs.microsoft.com/powerapps/administrator/powerapps-powershell)してインポートし、コマンドレットの "New-AdminDlpPolicy"、"Set-AdminDlpPolicy"、"Add-CustomConnectorToPolicy"、"Remove-CustomConnectorFromPolicy" を使用してポリシーを変更します。 参照として 'Get-Help -detailed' コマンドレットを使用します。


> [!IMPORTANT]
> HTTP コネクタを含めるように DLP ポリシーを作成または更新する場合は、スキーマ バージョン 2018-11-01 を使用します。 テンプレートまたは PowerShell を使用して HTTP サポートを追加しても、指定したポリシーにのみ影響します。 管理センター経由で作成された新しいポリシーには、HTTP コネクタは含まれません。



## <a name="next-steps"></a>次の手順

* [環境に関する詳細](environments-overview-admin.md)
* [Power Automate の詳細](getting-started.md)
* [管理センターの詳細](admin-center-introduction.md)
* [データ統合の詳細](https://docs.microsoft.com/common-data-service/entity-reference/dynamics-365-integration)
