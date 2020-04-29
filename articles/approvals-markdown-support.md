---
title: Markdown を使用して Power Automate の承認を書式設定する | Microsoft Docs
description: Markdown を使用して Power Automate の承認要求を書式設定する方法を説明します。
services: ''
suite: flow
documentationcenter: na
author: gcorvera
manager: kfile
editor: ''
tags: ''
ms.service: flow
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 4/27/2020
ms.author: gcorvera
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 739d407df91661a6a82aa72f2891a3dac3bda3cf
ms.sourcegitcommit: 28adfdffc00c149bc46fab85b7307e4e819000c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2020
ms.locfileid: "82189613"
---
# <a name="use-markdown-in-power-automate-approval-requests"></a>Power Automate の承認要求で Markdown を使用する


この記事では、[Markdown](https://en.wikipedia.org/wiki/Markdown) 構文を使って、承認要求に豊富な書式設定を追加する方法について説明します。

> [!IMPORTANT]
> 承認要求電子メールは、*アクション可能メッセージ*です。 [Microsoft Outlook クライアント](https://docs.microsoft.com/outlook/actionable-messages/#outlook-version-requirements-for-actionable-messages)でアクション可能メッセージがサポートされない場合、承認要求は HTML 形式で表示されます。 

> [!IMPORTANT]
> すべての Markdown レンダラーの実装は異なります。 詳細については、「[クライアント サポート](#client-support)」のセクションを参照してください。

## <a name="client-support"></a>クライアント サポート

クライアント間の Markdown サポートに整合性がありません。 Power Automate チームはこれらの不整合に対処しますが、不整合は残ります。 次の表は、サポートされているクライアントの既知の制限を示しています。

| 特徴 | Power Automate | Power Automate モバイル アプリ | Outlook デスクトップ | Outlook Web | Teams | Teams モバイル アプリ |  
|---------|--------|---------------|-----------------|-------------|-------|--------------|
| **ヘッダー** | はい | はい | はい | はい | " **_いいえ_** " | " **_いいえ_** " |
| **番号付きリスト** | はい | はい | " **_いいえ_** " | はい | はい | はい |
| **入れ子になった番号付きリスト** | はい | はい | " **_いいえ_** " | はい | はい | はい |
| **テーブル** | はい | はい | はい | はい | " **_いいえ_** " | " **_いいえ_** " |
| **イメージ** | " **_いいえ_** " | " **_いいえ_** " | " **_いいえ_** " | " **_いいえ_** " | " **_いいえ_** " | " **_いいえ_** " |
| **強制改行** | はい | はい | " **_いいえ_** " (代わりに空白行を使用) | はい | はい | はい |
| **空白行** | " **_いいえ_** " | " **_いいえ_** " | はい | はい | " **_いいえ_** " | はい |

## <a name="headers"></a>ヘッダー

ヘッダーを使用してコメントに構造を与えます。 ヘッダーは長いコメントをセグメント化して、読みやすくします。

見出しを設定するには、行をハッシュ文字 `#` で始めます。 行の先頭のハッシュ文字を増やすと (例: `####`)、注釈を小見出しで整理できます。 最大 6 レベルの見出しがサポートされています。

**例:**  
```Markdown
# This is a H1 header
## This is a H2 header
### This is a H3 header
#### This is a H4 header
##### This is a H5 header
```

**結果:**  
![フローのエクスポート](./media/approvals-markdown-support/mrkdown-headers.png)

## <a name="paragraphs-and-line-breaks"></a>段落と改行

段落や改行で分割することにより、テキストを読みやすくします。 改行の前に 2 つの space を入力して、ほとんどのクライアントが新しい行から始まるようにします。  
   
**例:**  
```Markdown
This is line 1.(space, space)
Now text will appear on the next line.
```

**結果:**    
This is line 1.  
Now text will appear on the next line. 

**例 2**  
```Markdown
This is line 1.(space, space)  

Line 2 has extra space before it.
```

**結果:**  
This is line 1.  

Line 2 has extra space before it.
  

## <a name="lists"></a>リスト

関連する項目をリストで整理します。 番号付きの順序ありリスト、または行頭文字だけの順序なしリストを追加できます。

順序ありリストは、リスト項目ごとに数字とピリオドで開始します。 順序なしリストは、`*` で開始します。 各リスト項目は新しい行で開始します。 新しい段落を始めるには、Markdown ファイルまたはウィジェットで、改行の前に 2 つのスペースを入力するか、連続して 2 つの改行を入力します。   

### <a name="ordered-or-numbered-lists"></a>順序ありリストまたは番号付きリスト

**例:**  
```Markdown
0. First item.
0. Second item.
0. Third item.
```

**結果:**  
1. First item.
2. Second item.
3. Third item.

### <a name="bullet-lists"></a>箇条書きリスト

**例:**  
```Markdown
- Item 1
- Item 2
- Item 3
```

**結果:**  
- Item 1
- Item 2
- Item 3

### <a name="nested-lists"></a>入れ子になったリスト

**例:**  
```Markdown
1. First item.
   - Item 1
   - Item 2
   - Item 3
1. Second item.
   - Nested item 1
   - Nested item 2
   - Nested item 3
```

**結果:**  
1. First item.

    - Item 1
    - Item 2
    - Item 3
2. Second item.
    - Nested item 1
    - Nested item 2
    - Nested item 3


## <a name="links"></a>リンク

HTTP および HTTPS の URL は、リンクとして自動的に書式設定されます。 

標準の Markdown リンク構文を使って、URL のテキスト ハイパーリンクを設定できます。

```Markdown
[Link Text](Link URL)
```

**例:**  
```Markdown
[Power Automate](https://flow.microsoft.com)
```

**結果:**  
[Power Automate](https://flow.microsoft.com)

## <a name="tables"></a>テーブル

構造化されたデータをテーブルで整理します。 

- 各テーブル行を独自の行の配置します。 
- テーブルのセルはパイプ文字 `|` を使って区切ります 
- テーブルの最初の 2 行は、列の見出しと、テーブルの要素の配置を設定します
- テーブルの見出しと本文を分けるときにコロン (`:`) を使って列の配置 (左、中央、右) を指定します 
- 新しい行を開始するには、HTML 改行タグ (`<br/>`) を使用します
- 各行は必ず CR または LF で終了してください。 

**例:**  
```Markdown
| Heading 1 | Heading 2 | Heading 3 |  
|-----------|:-----------:|-----------:|  
| Cell A1 | Cell A2 | Cell A3 |  
| Cell B1 | Cell B2 | Cell B3<br/>second line of text |  
```

**結果:**  
| Heading 1 | Heading 2 | Heading 3 |  
|-----------|:---------:|-----------:|  
| Cell A1 | Cell A2 | Cell A3 |  
| Cell B1 | Cell B2 | Cell B3<br/>テキストの 2 行目 |  

 
## <a name="emphasis-bold-italics-strikethrough"></a>強調 (太字、斜体、取り消し線)  

文字に太字、斜体、または取り消し線を適用することで、テキストを強調できます。 
- 斜体を適用するには: テキストをアスタリスク `*` またはアンダースコア `_` で囲みます   
- 太字を適用するには: テキストを 2 つのアスタリスク `**` で囲みます。    
- 取り消し線を適用するには: テキストを 2 個のチルダ文字 `~~` で囲みます。   

これらの要素を組み合わせて、複数の強調をテキストに適用できます。    

**例:**  
```Markdown
Use _emphasis_ in comments to express **strong** opinions and point out ~~corrections~~ 
**_Bold, italicized text_**  
**~~Bold, strike-through text~~**
```

**結果:**  
コメントに_強調_を使用して**強力**な意見を表現し、<s>修正</s>を指摘します   
**_太字、斜体のテキスト_**    
**~~太字、取り消し線テキスト~~**  

## <a name="special-characters"></a>特殊文字

<table width="650px">
<tbody valign="top">
<tr>
<th width="300px">構文</th>
<th width="350px">例/注意</th>
</tr>



<tr>
<td>
<p>次のいずれかの文字を挿入するには、前に円記号を付けます。</p>

<p style="margin-bottom:2px;">```\   backslash ``` </p>
<p style="margin-bottom:2px;"><code>\`</code>   `backtick`</p>
<p style="margin-bottom:2px;">```_   underscore  ```</p>
<p style="margin-bottom:2px;">```{}  curly braces  ``` </p>
<p style="margin-bottom:2px;">```[]  square brackets ```</p>
<p style="margin-bottom:2px;">```()  parentheses  ```</p>
<p style="margin-bottom:2px;">```#   hash mark  ``` </p>
<p style="margin-bottom:2px;">```+   plus sign  ```</p>
<p style="margin-bottom:2px;">```-   minus sign (hyphen) ```</p>
<p style="margin-bottom:2px;">```.   dot  ``` </p>
<p style="margin-bottom:2px;">```!   exclamation mark ```</p>


</td>
<td>特殊文字挿入の例
<p>```\\``` と入力すると、\\ と表示されます </p>
<p>```\_``` と入力すると、_ と表示されます </p>
<p>```\#``` と入力すると、\# と表示されます </p>
<p>```\(``` と入力すると、\( と表示されます </p>
<p>```\.``` と入力すると、\. と表示されます </p>
<p>```\!``` と入力すると、\! と表示されます </p>
</td>
</tr>

</tbody>
</table>
