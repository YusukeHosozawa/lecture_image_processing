# 課題６レポート

標準画像「sample」を原画像とする．この画像は縦800画像，横643画素による長方形のディジタルカラー画像である．

ORG=imread('sample.png'); % 原画像の入力
ORG = rgb2gray(ORG);
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって、原画像を読み込み、白黒濃淡画像として表示する。表示した結果を図１に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai6_1.png)  
図１ 原画像の白黒濃淡画像

白黒濃淡画像を閾値128で二値化する。

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって、閾値128の二値化画像ができる。表示した２値画像を図２で示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai6_2.png)  
図２ 閾値128での２値化画像

白黒濃淡画像をディザ法で二値化する。

IMG = dither(ORG); % ディザ法による二値化
imagesc(IMG); colormap(gray); colorbar; % 画像の表示

によって、二値化する。表示した２値画像を図３で示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai6_3.png)  
図３ ディザ法での２値化画像
