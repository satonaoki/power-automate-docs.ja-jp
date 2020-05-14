---
title: デスクトップ UI フローの作成方法を学習する | Microsoft Docs
description: Windows アプリケーション用のデスクトップ UI フローを作成する方法について説明します。
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
ms.date: 03/28/2020
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 3705d825a2b659e19975b6deeeae215bb1fad3d5
ms.sourcegitcommit: bba5bd4ae3879b6bf1521d8ed636374fe09709e7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3298860"
---
# <a name="create-and-test-desktop-ui-flows"></a>デスクトップ UI フローの作成とテスト

以下の手順では、電卓アプリを自動化して 2 つの数値を合計し、後で使用するために結果を格納する方法を説明します。

## <a name="create-a-desktop-ui-flow"></a>デスクトップ UI フローの作成

> [!TIP]
> 同様のパターンに従って他の Windows デスクトップ アプリを自動化できます。

1. UI フローを作成するために、[デバイスの準備ができている](setup.md#prerequisites)ことを確認します。

1. [Microsoft Edge  (バージョン 80 以降) ](https://www.microsoftedgeinsider.com) または Google Chrome を使用して [Power Automate](https://flow.microsoft.com) を開き、ご利用のデバイスと同じ職場、または学校のアカウントを使用してサイン インします。

1. **[マイ フロー]** > **[UI フロー]** > **[新規]** を選択します。

   ![新しい UI フローの作成](../media/create-windows-ui-flow/create-new.png "新しい UI フローの作成")

1. **[デスクトップ アプリ]** を選択し、**[次へ]** を選択します。

   ![デスクトップの選択](../media/create-windows-ui-flow/select-desktop.png "デスクトップの選択") 

1. **[フロー名]** フィールドに UI フローの名前を入力し、**[次へ]** を選択します。

   ![デスクトップの選択](../media/create-windows-ui-flow/give-a-name.png "デスクトップの選択") 

1. 下部にある **[次へ]** を選択して、オプションの **[入力の設定]** 画面をスキップします。このチュートリアルでは入力を使用しません。

1.  **パッケージのダウンロード**を選択します。
1.  **Setup.Microsoft.PowerAutomate.UIflow.exe** ファイルを開きます。 このファイルは、前の手順でダウンロードした後、**Downloads** フォルダーにあるはずです。
1.  UI フロー セットアップ インストーラーの指示に従い、インストールを完了させます。

    UI flows のインストーラーが完了すると、拡張機能のアクティブ化を求めるメッセージがブラウザーに表示されます。

1. Microsoft Edge (バージョン 80 以降) で、ブラウザーの右上にある各警告アイコンを選択し、**拡張機能の有効化** を選択します。
1. Google Chrome では、プロンプトが表示されたら、**[Enable extension]\(拡張機能の有効化\)** を選択します。

   > [!TIP]
   > ブラウザーにプロンプトが表示されない場合は、次のことを確認してください。
   > - Microsoft Edge (バージョン 80 以降) または Google Chrome ブラウザ を使用します。
   > - [Microsoft Edge (バージョン 80 以降)](https://www.microsoft.com/store/collections/edgeextensions/pc) または [Google Chrome](https://chrome.google.com/webstore/category/extensions) の拡張機能の更新が必要となる場合があります。

   拡張機能をインストールしたら、続行します。

1. **[アプリの記録]** カードを選択して展開します。

   ![[アプリの記録] の選択](../media/create-windows-ui-flow/select-record-app.png "[アプリの記録] の選択")

1. **[レコーダーの起動]** を選択します。

   ![[レコーダーの起動] の選択](../media/create-windows-ui-flow/select-launch-recorder.png "[レコーダーの起動] の選択")

   レコーダー コントロールが画面の上部に表示されます。

   ![レコーダー コントロール](../media/create-windows-ui-flow/recorder-control.png "レコーダー コントロール")

1. 電卓アプリを起動します。

     >[!TIP]
     >アプリのコントロールにマウスを置くと、各コントロールが青の枠線で強調表示されます。 コントロールを選択する前に、常に青の強調表示を待ちます。
     >
     >要素の周囲に青の強調表示が表示されない場合は、適切に記録されていない可能性があります。

1. レコーダー コントロールから **[記録]** を選択します。
1. 最初の数値を選択して **[+]** を選択し、2 つ目の数値を選択して **[=]** を選択します。

    ![電卓アプリ](../media/create-windows-ui-flow/app-to-record.png "電卓アプリ")
    
     > [!TIP] 
     > 自動化の信頼性を向上させるために、次の操作を行います。
     > - 記録を開始する "*前に*"、記録するアプリを開いて最大化します。
     > - アプリのタイトル バーをクリックし、タイトル バーにフォーカスが移動した状態で記録を開始します。

1. 記録する操作を完了したら、レコーダー コントロールで **[完了]** を選択します。

1. 記録したアプリを閉じます。

1. "<app name> スクリプトの実行" で始まるカードを選択すると、記録されたステップのスクリーンショットが表示されます。

     >[!TIP]
     >重複するステップを削除するには、**[...]** > **[削除]** を選択します。

    ![記録されたステップの表示](../media/create-windows-ui-flow/show-recorded-steps.png "記録されたステップの表示")

1. **次へ** を選択します。 

1. **[次へ]** を選択して、オプションの **[出力の設定]** のステップをスキップします。このチュートリアルでは出力を使用しません。

1. **[今すぐテスト]** ボタンを選択して UI フローをテストし、UI フローの実行を観察します。
    
 >[!IMPORTANT]
 >最適な結果を得るため、再生中はデバイスを操作しないでください。

1. **[保存して終了]** を選択して UI フローを保存します。


## <a name="known-issues-and-solutions"></a>既知の問題と解決策

- 現在、スクリーンショットは保存後に失われます。 修正に取り組んでいます。

- UI flows では各テストまたは実行のたびにアプリケーションの新しいインスタンスが起動されます。このため、UI フローの最後に [**[閉じる]** アクション](edit-desktop.md#add-a-manual-action)を追加することをお勧めします。

- 不要なアクションまたは重複するアクションを削除するには、記録されたアクションのカードで **[...]** > **[削除]** を選択します。

- 右クリックが正しく再生されない場合があります。 その場合は、記録中に左クリックによって対象のユーザー インターフェイス要素に UI flows のフォーカスを移動してから、右クリックします。

- 新しいバージョンのインストール後に、UI flows で Windows アプリケーションが記録または再生されなくなった場合は、[最新バージョン](https://go.microsoft.com/fwlink/?linkid=2102613&clcid=0x409)を使用していることをご確認ください。


### <a name="unsupported-application-types"></a>サポートされていないアプリケーションの種類

- Windows での対話 (エクスプローラー、スタートアップ メニュー、タスク バーなど)。

- Web ブラウザー (Chrome、IE、Microsoft Edge、Firefox、Mozilla など)。
    Web サイトを自動化するには、代わりに「[Web UI フローの作成](create-web.md)」を参照してください。

-   Java アプリケーション。

-   ClickOnce アプリケーション。

-   Web ビューを使用するアプリケーション (Electron アプリケーションなど)。

-   Microsoft Office 2016 およびそれ以前。 

-   Microsoft Office online。

### <a name="unsupported-configurations"></a>サポートされていない構成

-   マルチスクリーン。

-   仮想マシン クライアント (リモート デスクトップ、Citrix など) からの記録。

-   メイン ウィンドウのタイトルが同一である、アプリケーションの複数のインスタンス。

-   同じタイトルを持つアプリケーション ウィンドウ (たとえば、Microsoft Outlook  で同時にアクティブになっている **無題 – メッセージ (HTML)** という複数の新しいメール ウィンドウ)。

-   特定の 1 台のデバイスでの、複数の同時記録セッション。

-   特定の 1 台のデバイスでの、複数の同時再生セッション。 UI フローが同時に実行されている場合は、最初のフローが優先され、1 つ目のフローが完了しないうちは後続のフローは失敗します。

-   記録したデバイスとはキーボード レイアウトが異なるデバイスでの再生。

-   Microsoft Flow を使用しているブラウザーが別のデバイスまたは別の Windows セッションに存在する状態での、デバイスまたは Windows セッションを記録すること。

### <a name="unsupported-action-types-and-behaviors"></a>サポートされていないアクションの種類と動作

次のアクションは記録されません。

-   ダブルクリック。

-   マウスの移動。

-   マウスのホバー。

-   クリックしてドラッグ。

-   タッチ入力またはペン入力。

-   記録する前にアプリを開くこと。


## <a name="unreliable-behaviors-and-workarounds-for-microsoft-office-desktop"></a>Microsoft Office  (デスクトップ) の信頼性の低い動作と回避策

- 再生中、リボンが自動非表示に設定されている場合に発生する可能性のある問題を回避するには、再生を開始する前にリボンをピン留めします。
- クリックしてドラッグする方法で項目を選択しないでください。 たとえば、Shift キーを押しながらクリックして Microsoft Excel のセルを選択する、Microsoft Word または Microsoft PowerPoint でマウスをドラッグしてテキストを選択するなどの操作はしないでください。
- Microsoft Word および Microsoft PowerPoint デスクトップ アプリケーションでは、UI のフローで一部の要素が正しく機能しない場合があります。 たとえば、**ファイル** メニューのオプション ([空白から開始] など)、またはコントロールの右クリック (Microsoft Word での段落の追加や Microsoft PowerPoint でのスライドのレイアウト変更など) が機能しない場合があります。

## <a name="next-steps"></a>次のステップ

- 作成した [UI フローをトリガーする](run-ui-flow.md)方法について学習します。

- UI フローでさらに多くの操作を行う場合は、[入力と出力](inputs-outputs-web.md)パラメーターを使用して UI フローを作成することもできます。
