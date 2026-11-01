# Crowpanel-Esp32-s3-hm-2.8-inc-ekran-projesi
Elecrow CrowPanel Advance 2.8" (ESP32-S3) için Google Gemini yapay zeka sohbeti ve ders notları uygulaması. Türkçe arayüz, LovyanGFX, dokunmatik ekran klavyesi.
# CrowPanel AI Chat

Elecrow CrowPanel Advance 2.8" (ESP32-S3, 320x240, ST7789 + FT5x06 dokunmatik)
için geliştirilmiş, Google Gemini destekli yapay zeka sohbet ve ders notları
uygulaması. Proje, ESP32-2432S028R (CYD) kartındaki bir uygulamanın CrowPanel'e
uyarlanmış halidir.

## Özellikler
- Google Gemini ile sohbet
- Ekran üzerinden WiFi tarama ve ekran klavyesiyle şifre girişi (Türkçe karakter desteği)
- Sohbet geçmişinin kalıcı saklanması (NVS)
- Kişilik, dil, model ve parlaklık ayarları
- Ders notları bölümü: her dersin notu ayrı dosyada (`notlar_*.cpp`)
- UNO oyunu için hazırlanmış modül (`uno_ui.cpp`, şu an yer tutucu)

## Donanım
- Elecrow CrowPanel Advance 2.8" (ESP32-S3)

## Gerekli kütüphaneler
- LovyanGFX
- ArduinoJson v7

## Kurulum
1. Arduino IDE'de kartı **ESP32S3 Dev Module** olarak seçin.
2. Tüm dosyaları aynı sketch klasörüne koyun (`.ino`, `LovyanGFX_Driver.h`,
   `notlar*.cpp/.h`, `uno_ui.cpp/.h`).
3. `.ino` içindeki `API_KEY` değerine kendi Gemini API anahtarınızı yazın
   ([Google AI Studio](https://aistudio.google.com/) üzerinden alabilirsiniz).
4. Derleyip yükleyin.

## Dosya yapısı
| Dosya | Görev |
|---|---|
| `AI_esp_32_crowpanel_sohbeti_sonv2.ino` | Ana uygulama |
| `LovyanGFX_Driver.h` | Ekran ve dokunmatik sürücü ayarı |
| `notlar.cpp/.h`, `notlar_*.cpp` | Ders notları |
| `uno_ui.cpp/.h` | UNO oyunu modülü |

## Notlar
- Kendi API anahtarınızı kimseyle paylaşmayın ve depoya yüklemeyin.
- Donanımda her bölüm test edilmemiş olabilir; sorun bulursanız Issue açın.
