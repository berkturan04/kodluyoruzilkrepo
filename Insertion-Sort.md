# Insertion Sort Aşamaları

Başlangıç dizisi: [22, 27, 16, 2, 18, 6]

Adım 1 (i=1, key=27):
27, 22'den büyük olduğu için yer değiştirme yok.
→ [22, 27, 16, 2, 18, 6]

Adım 2 (i=2, key=16):
16, 27'den ve 22'den küçük olduğu için ikisi de sağa kayar, 16 başa yerleşir.
→ [16, 22, 27, 2, 18, 6]

Adım 3 (i=3, key=2):
2, sırasıyla 27, 22, 16'dan küçük olduğu için hepsi sağa kayar, 2 en başa yerleşir.
→ [2, 16, 22, 27, 18, 6]

Adım 4 (i=4, key=18):
18, 27'den ve 22'den küçük ama 16'dan büyük. 27 ve 22 sağa kayar, 18 aralarına yerleşir.
→ [2, 16, 18, 22, 27, 6]

Adım 5 (i=5, key=6):
6, sırasıyla 27, 22, 18, 16'dan küçük ama 2'den büyük. Hepsi sağa kayar, 6 uygun yere yerleşir.
→ [2, 6, 16, 18, 22, 27] (sıralanmış hali)


# Big-O Gösterimi (Insertion Sort)

| Durum | Big-O | Açıklama |
| Best Case | O(n) | Dizi zaten sıralıysa, her eleman sadece 1 kez karşılaştırılır |
| Average Case | O(n²) | Elemanlar rastgele sıradaysa |
| Worst Case | O(n²) | Dizi ters sıralıysa (büyükten küçüğe), her eleman baştan sona kaydırılır |


Uzay Karmaşıklığı (Space Complexity): O(1) — in-place bir algoritmadır, ekstra dizi kullanmaz.

# 18 Sayısının Time Complexity Açısından Durumu

18 sayısı diziде 4. sırada (index 3) yer alıyor; yani dizinin ne en başında ne de en sonunda, tam olarak ortalarında bulunuyor.

Bu nedenle, bu elemanı ararken (örneğin lineer/doğrusal arama ile):

* Best Case (En İyi Durum) → O(1): Aranan eleman ilk sırada olsaydı (burada 2 bu duruma girer)
* Worst Case (En Kötü Durum) → O(n): Aranan eleman son sırada ya da dizide hiç olmasaydı (burada 27 bu duruma girer)
* Average Case (Ortalama Durum) → O(n/2) ≈ O(n): Aranan eleman dizinin ortalarında bir yerde

18 sayısı, dizinin tam ortasına yakın bir konumda (4./6.) bulunduğu için "Average Case (Ortalama Durum)" kapsamına girer.

