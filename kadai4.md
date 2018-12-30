# 課題４レポート

標準画像「sample」を原画像とする．この画像は縦800画像，横643画素による長方形のディジタルカラー画像である．

ORG=imread('sample.png'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって、原画像を読み込み、２値画像として表示する。表示した結果を図１に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai4_1.png)  
図１ ２値化した原画像

２値化された原画像のヒストグラムを表示する。

imhist(ORG); % ヒストグラムの表示  

によって、原画像のヒストグラムを表示する。表示した結果を図２に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai4_2.png)  
図１ 原画像のヒストグラム
