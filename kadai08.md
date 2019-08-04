# レポート課題８

表準画像「penguin.jpg」を使用する。

ORG=imread('penguin.jpg'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

上記で原画像を読み込み、白黒濃淡画像に変更して以下に示す。

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai8-1.png)

図１．白黒濃淡画像

次に、閾値128で二値化した図を以下に示す。

IMG = ORG > 128; % 閾値128で二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai8-2.png)

図２．閾値128で二値化した画像

二値化した画像にラベリングを行う。

IMG = bwlabeln(IMG);

imagesc(IMG); colormap(jet); colorbar; % 画像の表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai8-3.png)

図３．二値化画像をラベリングした画像



