# HFST Kurulum Rehberi (Windows)

Bu rehber Windows'ta HFST kurulumunu ve test edilmesini anlatır.

---

## Yöntem 1: WSL (Önerilen) ✅

### Adım 1: WSL Kurulumu

```powershell
# PowerShell (Yönetici olarak)
wsl --install
```

Bilgisayarı yeniden başlatın, ardından Ubuntu'yu açın.

### Adım 2: HFST Kurulumu (Ubuntu/WSL)

```bash
# Sistem güncellemesi
sudo apt update && sudo apt upgrade -y

# HFST ve bağımlılıkları
sudo apt install -y hfst hfst-dev

# Ek araçlar
sudo apt install -y make gcc git python3 python3-pip

# Doğrulama
hfst-lookup --version
```

### Adım 3: Proje Dizinine Erişim

```bash
# Windows dosyalarına erişim
cd /mnt/c/Users/PC/Desktop/File/Project/berkeHocam

# veya symbolic link oluştur
ln -s /mnt/c/Users/PC/Desktop/File/Project/berkeHocam ~/berkeHocam
cd ~/berkeHocam
```

---

## Yöntem 2: Docker

```bash
# Dockerfile (proje köküne ekleyin)
FROM ubuntu:22.04
RUN apt-get update && apt-get install -y hfst hfst-dev python3 python3-pip
WORKDIR /app
```

```powershell
# Build ve çalıştır
docker build -t azerbaijani-fst .
docker run -it -v ${PWD}:/app azerbaijani-fst
```

---

## HFST Temel Komutları

| Komut | Açıklama | Örnek |
|-------|----------|-------|
| `hfst-lexc` | LEXC dosyasını derle | `hfst-lexc nouns.lexc -o nouns.hfst` |
| `hfst-twolc` | TWOLC kurallarını derle | `hfst-twolc phonology.twol -o phon.hfst` |
| `hfst-compose` | FST'leri birleştir | `hfst-compose lex.hfst phon.hfst -o combined.hfst` |
| `hfst-invert` | FST'yi ters çevir | `hfst-invert analyzer.hfst -o generator.hfst` |
| `hfst-lookup` | Kelime analizi | `echo "evlər" \| hfst-lookup az.hfst` |
| `hfst-fst2strings` | Tüm yolları listele | `hfst-fst2strings small.hfst` |

---

## Hızlı Test

WSL'de aşağıdaki komutu çalıştırarak kurulumu test edin:

```bash
# Test dosyası oluştur
cat > test.lexc << 'EOF'
LEXICON Root
ev Noun ;
kitab Noun ;

LEXICON Noun
+Noun:0 # ;
+Pl:lər # ;
EOF

# Derle
hfst-lexc test.lexc -o test.hfst

# Test et
echo "evlər" | hfst-lookup test.hfst
```

Beklenen çıktı:
```
evlər   ev+Noun+Pl
```

---

## Python HFST Binding

```bash
pip install hfst

# Test
python3 -c "import hfst; print('HFST Python OK')"
```

```python
# Kullanım örneği
import hfst

# FST yükle
analyzer = hfst.HfstInputStream("az.hfst").read()

# Analiz
results = analyzer.lookup("evlər")
for result in results:
    print(result)
```

---

## Sonraki Adımlar

1. [ ] WSL + HFST kurulumu
2. [ ] Test dosyası ile doğrulama
3. [ ] MorAz reposunu klonlayıp inceleme:
   ```bash
   git clone https://github.com/berkeozenc/MorAz.git
   cd MorAz
   make
   ```
