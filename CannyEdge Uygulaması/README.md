CannyEdge Uygulamas�

Canny kenar dedekt�r�, g�r�nt�lerdeki �ok �e�itli kenarlar� alg�lamak i�in �ok a�amal� bir algoritma kullanan bir kenar alg�lama operat�r�d�r.

Bu algoritma 5 a�amadan olu�ur.

1)G�r�lt� azaltma:G�r�nt�n�n arkas�nda yer alan matematik temelde t�revlere dayand���ndan, kenar alg�lama sonu�lar� g�r�nt� g�r�lt�s�ne kar�� olduk�a hassast�r.G�r�nt�deki g�r�lt�den kurtulman�n bir yolu, Gauss bulan�kl���n� p�r�zs�zle�tirmek i�in uygulamakt�r.

2)Gradyan hesaplamas�:Kenar alg�lama operat�rlerini kullan�p resmin gradyan�n� hesaplayarak kenar yo�unlu�unu ve y�n�n� alg�lar.Kenarlar, piksellerin yo�unlu�undaki de�i�ime kar��l�k gelir. Bunu tespit etmenin en kolay yolu, bu yo�unluk de�i�imini vurgulayan filtreleri her iki y�nde de uygulamakt�r.

3)Maksimum olmayan bast�rma i�lemi:�deal olarak, son g�r�nt�n�n ince kenarlar� olmal�d�r. Bu nedenle, kenarlar� inceltmek i�in maksimum olmayan bask�lama uygulamam�z gerekir.Prensip basittir: algoritma, gradyan yo�unluk matrisi �zerindeki t�m noktalardan ge�er ve kenar y�nlerinde maksimum de�eri olan pikselleri bulur.

4)�ift Threshold i�lemi:�ift e�ik ad�m�, 3 t�r pikselin belirlenmesini ama�lamaktad�r: g��l�, zay�f ve konuyla ilgili olmayan.G��l� pikseller yo�unlu�u o kadar y�ksek olan piksellerdir; son kenara katk�da bulunduklar�ndan eminiz.Zay�f pikseller, yo�unluk de�eri olarak kabul edilmek i�in yeterli olmayan, ancak kenar alg�lama i�in uygun olmad��� d���n�lebilecek kadar k���k olmayan bir yo�unluk de�erine sahip piksellerdir.Di�er pikseller kenar i�in uygun de�ildir.

5)Histeresiz ile Kenar Takibi:E�ik sonu�lar�na dayanarak, histerezis, zay�f pikselleri g��l� olanlara d�n��t�rmekten ibarettir.

Ben bu uygulamada ayn� �ekilde OpenCV k�t�phanesi yard�m�yla "cv2.Canny()"fonksiyonunu kullanarak al�nan canl� g�r�nt� �zerinde bir kenar belirleme uygulamas� yapt�m.