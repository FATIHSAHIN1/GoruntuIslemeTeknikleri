Template Matching Uygulamas�

Buradaki fikir, sa�lad���m�z �ablonla e�le�en ve belirli bir e�ik de�eri veren bir g�r�nt�n�n ayn� b�lgelerini bulmakt�r.

Kesin nesne e�le�meleri i�in, tam ayd�nlatma / �l�ek / a�� ile, bu sistem daha verimli �al��abilir. 

Bu ko�ullar�n genellikle kar��land��� bir �rnek, bilgisayardaki herhangi bir GUI ile ilgilidir. D��meler ve benzeri ��eler her zaman ayn�d�r, b�ylece �ablon e�le�tirmesini kullanabiliriz.

Ba�lamak i�in bir ana g�r�nt�ye ve bir �ablona ihtiyac�m�z olacak. �ablonunuzu, g�r�nt�de tam olarak arad���n�z "�ey" den almal�y�z.

Ben bu uygulamada ayn� giri�lere sahip bir PC g�rseli ald�m.

Burada �nemli olan e�le�tirmek istedi�imiz nesnenin �ablonda birden fazla ve ayn� �ekilde yer almas�.

Ben bu uygulamada OpenCV'nin "cv2.matchTemplate()" fonksiyonunu kullanarak e�le�tirme yapt�m.

Burada Threshold de�erini de�i�tirerek e�le�me do�rulu�unu kontrol edebiliriz.