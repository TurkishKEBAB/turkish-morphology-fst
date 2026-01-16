# Compiled FST Files

Bu klasör derlenmiş FST dosyalarını içerir.

## Dosyalar

| Dosya | Açıklama |
|-------|----------|
| `trmorph.hfst` | Ana morfolojik analizör |
| `generator.hfst` | Kelime üretici |

## Derleme

```bash
make
```

## Kullanım

```bash
echo "evler" | hfst-lookup trmorph.hfst
# Output: ev+Noun+Pl
```
