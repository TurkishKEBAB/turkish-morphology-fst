# trmorph-hfst

Türkiye Türkçesi için HFST tabanlı morfolojik analizör.

## 🎯 Proje Amacı

Türkiye Türkçesi'nin isim ve fiil morfolojisini sonlu durum dönüştürücüleri (FST) kullanarak modelleme ve web servisi olarak sunma.

## 🛠️ Teknolojiler

- **HFST** - Helsinki Finite-State Technology
- **Python** - Backend API
- **FastAPI** - Web framework

## 📁 Proje Yapısı

```
trmorph-hfst/
├── fst/
│   ├── lexicon/     # Kök sözlükler (.lexc)
│   ├── rules/       # Morfolojik kurallar (.twol)
│   └── compiled/    # Derlenmiş FST dosyaları
├── backend/
│   ├── api/         # REST API endpoints
│   ├── core/        # HFST wrapper
│   └── tests/       # Unit tests
├── frontend/        # Web arayüzü
└── docs/            # Dokümantasyon
```

## 🚀 Kurulum

```bash
# WSL gerekli (Windows)
wsl --install

# HFST kurulumu
sudo apt install hfst hfst-dev

# Derleme
make
```

## 📚 Referanslar

- [TRmorph](https://github.com/coltekin/TRmorph) - Türkçe morfolojik analizör
- [MorAz](https://github.com/berkeozenc/MorAz) - Azerbaycan Türkçesi analizör
- [HFST](https://github.com/hfst/hfst) - Helsinki Finite-State Technology

## 👥 Katkıda Bulunanlar

- [@TurkishKEBAB](https://github.com/TurkishKEBAB)
- [@berkeozenc](https://github.com/berkeozenc) - Danışman

## 📄 Lisans

MIT License
