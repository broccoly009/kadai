# レポート課題６

表準画像「penguin.jpg」を使用する。

ORG=imread('penguin.jpg'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

上記で原画像を読み込み、白黒濃淡画像に変更して以下に示す。

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai6-1.png)

図１．白黒濃淡画像

次に、256階調の白黒濃淡画像を128で二値化した場合の結果を示す。

IMG = ORG>128; % 128による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai6-2.png)

図２．128による二値化

次に、ディザ法によって二値化した場合の結果を示す。

IMG = dither(ORG); % ディザ法による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai6-3.png)

図３．ディザ法による二値化


同じ二値化でもディザ法では濃淡が表されているように見える。
