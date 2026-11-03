# Moje Kalorie — wersja startowa

Prywatna aplikacja PWA na iPhone'a. Dane posiłków i cel kalorii zapisują się lokalnie w przeglądarce (localStorage). Klasyfikacja zdjęć używa modelu Food-101 przez Transformers.js i WebAssembly; po pobraniu model może być buforowany przez przeglądarkę.

## Ważne ograniczenia tej wersji
- Model rozpoznaje jedną główną kategorię potrawy z listy 101 klas; nie rozdziela niezawodnie składników mieszanych dań.
- Gramatura nie jest mierzona ze zdjęcia. Użytkownik wpisuje/zmienia porcję.
- Wartości kcal i makro są orientacyjnymi wartościami startowymi dla wybranych dań, a nie bazą wszystkich produktów. Należy je zweryfikować.
- Pierwsze uruchomienie klasyfikatora wymaga internetu i pobrania modelu (duży plik, ok. 90 MB). Rozpoznawanie wykonuje się lokalnie w przeglądarce.
- To prototyp do testów, nie narzędzie medyczne ani precyzyjny pomiar dietetyczny.

## Publikacja bez opłat
PWA musi być dostępna pod adresem HTTPS. Można użyć darmowego GitHub Pages:
1. Utwórz prywatne repozytorium na GitHub (lub publiczne, jeśli nie przeszkadza Ci publiczny kod).
2. Wgraj wszystkie pliki z tego folderu do repozytorium.
3. W ustawieniach repozytorium włącz Pages, źródło `Deploy from a branch`, branch `main`, folder `/root`.
4. Otwórz otrzymany adres w Safari na iPhonie.
5. W Safari: Udostępnij → Dodaj do ekranu początkowego → Dodaj.

## Test lokalny
Serwis service worker i instalacja PWA wymagają HTTPS albo localhost. Samo otwarcie pliku index.html nie wystarczy do testu instalacji.

## Pliki
- index.html — aplikacja
- manifest.webmanifest — nazwa i ikony PWA
- sw.js — cache aplikacji
- icon-192.png / icon-512.png — ikony
