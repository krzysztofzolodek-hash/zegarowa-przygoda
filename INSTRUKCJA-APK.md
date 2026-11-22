# Jak zrobić plik APK – dwie metody

Masz do wyboru dwie drogi.

---

## Metoda A – Capacitor (pełna kontrola, natywny projekt)

### Co musisz mieć zainstalowane:
- **Node.js** 18+
- **Java JDK** 17 lub 21
- **Android Studio** (z Android SDK 34/35)

### Szybkie kroki:
```bash
cd Zegarowa-Przygoda/apk
npm install
npx cap add android
npx cap sync
npx cap open android
```
Potem w Android Studio: **Build → Build APK(s)**

Szczegółowa instrukcja znajduje się w pliku:
`apk/README.md`

---

## Metoda B – PWABuilder (najszybsza, bez programowania)

1. Wrzuć folder `pwa/` na dowolny darmowy hosting (Netlify Drop, GitHub Pages, Vercel…).
2. Wejdź na stronę: **https://www.pwabuilder.com**
3. Wklej adres swojej PWA.
4. Kliknij **Start** → wybierz **Android**.
5. Pobierz wygenerowany plik `.apk` lub `.aab`.

To najszybszy sposób, jeśli nie chcesz instalować Android Studio.

---

## Porównanie

| | Capacitor (A) | PWABuilder (B) |
|---|---|---|
| Trudność | Średnia | Bardzo łatwa |
| Potrzebne narzędzia | Node + Android Studio | Tylko przeglądarka |
| Czas | 15–40 min | 5–10 min |
| Kontrola nad projektem | Pełna | Ograniczona |
| Nadaje się do sklepu Google Play | Tak | Tak (przy podpisaniu) |
