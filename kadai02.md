# レポート課題２

標準画像「penguin.jpg」を使用する。

ORG=imread('penguin.jpg'); % 原画像の入力

ORG = rgb2gray(ORG); colormap(gray); colorbar;

imagesc(ORG); axis image; % 画像の表示


上記により原画像を読み込み白黒濃淡画像に変更する。結果を以下に示す。

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai2-1.png)

図１．白黒濃淡画像


次に、２階調にする処理を行う。白黒濃淡画像の0-255の256階調をを２つに分ける。

IMG = ORG>128;

imagesc(IMG); colormap(gray); colorbar; axis image;


![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai2-2.png)

図２．２階調処理画像


次に、４階調にする処理を行う。同じように0-255を４つに分ける。

IMG0 = ORG>64;

IMG1 = ORG>128;

IMG2 = ORG>192;

IMG = IMG0 + IMG1 + IMG2;

imagesc(IMG); colormap(gray); colorbar; axis image;

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai2-3.png)

図３．４階調処理画像


最後に、８階調にする処理を行う。同じように0-255を８つに分ける。

IMG0 = ORG>32;

IMG1 = ORG>64;

IMG2 = ORG>96;

IMG3 = ORG>128;

IMG4 = ORG>160;

IMG5 = ORG>192;

IMG6 = ORG>224;

IMG7 = ORG>256;

IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6 + IMG7;

imagesc(IMG); colormap(gray); colorbar; axis image;

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai2-4.png)

図４．８階調処理画像


