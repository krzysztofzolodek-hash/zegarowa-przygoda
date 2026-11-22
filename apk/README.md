# Zegarowa Przygoda – wersja APK (Capacitor)

Ten katalog zawiera projekt gotowy do zbudowania **natywnego pliku APK** na Androida.

---

## Wymagane środowisko programistyczne

Aby zbudować plik `.apk`, potrzebujesz na komputerze:

### 1. Podstawowe narzędzia
| Narzędzie | Wersja | Do czego |
|-----------|--------|----------|
| **Node.js** | 18 lub nowszy | uruchamianie Capacitora |
| **npm** | (idzie z Node.js) | instalacja pakietów |
| **Java JDK** | 17 lub 21 | kompilacja Androida |
| **Android Studio** | najnowsza stabilna | budowanie APK + emulator |

### 2. Android Studio – co zainstalować w środku
Po instalacji Android Studio otwórz **SDK Manager** i zaznacz:
- Android SDK Platform 34 (lub 35)
- Android SDK Build-Tools
- Android SDK Command-line Tools
- Android Emulator (opcjonalnie)

### 3. Zmienne środowiskowe (ważne!)
Dodaj do systemu:

```bash
# Przykład dla Linux / macOS (~/.bashrc lub ~/.zshrc)
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_HOME/cmdline-tools/latest/bin
```

Na Windows ustaw te same zmienne w „Zmienne środowiskowe”.

---

## Jak zbudować APK – krok po kroku

### Krok 1 – Wejdź do katalogu
```bash
cd Zegarowa-Przygoda/apk
```

### Krok 2 – Zainstaluj zależności
```bash
npm install
```

### Krok 3 – Dodaj platformę Android
```bash
npx cap add android
```

### Krok 4 – Synchronizuj pliki webowe
```bash
npx cap sync android
```

### Krok 5 – Otwórz projekt w Android Studio
```bash
npx cap open android
```

### Krok 6 – Zbuduj APK w Android Studio
1. Poczekaj, aż Gradle się zsynchronizuje.
2. Menu **Build → Build Bundle(s) / APK(s) → Build APK(s)**
3. Po zakończeniu kliknij **locate** – znajdziesz plik:
   ```
   android/app/build/outputs/apk/debug/app-debug.apk
   ```

### Krok 7 – Zainstaluj na tablecie
- Włącz **Opcje deweloperskie** + **Debugowanie USB** na tablecie
- Podłącz tablet kablem
- Przeciągnij plik `.apk` na tablet i zainstaluj  
  **lub** użyj komendy:
  ```bash
  adb install android/app/build/outputs/apk/debug/app-debug.apk
  ```

---

## Wersja release (podpisana)

Jeśli chcesz APK do dystrybucji (nie debug):

1. W Android Studio: **Build → Generate Signed Bundle / APK**
2. Stwórz keystore (lub użyj istniejącego)
3. Wybierz **APK** → release

---

## Przydatne komendy

```bash
npx cap sync          # synchronizuje zmiany z www/ do projektu Android
npx cap open android  # otwiera Android Studio
npx cap run android   # buduje i od razu instaluje na podłączonym urządzeniu
```

---

## Struktura katalogu apk/

```
apk/
├── www/                    ← pliki aplikacji (HTML, JS, ikony)
├── capacitor.config.json   ← konfiguracja Capacitora
├── package.json
└── README.md               ← ten plik
```

Po wykonaniu `npx cap add android` pojawi się dodatkowy katalog `android/`.
