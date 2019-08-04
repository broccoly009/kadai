# レポート課題１

画像「penguin」を原画像として使用する。

　ORG=imread('penguin.jpg'); % 原画像の入力
　imagesc(ORG); axis image; % 画像の表示

によって原画像を読み込み、表示した結果を図１に示す．
![原画像](https://github.com/broccoly009/kadai/blob/master/image/penguin.jpg)

図1　原画像


この画像を1/2サンプリングするには、1/2倍に縮小してから2倍に拡大すればよい。

　IMG = imresize(ORG,0.5); % 画像の縮小
　IMG2 = imresize(IMG,2,'box'); % 画像の拡大

以下に1/2サンプリングした画像を示す。

![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai1-1.png)

図2　1/2サンプリングの結果


以下1/4、1/8、1/16、1/32と間隔をあけてダウンサンプリングした結果を示す。

　IMG = imresize(ORG,0.5); % 画像の縮小
　IMG2 = imresize(IMG,4,'box'); % 画像の拡大
![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai1-2.png)

図3　1/4サンプリングの結果

　IMG = imresize(ORG,0.5); % 画像の縮小
　IMG2 = imresize(IMG,8,'box'); % 画像の拡大
![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai1-3.png)

図4　1/8サンプリングの結果

　IMG = imresize(ORG,0.5); % 画像の縮小
　IMG2 = imresize(IMG,16,'box'); % 画像の拡大
![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai1-4.png)

図5　1/16サンプリングの結果

　IMG = imresize(ORG,0.5); % 画像の縮小
　IMG2 = imresize(IMG,32,'box'); % 画像の拡大
![原画像](https://github.com/broccoly009/kadai/blob/master/image/kadai1-5.png)

図6　1/32サンプリングの結果


このように、サンプリング幅が大きくなると、モザイク状のサンプリング歪みが発生する。



