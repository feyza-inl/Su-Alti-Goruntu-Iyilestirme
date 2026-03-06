# Su Altı Görüntü İyileştirme

Derin öğrenme tabanlı sualtı görüntü iyileştirme projesi.
Real-ESRGAN modeli EUVP veri seti ile fine-tune edilmiştir.

## Proje Hakkında

Sualtı görüntüleri ışığın su ortamında soğurulması ve saçılması 
nedeniyle renk bozulması, bulanıklık ve düşük kontrast gibi 
sorunlar içermektedir. Bu projede Real-ESRGAN modeli sualtı 
görüntülerine özel olarak yeniden eğitilmiştir.

## Kullanılan Veri Setleri

- **UIEB** — 890 bozuk/referans sualtı görüntü çifti (test)
- **EUVP** — 11435 eşleştirilmiş sualtı görüntü çifti (eğitim)

## Kullanılan Model

- **Real-ESRGAN** — Genel amaçlı süper çözünürlük modeli
- Fine-tune: EUVP Paired veri seti ile yeniden eğitildi

## Sonuçlar

| Model | PSNR | SSIM | UCIQE |
|-------|------|------|-------|
| Vanilla Real-ESRGAN (2x) | 16.29 dB | 0.6579 | 0.2710 |
| Vanilla Real-ESRGAN (4x) | 16.63 dB | 0.6642 | 0.2710 |
| Fine-tuned Real-ESRGAN   | -        | -      | -      |

## Dosyalar

- `REAL_ESRGAN.ipynb` — scale=2 ile eğitim ve test
- `REAL_ESRGAN4ipynb.ipynb` — scale=4 ile eğitim ve test

## Gereksinimler
```
Python 3.10+
PyTorch
basicsr
realesrgan
opencv-python
scikit-image
```

## Kullanım

Google Colab üzerinde çalıştırılmıştır.
EUVP ve UIEB veri setleri Google Drive'a yüklenmiştir.
