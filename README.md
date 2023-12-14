# NMAP

Kısaca sözlük bilgisi vermek gerekirse **Nmap** açık kaynak kodlu TCP/IP sistemlerinin güvenlik açıklarını, cihazların çalışıp çalışmadığı ve açık bağlantı noktalarını incelemek için kullanılan bir ağ izleme aracıdır.

## Başlamadan Önce Bilinmesi Gerekenler

* Güvenlik duvarları, yönlendiriciler, proxy sunucuları ve diğer güvenlik aygıtları Nmap sonuçlarını manüpile edebilir, bu nedenle uzak sunucularda tarama yapmak yanıltıcı sonuçlar verebilir.
* Bazı taramalar yüksek yetki gerektirir (elevated privileges), Linux sistemlerinde root olarak işlem yapmanız gerekebilir.
* **En önemli madde ise izine veya yetkiye sahip olmadığınız ağlara tarama yapmak suç teşkil eder izniniz olmadan yabancı ağalara tarama yapmayın başınız belaya girebilir.**

# Tarama İşlemleri

## Tek Bir Hedef Üzerinde Tarama Yapmak

Kullanımı: `nmap <hedef-IP>`


