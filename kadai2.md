# 課題２レポート

標準画像「sample」を原画像とする．この画像は縦800画像，横643画素による長方形のディジタルカラー画像である．

ORG=imread('sample.png'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

によって、原画像を読み込み、２値画像として表示する。表示した結果を図１に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai2_1.png)  
図1 ２値化した原画像

　原画像を２値化するには原画像に１つの閾値を設け、その数値以上の数値は１(黒)、それ以下は0(白)としすることで表示することができる。原画像は256階調であるのでその半分の数値である128を閾値とする。
 
IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

２値化画像の結果を図２に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai2_2.png)  
図2 ２値化画像
