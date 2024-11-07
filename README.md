# Instrukcja instalacji bota

## Wymagania wstępne
Aby uruchomić bota muzycznego Discord, potrzebujesz kilku narzędzi i środowisk:

- Python 3.8 lub nowszy
- FFMPEG (do obsługi dźwięku)
- Token bota Discord (wygenerowany na stronie Discord Developer Portal)

## Krok 1: Zainstaluj Pythona

1. Przejdź na stronę [Python.org](https://www.python.org/downloads/) i pobierz najnowszą wersję Pythona.
2. Podczas instalacji zaznacz opcję "Add Python to PATH", aby móc korzystać z polecenia `python` w wierszu poleceń.
3. Jeśli korzystasz z Visual Studio Code, zaleca się pobranie Pythona z Microsoft Store, aby lepiej zintegrować środowisko programistyczne.

## Krok 2: Zainstaluj FFMPEG

Bot korzysta z FFMPEG do odtwarzania muzyki, więc konieczne jest jego pobranie.

1. Przejdź na stronę [FFmpeg](https://ffmpeg.org/download.html) i pobierz odpowiednią wersję dla swojego systemu operacyjnego.
2. Wypakuj archiwum, które pobrałeś (np. za pomocą programu WinRAR lub 7-Zip).
3. Znajdziesz tam folder o nazwie `ffmpeg`. Wewnątrz niego jest podfolder `bin` - to tam znajdują się najważniejsze pliki programu.
4. Aby bot mógł korzystać z FFMPEG, musisz dodać ten folder `bin` do zmiennych środowiskowych systemu (tzw. PATH). Dzięki temu system będzie wiedział, gdzie szukać FFMPEG, gdy będzie to potrzebne.
   - Kliknij prawym przyciskiem na "Mój komputer" > "Właściwości" > "Zaawansowane ustawienia systemu" > "Zmienna środowiskowa".
   - Znajdź zmienną `Path` i edytuj ją, dodając ścieżkę do folderu `bin` (np. `C:\ffmpeg\bin`).

## Krok 3: Stwórz aplikację bota na stronie Discord Developer Portal

1. Przejdź na [Discord Developer Portal](https://discord.com/developers/applications).
2. Kliknij przycisk "New Application", aby stworzyć nową aplikację.
3. Wprowadź nazwę bota i kliknij "Create".
4. Przejdź do zakładki "Bot" i kliknij "Add Bot", aby dodać bota do swojej aplikacji.
5. Skopiuj token bota – będzie potrzebny do skonfigurowania bota.
6. Przejdź do zakładki "OAuth2" > "URL Generator". Zaznacz uprawnienia bota, takie jak `bot` oraz `administrator`, a następnie wygeneruj i skopiuj link do zaproszenia bota na swój serwer.
7. Otwórz wygenerowany link i zaproś bota na swój serwer Discord.

## Krok 4: Klonowanie repozytorium

Aby pobrać kod źródłowy bota, musisz go sklonować (pobrać na swój komputer). W tym celu:

1. Otwórz wiersz poleceń (`CMD`) lub terminal, np. w systemie Windows możesz nacisnąć klawisz Windows, wpisać "cmd" i uruchomić Wiersz polecenia.
2. Przejdź do folderu, w którym chcesz umieścić kod bota, używając polecenia `cd` (np. `cd C:\TwojeProjekty`).
3. Następnie wpisz poniższe polecenie, aby sklonować repozytorium:

   ```bash
   git clone https://github.com/nazwauzytkownika/nazwarepozytorium.git
   ```

4. Przejdź do katalogu z botem:

   ```bash
   cd nazwarepozytorium
   ```

## Krok 5: Zainstaluj wymagane biblioteki

W katalogu projektu znajduje się plik `requirements.txt`, który zawiera listę wymaganych bibliotek do uruchomienia bota. Aby je zainstalować, użyj poniższego polecenia:

```bash
pip install -r requirements.txt
```

## Krok 6: Konfiguracja tokena bota

1. Utwórz plik 'token.env' w tym samym folderze, gdzie masz główny plik z kodem bota (discordbot.py).
2. Wklej token bota, który skopiowałeś wcześniej, w następujący sposób:

```
TOKEN=Twój_Token_Bota
```

Zapisz plik.

## Krok 7: Uruchomienie bota

Po skonfigurowaniu tokena bota możesz uruchomić bota, używając poniższego polecenia w CMD:

```bash
python discordbot.py
```

Po uruchomieniu bota, zobaczysz komunikat potwierdzający, że bot jest aktywny i połączony z serwerem Discord.

## Uwaga

Jeśli bot nie działa poprawnie, upewnij się, że:
- Wszystkie zależności zostały poprawnie zainstalowane.
- FFMPEG jest zainstalowany i jego ścieżka jest dodana do zmiennych środowiskowych systemu.
- Token bota jest poprawny.

