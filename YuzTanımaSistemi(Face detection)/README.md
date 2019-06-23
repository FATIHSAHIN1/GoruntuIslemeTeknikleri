Y�z Tan�ma Sistemi(Face detection)

Haar �zellik tabanl� kaskad s�n�fland�r�c�lar�n� kullanarak Nesne Tespiti, Paul Viola ve Michael Jones taraf�ndan 2001 y�l�nda "Basit �zellikler Kaskad�n� Kullanarak H�zl� Nesne Tespiti" ba�l�kl� makalesinde �nerilen etkili bir nesne alg�lama y�ntemidir.

Kaskad i�levi, bir�ok olumlu ve olumsuz g�r�nt�den e�itilmi�tir. Daha sonra di�er resimlerdeki nesneleri tespit etmek i�in kullan�l�r.

Burada y�z tan�ma ile �al��t�m.

OpenCV dedekt�r�n yan� s�ra bir e�itmen ile birlikte gelir. Kendi s�n�fland�r�c�m�z�, araba, u�ak vb. Herhangi bir nesne i�in e�itmek istiyorsak, bir tane olu�turmak i�in OpenCV kullanabiliriz.

Burada alg�lama ile ilgilenece�iz. OpenCV zaten y�z, g�zler, g�l�msemeler vb. ��in �nceden e�itilmi� s�n�fland�r�c�lar� i�erir. Bu XML dosyalar� opencv / data / haarcascades / klas�r�nde depolan�r. OpenCV ile bir y�z ve g�z dedekt�r� olu�turdum.

�ncelikle gerekli XML s�n�fland�r�c�lar�n� y�klememiz gerekiyor. Ard�ndan giri� resmimizi (veya videomuzu) gri tonlamal� modda y�kledim.

Sonras�nda g�r�nt�deki y�zleri buluyoruz. Y�zler bulunursa, alg�lanan y�zlerin pozisyonlar�n� Rect (x, y, w, h) olarak d�nd�r�r. Bu konumlara ula�t�ktan sonra, y�z i�in bir ROI olu�turabilir ve bu ROI'ye g�z alg�lama uygulayabiliriz.

Burada yap�lan uygulamada �nceden kaydedilmi� bir g�r�nt� kullan�lmad�.Webcam kullanarak anl�k y�z ve g�z tan�ma i�lemi yap�ld�.Dolay�s�yla hassasiyeti belirleyen �ok fazla parametre var.Bunu da dikkate almak gerekir.
