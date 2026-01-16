# Turkish Morphology FST

Türkiye Türkçesi için HFST tabanlı morfolojik analizör.

🚧 **Development in progress** 🚧

## Proje Hakkında

Bu proje, Türkiye Türkçesi'nin isim ve fiil morfolojisini Helsinki Finite-State Technology (HFST) kullanarak modellemeyi amaçlamaktadır.

## Yapı

```
turkish-morphology-fst/
├── fst/
│   ├── lexicon/    # Kök sözlükleri (.lexc)
│   ├── rules/      # Morfofonemik kurallar (.twol)
│   └── compiled/   # Derlenmiş FST dosyaları
├── backend/        # Python API (FastAPI)
├── frontend/       # Web arayüzü
└── docs/           # Dokümantasyon
```

## Gereksinimler

- HFST (Helsinki Finite-State Technology)
- Python 3.9+
- WSL (Windows için)

## Kurulum

Detaylı kurulum için: [docs/SETUP_GUIDE.md](docs/SETUP_GUIDE.md)

## Referanslar

- [MorAz - Azerbaijani Turkish Morphology](https://github.com/berkeozenc/MorAz)
- [TRmorph](https://github.com/coltekin/TRmorph)
- [Google Turkish Morphology](https://github.com/google-research/turkish-morphology)

## Katkıda Bulunanlar

- Berke Özenç (Danışman)
- [Sizin isminiz]

## Lisans

MIT License
