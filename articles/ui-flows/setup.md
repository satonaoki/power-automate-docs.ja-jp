---
title: デバイスで UI flows を設定する | Microsoft Docs
description: デバイスで UI flows を設定します
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
ms.date: 11/04/2019
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: e7d5e4219c46703019f995b625c6d672a767018a
ms.sourcegitcommit: 835b005284b9ae21ae1742a7d36b574ba3884bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2020
ms.locfileid: "74882123"
---
# <a name="set-up-ui-flows"></a>UI フローの設定

[このトピックはプレリリース版のドキュメントであり、変更される可能性があります。]

[!INCLUDE [view-pending-approvals](../includes/cc-rebrand.md)]

> [!IMPORTANT]
> 現在、UI flows 機能はリージョンにロールアウト中です。 お使いの環境に機能が表示されない場合、UI フローを作成できない場合、またはフロー内で実行しようとするとエラーが発生する場合は、しばらくしてからもう一度試してください。

デバイスを使用して UI フローを作成する前に、デバイスがここに記載されている要件を満たしていることを確認する必要があります。

> [!TIP]
> UI フローを作成する前に、[コネクタの一覧](https://flow.microsoft.com/connectors/)を調べて、自動化したいアプリケーションに既にコネクタがあるかどうかを確認します。 ある場合は、UI フローではなくフローを作成することを検討します。 [独自のコネクタ](https://docs.microsoft.com/connectors/custom-connectors/)を作成することもできます。

## <a name="prerequisites"></a>前提条件

- [有料版](https://flow.microsoft.com/pricing/)または[試用版](https://flow.microsoft.com/manage/)の Power Automate プラン。

- 管理者特権と Power Automate で Windows デバイスにサインインするための職場または学校アカウント。

- Windows 10、Windows Server 2016、または Windows Server 2019 が実行されているデバイス。
- 接続された US (QWERTY) キーボード。

- [次期バージョンの Microsoft Edge](https://www.microsoftedgeinsider.com) または Google Chrome。

- [Common Data Service データベース](https://docs.microsoft.com/power-platform/admin/create-database)のある[環境](https://docs.microsoft.com/power-platform/admin/environments-overview)。

## <a name="limitations"></a>制限事項

UI フロー (プレビュー) は英語で利用できます。

以下はサポートされていません。

-   デスクトップ UI フロー

    -   複数のモニター
    -   仮想マシン
    -   ダブルクリック、マウス ポイント、タッチ/ペン入力
    -   Windows での対話 (エクスプローラー、スタートアップ メニュー、タスク バーなど)

-   Web UI フロー

    -   右クリック
    -   ユーザー セッション情報 (Cookie など) は再生中に再利用されません。 Web サイトで必要なときにサインイン情報を埋め込むには、スクリプトを編集する必要があります。

機能固有の制限事項については、各機能のドキュメントをご覧ください。

## <a name="install-ui-flows-on-your-device"></a>デバイスに UI flows をインストールする

UI flows のインストーラーには、デスクトップ用の UI フローを記録、編集、テストするために必要なすべてのコンポーネントが含まれています。 

>[!IMPORTANT]
>UI flows のインストーラーでは、Webdriver コンポーネントと UI flows ブラウザー拡張機能がインストールされます。 これらはどちらも、デスクトップ用の UI フローを記録、テスト、実行するために必要です。

UI flows アプリをインストールするには、次の手順のようにします。

1. [UI flows のインストーラーをダウンロードします](https://go.microsoft.com/fwlink/?linkid=2102613)。
1. **Setup.Microsoft.Flow.UIflow.exe** ファイルを開きます。 このファイルは、前の手順でダウンロードした後、**Downloads** フォルダーにあるはずです。
1. **UI フロー (プレビュー) セットアップ** インストーラーの指示に従って、インストールを完了します。

> [!TIP]
> データ コレクションの設定を変更したい場合は、UI flows を再インストールして、設定を変更します。

## <a name="activate-the-ui-flows-browser-extension"></a>UI flows ブラウザー拡張機能をアクティブにする 

UI flows のインストーラーが完了すると、拡張機能のアクティブ化を求めるメッセージがブラウザーに表示されます。

- Microsoft Edge (Chromium) では、ブラウザーの右上にある各警告アイコンを選択し、 **[Enable extension]\(拡張機能の有効化\)** を選択します。
-   Google Chrome では、プロンプトが表示されたら、 **[Enable extension]\(拡張機能の有効化\)** を選択します。  

> [!TIP]
> ブラウザーにプロンプトが表示されない場合は、次のことを確認してください。
> - Microsoft Edge (Chromium) または Google Chrome を使用する必要があります
> - 場合によっては、拡張機能を手動で有効にする必要があります。 Microsoft Edge (Chromium) の場合は **edge://extensions** に移動し、Google Chrome の場合は **chrome://extensions** に移動します。
> - Power Automate の UI flows 拡張機能が表示されない場合は、[UI flows インストーラー](https://go.microsoft.com/fwlink/?linkid=2102613)を使用して再インストールできます。

<!-- To do for Gautier: check if the below is not bugged as there was one at some point.
> - Reinstall the extension from the Chrome store
Navigate to this link https://chrome.google.com/webstore/detail/microsoft-flow-preview/jcajipieipkmjpfakbdhmjidmhidogoo and install it manually, that will fix any issues. (For Edge Chromium, use the same link and accept when prompted to install from external stores.)
-->

## <a name="optional-install-selenium-ide-to-automate-web-applications"></a>(省略可能) Selenium IDE をインストールして Web アプリケーションを自動化する

オープンソース ツールの Selenium IDE を使用すると、Web サイトでの人間の操作を記録して再生することができます。

UI flows を使用すると、Power Automate から Selenium IDE スクリプトを実行し、Common Data Service に安全に (適切な IT ガバナンスで) 保存することができます。

Selenium IDE をインストールするには、次の手順のようにします。

1. Microsoft Edge または Google Chrome の次バージョン用の Selenium IDE を[ダウンロードしてインストール](https://go.microsoft.com/fwlink/?linkid=2107665)します。

1. Microsoft Edge (Chromium) では、 **[Allow extensions from other stores]\(他のストアからの拡張機能を許可する\)** を選択し、 **[Add to Chrome]\(Chrome に追加\)** を選択します。

## <a name="install-the-on-premises-data-gateway"></a>オンプレミス データ ゲートウェイをインストールする

[イベント、スケジュール、またはボタン フロー](../getting-started.md#types-of-flows)から UI フローをトリガーするには、ゲートウェイが必要です。

>[!TIP]
>デバイスで UI フローを作成、編集、テストするだけの場合は、ゲートウェイは必要ありません。

必要な場合は、[オンプレミス データ ゲートウェイをインストール](https://docs.microsoft.com/data-integration/gateway/service-gateway-install)します。

## <a name="uninstall-ui-flows"></a>UI flows をアンインストールする

1. **[スタート]** メニューを開き、 **[設定]**  >  **[アプリ]** を選択します。
1. **[UI フロー (プレビュー)]** を探して選択します。
1. **[アンインストール]** を選択します。

## <a name="next-steps"></a>次の手順

- [デスクトップ UI フローの作成](create-desktop.md)について学習します。
- [Web UI フローの作成](create-web.md)について学習します。
- [UI フロー](run-ui-flow.md)の実行方法について学習します。
- [UI フローの管理](manage.md)について学習する。
- [オンプレミス ゲートウェイ](../gateway-reference.md#use-a-gateway)の詳細について学習する

## <a name="limitations"></a>制限事項
- UI フローを記録、テスト、実行するには、各コンポーネントの最新バージョンが必要です。
- 最新バージョンをインストールする前に、以前のバージョンをアンインストールしてください。


