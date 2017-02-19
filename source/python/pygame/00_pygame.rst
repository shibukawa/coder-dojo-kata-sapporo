========================================================
Pythonでゲームを作りますが、何か of Python3
========================================================

目的
===============

簡単なシューティングゲームを作って、Pythonに馴染んてもらう。

.. note::
 元ネタは `Pythonでゲーム作りますが何か？ - 人工知能に関する断創録`_ です。

.. warning::
 この資料はPythonの基本文法をすっ飛ばしていますので、Pythonの基本文法に関しては、
 `Dive into Python3`_ もしくは `Pythonチュートリアル`_ （こちらのほうが詳しいです） をお読みいただけると幸いです。

 またこのKataではコマンド操作を必要としますので、最低限以下のコマンド操作を伝授させてください。

 + cd （ディレクトリ移動(Windowsでは引数なしの場合、現在ディレクトリのパス表示)）
 + dir （現在ディレクトリの内容を表示）
 + pwd （macOS, Linuxの場合の現在ディレクトリのパス表示）
 + ls （macOS, Linuxの場合の現在ディレクトリの内容を表示）

.. tip::
 伝授する際のコツは、書くキーワードがScratchなどの何に対応するのかを伝えながらだと、わかりやすいかもしれません。

.. _`Pythonでゲーム作りますが何か？ - 人工知能に関する断創録`: http://aidiary.hatenablog.com/entry/20080507/1269694935
.. _`Dive into Python3`: http://diveintopython3-ja.rdy.jp/
.. _`Pythonチュートリアル`: http://docs.python.jp/3/tutorial/

用意するもの
=============

+ Python3 (Windows, Mac, Linux)
+ Pygame
+ Pythonのソースコードが編集できるエディタ（Atom推奨。PyCharmでも可）
+ （できれば）ゲームに使う画像・音楽素材。

カリキュラム（？）
========================

.. toctree::
    :maxdepth: 1
    :caption: 目次

    01_environment
    02_view_window
    03_make_sprite
    04_inherich
    05_move_enemy
    06_razor.rst
    07_game_status
    08_file_separate
    09_epilogue
