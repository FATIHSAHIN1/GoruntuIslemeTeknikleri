�zellik E�le�tirme(Homography)

�zellik e�leme, m�kemmel e�le�menin gerekli oldu�u �ablon e�le�tirmenin(template matching) biraz daha etkileyici bir s�r�m� olacak.

Bulmay� umdu�umuz resimle ba�l�yoruz ve sonra bu resmi ba�ka bir resim i�inde arayabiliyoruz. Buradaki fark yarat�c� k�s�m, g�r�nt�n�n ayn� ���kland�rma, a��, d�n�� vb. olmas� gerekmez. �zelliklerin sadece e�le�mesi gerekiyor.

Ba�lamak i�in baz� �rnek resimlere ihtiyac�m�z var. Bizim "�ablon" veya resmimizle e�le�meye �al��aca��z:

Burada, �ablon resmimiz, �ablonda arayaca��m�z resimden biraz daha k���k. Ayn� zamanda farkl� bir rotasyon ve baz� farkl� g�lgeler yok ama e�er bu �zelliklere sahip ba�ka g�rseller olursa daha iyi sonu�lar alabiliriz.

Bu uygulamada bir ""brute force" e�le�tirme �ekli kullanaca��z. Her iki resimdeki t�m �zellikleri bulaca��z. Sonra bu �zellikleri e�le�tiriyoruz. Daha sonra istedi�imiz kadar �ekip ��karabiliriz. Yine de dikkatli olmakta fayda var ��nk� 500 e�le�me s�ylersek, bir�ok yanl�� elde edebiliriz.

Burada e�le�tirme i�lemini "cv2.drawMatches()"fonksiyonunu kullanarak ger�ekle�tirdim.
