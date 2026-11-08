# Dziewięć pierwszych piątków — aplikacja

Samodzielna aplikacja (PWA) na Androida: działa bez internetu i bez Claude'a, dane zostają na telefonie dziecka.

## Jak uruchomić na Androidzie (najprostsza droga)
1. Załóż darmowe konto na github.com i utwórz nowe repozytorium (np. `9-piatkow`).
2. Wgraj całą zawartość tego folderu (index.html, manifest.json, sw.js, lib/, icons/).
3. Settings → Pages → Branch: `main` → Save. Po minucie aplikacja będzie pod adresem
   `https://TWOJA-NAZWA.github.io/9-piatkow/`.
4. Otwórz ten adres w Chrome na Androidzie → menu ⋮ → „Zainstaluj aplikację”.
   Ikona pojawi się na ekranie głównym, aplikacja działa offline.

Uwaga: aparat i podpisy kodów wymagają adresu https:// — otwarcie samego pliku z dysku nie wystarczy.

## Jak zrobić plik APK / wersję do Google Play
1. Wejdź na https://www.pwabuilder.com i wpisz adres z kroku 3.
2. Wybierz „Package for stores” → Android. Dostaniesz gotowy plik .apk (do instalacji
   bezpośredniej) oraz .aab (do Sklepu Google Play, konto dewelopera: jednorazowo 25 USD).

## Jak działa potwierdzanie (QR)
- Ksiądz w aplikacji: Ustawienia → Panel duszpasterza → tworzy klucz parafii (PIN).
- **Kod parafii** dzieci skanują raz (np. na katechezie).
- **Kod na pierwszy piątek** ksiądz generuje na konkretną datę, drukuje lub pokazuje po Mszy.
  Kod jest podpisany kryptograficznie (ECDSA P-256) — dziecko nie podrobi go samo.
- Aplikacja przyjmuje kod tylko w dniu, na który go wydano, i pilnuje ciągłości
  9 piątków z rzędu. Gdy piątek zostanie pominięty, proponuje nową serię.
- „Tryb próbny” w ustawieniach wyłącza sprawdzanie dnia — do testów.

Ograniczenie: zdjęcie kodu przesłane koledze zadziała tego samego dnia. Dlatego najlepiej
pokazywać kod osobiście, np. przy wyjściu z kościoła lub po spowiedzi.
