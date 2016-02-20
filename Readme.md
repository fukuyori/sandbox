SIFT – Multi-functional copy tool
====
ー　気の利いたコピーツール。ディスクの整理にも使えます。ー

OVERVIEW
------
If when you have to look for a file from deep in the hierarchy structure directory, please try to use this tool. Or, also useful when you must be singled out what is in Excel table from among the large number of files. In addition, even if you want to change all at once a large number of file names, you will have this tool will help.

This tool is, by incorporating the **SQLite** library, you have to handle a large number of files. By combining the capabilities of this tool, you can organize the disk drive in your PC and the cloud strage. Also it is possible to organize efficiently a large number of files that are stored in the large-capacity servers that are used in the business.

もしあなたが階層構造の深いディレクトリの中からファイルを探さなければならない時、このツールを使用してみてください。あるいは、大量のファイルの中からメモ帳やエクセルに記載されたファイルを選び出さなければならない時にも役に立ちます。更に、大量のファイル名を一括して変更したい場合にも、このツールが助けになるでしょう。

このツールは、**SQLite**を組み込むことで、大量のファイルを扱えるようにしています。200,000件程度までの動作確認をしています。このツールの機能を組み合わせて、ＰＣのディスクや、クラウドのディスクの整理、業務で使用している大容量サーバーに保存された大量のファイルを効率よく整理することもできます。

INSTALL
------
+ Download Latest stable version: release page.
+ Unzip it and put it into your user directory.
+ Run installer program.
+ To run, you need installation of the .NET Framework 4.0.
+ 実行には .NET Framework 4.0 のインストールが必要です。

HOW TO USE
------
####1. コピー元、コピー先、コピー方法の設定
(The setting of copy source, destination and copying method)

上部は、コピー元ファイルの場所とコピー先を選択するテキストボックスとフォルダ選択のボタンがあります。その右には、コピー開始ボタンです。コピーを開始するには、コピー元、コピー先が指定され、コピー元、コピー先が同一でない場合、開始されます。
その下には、ファイルを表示する方法として、サブフォルダまで含めるか選択することができます。また、コピー元のフォルダ構造を維持してコピーするか、フォルダ構造を無視して全てコピー先に一律コピーするか選択できます。上書きにチェックがない場合は、コピー先に同名のファイルがあると、ファイル名の後に「(1)」のように番号を付けてコピーが行われます。上書きにチェックが入っていると、同名のファイルは後続のコピー作業で上書きされてしまいます。その場合、ファイルの日付をチェックし、ファイルがより新しいものであればコピーするよう選択もできます。

####2. ファイル名表示、選択モード
(File name display , selection mode)

Siftの下部には３つのモードがあります。それぞれ、画面中の青黄赤色のバーの左右に遷移のためのボタンが用意されています。
The bottom has three modes. Respectively, the buttons for the transition to the left and right of the blue yellow-red in the screen bar are available.

１番目は、ファイルの表示・選択のための画面で、青色のバーが表示されています。
コピー元で選択されたフォルダにあるファイルが表示されます。ファイル名のチェックボックスにチェックを入れてコピーを開始することができます。検索のテキストボックスを使用して、検索に一致したファイルをまとめてチェックすることもできます。
検索には、ワイルドカードが使用でき、「%」は任意の数の文字、「_」は任意の一文字と一致します。検索対象は、一覧に表示されている、サブフォルダも含めたファイル名となりますので、サブフォルダ内のファイルを検索する場合は、頭に「%」を付けて検索してください。

    Example:
    
        %FileName.doc
        %FileName%
        %FileNam_.doc

また、「－」ボタンで検索対象を除外することもできますので、「%.xls」でエクセルファイルを選択した後、「%コピー%」と入力して「－」ボタンを押すと、ファイル名に「コピー」を含むファイルを除外することができます。

ファイル名を指定して、「M」キーでチェックを入れ、「U」キーでチェックを外し、「O」キーでファイルを開き、「I」キーでフォルダを開くことができます。

####3. コピー対象ファイル名ペーストモード 
(The target file name paste mode)

２番の画面は、ファイル名をここにペーストしてファイルを選択することができます。例えば、コピーしたいファイル名がエクセルで渡された場合、エクセルのセルをコピーし、ここにペーストすることで検索が開始されます。検索文字は、前後にワイルドカード「%」が付与されますので、拡張子を含んでいなくても検索できます。複数のファイル名と一致する場合は、すべて選択されます。
ファイル名一覧画面で、全選択＆コピー（Ctrl+A ,Ctrl+C）し、エクセルファイルに張り付けた後、エクセル上で操作して必要なファイルを選び出し、この画面に張り付けてコピーを行うなどといったこともできます。

