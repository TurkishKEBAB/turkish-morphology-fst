# Morfofonemik Kurallar

Bu klasör ses değişim kurallarını içerir.

## Dosyalar

| Dosya | Açıklama |
|-------|----------|
| `phonology.twol` | Ses uyumu kuralları |
| `nominal.twol` | İsim çekim kuralları |
| `verbal.twol` | Fiil çekim kuralları |

## Format (TWOLC)

```twolc
Alphabet
  a b c ç d e f g ğ h ı i j k l m n o ö p r s ş t u ü v y z
  A:a A:e  ! Büyük ünlü uyumu
  I:ı I:i I:u I:ü  ! Küçük ünlü uyumu
  D:d D:t  ! Ünsüz uyumu
;

Rules
"Büyük Ünlü Uyumu"
A:e <=> FrontVowel: Cons* _ ;
```
