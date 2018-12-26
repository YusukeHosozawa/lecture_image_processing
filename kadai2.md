# 課題２レポート

標準画像「sample」を原画像とする．この画像は縦800画像，横643画素による長方形のディジタルカラー画像である．

ORG=imread('sample.png'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

によって、原画像を読み込み、２値画像として表示する。表示した結果を図１に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai2_1.png)  
図1 ２値化した原画像

　原画像を２階調にするには原画像に１つの閾値を設け、その数値以上の数値は１(黒)、それ以下は0(白)としすることで表示することができる。原画像は256階調であるのでその半分の数値である128を閾値とする。
 
IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

２値化画像の結果を図２に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai2_2.png)  
図2 ２階調画像

　原画像を４階調にするには，階調数に閾値を３つ設けることで４つの濃度に分けることができる。最大の閾値は256×(3/4)=192、
中間の閾値は256×(2/4)=128、最小の閾値は256×(1/4)=64

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;
