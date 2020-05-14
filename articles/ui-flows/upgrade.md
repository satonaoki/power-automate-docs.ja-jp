---
title: 以前のリリースから UI フロー アプリと接続を更新する |Microsoft Docs
description: 以前のリリースから UI フロー アプリと接続を更新します。
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
ms.date: 03/03/2020
ms.author: DeonHe
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: b73c550eb22948ea3c0e9ac14adf15674869da61
ms.sourcegitcommit: bba5bd4ae3879b6bf1521d8ed636374fe09709e7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3298684"
---
# <a name="upgrade-ui-flows-app-and-connections-from-previous-releases"></a>以前のリリースから UI フロー アプリと接続をアップグレードする

無人サポートにより、2 月のリリースでいくつかの基になるコンポーネントを変更し、いくつかの機能を追加しました。 これらの新機能 (無人機能を含む) を使用するには、ローカル UI フロー アプリとゲートウェイ接続を更新する必要があります。

### <a name="what-does-it-mean-for-my-existing-ui-flows"></a>既存の UI フローはどうなりますか。

UI フロー アプリまたはゲートウェイへの接続を更新するまでは、何もする必要はありません。 同時に両方を更新する必要があります。

### <a name="how-do-i-upgrade"></a>アップグレードするには?

1.  [最新の UI フロー アプリ](https://go.microsoft.com/fwlink/?linkid=2102613&clcid=0x409)をダウンロードし、デバイスにインストールします。

1.  UI フロー アプリがインストールされているデバイスごとに、次の手順に従います。

    1. [Power Automate](https://powerautomate.microsoft.com) にサインインする。
    1. 画面の左側にある **[データ]** を展開します。
    1. **[接続]** を選択します。
    1. デバイスをターゲットとする UI フロー接続を編集します。
    1. 接続の資格情報を入力し、保存します。

    >[!IMPORTANT]
    >「[UI フローの接続とマシンの資格情報をセットアップする](setup.md#setup-ui-flows-connections-and-machine-credentials)」で説明しているように、適切な資格情報を使用するようにしてください。 正しい資格情報を使用すると、確実に接続が更新され、一般公開されている UI フローに対してコード パスが使用されるようになります。

## <a name="next-steps"></a>次のステップ

- [UI フローの設定](setup.md)方法について学習します。 
- ワークフローを自動化するために使用できる[さまざまな種類のフロー](..\getting-started.md#types-of-flows)の詳細について学習する。


