# 🚀 JAK WYSTAWIĆ DUCKONBOARD NA GITHUB

## 📋 Wymagania wstępne

1. **Konto GitHub** - jeśli nie masz, załóż na [github.com](https://github.com/signup)
2. **Git zainstalowany** - sprawdź w terminalu: `git --version`
   - Jeśli nie masz: [git-scm.com/downloads](https://git-scm.com/downloads)

---

## 🎯 METODA 1: Przez przeglądarkę (NAJŁATWIEJSZE!)

### Krok 1: Stwórz nowe repozytorium

1. Zaloguj się na GitHub
2. Kliknij przycisk **[+]** w prawym górnym rogu → **New repository**
3. Wypełnij formularz:
   - **Repository name**: `duckonboard`
   - **Description**: `🦆 Find Your Perfect Snowboard`
   - **Public** ← WAŻNE! (dla GitHub Pages)
   - ✅ **Add a README file** (odznacz - dodamy własny)
   - ✅ **Add .gitignore** (wybierz: None - mamy własny)
   - **License**: MIT
4. Kliknij **Create repository**

### Krok 2: Upload plików

1. Na stronie nowo utworzonego repo kliknij **uploading an existing file**
2. Przeciągnij i upuść pliki:
   - `index.html`
   - `logo-standard.png`
   - `logo-pride.png`
   - `README.md`
   - `LICENSE`
   - `gitignore.txt` ← **WAŻNE: po uploadzie przemianuj na `.gitignore`** (dodaj kropkę)
3. W polu **Commit changes** wpisz: `Initial commit - DuckOnBoard v1.0`
4. Kliknij **Commit changes**
5. **Przemianuj gitignore.txt**:
   - Kliknij na plik `gitignore.txt`
   - Kliknij ikonę ołówka (Edit)
   - Zmień nazwę na `.gitignore` (z kropką!)
   - Commit changes

### Krok 3: Włącz GitHub Pages

1. Kliknij **Settings** (⚙️ na górze)
2. W menu bocznym: **Pages**
3. W sekcji **Source**:
   - Branch: **main**
   - Folder: **/ (root)**
4. Kliknij **Save**
5. ⏳ Poczekaj 1-2 minuty
6. Odśwież stronę - zobaczysz link:  
   `https://[TWOJA-NAZWA].github.io/duckonboard/`

### Krok 4: Przetestuj!

1. Kliknij na link z GitHub Pages
2. Sprawdź czy aplikacja działa
3. ✅ Gotowe!

---

## 🖥️ METODA 2: Przez Terminal (dla zaawansowanych)

### Krok 1: Stwórz repo na GitHub

1. Zaloguj się na GitHub
2. Kliknij **[+]** → **New repository**
3. Nazwij: `duckonboard`
4. Zaznacz **Public**
5. **NIE** dodawaj README ani .gitignore (mamy własne)
6. Kliknij **Create repository**

### Krok 2: Lokalnie - przygotuj pliki

```bash
# Utwórz folder projektu
mkdir duckonboard
cd duckonboard

# Skopiuj pliki (zamień ścieżki na właściwe)
# - index.html
# - README.md
# - .gitignore
# - LICENSE

# Zainicjuj Git
git init

# Dodaj wszystkie pliki
git add .

# Pierwszy commit
git commit -m "Initial commit - DuckOnBoard v1.0"

# Zmień nazwę głównej gałęzi na 'main'
git branch -M main

# Dodaj remote (zamień TWOJA-NAZWA)
git remote add origin https://github.com/TWOJA-NAZWA/duckonboard.git

# Push do GitHub
git push -u origin main
```

### Krok 3: Włącz GitHub Pages

1. Idź na stronę repo: `https://github.com/TWOJA-NAZWA/duckonboard`
2. **Settings** → **Pages**
3. Source: **main** branch, **/ (root)** folder
4. **Save**
5. Po ~1 minucie odśwież i skopiuj link

### Krok 4: Aktualizacja README

```bash
# Edytuj README.md i zmień:
# [TWOJA-NAZWA] → twoja prawdziwa nazwa użytkownika GitHub

git add README.md
git commit -m "Update GitHub username in README"
git push
```

---

## 🔧 TROUBLESHOOTING

### Problem: "Permission denied (publickey)"

**Rozwiązanie:**
```bash
# Użyj HTTPS zamiast SSH
git remote set-url origin https://github.com/TWOJA-NAZWA/duckonboard.git
git push -u origin main
```

### Problem: Strona nie działa po włączeniu GitHub Pages

**Sprawdź:**
1. Czy repo jest **Public** (nie Private)?
2. Czy plik nazywa się **dokładnie** `index.html`?
3. Czy czekałeś 1-2 minuty po włączeniu Pages?
4. Odśwież stronę z **CTRL+F5** (hard refresh)

### Problem: Strona pokazuje 404

**Rozwiązanie:**
- Sprawdź w Settings → Pages czy source to **main** i **/ (root)**
- Upewnij się że plik `index.html` jest w głównym folderze (nie w podfolderze)

### Problem: Git nie jest zainstalowany

**Windows:**
```
Pobierz z: https://git-scm.com/download/win
```

**macOS:**
```bash
brew install git
# lub
xcode-select --install
```

**Linux (Ubuntu/Debian):**
```bash
sudo apt-get update
sudo apt-get install git
```

---

## 📝 CHECKLIST - Czy wszystko działa?

Przed publikacją sprawdź:

- [ ] Repo jest **Public**
- [ ] Plik nazywa się **index.html** (nie Index.html ani INDEX.HTML)
- [ ] GitHub Pages jest **włączone** (Settings → Pages)
- [ ] Link działa: `https://[TWOJA-NAZWA].github.io/duckonboard/`
- [ ] Aplikacja ładuje się poprawnie
- [ ] Wszystkie 5 ekranów działa
- [ ] Przełączanie motywów działa (⚙️ ikona)
- [ ] Algorytm oblicza wyniki
- [ ] Kopiowanie do schowka działa

---

## 🎨 CUSTOMIZACJA

### Zmień kolory

W pliku `index.html` znajdź sekcję CSS i edytuj:

```css
/* Zmień kolor akcentu (domyślnie cyan) */
background: linear-gradient(135deg, #00D9FF 0%, #00B8D4 100%);
                                    ↑ tutaj      ↑ i tutaj

/* Przykłady innych kolorów: */
/* Czerwony: #FF0080 → #FF0060 */
/* Zielony: #00FF80 → #00CC60 */
/* Fioletowy: #9D00FF → #7D00CC */
```

### Dodaj własne logo

1. Przygotuj plik PNG (np. `logo.png`)
2. Upload do repo
3. W `index.html` zamień emoji kaczki:

```html
<!-- Zamiast: -->
<div class="logo">🦆</div>

<!-- Użyj: -->
<img src="logo.png" alt="Logo" style="width: 80px; height: 80px;">
```

### Zmień emoji

W pliku `index.html` szukaj emoji i zamień na własne:
- 🦆 → Twoje logo
- 🌱 🎿 ⚡ 🔥 → Ikony poziomów
- 🏔️ 🎪 ⛰️ ☁️ → Ikony stylów

---

## 📊 STATYSTYKI I ANALITYKA

### Dodaj Google Analytics (opcjonalnie)

1. Stwórz konto: [analytics.google.com](https://analytics.google.com)
2. Skopiuj tracking code
3. Wklej przed `</head>` w `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 🚀 CO DALEJ?

### 1. Promuj aplikację!

Udostępnij link:
- Reddit: r/snowboarding, r/javascript
- Facebook: Grupy snowboardowe
- Instagram: #snowboard #webdev
- LinkedIn: Posty z projektem

### 2. Zbieraj feedback

- Dodaj formularz Google Forms
- Stwórz Issues na GitHub
- Monitor komentarzy w social media

### 3. Rozwijaj projekt

Sprawdź roadmap w `README.md`:
- Firebase Authentication
- System komentarzy
- Multi-język
- Aplikacja mobilna (.NET MAUI)

---

## 💡 WSKAZÓWKI

### Szybkie aktualizacje

```bash
# Po zmianie plików:
git add .
git commit -m "Opis zmian"
git push

# GitHub Pages zaktualizuje się automatycznie w ~1 minutę
```

### Testuj lokalnie przed push

```bash
# Uruchom prosty serwer HTTP
python -m http.server 8000

# Otwórz: http://localhost:8000
```

### Backup

```bash
# Pobierz całe repo:
git clone https://github.com/TWOJA-NAZWA/duckonboard.git

# Zawsze miej kopię lokalną!
```

---

## 🆘 POTRZEBUJESZ POMOCY?

- **GitHub Docs**: [docs.github.com](https://docs.github.com)
- **Git Tutorial**: [git-scm.com/docs](https://git-scm.com/docs)
- **Stack Overflow**: [stackoverflow.com](https://stackoverflow.com)

**Albo stwórz Issue na GitHub i poproś o pomoc społeczność!** 💪

---

**Good luck! 🦆🏂**
