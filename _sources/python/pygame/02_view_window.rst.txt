
やってみよう
++++++++++++++++

では実際にゲームを作っていきましょう。

画面を表示する
------------------

.. code-block:: python
 :linenos:

 import pygame
 from pygame.locals import *
 import sys

 SCREEN_SIZE = (800, 600) # スクリーンサイズ(px指定)

 # Pygame初期化
 pygame.init()
 # SCREEN_SIZEの画面作成
 screen = pygame.display.set_mode(SCREEN_SIZE)
 # タイトルバーの文字列セット
 pygame.display.set_caption("プチプチシューティング")

 # ゲームイベントループ
 while True:
  screen.fill((0, 0, 255)) # 画面を真っ青で塗りつぶす。
  pygame.display.update() # 画面を更新
  # イベント処理
  for event in pygame.event.get():
      if event.type == QUIT: # 終了イベント
         sys.exit()

このコードを書いたら、名前を ``game.py`` として保存し、コマンドでファイルの保存したディレクトリまで移動して、
``python game.py`` と実行してみましょう。

.. image:: img/001.png
   :alt: 真っ青な実行結果。

この画面が出てきたら正解です。
しかし真っ青な画面は目が痛くなるので、真っ黒な画面にしましょう。

.. hint::
   + *fill* というのは「塗る」という意味です。
   + コンピューターでは基本的に、赤・緑・青の光の三原色で色を記録します。
   + 勇気のあるNinjaは、上のソースコードの以下の部分を消して実行してみよう！　しかし危険が伴うぞ！::
       for event in pygame.event.get():
           if event.type == QUIT: #終了イベント
               sys.exit()

.. danger::
   「ヒント」の一番最後は、プログラムを終了させなくする技なので、Mentorの皆様、および先輩Ninjaは
   強制終了の方法を伝えておくこと。

.. note::
   importってなんですか？
     ライブラリやモジュールというものを読み込んでいます。ライブラリというのは、簡単に言えば説明書です。
     説明書を渡して、いまあなたが触っているPythonという言語が、画面を表示したりする方法を会得しています。
     また、モジュールというのは、別のプログラムのことを言います。プログラムはバラバラに分解して作ることが
     できるんですよ。
