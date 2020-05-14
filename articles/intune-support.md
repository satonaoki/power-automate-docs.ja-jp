---
title: Power Automate モバイル アプリでは Microsoft Intune のモバイル アプリケーション管理がサポートされるようになりました。 | Microsoft Docs
description: Power Automate モバイル アプリでは Microsoft Intune のモバイル アプリケーション管理がサポートされるようになりました。
services: ''
suite: flow
documentationcenter: na
author: msftman
manager: kvivek
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/29/2019
ms.author: deonhe
ms.openlocfilehash: 521876e669e87c40f6108c46d7e4e0aee962ca34
ms.sourcegitcommit: d336e5ffb6cf07e5c8fefe19a87dd7668db9e074
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2020
ms.locfileid: "3297540"
---
# <a name="power-automate-mobile-app-supports-microsoft-intune"></a>Power Automateモバイルアプリは Microsoft Intune に対応しています


iOS および Android 用の Power Automate モバイル アプリでは、デバイスの登録なしで Intune のモバイル アプリケーション管理 (MAM) をすることができます。 MAM を使用すると、IT 管理者は、組織のデータを保護するモバイル データ ポリシーを作成して適用することができます。

## <a name="why-intune-support-is-important"></a>Intune のサポートが重要である理由

組織は、従業員のモバイル デバイスに存在するデータの制御を強化することを模索しています。 組織は、従業員が組織を去る場合に、そのデータがデバイスに移動する方法を制限し、データが確実に削除されるようにしたい場合があります。

## <a name="what-is-microsoft-application-management-mam"></a>Microsoft Application Management (MAM) の概要

MAM を使用すると、組織はテナント内でのアプリの使用方法を管理するポリシーを作成できます。 これには、アプリデータの暗号化を適用したり、承認されたアプリケーションのみにデータをコピーまたは抽出する機能を制限したり、デバイスに PIN を適用したりすることが含まれます。

### <a name="prerequisites"></a>前提条件

- Intune [アプリ保護ポリシー](https://docs.microsoft.com/intune/app-protection-policies)。
- Azure Active Directory (Azure AD) グループ。
- ポータル サイト。 MAM を使用する主な利点の 1 つは、デバイスを Intune MAM に登録する必要がないことです。 必要なのはポータル サイトだけです。これは、App Store および Google Play ストアから入手できます。
- iOS、Android、Windows Phone 用の モバイル アプリ Power Automate のバージョン 2.31.0、

## <a name="create-an-app-protection-policy-assign-apps-to-the-policy-define-settings-and-add-users-to-an-azure-ad-group"></a>アプリ保護ポリシーの作成、ポリシーへのアプリの割り当て、設定の定義、および Azure AD グループへのユーザーの追加を行う

Power Automate モバイル アプリを管理するには、次のことを行う必要があります。

1. アプリ保護ポリシーを作成する
1. アプリ保護ポリシーに Power Automate モバイル アプリを割り当てます。
1. ポリシー設定を割り当てる。 たとえば、 Power Automate モバイル アプリが実行されるモバイル デバイスへのアクセスに対して PIN を要求するポリシーを割り当てることができます。
1. アプリ保護ポリシーを特定の Azure AD グループに適用します。
1. アプリ保護ポリシーが適用されるすべてのユーザーを Azure AD グループに追加します。

アプリにアクセスする Power Automate モバイル アプリ ユーザーに対して事前に PIN を入力することを求める [アプリ保護ポリシー](https://docs.microsoft.com/intune/app-protection-policies) を作成するには、次の手順に従います。 


## <a name="test-the-app-protection-policy"></a>アプリ保護ポリシーをテストする

アプリ保護ポリシーを作成し、ユーザーを Azure AD グループに割り当てたら、Power Automate モバイル アプリを使用して、ポリシーが動作することを確認します。

ポリシーが動作することを確認するには、次の手順を行います。

1. アプリ保護ポリシーで定義したプラットフォームのいずれかと一致するプラットフォームを備えたデバイスに、Power Automate モバイル アプリをインストールします。
1. モバイル アプリの使用を、PIN を持つユーザーに限定する Azure AD グループ内のアカウントを使用してモバイル アプリにサインインします。

次のことを求めるメッセージが表示されます。
1. ポータル サイトをインストールする。
1. アプリ保護ポリシーの条件を満たす PIN がまだない場合は、PIN を設定する。


## <a name="learn-more"></a>詳細はこちら

[アプリ保護ポリシー](https://docs.microsoft.com/intune/app-protection-policies)を作成する方法

