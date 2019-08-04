# 課題レポート４

表準画像「penguin.jpg」を使用する。

ORG=imread('penguin.jpg'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

上記で原画像を読み込み、白黒濃淡画像に変更して以下に示す。


![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai4-1.png)

図１．白黒濃淡画像


次に、画像のヒストグラムを表示する。

imhist(ORG); % ヒストグラムの表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai4-2.png)

図２．ヒストグラム





