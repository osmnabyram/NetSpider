# WiFi Handshake ve Deauthentication Otomasyon Aracı

Bu proje, **Aircrack-ng** araç setini temel alarak Wi-Fi ağları üzerinde **handshake yakalama**, **deauthentication** ve **parola deneme** süreçlerini yarı otomatik hale getiren **Python tabanlı** bir siber güvenlik aracıdır.

Araç; manuel olarak yürütülmesi zahmetli olan komut zincirlerini otomatikleştirerek, **eğitim**, **CTF**, **laboratuvar ortamları** ve **izinli sızma testlerinde** pratik kullanım sunar.

![image](https://github.com/user-attachments/assets/31f25032-a859-48a0-9ca5-693b2d66c9cf)

---

## Genel Amaç

- Wi-Fi ağlarını taramak  
- Hedef access point üzerinde handshake yakalamak  

- Deauthentication saldırılarını otomatikleştirmek  
- Handshake doğrulama ve parola denemelerini tek akışta yürütmek  
- Kullanıcıyı terminal üzerinden adım adım yönlendirmek  

---

## Temel Özellikler

- Açılış animasyonu ve ASCII banner  
- Otomatik Wi-Fi adaptörü (`wlan0`) kontrolü  
- Monitor mode yönetimi (`airmon-ng`)  
- Canlı Wi-Fi ağ taraması (`airodump-ng`)  
- BSSID ve kanal bazlı hedef dinleme  
- Ayrı terminalde deauthentication yönetimi  
- Handshake doğrulama (`aircrack-ng`)  
- Bruteforce otomasyonu (`crunch + john + aircrack-ng`)  
- Süreç sonlandırma ve temiz kapatma desteği  

---

## Kullanılan Araçlar

- Python 3  
- Bash  
- Aircrack-ng  
  - airmon-ng  
  - airodump-ng  
  - aireplay-ng  
  - aircrack-ng  
- Crunch  
- John the Ripper  
- Linux tabanlı işletim sistemi  

---

## Gereksinimler

Aracın çalışabilmesi için sistemde aşağıdakiler kurulu olmalıdır:

- Linux (Kali, Parrot, Ubuntu vb.)  
- Python 3.x  
- Aircrack-ng  
- Crunch  
- John the Ripper  
- Monitor mode destekleyen Wi-Fi adaptörü  
- gnome-terminal  

---

## Kurulum

```bash
git clone https://github.com/osmnabyram/NetSpider.git
cd NetSpider
chmod +x netspider.py
```

## Kullanım

Aracı çalıştırmak için **root yetkisi** gereklidir:

```bash
sudo python3 netspider.py
```

## Çalışma Akışı

• Wi-Fi adaptörü kontrol edilir  
• Monitor mode aktif edilir  
• Çevredeki Wi-Fi ağları listelenir  
• Hedef BSSID, kanal ve kayıt dosyası adı girilir  
• Hedef dinlemeye alınır  
• Deauthentication işlemi ayrı terminalde yürütülür  
• Handshake yakalanırsa doğrulama ve parola denemesi başlatılır  
• İşlem sonunda monitor mode kapatılır  

## Örnek Kullanım Senaryosu

• Eğitim ortamında bir WPA/WPA2 ağı belirlenir  
• İstemciler deauthentication ile bağlantıdan düşürülür  
• Handshake yakalanır  
• Parola güvenliği test edilir  
• Sonuçlar analiz edilir  

## Yasal Uyarı

Bu araç yalnızca **eğitim amaçlı**, **CTF**, **laboratuvar ortamları** ve **açık izin verilmiş sızma testlerinde** kullanılmak üzere geliştirilmiştir.

Yetkisiz ağlara veya sistemlere karşı kullanımı **yasadışıdır** ve hukuki sorumluluk doğurur.

Geliştirici, bu aracın kötüye kullanımından doğabilecek herhangi bir zarardan **sorumlu değildir**.
