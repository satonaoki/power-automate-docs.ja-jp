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
ms.date: 03/04/2020
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 825ebceb042215c379340f1e1b7e2dae6f921c2c
ms.sourcegitcommit: 84fb0547e79567efa19d7c16857176f7f1b53934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "79196041"
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

- Windows 10 Pro、Windows Server 2016、または Windows Server 2019 が実行されているデバイス。

- [Microsoft Edge](https://www.microsoftedgeinsider.com) または Google Chrome ブラウザー。

- [Common Data Service データベース](https://docs.microsoft.com/power-platform/admin/create-database)のある[環境](https://docs.microsoft.com/power-platform/admin/environments-overview)。

- サポート対象のキーボードが接続されていること。

## <a name="limitations"></a>制限事項

UI フローを記録、テスト、実行するには、各コンポーネントの最新バージョンが必要です。

以下はサポートされていません。
- Windows 10 Home のインストールはサポートされていません。

-   デスクトップ UI フロー

    -   複数のモニター
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

> [!WARNING]
> データ コレクションの設定を変更する必要がある場合は、UI フロー アプリをアンインストールしてから再インストールする必要があります。 最初に UI フロー アプリをアンインストールせずにデータ コレクションの設定を変更すると、UI フローは機能しなくなります。

## <a name="activate-the-ui-flows-browser-extension"></a>UI flows ブラウザー拡張機能をアクティブにする 

UI flows のインストーラーが完了すると、拡張機能のアクティブ化を求めるメッセージがブラウザーに表示されます。

- Microsoft Edge で、ブラウザーの右上にある各警告アイコンを選択し、 **[拡張機能の有効化]** を選択します。
-   Google Chrome では、プロンプトが表示されたら、 **[Enable extension]\(拡張機能の有効化\)** を選択します。  

> [!TIP]
> ブラウザーにプロンプトが表示されない場合は、次のことを確認してください。
> - Microsoft Edge または Google Chrome を使用する必要があります。
> - 場合によっては、拡張機能を手動で有効にする必要があります。 Microsoft Edge の場合は **edge://extensions** に移動し、Google Chrome の場合は **chrome://extensions** に移動します。
> - Power Automate の UI flows 拡張機能が表示されない場合は、[UI flows インストーラー](https://go.microsoft.com/fwlink/?linkid=2102613)を使用して再インストールできます。


## <a name="install-selenium-ide-to-automate-web-applications"></a>Selenium IDE をインストールして Web アプリケーションを自動化する

オープンソース ツールの Selenium IDE を使用すると、Web サイトでの人間の操作を記録して再生することができます。

UI flows を使用すると、Power Automate から Selenium IDE スクリプトを実行し、Common Data Service に安全に (適切な IT ガバナンスで) 保存することができます。

Selenium IDE をインストールするには、次の手順のようにします。

1. Microsoft Edge または Google Chrome の次バージョン用の Selenium IDE を[ダウンロードしてインストール](https://go.microsoft.com/fwlink/?linkid=2107665)します。

1. Microsoft Edge で、 **[Allow extensions from other stores]** \(他のストアからの拡張機能を許可する\) を選択し、 **[Add to Chrome]** \(Chrome に追加\) を選択します。

## <a name="install-the-on-premises-data-gateway"></a>オンプレミス データ ゲートウェイをインストールする

[イベント、スケジュール、またはボタン フロー](../getting-started.md#types-of-flows)から UI フローをトリガーするには、ゲートウェイが必要です。 リモート デバイス上。

>[!TIP]
>デバイスで UI フローを作成、編集、テストするだけの場合は、ゲートウェイは必要ありません。

必要な場合は、[オンプレミス データ ゲートウェイをインストール](https://docs.microsoft.com/data-integration/gateway/service-gateway-install)します。

## <a name="setup-ui-flows-connections-and-machine-credentials"></a>UI フローの接続とマシンの資格情報をセットアップする

1. [Power Automate](https://powerautomate.microsoft.com) にサインインします。
1. 画面の左側にある **[データ]** を展開します。
1. **[接続]** を選択します。

   ![[接続] タブのスクリーンショット](../media/ui-flows-setup/connections-tab.png)

1. [新しい接続] を選択します。

   ![接続のスクリーンショット](../media/ui-flows-setup/new-connection.png)

1. "*UI フロー*" を検索し、**[UI フロー (プレビュー)] を選択します。

   ![検索ボックスのスクリーンショット](../media/ui-flows-setup/search-ui-flow.png)

1. ゲートウェイ*ごとに*、ゲートウェイ情報とデバイスの資格情報を指定します。 

    - **ドメインとユーザー名**:デバイス アカウントを指定します。 ローカル アカウントを使用するには、ユーザー名 (“MACHINENAME\\User”、“local\\User” など) または Active Directory アカウント (“DOMAIN\\User” など) を使用します。
    - **パスワード**:アカウントのパスワード。
    - **ゲートウェイの選択**:構成するいずれかのゲートウェイを選択します。

      ![接続のために資格情報を入力する場所を示すスクリーンショット](../media/ui-flows-setup/credentials-screen.png)

1. **[作成]** を選択します。

## <a name="supported-keyboard-layouts"></a>サポート対象のキーボード レイアウト

- US キーボード: 英語 (米国)
- US キーボード: 英語 (オーストラリア)
- US キーボード: 英語 (カナダ)
- Microsoft Pinyin: 中国語 (簡体字、中国)
- ドイツ語キーボード: ドイツ語 (ドイツ)
- Microsoft IME: 日本語 (日本)
- UK キーボード: 英語 (イギリス)
- フランス語キーボード: フランス語 (フランス)
- ロシア語キーボード: ロシア語 (ロシア)
- ポルトガル語 (ブラジル ABNT) キーボード: ポルトガル語 (ブラジル)
- ポルトガル語 (ブラジル ABNT2) キーボード: ポルトガル語 (ブラジル)
- Microsoft IME: 韓国語 (韓国)
- スペイン語キーボード: スペイン語 (スペイン)
- イタリア語キーボード: イタリア語 (イタリア)
- ラテン アメリカ語キーボード: スペイン語 (メキシコ)
- ポーランド語 (プログラマ) キーボード: ポーランド語 (ポーランド)
- 米国 - 国際キーボード - オランダ語 (オランダ)
- トルコ語 Q キーボード - トルコ語 (トルコ)
- インド語キーボード - 英語 (インド)

## <a name="supported-languages"></a>サポートされている言語

UI flows で英語以外にサポートされる言語は次のとおりです。

|||||
----|-----|-----|--------
バスク語  | フランス語    | ラトビア語   | スロバキア語
ブルガリア語   |   ガリシア語    |   リトアニア語  |   スロベニア語
カタルニア語 |   ドイツ語      |マレー語  |   Spanish
簡体中国語    |   ギリシャ語   |   ノルウェー語   |   スウェーデン語
繁体中国語   |   ヒンディー語   |   ポーランド語  |   タイ語
クロアチア語    |   ハンガリー語   |   ポルトガル語 (ブラジル) |   トルコ語
チェコ語   |   インドネシア語  |   ポルトガル語 (ポルトガル)       |ウクライナ語
デンマーク語  |   イタリア語 |   ルーマニア語    |   ベトナム語
オランダ語       |日本語   |   ロシア語 
エストニア語    |カザフ語 |   セルビア語 (キリル、セルビア)  
フィンランド語     |韓国語     |セルビア語 (ラテン、セルビア)

## <a name="uninstall-ui-flows"></a>UI flows をアンインストールする

1. **[スタート]** メニューを開き、 **[設定]**  >  **[アプリ]** を選択します。
1. **[UI フロー (プレビュー)]** を探して選択します。
1. **[アンインストール]** を選択します。

## <a name="learn-more"></a>詳細情報

- 以前のリリースから [UI フローをアップグレードする](upgrade.md)
- [デスクトップ UI フローの作成](create-desktop.md)について学習します。
- [Web UI フローの作成](create-web.md)について学習します。
- [UI フロー](run-ui-flow.md)の実行方法について学習します。
- [UI フローの管理](manage.md)について学習する。
- [オンプレミス ゲートウェイ](../gateway-reference.md#use-a-gateway)の詳細について学習する
