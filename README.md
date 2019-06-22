# GoruntuIslemeTeknikleri
OpenCV kullanarak Python üzerinde Temel Görüntü işleme Tekniklerinin Uygulanması

1-Görüntü üzerinde MOG filtresinin uygulanması

Gaussianların Karışımı( Mixture of Gaussians=MOG), statik kameralardan hareketli cisimleri saptamak için arkaplan modellemesi için yaygın olarak kullanılan bir yaklaşımdır.

Ben de OpenCV destekli "createBackgroundSubtractorMOG2()"fonksiyonuyla alınan bir görüntü üzerindeki hareketli nesneleri tespit etmek için kullanılan filtreleme işlemini yaptım.

NOT:Eğer alınan bir görüntü üzerinde bu işlemi yapmak istiyorsanız,elinizdeki bu görüntüleri proje dosyasına atmalısınız.

Test1:Video içinde seçilmiş orijinal video görüntüsü.
Test2:MOG uygulanmış video görüntüsü.

2-CannyEdge Uygulaması

Canny kenar dedektörü, görüntülerdeki çok çeşitli kenarları algılamak için çok aşamalı bir algoritma kullanan bir kenar algılama operatörüdür.

Bu algoritma 5 aşamadan oluşur.

  1-Gürültü azaltma:Görüntünün arkasında yer alan matematik temelde türevlere dayandığından, kenar algılama sonuçları görüntü gürültüsüne karşı oldukça hassastır.Görüntüdeki gürültüden kurtulmanın bir yolu, Gauss bulanıklığını pürüzsüzleştirmek için uygulamaktır.

  2-Gradyan hesaplaması:Kenar algılama operatörlerini kullanıp resmin gradyanını hesaplayarak kenar yoğunluğunu ve yönünü algılar.Kenarlar, piksellerin yoğunluğundaki değişime karşılık gelir. Bunu tespit etmenin en kolay yolu, bu yoğunluk değişimini vurgulayan filtreleri her iki yönde de uygulamaktır.

  3-Maksimum olmayan bastırma işlemi:İdeal olarak, son görüntünün ince kenarları olmalıdır. Bu nedenle, kenarları inceltmek için maksimum olmayan baskılama uygulamamız gerekir.Prensip basittir: algoritma, gradyan yoğunluk matrisi üzerindeki tüm noktalardan geçer ve kenar yönlerinde maksimum değeri olan pikselleri bulur.

  4-Çift Threshold işlemi:Çift eşik adımı, 3 tür pikselin belirlenmesini amaçlamaktadır: güçlü, zayıf ve konuyla ilgili olmayan.Güçlü pikseller yoğunluğu o kadar yüksek olan piksellerdir; son kenara katkıda bulunduklarından eminiz.Zayıf pikseller, yoğunluk değeri olarak kabul edilmek için yeterli olmayan, ancak kenar algılama için uygun olmadığı düşünülebilecek kadar küçük olmayan bir yoğunluk değerine sahip piksellerdir.Diğer pikseller kenar için uygun değildir.


  5-Histeresiz ile Kenar Takibi:Eşik sonuçlarına dayanarak, histerezis, zayıf pikselleri güçlü olanlara dönüştürmekten ibarettir.

Ben bu uygulamada aynı şekilde OpenCV kütüphanesi yardımıyla "cv2.Canny()"fonksiyonunu kullanarak alınan canlı görüntü üzerinde bir kenar belirleme uygulaması yaptım.

3-Template Matching Uygulaması

Buradaki fikir, sağladığımız şablonla eşleşen ve belirli bir eşik değeri veren bir görüntünün aynı bölgelerini bulmaktır.

Kesin nesne eşleşmeleri için, tam aydınlatma / ölçek / açı ile, bu sistem daha verimli çalışabilir. 

Bu koşulların genellikle karşılandığı bir örnek, bilgisayardaki herhangi bir GUI ile ilgilidir. Düğmeler ve benzeri öğeler her zaman aynıdır, böylece şablon eşleştirmesini kullanabiliriz.

Başlamak için bir ana görüntüye ve bir şablona ihtiyacımız olacak. Şablonunuzu, görüntüde tam olarak aradığınız "şey" den almalıyız.

Ben bu uygulamada aynı girişlere sahip bir PC görseli aldım.

Burada önemli olan eşleştirmek istediğimiz nesnenin şablonda birden fazla ve aynı şekilde yer alması.

Ben bu uygulamada OpenCV'nin "cv2.matchTemplate()" fonksiyonunu kullanarak gerçekleştirdim.

Burada Threshold değerini değiştirerek eşleşme doğruluğunu kontrol edebiliriz.











