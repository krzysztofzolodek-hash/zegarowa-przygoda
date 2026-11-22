# Zegarowa Przygoda – wersja 0.1.0 (PWA)

**Nauka zegara w wielkiej przygodzie!**

Wersja gotowa do **zainstalowania na tablecie/telefonie z Androidem**.

---

## Jak zainstalować na Androidzie (tablet / telefon)

1. Skopiuj cały folder `Zegarowa-Przygoda-PWA` na tablet  
   **albo** wrzuć go na prosty hosting / Google Drive / lokalny serwer.

2. Otwórz plik `index.html` w przeglądarce **Chrome**.

3. W Chrome naciśnij menu (trzy kropki) → **„Zainstaluj aplikację”**  
   lub **„Dodaj do ekranu głównego”**.

4. Potwierdź instalację.

5. Na ekranie głównym pojawi się ikona **Zegarowa Przygoda**.  
   Od tej pory działa jak zwykła aplikacja (pełny ekran, offline).

> Uwaga: Żeby instalacja działała najlepiej, pliki powinny być serwowane przez `http://` lub `https://` (nie `file://`).  
> Najprostsze rozwiązania:
> - wrzuć folder na Netlify / GitHub Pages / Vercel
> - albo użyj aplikacji typu „Simple HTTP Server” na komputerze i połącz się z tabletem w tej samej sieci Wi-Fi

---

## Zawartość pakietu

```
Zegarowa-Przygoda-PWA/
├── index.html          ← główna aplikacja
├── manifest.json       ← konfiguracja PWA
├── sw.js               ← Service Worker (offline)
├── icons/              ← ikony aplikacji
│   ├── icon-48.png
│   ├── icon-72.png
│   ├── ...
│   └── icon-512.png
├── README.md
├── CHANGELOG.md
└── VERSION
```

---

## Historia ustaleń (skrót)

- Nazwa: **Zegarowa Przygoda**
- Styl: edukacyjno-zabawowy
- Hasło: „Nauka zegara w wielkiej przygodzie!”
- Ikona: kolorowy zegar + kompas + mapa skarbów + gwiazdka
- Wersja 0.0.1 – pełna webowa aplikacja
- Wersja 0.1.0 – PWA gotowa do instalacji na Androidzie

---

## Wersja

**0.1.0** – listopad 2026
