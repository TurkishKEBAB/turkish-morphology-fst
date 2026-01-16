# Turkish Morphology FST - Lexicon Files

Bu dizin, HFST için lexicon (sözlük) dosyalarını içerir.

## Dosyalar

- `nouns.lexc` - İsim kökleri
- `verbs.lexc` - Fiil kökleri  
- `affixes.lexc` - Ek tanımları

## Format

LEXC formatı kullanılmaktadır. Örnek:

```lexc
LEXICON Root
Nouns ;
Verbs ;

LEXICON Nouns
ev:ev NounSuffixes ;
kitap:kitap NounSuffixes ;
```
