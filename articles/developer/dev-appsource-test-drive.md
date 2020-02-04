---
title: AppSource で顧客がフローを体験できるようにする | Microsoft Docs
description: AppSource を使用してお客様とアプリを共有し、ビジネスの潜在顧客を生成します。
services: ''
suite: flow
documentationcenter: na
author: MSFTMAN
manager: KVivek
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/09/2017
ms.author: Deonhe
search.app:
- Flow
search.audienceType:
- developer
ms.openlocfilehash: 67e38b8c3b2a7f32c88ecc31c88cfdb654d23310
ms.sourcegitcommit: 835b005284b9ae21ae1742a7d36b574ba3884bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2020
ms.locfileid: "74362926"
---
# <a name="let-customers-test-drive-your-flows-on-appsource"></a>AppSource で顧客がフローを体験できるようにする
[!INCLUDE [view-pending-approvals](../includes/cc-rebrand.md)]
アプリと Power Automate がどのように統合されているかを顧客に紹介したい場合があります。 顧客と Power Automate の統合を共有し、潜在顧客を作り出す手段として、[AppSource.com](https://appsource.microsoft.com) で体験版ソリューションが提供されるようになりました。

## <a name="what-is-a-test-drive-solution"></a>体験版ソリューションとは
体験版ソリューションでは、アプリケーションをインストールすることなく、実際のアプリを顧客に試してもらうことができます。 顧客は、Azure Active Directory (AAD) アカウントを使用して AppSource.com にサインインし、Web ブラウザーでアプリを実行するだけです。 体験版がなければ、お客様はアプリに関する説明を読んだり、ビデオを見たりするしかありません。 体験版を使用すると、ソリューションの内容やアプリの機能についてよく理解することができます。 アプリを実際に使用する経験を持つことができます。 顧客は中を見てアプリのしくみを調べることはできないので、アプリの知的財産権が保護されます。 Microsoft は潜在顧客の情報を収集してアプリの開発者と共有し、ビジネスの成長を支援します。

## <a name="how-do-i-build-a-test-drive-solution"></a>体験版ソリューションの構築方法
体験版ソリューション用のアプリの作成は、普通のアプリの作成方法とほぼ同じですが、ユーザーに読み取り専用ユーザーとしてのアクセス権を付与できるデータ ソースを使用する必要があります。 既に設定されているデータ ソースを使えば、問題なく試すことができます。最終的に顧客に配布される完全なソリューションには書き込み可能なデータが含まれますが、体験版ソリューションには読み取り専用のデータで十分です。

### <a name="embed-flow-into-your-product"></a>製品へのフローの組み込み
ユーザーに読み取り専用アクセス権を付与できるデータ ソースを用意したら、Power Automate をアプリケーションに組み込むことができます。 [組み込みについて詳しくは、こちらをご覧ください](embed-flow-dev.md)。 アプリケーションに固有のテンプレートがよくわかるように、検索機能を使用できます。 たとえば、アプリケーションが Dynamics 365 にデータを作成する場合、データを取得する Dynamics 365 テンプレートを強調してユーザーにメールを送ることができます。 

## <a name="how-do-i-list-my-test-drive-solution-on-appsourcecom"></a>AppSource.com に体験版ソリューションを表示する方法
アプリの準備ができたら、AppSource.com で公開します。 そのための手順を始めるには、flow.microsoft.com で[申し込みフォーム](https://flow.microsoft.com/partners/get-listed/)を作成してください。 申し込むと、AppSource.com で公開するためにアプリを送信する方法が記載されたメールを受け取ります。