####4. コピー先ファイル名変更モード
(The destination file name change mode)

３番目の画面では、コピー先のファイル名を変更することができます。表示されたファイル名を１つ１つ変更することもできますが、「変換形式」のテキストボックスに変換ルールを入力して、一括変換することもできます。
　変換ルールの書式は、「`<`」と「`>`」で囲まれた記号を使って作成します。
　元のファイル名は、記号、数字で分割され「`<1>`」のように数字を「`<>`」で囲った記号に置き換えられます。また、「`<0>`」は元のファイル名全体、「`<f>`」は拡張子を除くファイル名、「`<e>`」は拡張子部分を示しています。更に、「`<n>`」は、一覧に表示されたファイルに、１から順番に番号を振ってくれます。表示されたファイル名がどのように記号で表現されるかは、ファイル名を右クリックし、「パターン表示」を選択すると表示されます。

    Example:
    
        元のファイル名	file0123_456.doc は、以下のようになります。
        <0> = file0123_456.doc
        <1> = file
        <2> = 0123
        <3> = 456
        <4> = doc
        <f> = file0123_456
        <e> = .doc

        変換ルール 「NewName_<2><3><e>」を適用すると、「NewName_0123456.doc」と変換されます。

####5. 履歴数、検索ファイル数の設定
(Number of history, and number of searches files)

選択されたコピー元、コピー先は、履歴に保存されます。次回からは、この履歴から選択することができますが、この履歴の保存数を変更できます。上部メニューの「ファイル」→「設定」を選んで、設定画面から入力してください。
また、この設定画面の「検索数」は、コピー元で表示するファイルの数を設定します。検索したファイル数がこの数を超えた場合、検索を中止するか継続するかの選択ができます。ファイル数のチェックは、１フォルダ単位で行っています。１つのフォルダの中に大量のファイルがある場合は、それを全て検索した後で選択画面が表示されますので、設定したファイル数を大幅に超えてしまうことがあります。

####6. FastCopyの使用
(Use FastCopy)

コピー処理に「FastCopy高速コピー＆削除」を使用することもできます。白水啓章さんのホームページからFastCopyをダウンロードし、インストールしてください。(http://ipmsg.org/tools/fastcopy.html)

使用するには、　「ファイル」→「設定」から「使用しない」をクリックしてください。FastCopyが通常のProgram FilesあるいはProgram Files (x86)にインストールされていれば、使用可能になります。

複数のサブフォルダーのファイルを、ディレクトリ構造のままコピーする場合、FastCopyがフォルダ単位の処理となり、その度に起動されます。そのため、起動のオーバーヘッドが大きくなり、通常のコピーより遅くなってしまいます。ネット上の大きなファイルをコピーする時以外は、「使用（ディレクトリ構造無視のみ）」に設定しておくのがいいでしょう。

AUTHOR
------
self@spumoni.org

REPORTING BUGS
------
Report to self@spumoni.org

COPYRIGHT 
------
The MIT License (MIT)

Copyright (c) 2016 SPUMONI.ORG

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

以下に定める条件に従い、本ソフトウェアおよび関連文書のファイル（以下「ソフトウェア」）の複製を取得するすべての人に対し、ソフトウェアを無制限に扱うことを無償で許可します。これには、ソフトウェアの複製を使用、複写、変更、結合、掲載、頒布、サブライセンス、および/または販売する権利、およびソフトウェアを提供する相手に同じことを許可する権利も無制限に含まれます。

上記の著作権表示および本許諾表示を、ソフトウェアのすべての複製または重要な部分に記載するものとします。

ソフトウェアは「現状のまま」で、明示であるか暗黙であるかを問わず、何らの保証もなく提供されます。ここでいう保証とは、商品性、特定の目的への適合性、および権利非侵害についての保証も含みますが、それに限定されるものではありません。 作者または著作権者は、契約行為、不法行為、またはそれ以外であろうと、ソフトウェアに起因または関連し、あるいはソフトウェアの使用またはその他の扱いによって生じる一切の請求、損害、その他の義務について何らの責任も負わないものとします。 

----
####SQLite

SQLite is public domain. <https://www.sqlite.org/copyright.html>


