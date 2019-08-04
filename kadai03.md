# レポート課題３

標準画像「penguin.jpg」を使用する。

ORG=imread('penguin.jpg'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

上記により原画像を読み込み白黒濃淡画像に変更し、以下に示す。

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai3-1.png)

図１．白黒濃淡画像



次に、輝度値が64以上の画素を1，その他を0に変換したものを示す。

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai3-2.png)

図２．輝度値が64以上の画素を1，その他を0に変換



次に、輝度値が96以上の画素を1，その他を0に変換したものを示す。

IMG = ORG > 96; % 輝度値が96以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai3-3.png)

図３．輝度値が96以上の画素を1，その他を0に変換



次に、輝度値が128以上の画素を1，その他を0に変換したものを示す。

IMG = ORG > 128; % 輝度値が128以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai3-4.png)

図４．輝度値が128以上の画素を1，その他を0に変換



最後に、輝度値が192以上の画素を1，その他を0に変換したものを示す。

IMG = ORG > 192; % 輝度値が192以上の画素を1，その他を0に変換

imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai3-5.png)

図４．輝度値が192以上の画素を1，その他を0に変換


