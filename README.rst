=======================================
Python 官方說明文件臺灣繁體中文翻譯計畫
=======================================

本 GitHub repository 含有 Python 官方說明文件的 zh_TW 翻譯。實際的翻譯內容\
在這個 repository 裡以 Python 的穩定發行版本作為 branch 名稱，請參考 3.6 等
branch 以查看目前的翻譯內容。此 master branch 則為專案的貢獻說明。

您可以在 https://python-doc-tw.github.io/ 瀏覽目前翻譯的成果。目前以
Python 3.6 為翻譯的對象，**暫時不考慮 Python 2.7 的翻譯工作**。未來有新的
Python 發行版本時，也將會將翻譯滾動至新的版本。

想問問題、認識翻譯同好，歡迎加入 Telegram 聊天室 `t.me/PyDocTW`_

.. _t.me/PyDocTW: https://t.me/PyDocTW


授權與 License
==============

以下為 Documentation Contribution Agreement，說明文件貢獻協議，請在貢獻以前\
務必詳讀以下內容。原文後附有中文翻譯，但譯文不保證完全正確，請以原文為準。

Documentation Contribution Agreement
------------------------------------

NOTE REGARDING THE LICENSE FOR TRANSLATIONS: Python's documentation is
maintained using a global network of volunteers. By posting this
project on Transifex, Github, and other public places, and inviting
you to participate, we are proposing an agreement that you will
provide your improvements to Python's documentation or the translation
of Python's documentation for the PSF's use under the CC0 license
(available at
https://creativecommons.org/publicdomain/zero/1.0/legalcode). In
return, you may publicly claim credit for the portion of the
translation you contributed and if your translation is accepted by the
PSF, you may (but are not required to) submit a patch including an
appropriate annotation in the Misc/ACKS or TRANSLATORS file. Although
nothing in this Documentation Contribution Agreement obligates the PSF
to incorporate your textual contribution, your participation in the
Python community is welcomed and appreciated.

You signify acceptance of this agreement by submitting your work to
the PSF for inclusion in the documentation.

中文翻譯
~~~~~~~~

請注意此予翻譯專案的授權：Python 的說明文件是以全球的志工社群來維護。透過張貼\
此專案在 Transifex、GitHub 以及其他公眾場合，以及邀請您參與，我們向您提出一個\
協議：您必須將您對於 Python 說明文件或是 Python 說明文件翻譯的貢獻以 CC0\
（請參考 https://creativecommons.org/publicdomain/zero/1.0/legalcode）的方式\
授權給 PSF 使用。您可以公開地聲明您所貢獻翻譯的部分，並且如果您的翻譯被 PSF
採用，您可以（但並不須要）送出一個修改，其包含在 Misc/ACKS 或是 TRANSLATORS
檔案裡增加合適的注釋。雖然這個說明文件貢獻協議並沒有說明 PSF 有義務納入您的\
文本貢獻，您在 Python 社群的參與是受歡迎且受感激的。

您在對 PSF 送出說明文件貢獻的同時，即表示同意上述的協議。


參加翻譯
========

如何參加翻譯
------------

實際的翻譯即為修改 po 檔，流程遵照標準的 **GitHub Flow**，請 fork 此專案並在您\
自己的 fork 裡新增一個 branch，修改 po 檔內容並 commit、push 以後對此專案發出
pull request（記得 base 是此專案的其中一個 branch；目前只有 3.6），至少有一人\
審查過翻譯以後，才可以 merge 進入此 repository 中。

在對任何檔案進行貢獻之前，請先在本專案\ **新增一個 issue**，註明您正在翻譯的頁面\
名稱，並將該 issue **assign 給自己**，讓大家知道您正在修改該頁面，以避免多人\
同時貢獻同一個檔案的衝突。

編輯 po 檔的方式主要可以分為兩種，以 Transifex 作為工具或是使用其他翻譯工具：

1. 使用 Transifex 作為翻譯工具
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

您可以註冊 Transifex 帳號並加入我們的 `Transifex 專案
<https://www.transifex.com/python-tw-doc/python-36-tw>`_，並且在上面\
編輯您所要翻譯的頁面，並且在您本機上透過 command line 從此專案的 clone 的\
根目錄位置執行以下指令：

.. code-block:: bash

  $ ./txpull <po 檔的路徑>

此指令會需要 PyPI 上的 ``transifex-client`` 和 ``poindent``，|gettext|_、
``tac`` 等指令。這個小工具可以幫您把您在 Transifex 上針對特定檔案的翻譯 pull
下來，並且修正換行格式的錯誤。您在使用 txpull 以後就可以 commit 以及 push 了。

.. |gettext| replace:: ``gettext``
.. _gettext: https://www.gnu.org/software/gettext/

2. 使用其他翻譯工具
~~~~~~~~~~~~~~~~~~~

使用 Transifex 並非強迫性，您可以使用其他翻譯工具，如：

- 推薦：`poedit <https://www.poedit.net/>`_
- gted
- gtranslator
- lokalize
- betterpoeditor
- 適當模式底下的 vim 或 emacs
- Vé on Android
- 可能還有更多其他的

編輯完檔案以後，請執行以下指令以確保檔案的換行格式一致（需要安裝
|poindent|_）：

.. |poindent| replace:: ``poindent``
.. _poindent: https://pypi.org/project/poindent/

.. code-block:: bash

  $ poindent <po 檔的路徑>

執行完 ``poindent`` 以後即可 commit、push 等。


翻譯守則
--------

#. 譯文應兼顧前後文大意。

#. 中文句使用全形標點符號；英文句維持半形的標點符號。

   例如：「」（）、，。

   例如：Python is supported by Python Software Foundation (PSF).

#. 中英文交雜時要插入空白；符號英文間不用。

   例如：使用 CPU 運算、使用「CPU」運算

#. 專有名詞應該參考 Transifex 上 Glossary 裡對照表的翻譯方式。

#. 專有名詞可以選擇不翻譯。

   例如：CPU、Unicode

#. 在翻譯名稱不常用或不確定的情形，宜用括號註解或直接保留原文。單頁只要首次\
   出現有註解即可。

   例如：正規表示式 (regular expression)

   例如：Network News Transfer Protocol、Portable Network Graphics
   （可攜式網路圖形）

#. 務必保留 reStructuredText 格式（如：超連結名稱）

#. po 檔單行不應超過 79 字元寬度（可以使用 |poindent|_ 來確保格式）

#. 高頻詞保留原文。因為翻譯後不一定能較好理解市面上 Python 的文章。 這些高頻詞\
   在 Glossary 中的譯文仍保持原文，並加註市面上的翻譯。

   例如：``int``、``float``、``str``、``bytes``、``list``、``tuple``、
   ``dict``、``set``、``iterator``、``generator``、``iterable``


問題回報與討論
--------------

如果有需要共同討論的問題，請開設一個新的 Issue_。如果是翻譯上遇到困難需要\
幫助，則可以使用 Telegram_。

.. _Issue: https://github.com/python-doc-tw/python-docs-zh-tw/issues
.. _Telegram: https://t.me/PyDocT

另外，此翻譯的 coordinator 為 `adrianliaw <https://github.com/adrianliaw>`_，\
您也可以透過此 email 聯繫：``adrianliaw2000 at gmail dot com``。


額外翻譯資源
------------

- Telegram group `t.me/PyDocTW`_
- `Doc-SIG mailing list <https://mail.python.org/mailman/listinfo/doc-sig>`_
- `PEP 545 <https://www.python.org/dev/peps/pep-0545/>`_
- 我們的 `Transifex 專案 <https://www.transifex.com/python-tw-doc/>`_
- 我們在 Transifex 上的 `Glossary
  <https://www.transifex.com/python-tw-doc/python-36-tw/glossary/zh-Hant/>`_


維護、預覽
==========

以下的指令皆預設在本機端 ``python-docs-zh-tw`` clone 的根目錄執行，同時預設\
在同一個目錄底下有一個 CPython clone，如下：

::

  ~/
  ├── python-docs-zh-tw/
  └── cpython/

若要在本機端 clone 一個 CPython，可以使用以下指令：

.. code-block:: bash

  $ git clone --depth 1 --no-single-branch https://github.com/python/cpython.git

這樣可以避免下載完整的 commit 歷史（對輸出文件沒什麼幫助），但仍然能把所有的
branch clone 下來。

與 CPython 同步最新的 pot 檔
----------------------------

.. code-block:: bash

  $ make merge

本地端 build 文件
-----------------

.. code-block:: bash

  $ make

Acknowledgement
===============

This translation project is highly influenced by python-doc-ja_ and
python-doc-fr_'s translation architecture and workflow (i.e. a shameless
copy). We truly appreciate their contributions.

.. _python-doc-ja: https://github.com/python-doc-ja/python-doc-ja
.. _python-doc-fr: https://github.com/python/python-docs-fr
