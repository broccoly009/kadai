# レポート課題１０

表準画像「penguin.jpg」を使用する。

ORG=imread('penguin.jpg'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

上記で原画像を読み込み、白黒濃淡画像に変更して以下に示す。

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai10-1.png)

図１．白黒濃淡画像

次に、プレウィット法でエッジを抽出する。

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai10-2.png)

図１．プレウィット法でエッジを抽出した画像

次に、ソベル法でエッジを抽出する。

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai10-3.png)

図１．ソベル法でエッジを抽出した画像

最後に、キャニー法でエッジを抽出する。

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai10-4.png)

図１．キャニー法でエッジを抽出した画像



