# Industrial Simulation Studio — sürümler

Elektrik panosu tasarımı, elektriksel simülasyon ve Modbus RTU / RS-485 testlerini birleştiren Windows
uygulamasının derlenmiş sürümleri. Bu depo yalnızca indirme içindir; kaynak kod ayrı tutulur.

**İndir:** [En son sürüm](https://github.com/alizobu92/industrial-simulation-studio-releases/releases/latest)

## Kurulum

1. `IndustrialSimulationStudio-<sürüm>-windows-x64.zip` dosyasını indirin.
2. Zip'i yazılabilir bir klasöre **çıkarın**, örneğin `Belgeler` ya da `Masaüstü`. Uygulamayı zip içinden
   çalıştırmayın. `Program Files` altına koymayın, yoksa kendini güncelleyemez.
3. `IndustrialSimulationStudio\IndustrialSimulationStudio.exe` dosyasını çalıştırın. Exe, yanındaki DLL'ler ve
   `data` klasörüyle birlikte çalışır.
4. Örnek proje için klasördeki `ornek-pano.issproj` dosyasını **Aç** ile açın.

Gereksinim: Windows 10/11 x64. Exe imzalı olmadığı için Windows SmartScreen "Bilinmeyen yayımcı" uyarısı
verebilir. Devam etmek için *Ek bilgi → Yine de çalıştır*.

## Güncellemeler

0.4.1 ve sonraki sürümler kendini günceller:

- Uygulama açılışta bu depodaki en son sürüme bakar ve yeni sürüm varsa bildirir. Elle denetlemek için:
  *Ayarlar (dişli) → Güncellemeleri denetle…*.
- *İndir ve kur* paketi indirir ve SHA-256 özetiyle doğrular. *Yeniden başlat ve kur* uygulamayı kapatır,
  dosyaları değiştirir ve açık projeyle yeniden açar. Hiçbir şey onayınız olmadan kurulmaz.
- Projeleriniz ve ayarlarınız güncellemeden etkilenmez.

0.4.0 kullanıyorsanız 0.4.1'i bir kez elle indirip eski klasörün üzerine çıkarmanız gerekir.

## Doğrulama

Her sürümde zip'in yanında `.sha256` dosyası bulunur. PowerShell ile kontrol:

```powershell
Get-FileHash .\IndustrialSimulationStudio-0.4.1-windows-x64.zip -Algorithm SHA256
```

> Simülasyon sonuçları gerçek ölçümün, sertifikalı mühendislik analizinin veya saha doğrulamasının yerine
> geçmez. Bu proje ENTES ile bağlantılı değildir. ENTES ürün bilgileri, yayımlanmış belgelerinden kaynak
> gösterilerek derlenmiştir.
