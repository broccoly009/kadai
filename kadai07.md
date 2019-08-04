# レポート課題７

表準画像「penguin.jpg」を使用する。

ORG=imread('penguin.jpg'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

imhist(ORG); % 濃度ヒストグラムを生成、表示

上記で原画像を読み込み、白黒濃淡画像に変更したものと、濃度ヒストグラムを以下に示す。












