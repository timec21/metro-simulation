# metro-simulation
Bu proje, bir şehir metrosundaki istasyonlar arasındaki en hızlı veya en az aktarmalı rotayı bulmak için A algoritmasını* kullanan bir Python uygulamasıdır. Kullanıcı, başlangıç ve hedef istasyonları belirlediğinde, sistem en kısa sürede varış sağlayan rotayı hesaplar.

Metro Ağı
Bu proje, bir metro ağındaki istasyonlar ve hatlar arasında bağlantılar kurarak, en az aktarma veya en hızlı rotayı bulmayı amaçlamaktadır. Projede istasyonlar ve hatlar bir grafik veri yapısı olarak modellenmiş, Breadth-First Search (BFS) ve A* algoritmaları kullanılarak en iyi yollar hesaplanmıştır.

Özellikler

İstasyon Tanımlama: Her istasyon, benzersiz bir kimlik (ID), ad ve hat bilgisi ile tanımlanır.
Bağlantı Kurma: İstasyonlar arasında seyahat süresi baz alınarak bağlantılar oluşturulur.
En Az Aktarma Rotası: BFS algoritması kullanılarak, iki istasyon arasında en az aktarma yaparak ulaşılabilecek en kısa yol bulunur.
En Hızlı Rota: A* algoritması kullanılarak, iki istasyon arasında en kısa sürede ulaşılabilecek yol hesaplanır.

Kullanılan Algoritmalar

1. Breadth-First Search (BFS)
En az aktarma ile bir istasyondan diğerine ulaşmak için kullanılır. BFS, kuyruk yapısını kullanarak en kısa bağlantıyı arar ve ilk bulunan çözümü döndürür.

3. A* Algoritması
A* algoritması, en hızlı rotayı bulmak için kullanılır.
G-Score (Gerçek Maliyet): Başlangıç noktasından belirli bir istasyona kadar olan gerçek maliyeti ifade eder.
H-Score (Heuristik): Hedefe olan tahmini uzaklığı hesaplamak için kullanılır. Bu projede, istasyonlar arasındaki doğrudan mesafe tahmini olarak belirlenmiştir.
F-Score: F = G + H formülüyle hesaplanır. En düşük F değerine sahip olan yol öncelikli olarak işlenir.

Kullanım

İstasyonları ve Hatları Tanımlayın:
istasyon_ekle(idx, ad, hat): Yeni bir istasyon ekler.
baglanti_ekle(istasyon1_id, istasyon2_id, sure): İki istasyon arasında bağlantı kurar.

Rota Bulma:
en_az_aktarma_bul(baslangic_id, hedef_id): En az aktarma ile ulaşılacak rotayı döndürür.
en_hizli_rota_bul(baslangic_id, hedef_id): En kısa sürede ulaşılacak rotayı ve toplam süresini döndürür.

Örnek Senaryo

Aşağıdaki gibi istasyonlar ve hatlar eklendiğinde:

Kırmızı Hat: Kızılay, Ulus, Demetevler, OSB
Mavi Hat: AŞTİ, Kızılay, Sıhhiye, Gar
Turuncu Hat: Batıkent, Demetevler, Gar, Keçiören

Ve bağlantılar tanımlandığında, sistem en kısa ve en hızlı yolları hesaplayabilir.


![image](https://github.com/user-attachments/assets/b1d2ce0c-2154-4dc9-b49e-139db2517ee0)

