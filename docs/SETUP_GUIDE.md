# HFST Kurulumu

## WSL + HFST (Windows)

```powershell
# 1. WSL kur (PowerShell admin)
wsl --install
# Bilgisayarı yeniden başlat
```

```bash
# 2. Ubuntu'da HFST kur
sudo apt update
sudo apt install -y hfst

# 3. Test
hfst-lookup --version
```

## Proje Klasörüne Erişim

```bash
cd /mnt/c/Users/PC/Desktop/File/Project/berkeHocam
```

## Temel Komutlar

| Komut | Ne yapar |
|-------|----------|
| `hfst-lexc file.lexc -o out.hfst` | Sözlük derle |
| `hfst-twolc file.twol -o out.hfst` | Kural derle |
| `echo "evler" \| hfst-lookup tr.hfst` | Analiz yap |
