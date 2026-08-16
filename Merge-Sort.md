# Adım 1: Bölme (Divide) Aşaması
Dizi ortadan ikiye bölünür ve bu işlem alt diziler tek elemanlı olana kadar recursive (özyinelemeli) olarak tekrarlanır.
* Ana Dizi: [16, 21, 11, 8, 12, 22]
* 1. Bölünme: [16, 21, 11] ve [8, 12, 22]
* 2. Bölünme:Sol taraf: [16, 21] ve [11]Sağ taraf: [8, 12] ve [22]
* 3. Bölünme (Tek elemanlı diziler - Taban Durum):[16], [21], [11][8], [12], [22]

# Adım 2: Birleştirme ve Sıralama (Merge) Aşaması
Tek elemanlı diziler ikili olarak karşılaştırılıp sıralı bir şekilde birleştirilir.
1. Birleştirme Grubu:[16] ve [21] $\rightarrow$ [16, 21] (Zaten sıralı)
* [11] tek başına kalır $\rightarrow$ [11]
* [8] ve [12] $\rightarrow$ [8, 12] (Zaten sıralı)
* [22] tek başına kalır $\rightarrow$ [22]
2. Birleştirme Grubu (Orta Seviye Birleştirme):
* [16, 21] ve [11] dizileri birleştirilir: 
    * 11, 16'dan küçük olduğu için başa gelir $\rightarrow$ [11, 16, 21]
* [8, 12] ve [22] dizileri birleştirilir:
    * 8 ve 12, 22'den küçük olduğu için önce eklenir $\rightarrow$ [8, 12, 22]
# 3. Son Birleştirme (Ana Diziyi Oluşturma)
Elimizde iki adet sıralı alt dizi kaldı: [11, 16, 21] ve [8, 12, 22]
İki dizinin elemanları baştan itibaren karşılaştırılarak tek bir sıralı dizi haline getirilir:
* 8, 11'den küçük $\rightarrow$ [8]
* 11 ve 12 karşılaştırılır, 11 küçük $\rightarrow$ [8, 11]
* 16 ve 12 karşılaştırılır, 12 küçük $\rightarrow$ [8, 11, 12]
* 16 ve 22 karşılaştırılır, 16 küçük $\rightarrow$ [8, 11, 12, 16]
* 21 ve 22 karşılaştırılır, 21 küçük $\rightarrow$ [8, 11, 12, 16, 21]
* Kalan eleman eklenir $\rightarrow$ [8, 11, 12, 16, 21, 22]

# Sonuç
Merge Sort algoritması sonucunda sıralanmış dizi:[8, 11, 12, 16, 21, 22]
