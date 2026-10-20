# LiDAR Toolbox — wydania

Wersje skompilowane programu LiDAR Toolbox (klasyfikacja chmur punktów ALS dla linii
elektroenergetycznych). Repozytorium zawiera tylko pliki wydań, bez kodu źródłowego.
Do uruchomienia programu potrzebny jest klucz licencji.

## Aktualizacja

Zainstalowany program sam sprawdza nowe wersje. Wystarczy kliknąć wersję w pasku stanu
i wybrać „Pobierz i zainstaluj”. Pobierane są tylko zmienione części programu.

## Nowa instalacja

1. Pobierz z [najnowszego wydania](../../releases/latest) wszystkie pliki `app-…`, `ml-…` i `models-…`.
2. Jeśli paczka ma części (`.zip.001`, `.zip.002`), połącz je w jeden plik `.zip`, np. w wierszu poleceń:
   `copy /b ml-WERSJA.zip.001 + ml-WERSJA.zip.002 ml-WERSJA.zip`.
3. Rozpakuj wszystkie paczki do jednego folderu, np. `C:\LiDAR_Toolbox`.
4. Uruchom `LiDAR_Toolbox.exe` i wpisz klucz licencji.

Szczegóły (sterownik NVIDIA, ustawienia Windows, pierwsze uruchomienie): `Instrukcja_instalacji.pdf`
w folderze programu.

## Pliki wydania

| Plik | Zawartość |
|---|---|
| `app-<wersja>.zip` | program |
| `ml-<wersja>.zip[.NNN]` | środowisko ML (torch, CUDA); zmienia się rzadko |
| `models-<wersja>.zip` | modele dostarczane z programem |
| `manifest.json`, `manifest.json.sig` | opis wersji i podpis używany przez aktualizację w programie |

Paczka bez zmian względem poprzedniej wersji nie jest wysyłana ponownie. Wtedy jej plik jest w jednym
z wcześniejszych wydań, a `manifest.json` wskazuje, w którym.
