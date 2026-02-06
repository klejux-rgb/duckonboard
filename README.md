# 🦆 DuckOnBoard - Find Your Perfect Snowboard

![DuckOnBoard Logo](https://img.shields.io/badge/DuckOnBoard-v1.0-00D9FF?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHRleHQgeT0iMjAiIGZvbnQtc2l6ZT0iMjAiPvCfpoY8L3RleHQ+PC9zdmc+)

**Interaktywna aplikacja webowa do doboru deski snowboardowej**

## 📱 Demo

👉 **[ZOBACZ DEMO NA ŻYWO](https://[TWOJA-NAZWA].github.io/duckonboard/)**

## ✨ Funkcje

- 🎯 **Profesjonalny algorytm rekomendacji** - oddzielne obliczenia dla dzieci i dorosłych
- 📊 **Dynamiczne formularze** - suwaki zsynchronizowane z polami tekstowymi
- 🎨 **3 motywy kolorystyczne** - Standard Dark, Standard Light, Pride
- 🌟 **System ocen 5-gwiazdkowy** - dostępny dla wszystkich użytkowników
- 📋 **Kopiowanie do schowka** - gotowy opis dla sprzedawcy
- 🔐 **Symulacja logowania** - Firebase Auth (Google, Facebook, Apple, Email)
- 📱 **Responsywny design** - działa na wszystkich urządzeniach
- 🚫 **Brak zależności** - czysty HTML/CSS/JavaScript

## 🚀 Szybki start

### Opcja 1: Otwórz lokalnie

1. Pobierz plik `index.html`
2. Otwórz w przeglądarce (double-click)
3. Gotowe! 🎉

### Opcja 2: Wystaw na GitHub Pages

```bash
# 1. Sklonuj repozytorium
git clone https://github.com/TWOJA-NAZWA/duckonboard.git
cd duckonboard

# 2. Skopiuj plik index.html do repo

# 3. Commit i push
git add .
git commit -m "Initial commit - DuckOnBoard v1.0"
git push origin main
```

**Następnie w ustawieniach GitHub:**
1. Idź do **Settings** → **Pages**
2. Source: **Deploy from branch**
3. Branch: **main** → folder: **/ (root)**
4. Kliknij **Save**
5. Poczekaj ~1 minutę
6. Twoja aplikacja będzie dostępna pod:  
   `https://[TWOJA-NAZWA].github.io/duckonboard/`

## 🎮 Jak używać

### 1. Ekran startowy
- **Użyj bez logowania** - anonimowe korzystanie (z reklamami)
- **Zaloguj się** - dostęp do dodatkowych funkcji (bez reklam na formularzach)

### 2. Formularz (3 kroki)
- **Krok 1/3**: Wiek, waga, wzrost (można pominąć)
- **Krok 2/3**: Poziom umiejętności (można pominąć)
- **Krok 3/3**: Styl jazdy - **multi-select!** (można wybrać kilka)

### 3. Wyniki
- **Długość deski** - główna rekomendacja
- **Czego szukać w sklepie** - prosta lista
- **Tekst dla sprzedawcy** - gotowy opis do skopiowania
- **Parametry techniczne** - rozwijana sekcja (Shape, Profil, Flex)

### 4. Ocena
- **Gwiazdki 1-5** - dla wszystkich
- **Komentarze** - tylko dla zalogowanych
- **Zapisz do historii** - tylko dla zalogowanych

## 🧮 Algorytm

### Dla dzieci (<15 lat)
- Bazuje na **tabelach wysokości → długość**
- **NIE** oblicza Shape/Profil/Flex
- Łagodne korekty stylu i poziomu

### Dla dorosłych (≥15 lat)
**Podstawowy wzór:**
```
Długość = Wzrost - 15cm + korekty
```

**Korekty:**
- **Waga**: <50kg: -4cm | 50-60kg: -2cm | 80-90kg: +2cm | >90kg: +3cm
- **Poziom**: Początkujący: -4cm | Ekspert: +2cm
- **Styl**: Freestyle: -6cm | Freeride: +4cm | Powder: +10cm

**Shape/Profil/Flex:**
- Obliczane **TYLKO** gdy podano poziom **I** styl jazdy
- W przeciwnym razie: `---` (pominięte)

## 🎨 Motywy

### Standard Dark (domyślny)
- Tło: `#0A0A0A`
- Akcent: `#00D9FF` (cyan)
- Logo: Kaczka z czarnym hełmem

### Standard Light
- Tło: `#F5F5F5`
- Akcent: `#00D9FF`
- Logo: Kaczka z czarnym hełmem

### Pride 🌈
- Tło: Gradient tęczowy
- Akcent: `#00D9FF`
- Logo: Kaczka z różowym hełmem

**Zmiana motywu:** Kliknij ikonę ⚙️ w prawym górnym rogu

## 📢 Reklamy (AdMob)

### Ekran startowy (Launch)
- ❌ **BRAK reklam**

### Formularze (1/3, 2/3, 3/3)
- ✅ **Top banner 300x50** - tylko dla niezalogowanych
- ❌ **Zalogowani** - bez reklam

### Wyniki
- ✅ **Top banner 300x50** - **dla wszystkich** (zalogowani + niezalogowani)

## 🔐 Firebase Integration (TODO)

Aktualnie aplikacja **symuluje** logowanie. Aby dodać prawdziwe Firebase:

1. Stwórz projekt w [Firebase Console](https://console.firebase.google.com/)
2. Dodaj Firebase SDK do `index.html`:
```html
<script src="https://www.gstatic.com/firebasejs/9.x.x/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.x.x/firebase-auth.js"></script>
```
3. Skonfiguruj Authentication (Google, Facebook, Apple, Email)
4. Zastąp funkcje `loginGoogle()`, `loginFacebook()` itp. prawdziwymi wywołaniami Firebase

## 🛠️ Technologie

- **HTML5** - struktura
- **CSS3** - stylowanie (Flexbox, Grid, Animations)
- **Vanilla JavaScript** - logika (ES6+)
- **Local Storage** - zapisywanie ustawień motywu
- **Clipboard API** - kopiowanie tekstu

## 📦 Struktura projektu

```
duckonboard/
├── index.html          # Cała aplikacja (single file)
├── logo-standard.png   # Logo z czarnym hełmem (Standard/Light mode)
├── logo-pride.png      # Logo z różowym hełmem (Pride mode)
├── README.md           # Ten plik
├── GITHUB_SETUP.md     # Instrukcja wdrożenia
├── LICENSE             # Licencja MIT
└── .gitignore          # Git ignore rules
```

## 🎯 Roadmap

### v1.0 (obecna) ✅
- [x] 5 ekranów (Launch, Form 1-3, Results)
- [x] Algorytm dla dzieci i dorosłych
- [x] 3 motywy kolorystyczne
- [x] System ocen
- [x] Kopiowanie do schowka

### v1.1 (planowane)
- [ ] Prawdziwe Firebase Authentication
- [ ] Firebase Firestore (historia, komentarze)
- [ ] Google AdMob integracja
- [ ] Animacje przejść między ekranami

### v1.5 (future)
- [ ] Historia rekomendacji (chmura)
- [ ] System komentarzy społeczności
- [ ] Rekomendacje wiązań i butów
- [ ] Multi-język (EN, PL, DE)

### v2.0 (long-term)
- [ ] Narty (skiing)
- [ ] Kitesurfing
- [ ] Rowery (bicycles)
- [ ] Tenis (tennis)

## 🤝 Contributing

Pull requesty mile widziane! Jeśli masz pomysły na ulepszenia:

1. Fork projektu
2. Stwórz branch (`git checkout -b feature/NoweFunkcje`)
3. Commit zmian (`git commit -m 'Dodano nowe funkcje'`)
4. Push do brancha (`git push origin feature/NoweFunkcje`)
5. Otwórz Pull Request

## 📄 Licencja

Ten projekt jest licencjonowany na **MIT License** - szczegóły w pliku [LICENSE](LICENSE)

## 📧 Kontakt

Autor: **Rafał**

- GitHub: [@TWOJA-NAZWA](https://github.com/TWOJA-NAZWA)
- Email: twoj@email.com

## 🙏 Podziękowania

- Claude (Anthropic) - za pomoc w rozwoju
- Społeczność snowboardowa - za feedback i testy
- Producenci desek - za dane techniczne

## 📊 Statystyki

![GitHub stars](https://img.shields.io/github/stars/TWOJA-NAZWA/duckonboard?style=social)
![GitHub forks](https://img.shields.io/github/forks/TWOJA-NAZWA/duckonboard?style=social)
![GitHub issues](https://img.shields.io/github/issues/TWOJA-NAZWA/duckonboard)

---

**Made with ❤️ and 🦆 by snowboarders, for snowboarders**

🏂 **Happy shredding!** 🏂
