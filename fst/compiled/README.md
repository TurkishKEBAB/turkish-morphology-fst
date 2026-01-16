# Derlenmiş FST Dosyaları

Bu klasör derlenmiş HFST dosyalarını içerir.

## Dosyalar

| Dosya | Açıklama |
|-------|----------|
| `turkish.hfst` | Ana analizör |
| `turkish.hfstol` | Optimized lookup |

## Kullanım

```bash
# Analiz
echo "evler" | hfst-lookup turkish.hfst

# Üretim
echo "ev+Noun+Pl" | hfst-lookup -I turkish.hfst
```

> **Not:** `.hfst` dosyaları git'e eklenmez (gitignore'da).
