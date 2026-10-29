# LEVY CUSTOM — 1 OF 1

Statyczny prototyp strony promującej ręcznie malowane dżinsy. Łączy prezentację produktu, opis procesu personalizacji, FAQ i wezwania do przejścia na zewnętrzną platformę sprzedażową.

**Status:** demo landing page. Repozytorium zawiera warstwę prezentacyjną; zakupy nie są obsługiwane przez tę stronę.

## Co jest zaimplementowane

- Responsywny układ z sekcjami otwierającymi ofertę, porównaniem alternatyw i opisem procesu pracy.
- Sekcja FAQ z rozwijaniem odpowiedzi; otwarcie kolejnej pozycji zamyka poprzednią.
- Animacje sekcji przy przewijaniu, oparte na `IntersectionObserver`.
- Odnośniki do Vinted i TikToka oraz nawigacja do końcowej sekcji oferty.

## Stos i architektura

[index.html](index.html) zawiera cały HTML, CSS i JavaScript. Projekt nie używa frameworka, bundlera, pakietów npm, backendu ani bazy danych.

Wygląd opiera się na osadzonych stylach i zmiennych CSS. Skrypt obserwuje elementy `.reveal` i obsługuje kliknięcia `.faq-q`. Zewnętrznie pobierane są fonty Space Mono, Instrument Serif i DM Sans z Google Fonts.

## Uruchomienie lokalne

Wymagania: Git, Python 3 i współczesna przeglądarka.

```sh
git clone https://github.com/dzwoniar/LEVY-CUSTOM.git
cd LEVY-CUSTOM
python -m http.server 8000 --bind 127.0.0.1
```

Otwórz [http://127.0.0.1:8000](http://127.0.0.1:8000). Zatrzymanie serwera: `Ctrl+C`. Brak kroku instalacji i budowania.

## Struktura i miejsca zmian

```text
.
├── index.html   # oferta, FAQ, style i skrypty
└── README.md    # dokumentacja projektu
```

Treści i docelowe adresy CTA są bezpośrednio w HTML. Kolory oraz typografię zmienisz w `<style>`, a zachowanie FAQ i animacji w końcowym `<script>`.

## Granice demo

Linki sprzedażowe prowadzą do ogólnej strony Vinted, a link społecznościowy do ogólnej strony TikToka. Nie wskazują konkretnego profilu ani oferty. W kodzie nie ma katalogu produktów, koszyka, płatności ani formularza zamówienia.

Deklaracje o produkcie, dostawie i warunkach transakcji są treścią demonstracyjnej strony. Uruchomienie realnej oferty wymaga potwierdzenia tych treści i podmiany odnośników na docelowe.

## Sprawdzenie po zmianach

Repozytorium nie zawiera testów automatycznych. Sprawdź lokalnie układ na telefonie i komputerze, widoczność sekcji podczas przewijania oraz otwieranie i zamykanie FAQ. Docelowe adresy CTA można zweryfikować w kodzie bez wykonywania transakcji.
