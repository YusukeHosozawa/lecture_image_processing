# 課題３レポート

標準課題「sample」を原画像とする。この画像は縦800画像，横643画素による長方形のディジタルカラー画像である．

ORG=imread('sample.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって、原画像を読み込み、白黒濃淡画像として表示する。表示した結果を図１に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai3_1.png)  
図１ 原画像の白黒濃淡画像

原画像の輝度値が64以上の画素を１、それ以外の画素を０に変換する。
 
IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;

変換した画像の結果を図２に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai3_2.png)  
図２ 輝度値変換画像１

原画像の輝度値が96以上の画素を１、それ以外の画素を０に変換する。
 
IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;

変換した画像の結果を図３に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai3_3.png)  
図３ 輝度値変換画像２

原画像の輝度値が128以上の画素を１、それ以外の画素を０に変換する。

IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  

変換した画像の結果を図４に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai3_4.png)  
図４ 輝度値変換画像３

原画像の輝度値が192以上の画素を１、それ以外の画素を０に変換する。

IMG = ORG > 192;
imagesc(IMG); colormap(gray); colorbar;

変換した画像の結果を図５に示す。

![原画像](https://github.com/YusukeHosozawa/lecture_image_processing/blob/master/image/kadai3_5.png)  
図５ 輝度値変換画像４
