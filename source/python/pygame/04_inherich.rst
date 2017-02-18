
「俺はこれから本気出す」 - プレイヤー・キャラクター、動く。
--------------------------------------------------------------------------

さて、せっかく出した画像なので、動かしたいですよね。できれば自分の思ったとおりに。

もちろんゲームなので、キーボードに反応して動いてくれないとつまらないですね。
ということでここからはそれを作っていきます。

同じく ``game.py`` を以下のように書き換えましょう。

.. code-block:: python
 :linenos:

 import pygame, math
 from pygame.locals import *
 import sys

 SCR_RECT = Rect(0, 0, 800, 600) # スクリーンサイズ(px指定)

 # キャラクターのスプライト（クラス）を作る
 class CharacterSprite(pygame.sprite.Sprite):
     def __init__(self, filename, x, y, vx, vy):
         pygame.sprite.Sprite.__init__(self)
         self.image = pygame.image.load(filename).convert_alpha()
         width = self.image.get_width()
         height = self.image.get_height()
         self.rect = Rect(x, y, width, height)
         self.vx = vx
         self.vy = vy

     def update(self):
         # 画面からはみ出ないようにする
         self.rect = self.rect.clamp(SCR_RECT)
     def draw(self, screen):
         screen.blit(self.image, self.rect)

 # プレイヤーのスプライト（クラス）を作る
 class PCSprite(CharacterSprite):
     def move(self, press):
         if press[K_LEFT]:
             self.rect.move_ip(-self.vx, 0)
         if press[K_RIGHT]:
             self.rect.move_ip(self.vx, 0)
         if press[K_UP]:
             self.rect.move_ip(0, -self.vy)
         if press[K_DOWN]:
             self.rect.move_ip(0, self.vy)

 if __name__ == '__main__':
     pygame.init()
     screen = pygame.display.set_mode(SCR_RECT.size)
     pygame.display.set_caption("プチプチシューティング")

     # スプライト作成
     MyPC = PCSprite("pc_img.png", 400, 500, 100, 100)

     # 画面の更新時間を管理するオブジェクト
     fps = pygame.time.Clock()

     # ゲームイベントループ
     while True:
         screen.fill((0, 0, 0))
         fps.tick(60)

         # スプライト更新
         MyPC.update()

         # スプライトを描画
         MyPC.draw(screen)

         pygame.display.update() # 画面を更新

         # イベント処理
         for event in pygame.event.get():
             if event.type == QUIT: # 終了イベント
                 sys.exit()
             if event.type == KEYDOWN:
                 if event.key == K_ESCAPE:
                     sys.exit()
                 pressed_keys = pygame.key.get_pressed()
                 MyPC.move(pressed_keys)

はい！　ここでまどろっこしい書き方がさらにまどろっこしくなった様に見えるけど、
``PCSprite`` という新しいクラスを作りました。

| 「おや？　新しいクラスを作ったのなら、画像を表示するための処理を書かなくていいの？」
| って思ったNinja、鋭い。

| ``PCSprite`` の後ろに ``(CharacterSprite)`` と書いていますね。これは
| 「CharacterSpriteの機能をクローンします」
| という指示になります。これ、難しい言葉で言うと **継承（けいしょう）** って言います。

そして、イベント処理のところにキーボードの情報を受け取るようにして、更に ``PCSprite``　を
ベースに作った ``MyPC`` の ``move``　メソッドに、どのキーボードが押されているかを
送っています。　送られたキーボードの情報は、 ``MyPC`` の ``move`` は ``PCSprite`` の
``move`` と同じ動き（ただしデータは *MyPCが持っているデータ* ） をするので、キャラクターが動く
という仕組みです。

ちょっとむずかしかったかな。

.. attention::
    実はここまで書いておいて申し訳ないのですが、このコード、正しくないです。

    なんでそんなコードを書いたかというと、簡単なPythonのイントロダクションも兼ねて筆者がまっさらなところから書きました。

    またもうひとつ言い訳をしてしまうと、プログラミングというのは常に試行錯誤しながら作っていくものなので、
    一直線で完成に近づくものではないことは、もう優秀なNinja諸君ならわかっているとは思う。

    つまりこのコードも試行錯誤しながら書いては、資料としてまとめているのだ！

    ということで次の章からガラリとコードが変わるので、ご容赦ください。
