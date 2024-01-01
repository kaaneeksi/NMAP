# -PN Parametresi - Ping'siz Scan

Nmap varsayılan olarak, açık portları taramadan önce hedefin aktif olup olmadığını anlamak için ping atar. 
Fakat bu olay, atılan pinglere yanıt vermeyen cihazların atlanmasına neden olur yani pinge cevap vermeyen cihazlara port taraması yapmaz.

`nmap -PN <hedef-ıp>` taraması ile ping işlemi yapılamayan sistemlerde açık portların tespiti yapılabilir.

# -sP Parametresi - Ping Scan

Bu parametre ile bir port taramasından önce, ağdaki cihazların hangilerinin aktif olduğunu görmek için kullanabiliriz.
Ayrıca `-sP` parametresini kullandığımızda **ARP Ping** işlemi gerçekleştirir ve keşif edilen sistemlerin MAC adreslerini verir.

ÖRN: `nmap -sP 198.168.1.0/24`

# -PA TCP Ack Ping

Bu parametre ACK paketleri ile ping taraması yapar, ICMP pinglerinin engellendiği durumlarda işe yaraya bilir.

ÖRN: `nmap -PA <hedef-ıp>`

# -sS TCP Syn Scan

Bu tarama parametresi hedefe SYN paketleri göndererek, en çok kullanılan 1000 TCP portunu belirlemeye çalışır fakat hedef cihaz üzerinde **loglanma** riski vardır.
Yani bu tarama bir gizlilik garanti etmez paket yakalama veya gelişmiş güvenlik duvarlarına yakalabilirsiniz.

ÖRN: `nmap -sS <hedef-ıp>`

# -sT TCP Connect Scan

**-sT** parametresi herhangi bir gizlilik olmadan doğrudan hedef sistemde bir port taraması yapar.

ÖRN: `nmap -sT <hedef-ıp>`

# -sA TCP Ack Scan

**-sA** parametresi, hedef sistemin bir güvenlik duvarı ile korunup korunmadığını belirlemek için kullanılabilir.Bu parametre filitrelenmiş veya filitrelenmemiş olan portları gösterir
fakat onların açık mı kapalı mı olduğu göstermez

ÖRN: `nmap -sA <hedef-ıp>`

