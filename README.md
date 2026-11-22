HEAD
# zegarowa-przygoda

# Zegarowa Przygoda

**Nauka zegara w wielkiej przygodzie!**

Aplikacja edukacyjno-zabawowa do nauki odczytywania godziny na zegarze wskazówkowym.

---

## Struktura projektu (reguła)

```
Zegarowa-Przygoda/
├── icons/                  ← wspólna ikona dla wszystkich wersji
├── apk/                    ← projekt Capacitor (do budowania natywnego APK)
├── pwa/                    ← wersja do instalacji na Androidzie (PWA)
├── web/                    ← wersja webowa (działa od razu w przeglądarce)
├── README.md
└── INSTRUKCJA-APK.md       ← jak zrobić plik APK (dwie metody)
```

### Zasady:
- Ikona jest **jedna** i leży w katalogu `icons/`
- Wszystkie wersje korzystają z tych samych ikon
- Każda wersja ma własny `VERSION`, `CHANGELOG.md` i `README.md`

---

## Wersje

| Katalog | Wersja | Opis |
|---------|--------|------|
| `web/`  | 0.0.1  | Czysta wersja HTML – otwierasz i działa |
| `pwa/`  | 0.1.0  | Wersja do zainstalowania z Chrome (PWA) |
| `apk/`  | 0.1.0  | Projekt Capacitor – z niego budujesz prawdziwy plik `.apk` |

---

## Jak zrobić plik APK?

Zobacz plik **`INSTRUKCJA-APK.md`** – są tam dwie metody:
- **A)** Capacitor + Android Studio
- **B)** PWABuilder (najszybsza)

---

## Historia ustaleń

- Nazwa: **Zegarowa Przygoda**
- Styl: edukacyjno-zabawowy
- Hasło: „Nauka zegara w wielkiej przygodzie!”
- Ikona: kolorowy zegar + kompas + mapa skarbów + gwiazdka (wspólna)
- Wersja 0.0.1 – pełna webowa aplikacja
- Wersja 0.1.0 – PWA + projekt Capacitor pod APK

---

**Ostatnia aktualizacja:** 22 listopada 2026
fcf161d (Pierwsza wersja - Zegarowa Przygoda)
