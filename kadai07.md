# レポート課題７

表準画像「penguin.jpg」を使用する。

ORG=imread('penguin.jpg'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

imhist(ORG); % 濃度ヒストグラムを生成、表示

上記で原画像を読み込み、白黒濃淡画像に変更したものと、濃度ヒストグラムを以下に示す。

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai7-1.png)

図１．白黒濃淡画像

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai7-2.png)

図２．濃度ヒストグラム

次に、画素のダイナミックレンジを0〜255に拡大する。

ORG = double(ORG);

mn = min(ORG(:)); % 濃度値の最小値を算出

mx = max(ORG(:)); % 濃度値の最大値を算出

ORG = (ORG-mn)/(mx-mn)*255;

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

ORG = uint8(ORG); % この行について考察せよ

imhist(ORG); % 濃度ヒストグラムを生成、表示


uint8は、変数を8ビットの符号なし整数に変換して格納する。今回はダイナミックレンジを拡大した時にORGを少数に変換し、そのままではヒストグラムを生成することができないのでuint8を使用した。

以下にダイナミックレンジを拡大した画像とその濃度ヒストグラムを示す。

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai7-3.png)

図３．ダイナミックレンジを拡大した白黒濃淡画像

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai7-4.png)

図４．ダイナミックレンジを拡大した濃度ヒストグラム

ダイナミックレンジの変更前後で違いが見られないが、これはカメラで撮影した時点でダイナミックレンジが0~255に対応していたためだと思われる。





