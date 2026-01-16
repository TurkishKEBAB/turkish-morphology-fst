# GitHub Projects Kurulum Rehberi

Bu rehber Azerbaycan Türkçesi FST projesi için GitHub Projects kurulumunu anlatır.

---

## Adım 1: GitHub Repository

```bash
cd c:/Users/PC/Desktop/File/Project/berkeHocam
git init
git add .
git commit -m "Initial commit: Azerbaijani Turkish FST project structure"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADI/azerbaijani-fst.git
git push -u origin main
```

---

## Adım 2: GitHub Projects Oluşturma

1. GitHub'da repository'ye git
2. **Projects** sekmesine tıkla
3. **New project** → **Board** seç
4. İsim: "Azerbaycan Türkçesi FST - Mart 2026"

---

## Adım 3: Kolonlar

| Kolon | Açıklama |
|-------|----------|
| **Backlog** | Tüm görevler |
| **This Week** | Bu haftanın görevleri |
| **In Progress** | Üzerinde çalışılan |
| **Review** | Hoca incelemesi bekleyen |
| **Done** | Tamamlanan |

---

## Adım 4: Labels (Etiketler)

```
🔵 lexicon       - Sözlük işleri
🟢 morphotactics - Morfoloji kuralları
🟡 phonology     - Ses kuralları
🔴 backend       - API geliştirme
🟣 frontend      - Web arayüzü
📝 docs          - Dokümantasyon
🧪 test          - Test yazımı
```

---

## Adım 5: Milestones

| Milestone | Tarih | Kapsam |
|-----------|-------|--------|
| M1: Kurulum | 22 Ocak | HFST + temel yapı |
| M2: Nominal | 29 Ocak | İsim morfolojisi |
| M3: Verbal | 12 Şubat | Fiil morfolojisi |
| M4: API | 19 Şubat | Web servisi |
| M5: Final | 1 Mart | Teslim |

---

## Issues Şablonu

### Yeni Lexicon Issue
```markdown
## Görev
[Açıklama]

## Acceptance Criteria
- [ ] En az X kök eklendi
- [ ] Testler geçiyor
- [ ] Hoca onayladı

## Bağlantılar
- Paper: [link]
- Referans: MorAz words.lexc
```

---

## Haftalık Toplantı Template

```markdown
# Haftalık Toplantı - [TARİH]

## Bu hafta yapılanlar
-

## Sorunlar/Engeller
-

## Gelecek hafta planı
-

## Hoca notları
-
```
