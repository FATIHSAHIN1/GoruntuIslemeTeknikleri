
Threshold Uygulamas�

Giri� olarak verilen g�r�nt�y� ikili g�r�nt�ye �evirmek i�in kullan�lan bir y�ntemdir.

�kili g�r�nt� (binary), g�r�nt�n�n siyah ve beyaz olarak tan�mlanmas�d�r.

Morfolojik operat�rler gibi g�r�nt� �zerindeki g�r�lt�leri azaltmak veya nesne belirlemek gibi farkl� ama�lar i�in kullan�l�r.

Giri� olarak verilen g�r�nt� �zerinde uygulanan thresholding tipine ba�l� olarak, pikselleri verilen e�ik de�erine g�re siyah ya da beyaz olarak g�nceller.

E�er piksel de�eri bir e�ik de�erden b�y�kse, bir de�ere (beyaz olabilir), ba�ka bir de�ere (siyah olabilir) atan�r.

Kullan�lan i�lev cv2.threshold'd�r.

�lk arg�man gri tonlamal� olmas� gereken kaynak g�r�nt�s�d�r.Yani uygulamaya ba�larken ilk yap�lan g�rseli gri tonlamal� g�r�nt�ye �evirmektir.

�kinci arg�man, piksel de�erlerini s�n�fland�rmak i�in kullan�lan e�ik de�eridir.

���nc� arg�man, piksel de�eri e�ik de�erden daha b�y�kse (bazen daha azsa) verilecek de�eri temsil eden maxVal'dir.

OpenCV farkl� e�ikleme stilleri sa�lar ve fonksiyonun d�rd�nc� parametresi taraf�ndan karar verilir. 