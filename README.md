# NMAP

Kısaca sözlük bilgisi vermek gerekirse **Nmap** açık kaynak kodlu TCP/IP sistemlerinin güvenlik açıklarını, cihazların çalışıp çalışmadığı ve açık bağlantı noktalarını incelemek için kullanılan bir ağ izleme aracıdır.

## Başlamadan Önce Bilinmesi Gerekenler

* Güvenlik duvarları, yönlendiriciler, proxy sunucuları ve diğer güvenlik aygıtları Nmap sonuçlarını manüpile edebilir, bu nedenle uzak sunucularda tarama yapmak yanıltıcı sonuçlar verebilir.
* Bazı taramalar yüksek yetki gerektirir (elevated privileges), Linux sistemlerinde root olarak işlem yapmanız gerekebilir.
* **En önemli madde ise izine veya yetkiye sahip olmadığınız ağlara tarama yapmak suç teşkil eder izniniz olmadan yabancı ağalara tarama yapmayın başınız belaya girebilir.**

# Tarama İşlemleri

## NMAP Hedef Belirtme

* tek bir hedef için `nmap <hedef-IP>`

![tek-hedef](https://github.com/kaaneeksi/NMAP/blob/main/G%C3%B6rseller/NMAP-tek-hedef.png)

* İki tane IP'yi taramak istiyorsak `nmap <hedef-ıp> <hedef-ıp-2>` şeklinde araya bir boşluk koyarak yapabiliriz.

![tek-hedef](https://github.com/kaaneeksi/NMAP/blob/main/G%C3%B6rseller/NMAP-iki-hedef.png)

* Belli bir IP aralığını taramak istiyorsak `nmap <hedef-ıp-aralığı>` 

örnek olarak: `nmap 10.0.2.1-45` yani 10.0.2.1 IP sinden 10.0.2.45 IP aralığıını taramasını istedik.

![tek-hedef](https://github.com/kaaneeksi/NMAP/blob/main/G%C3%B6rseller/NMAP-aralik.png)

* Eğer bir liste içindeki IP leri tarmak istiyorsak `nmap -iL <hedef-listesi-adı>`

![tek-hedef](https://github.com/kaaneeksi/NMAP/blob/main/G%C3%B6rseller/NMAP-hedeflist.png)

* Eğer belli bir IP aralığında tarama yapmak istemediğimiz hedefler var ise `--exclude` parametresi ile bu IP leri esgeçe biliriz.

Örnek: `nmap <hedef-ıp-aralığı> --exclude <tarama-yapılmayacak-hedef-veya-hedefler>`

![tek-hedef](https://github.com/kaaneeksi/NMAP/blob/main/G%C3%B6rseller/NMAP-exclude.png)

**Fakat parametresiz nmap taraması yapmak nmap e hakaret sayılır.**




