# はじめに
これは自分がGANの理解をしたくて実装したときの記録です。
間違っているかもしれないのでご了承ください。

# コードの説明
データセットはCIFAR-10を使用しました。pytorchを用いました。
## gan.py
一般的なGANのコードを書きました。
## ls_gan.py
LSGANの実装をしました。
## c_gan.py
Conditional GANの実装をしました。

# 評価について
SWDという手法を用いて評価しました。swd.pyに書きました。
生成画像と本物画像の分布間の距離を測ります。
そのため、スコアが近いほどGANがうまく学習できています。
以下のように使います。
```
from swd import swd
swd(real, fake)
```