# レポート課題９

表準画像「penguin.jpg」を使用する。

ORG=imread('penguin.jpg'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

上記で原画像を読み込み、白黒濃淡画像に変更して以下に示す。

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai9-1.png)

図１．白黒濃淡画像

以下の処理でノイズを添付し表示する。

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai9-2.png)

図２．ノイズ添付画像

次に、平滑化フィルタでノイズを除去した画像を示す。

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai9-3.png)

図３．平滑化フィルタでノイズ除去した画像

次に、メディアンフィルタでノイズを除去した画像を示す。

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai9-4.png)

図４．メディアンフィルタでノイズ除去した画像

最後に、フィルタを設計しノイズを除去した画像を示す。

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計

IMG = filter2(f,IMG,'same'); % フィルタの適用

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai9-5.png)

図５．設計したフィルタでノイズ除去した画像





