Grabcut �n Plan ��karma

Buradaki ama� �n plan� bulmak ve arka plan� kald�rmakt�r.

Bu bir ye�il ekran�n yapt���n� yapaca��z.Sadece burada ye�il ekrana ihtiyac�m�z olmayacak.

�lk ba�ta cv2, numpy ve matplotlib'i i�e aktard�k.

Sonra g�r�nt�y� y�kl�yoruz, maske olu�turuyoruz, algoritman�n dahili olarak kulland��� arkaplan ve �n plan modelini belirtiyoruz.

As�l �nemli k�s�m tan�mlad���m�z do�rultudur. Bu rect = (start_x, start_y, width, height).Ana nesneyi �evreleyen dikd�rtgen budur.

Buradaki koordinatlar bu g�rsele ait.Farkl� g�rseller i�in farkl� g�rseller kullanmak gerekir.

Bu y�zden biz burada birka� parametre ald�k ve cv2.grabCut kulland�k.

�nce giri� g�r�nt�s�, ard�ndan maske, sonra ana nesnemiz i�in dikd�rtgen, arka plan modeli, �n plan modeli, �al��t�r�lacak yineleme miktar� ve hangi modu kulland���m�z� belirtiyoruz.