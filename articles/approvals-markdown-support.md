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
ms.date: 4/23/2018
ms.author: gcorvera
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 4633df9687662c49757dd9cbb4d1d88892dfbe51
ms.sourcegitcommit: 84fb0547e79567efa19d7c16857176f7f1b53934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "79193636"
---
# <a name="use-markdown-in-power-automate-approval-requests"></a>Power Automate の承認要求で Markdown を使用する


この記事では、[Markdown](https://en.wikipedia.org/wiki/Markdown) 構文を使って、承認要求に豊富な書式設定を追加する方法について説明します。

> [!IMPORTANT]
> 承認要求電子メールは、*アクション可能メッセージ*です。 [Microsoft Outlook クライアント](https://docs.microsoft.com/outlook/actionable-messages/#outlook-version-requirements-for-actionable-messages)でアクション可能メッセージがサポートされない場合、承認要求は HTML 形式で表示されます。 

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

段落や改行で分割することにより、テキストを読みやすくします。 新しい段落を始めるには、改行の前に 2 つのスペースを入力するか、連続して 2 つの改行を入力します。   
   
**例**

Enter キーを使ってテキスト間に行を追加します。
これによってテキストにより適切な間隔が空き、読みやすくなります。

**結果:**    
Enter キーを使ってテキスト間に行を追加します。      
これによってテキストにより適切な間隔が空き、読みやすくなります。


**例 2**

行の末尾の前にスペースを 2 つ追加します。(スペース、スペース)     
これによって段落間に空白が追加されます。

**結果:**  
行の末尾の前にスペースを 2 つ追加します。   

これによって段落間に空白が追加されます。
  

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

<pre>

- Item 1
- Item 2
- Item 3

</pre>

**結果:**

- Item 1
- Item 2
- Item 3

### <a name="nested-lists"></a>入れ子になったリスト

**例:**
<pre>

1. First item.
   - Item 1
   - Item 2
   - Item 3
1. Second item.
   - Nested item 1
   - Nested item 2
   - Nested item 3

</pre>

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
<pre>
&#91;Power Automate](https://flow.microsoft.com)
</pre>

**結果:**

[Power Automate](https://flow.microsoft.com)

### <a name="anchor-links"></a>アンカー リンク

HTML としてレンダリングされるときは、すべての見出しにアンカー ID が割り当てられます。 ID は見出しテキストであり、スペースはダッシュ (-) に置き換えられ、すべてが小文字になります。

**例:**

<pre>
###Link to a heading in the page
</pre>

<br/>

**結果:**

セクションに対するアンカー リンクの構文。

<pre>
[Link to a heading in the page](#link-to-a-heading-in-the-page)
</pre> 
<br/>
ID はすべて小文字であり、リンクは大文字と小文字が区別されるため、見出し自体では大文字が使用されていても、必ず小文字のみを使います。


## <a name="tables"></a>テーブル

構造化されたデータをテーブルで整理します。 

- 各テーブル行を独自の行の配置します。 
- テーブルのセルはパイプ文字 `|` を使って区切ります 
- テーブルの最初の 2 行は、列の見出しと、テーブルの要素の配置を設定します
- テーブルの見出しと本文を分けるときにコロン (`:`) を使って列の配置 (左、中央、右) を指定します 
- 新しい行を開始するには、HTML の改行タグ (`<br/>`) を使用します (Wiki 内では機能しますが、他の場所では機能しません)  
- 各行は必ず CR または LF で終了してください。 

**例:**

```
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

<pre>
Use _emphasis_ in comments to express **strong** opinions and point out ~~corrections~~ 
**_Bold, italicized text_**  
**~~Bold, strike-through text~~**
</pre>

<br/>

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
