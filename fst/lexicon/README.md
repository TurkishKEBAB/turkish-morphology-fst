# FST Lexicon Files

Bu klasör FST lexicon dosyalarını içerir.

## Dosyalar

| Dosya | Açıklama |
|-------|----------|
| `nouns.lexc` | İsim kökleri |
| `verbs.lexc` | Fiil kökleri |
| `adjectives.lexc` | Sıfat kökleri |
| `closed_class.lexc` | Kapalı sınıf kelimeler |

## Format

```lexc
LEXICON Root
ev Noun ;
kitap Noun ;

LEXICON Noun
+N:0 NounInfl ;
```

## Referans

- [HFST LEXC Tutorial](https://github.com/hfst/hfst/wiki/HfstLexcAndTwolcTutorial)
