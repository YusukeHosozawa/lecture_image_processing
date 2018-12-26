# 課題２レポート

標準画像「sample」を原画像とする．この画像は縦800画像，横643画素による長方形のディジタルカラー画像である．

ORG=imread('sample.png'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

によって、原画像を読み込み、２値画像として表示する。表示した結果を図１に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai2_1.png)  
図１ ２値化した原画像

　原画像を２階調にするには原画像に１つの閾値を設け、その数値以上の数値は１(黒)、それ以下は0(白)としすることで表示することができる。原画像は256階調であるのでその半分の数値である128を閾値とする。
 
IMG = ORG>128;  
imagesc(IMG); colormap(gray);
colorbar; axis image;

２値化画像の結果を図２に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai2_2.png)  
図２ ２階調画像

　原画像を４階調にするには，階調数に閾値を３つ設けることで４つの濃度に分けることができる。最大の閾値は256×(3/4)=192、
中間の閾値は256×(2/4)=128、最小の閾値は256×(1/4)=64となる。すなわち、

IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
imagesc(IMG); colormap(gray); colorbar;  axis image;

とする。４階調画像の結果を図３に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai2_3.png)  
図３　４階調画像

　原画像を８階調にするには、階調数に閾値を７つ設けることで８つの濃度に分けることができる。閾値は上から256×(7/8)=224、
256×(6/8)=192、256×(5/8)=160、256×(4/8)=128、256×(3/8)=96、256×(2/8)=64、256×(1/8)=32となる。すなわち、

IMG0 = ORG>32;  
IMG1 = ORG>64;  
IMG2 = ORG>96;  
IMG3 = ORG>128;   
IMG4 = ORG>160;   
IMG5 = ORG>192;  
IMG6 = ORG>224;  
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;  
imagesc(IMG); colormap(gray); colorbar; axis image;

とする。８階調画像の結果を図４に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai2_4.png)
図４　８階調画像
