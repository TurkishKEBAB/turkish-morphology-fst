# Project Setup Guide

## 🚀 GitHub Repository Kurulumu

Proje yapısı hazır ve ilk commit yapıldı. Şimdi GitHub'a yüklemek için şu adımları izleyin:

### Adım 1: GitHub'da Yeni Repo Oluştur

1. [GitHub New Repository](https://github.com/new) sayfasına gidin
2. Repository name: `turkish-morphology-fst`
3. Description: `Türkiye Türkçesi biçimbilgisi için FST tabanlı web servisi`
4. Public seçin
5. ❌ "Add a README file" - SEÇMEYİN
6. ❌ "Add .gitignore" - SEÇMEYİN  
7. "Create repository" butonuna tıklayın

### Adım 2: Kodu GitHub'a Gönder

PowerShell'de şu komutları çalıştırın:

```powershell
cd "c:\Users\PC\Desktop\File\Project\berkeHocam"

# Remote ekle (YOUR_USERNAME yerine GitHub kullanıcı adınızı yazın)
git remote add origin https://github.com/YOUR_USERNAME/turkish-morphology-fst.git

# Branch'i main olarak yeniden adlandır
git branch -M main

# Push
git push -u origin main
```

### Adım 3: Diagram'ları Kontrol Et

Push sonrası GitHub'da şunları göreceksiniz:
- ✅ README.md ana sayfada görünür
- ✅ docs/diagrams/fst_diagrams.png resmi yüklenmiş olmalı
- ✅ Proje yapısı (fst/, backend/, frontend/, docs/)

---

## 📋 Sonraki Adımlar

GitHub repo hazır olduktan sonra:

1. **GitHub Issues** oluşturma
2. **Trello Board** kurulumu
3. **FST Development** başlatma
