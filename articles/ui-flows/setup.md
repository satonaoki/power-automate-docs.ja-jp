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
ms.date: 03/24/2020
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 97456d637dd272a465559d4cee8fb1d17fe3de8d
ms.sourcegitcommit: bba5bd4ae3879b6bf1521d8ed636374fe09709e7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3298772"
---
# <a name="set-up-ui-flows"></a>UI フローの設定

デバイスを使用して UI フローを作成する前に、デバイスがここに記載されている要件を満たしていることを確認する必要があります。

> [!TIP]
> UI フローを作成する前に、[コネクタの一覧](https://flow.microsoft.com/connectors/)を調べて、自動化したいアプリケーションに既にコネクタがあるかどうかを確認します。 ある場合は、UI フローではなくフローを作成することを検討します。 [独自のコネクタ](https://docs.microsoft.com/connectors/custom-connectors/)を作成することもできます。

## <a name="prerequisites"></a>前提条件

- [有料版](https://flow.microsoft.com/pricing/) または [試用版](https://flow.microsoft.com/manage/) の Power Automate プラン。

- 管理者特権と Power Automate で Windows デバイスにサインインするための職場または学校アカウント。

- Windows 10 Pro、Windows Server 2016、または Windows Server 2019 を実行するデバイス。

- [Microsoft Edge](https://www.microsoft.com/edge/) (バージョン 80 以降)   または Google Chrome ブラウザー。

- [Common Data Service データベース](https://docs.microsoft.com/power-platform/admin/create-database) のある [環境](https://docs.microsoft.com/power-platform/admin/environments-overview)。

- サポート対象のキーボードが接続されていること。

## <a name="limitations"></a>制限

UI フローを記録、テスト、実行するには、各コンポーネントの最新バージョンが必要です。

以下はサポートされていません。
- Windows 10 Home のインストールはサポートされていません。

-   デスクトップ UI フロー

    -   複数のモニター
    -   ダブルクリック、マウス ポイント、タッチ/ペン入力
    -   Windows での対話 (エクスプローラー、スタートアップ メニュー、タスク バーなど)

-   Web UI フロー

    -   右クリックします。
    -   ユーザー セッション情報 (Cookie など) は再生中に再利用されません。 Web サイトで必要なときにサインイン情報を埋め込むには、スクリプトを編集する必要があります。

機能固有の制限事項については、各機能のドキュメントをご覧ください。

## <a name="install-ui-flows-on-your-device"></a>デバイスに UI flows をインストールする

UI flows のインストーラーには、デスクトップ用の UI フローを記録、編集、テストするために必要なすべてのコンポーネントが含まれています。 

>[!IMPORTANT]
>UI flows のインストーラーでは、Webdriver コンポーネントと UI flows ブラウザー拡張機能がインストールされます。 これらはどちらも、デスクトップ用の UI フローを記録、テスト、実行するために必要です。

UI flows アプリをインストールするには、次の手順のようにします。

1. [UI flows のインストーラーをダウンロードします](https://go.microsoft.com/fwlink/?linkid=2102613)。
1. **Setup.Microsoft.PowerAutomate.UIflow.exe** ファイルを開きます。 このファイルは、前の手順でダウンロードした後、**Downloads** フォルダーにあるはずです。
1. **UI フロー セットアップ** インストーラーの指示に従い、インストールを完了させます。

### <a name="set-data-collection-options"></a>データ収集オプションを設定する

使用状況データを Microsoft に送信しない場合は、インストール時に既定の設定を変更できます。 これを行うには、**[使用状況データの収集を Microsoft に許可して UI フローを向上させる]** をオフにします。

![データ収集オプションを示す画像](../media/ui-flows-setup/data-collection-settings.png)

## <a name="activate-the-ui-flows-browser-extension"></a>UI flows ブラウザー拡張機能をアクティブにする 

UI flows のインストーラーが完了すると、拡張機能のアクティブ化を求めるメッセージがブラウザーに表示されます。

- [Microsoft Edge](https://www.microsoft.com/edge/) (バージョン 80 以降) で、ブラウザーの右上にある各警告アイコンを選択し、**拡張機能の有効化** を選択します。
-   Google Chrome では、プロンプトが表示されたら、**[Enable extension]\(拡張機能の有効化\)** を選択します。  

> [!TIP]
> ブラウザーにプロンプトが表示されない場合は、次のことを確認してください。
> - [Microsoft Edge](https://www.microsoft.com/edge/) (バージョン 80 以降) または Google Chrome を使用します。
> - 場合によっては、拡張機能を手動で有効にする必要があります。 Microsoft Edge の場合は **edge://extensions** に移動し、Google Chrome の場合は **chrome://extensions** に移動します。
> - Power Automate の UI フロー 拡張機能が表示されない場合は、[UI フロー インストーラー](https://go.microsoft.com/fwlink/?linkid=2102613) を使用して再インストールできます。


## <a name="install-selenium-ide-to-automate-web-applications"></a>Selenium IDE をインストールして Web アプリケーションを自動化する

オープンソース ツールの Selenium IDE を使用すると、Web サイトでの人間の操作を記録して再生することができます。

UI フロー を使用すると、Power Automate から Selenium IDE スクリプトを実行し、Common Data Service に安全に (適切な IT ガバナンスで) 保存することができます。

Selenium IDE をインストールするには、次の手順のようにします。

1. [Microsoft Edge](https://www.microsoft.com/edge/) (バージョン 80 以降) または Google Chrome の Selenium IDE を [ダウンロードしてインストールします](https://go.microsoft.com/fwlink/?linkid=2107665)。

1. Microsoft Edge (バージョン 80 以降) で、**他のストアからの拡張機能を許可する** を選択し、**Chrome に追加** を選択します。

## <a name="install-the-on-premises-data-gateway"></a>オンプレミス データ ゲートウェのインストール

[イベント、スケジュール、またはボタン フロー](../getting-started.md#types-of-flows)から UI フローをトリガーするには、ゲートウェイが必要です。 リモート デバイス上。

>[!TIP]
>デバイスで UI フローを作成、編集、テストするだけの場合は、ゲートウェイは必要ありません。

必要な場合は、[オンプレミス データ ゲートウェイをインストール](https://docs.microsoft.com/data-integration/gateway/service-gateway-install)します。


>[!IMPORTANT]
>ゲートウェイをインストールすると、既定で、Power Automate が使用するリージョンになります。


## <a name="setup-ui-flows-connections-and-machine-credentials"></a>UI フローの接続とマシンの資格情報をセットアップする

1. [Power Automate](https://powerautomate.microsoft.com) にサインインする。
1. 画面の左側にある **[データ]** を展開します。
1. **[接続]** を選択します。

   ![[接続] タブのスクリーンショット](../media/ui-flows-setup/connections-tab.png)

1. [新しい接続] を選択します。

   ![接続のスクリーンショット](../media/ui-flows-setup/new-connection.png)

1. "*UI フロー*" を検索し、**[UI フロー]** を選択します。

   ![検索ボックスのスクリーンショット](../media/ui-flows-setup/search-ui-flow.png)

1. ゲートウェイ情報とデバイスの資格情報を指定します。 

    - **ドメインとユーザー名**: デバイス アカウントを提供します。 ローカル アカウントを使用するには、ユーザー名 (“MACHINENAME\\User”、“local\\User” など) または Active Directory アカウント (“DOMAIN\\User” など) を使用します。
    - **パスワード**: アカウントのパスワード。
    - **ゲートウェイを選択**: 使用するゲートウェイを選択します。

      ![接続のために資格情報を入力する場所を示すスクリーンショット](../media/ui-flows-setup/credentials-screen.png)

1. **作成**を選びます。

## <a name="troubleshoot-missing-gateway"></a>ゲートウェイが見つからない場合のトラブルシューティング

次の理由により、接続の作成中にゲートウェイが一覧に表示されない場合があります。

- ゲートウェイは、Power Automate リージョンとは異なるリージョンにインストールされる場合があります。 この問題を解決するには、デバイスからゲートウェイをアンインストールしてから、[適切な Power Automate リージョン](../regions-overview.md#region-mappings-for-power-automate-and-gateways) 選択して、再インストールします。
- ゲートウェイがその所有者によって削除されました。

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

UI フローで英語以外にサポートされる言語は次のとおりです。

|||||
----|-----|-----|--------
バスク語  | フランス語    | ラトビア語   | スロバキア語
ブルガリア語   |   ガリシア語    |   リトアニア語  |   スロベニア語
カタルニア語 |   ドイツ語      |マレー語  |   スペイン語
簡体中国語    |   ギリシャ語   |   ノルウェー語   |   スウェーデン語
中国語 (繁体字)   |   ヒンディー語   |   ポーランド語  |   タイ語
クロアチア語    |   ハンガリー語   |   ポルトガル語 (ブラジル) |   トルコ語
チェコ語   |   インドネシア語  |   ポルトガル語 (ポルトガル)       |ウクライナ語
デンマーク語  |   イタリア語 |   ルーマニア語    |   ベトナム語
オランダ語       |日本語   |   ロシア語 
エストニア語    |カザフ語 |   セルビア語 (キリル、セルビア)  
フィンランド語     |韓国語     |セルビア語 (ラテン、セルビア)

## <a name="uninstall-ui-flows"></a>UI flows をアンインストールする

1. **[スタート]** メニューを開き、**[設定]** > **[アプリ]** を選択します。
1. **[UI フロー]** を検索して選択します。
1. **[アンインストール]** を選択します。

## <a name="learn-more"></a>詳細はこちら

- 以前のリリースから [UI フローをアップグレードする](upgrade.md)
- [デスクトップ UI フローの作成](create-desktop.md)について学習します。
- [Web UI フローの作成](create-web.md)について学習します。
- [UI フロー](run-ui-flow.md)の実行方法について学習します。
- [UI フローの管理](manage.md)について学習する。
- [オンプレミス ゲートウェイ](../gateway-reference.md#use-a-gateway)の詳細について学習する
