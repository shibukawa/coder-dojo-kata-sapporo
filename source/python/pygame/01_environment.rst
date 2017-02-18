環境構築
++++++++++++

Python3
------------

1. Python自体をインストールします。

  Windows Mac

    公式サイトから適切なインストーラーをダウンロード。

  Linux(Ubuntu 16.04)

    以下コマンド実行。::

      sudo pip3 install pygame

  もし何か問題があればエラーメッセージを見て解決してください。大抵「pip3が入っていない」、
  「管理者権限で動かしていないためインストールできない」などが多いです。

2. コマンドプロンプト・もしくはターミナルで以下を実行してください。 ``Python 3.x.y`` と表示されたら成功です。::

    python -V
    python3 -V


Atom
-----------

1. Atom_ 本体をダウンロードします。

.. _Atom: https://atom.io/

2. Atomのインストールが終わったら、Atomで以下のパッケージをダウンロード・インストールします。
   好みで他のパッケージを入れたり、逆に抜いたりしてください。

 + japanese-menu
 + file-icons
 + atom-beautify
 + tabs-to-spaces
 + highlight-selected
 + term3（できれば）
 + autocomplete-paths
 + autocomplete-python
 + symbols-tree-view

PyCharm Community Edition(任意)
---------------------------------------

もっと高性能なエディタ（IDE）が良いということであれば、 PyCharm_ をおすすめします。
しかし、UIが英語限定です。

.. _PyCharm: http://www.jetbrains.com/pycharm/

気をつけていただきたいのが、 *Professional Edition*　は有料のため、 *Community Edition* を
選択してください。
