# FST Rules Files

Bu klasör morfolojik ve fonolojik kuralları içerir.

## Dosyalar

| Dosya | Açıklama |
|-------|----------|
| `nominal.twol` | İsim çekimleri |
| `verbal.twol` | Fiil çekimleri |
| `phonology.twol` | Ses uyumu kuralları |

## Format

```twol
Alphabet
  a b c ç d e f g ğ h ı i j k l m n o ö p r s ş t u ü v y z
  A:a A:e  ! Büyük ünlü uyumu
  I:ı I:i I:u I:ü  ! Küçük ünlü uyumu
;

Rules
"Büyük Ünlü Uyumu"
A:e <=> _ ;
    where A in (a e) ;
```

## Referans

- [HFST TWOLC Tutorial](https://github.com/hfst/hfst/wiki/HfstLexcAndTwolcTutorial)
