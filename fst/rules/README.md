# Ses Kuralları

Ünlü uyumu, ünsüz değişimleri vs. burada.

## Örnek Format

```twolc
Alphabet
  a e ı i o ö u ü
  A:a A:e  ! büyük ünlü uyumu
;

Rules
"Büyük Ünlü Uyumu"
A:e <=> FrontVowel: Cons* _ ;
```
