# Hairo

Hairo, Debian Stable tabanı üzerine inşa edilmiş, hafiflik, hız ve modern estetiği bir araya getirmeyi hedefleyen özel bir Linux dağıtımı projesidir. Hantal ve kaynak tüketen masaüstü ortamları yerine, XFCE'nin hızı ile Pardus'un kullanışlı araçlarını harmanlar.

Sistem, baştan sona alışılmış Windows masaüstü düzeni (altta görev çubuğu, solda başlat menüsü) referans alınarak, ancak fütüristik bir "Deep Ocean ve Neon Mor" estetiği ile tasarlanmıştır.

## 🚀 Öne Çıkan Özellikler

* **Özel Çekirdek (Kernel):** Standart Debian çekirdeği yerine, maksimum performans ve donanım uyumluluğu için özel olarak derlenmiş, `-hairo` mühürlü güncel **XanMod Kernel** kullanır.
* **Masaüstü Ortamı:** Gereksiz servislerden arındırılmış, Whisker Menu eklentisiyle tam bir Windows düzenine kavuşturulmuş XFCE4.
* **Pardus Entegrasyonu:** Sistemin DNA'sına Pardus 23 (yirmiuc) repoları işlenmiştir. `pardus-power-manager` ve `pardus-pen` gibi özel araçlar yerleşik olarak gelir.
* **Modern Mağaza:** Yazılım yönetimi için eski nesil araçlar yerine, Flatpak desteğiyle birlikte gelen evrensel `gnome-software` (Yazılımlar) kullanılır.
* **Özel Estetik:** 
  * Arc-Dark pencere teması ve Papirus-Dark ikon paketi.
  * *Deep Ocean* (`#0B132B`) alt panel ve arka plan referansları.
  * *Neon Mor* (`#9D00FF`) CSS destekli sistem seçim ve vurgu renkleri.
* **Geliştirici Odaklı:** Standart bash yerine modern ve hızlı `zsh` kabuğu ile `Alacritty` terminal emülatörü varsayılan olarak gelir.

## 🛠️ Mimari ve Teknolojik Altyapı

Bu işletim sistemi, Debian'ın resmi `live-build` araç seti kullanılarak sıfırdan "chroot" ortamında inşa edilmektedir.

* **Taban:** Debian Stable (amd64)
* **Paket Yöneticisi:** APT & Flatpak
* **Önyükleyici:** GRUB-EFI (UEFI sistemler için tam uyumluluk)

## 🏗️ Sistemi Kendi Bilgisayarınızda Derlemek

Kendi `live-image-amd64.hybrid.iso` dosyanızı oluşturmak için Debian/Ubuntu tabanlı bir sistemde şu adımları izleyebilirsiniz:

**1. Gerekli araçları kurun:**
```bash
sudo apt update
sudo apt install live-build git
