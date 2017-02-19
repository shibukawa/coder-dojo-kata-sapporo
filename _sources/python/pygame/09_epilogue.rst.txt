この次は？
======================

さて、これで君はPythonという言語でゲームを作れるようになった。このゲームを改造して爆発エフェクトを追加したり、
BGMや効果音をつけたり、あるいはレーザーを拡散させたって構わない。

更に言うと、全く別のゲームを作り始めても構わない。RPGでも構わないし、サウンドノベルでも全く問題ない。

もしできるのなら、2DのMinecraftのような、オープンワールドゲームを作ったって構わない。

もしもっと腕に自信があるのなら、 Panda3D_ で3Dのゲームに挑戦してもいいだろう。

.. _Panda3D: https://www.panda3d.org/

-------------------------------------------

Pythonが嫌だった？　なるほど、君はそういうNinjaなんだね。

であれば他のゲームエンジンを使ってみるのも一つだ。

例えば最近これを書いているメンターがハマった `Strange Telephone`_ というゲームは `LÖVE - Free 2D Game Engine`_
というゲームエンジンを使っているし、日本製でユニークなものとしては `Star Ruby`_ という Ruby_ 用のゲームエンジンもある。

最近は個人製作であれば（売り物を作るわけでなければ）無料で使える3Dゲームエンジンもある。
主に Unity_ や　`Unreal Engine`_ だが、完全無料でオープンソースという観点では、
Blender_ もある。（ただし現時点（2017年02月19日現在）では最新のレンダリングエンジンによるゲーム開発は
できない様子。）

もっとも、もっと腕に自信があるのなら、今だったらC++を学んでC++対応のゲームエンジンでゲームを作ると、
ハイパフォーマンスのゲームはできるかもしれないし、むしろ D_ や　Go_ や Rust_ それに Nim_ と言った
マイナー言語で1からゲームエンジンを作り、そしてゲームを作るのだって構わない。 SDL_ を叩いて色々できるものが
作れれば、それこそクロスプラットフォーム（Windows, macOS, Linux, iOS, Android)ゲームを作れる。

ああ、コンシューマー機（Nintendo Switch, PS4, XBOX ONE, etc...)だと、やはり選択肢は限られて、
Unity_ や `Unreal Engine`_ を使ったほうがいいだろう。

とあれこれ言ったが、やっぱりPythonはいい言語である。 Pythonの宣伝文句をもう少し唱っておくなら、
有名ドコロの3Dグラフィック編集ソフト（ Maya_ , Blender_ ）のスクリプト言語としても使えるし、
最近だとAIとかと一緒にされる深層学習や機械学習のライブラリも結構あるわけで、割と楽しい世界が広がってる
と、この記事を書いているメンターは思う。

Pythonは好きだがPygameが嫌？　まあ、この文章を読んでくれ。

`初心者のためのpygameガイド`_

.. _`Strange Telephone`: http://magniflop.com/st
.. _`LÖVE - Free 2D Game Engine`: https://love2d.org/
.. _`Star Ruby`: http://www.starruby.info/ja/
.. _Ruby: http://www.ruby-lang.org/ja/
.. _Unity: https://unity3d.com/jp/unity
.. _`Unreal Engine`: https://www.unrealengine.com/ja/what-is-unreal-engine-4
.. _Blender: https://www.blender.org/
.. _D: http://dlang.org/
.. _Go: https://golang.org/
.. _Rust: https://www.rust-lang.org/en-US/
.. _Nim: https://nim-lang.org/index.html
.. _SDL: https://www.libsdl.org/
.. _Maya: http://www.autodesk.co.jp/products/maya/overview
.. _`初心者のためのpygameガイド`: http://www.unixuser.org/~euske/doc/pygame/newbieguide-j.html

---------------------------------------------

ゲームに使う素材を作りたいのであれば、また今度お話しよう。

あとがき
======================

実はPythonでゲームを作ったのは今回が初めてです。
なので、最初のソースコードと最後に出来上がったソースコードが全く違うものになっていると思います。

でもそれでいいと思います。
そんな最初からいきなり綺麗なコードをかける人がいたら、それは設計者か神様です。

プログラミングは粘土遊びやスケッチに似ています。

意外かもしれませんが、書いては消してということを結構します。

自分の頭の中のイメージを実装するために、色んなことを調べて、そしてコードにしていく。

この楽しみを少しでも多くのNinjaに知っていただければ幸いです。
