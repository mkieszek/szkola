# Przykład projektu Scratch - "Animowana Kartka" (Klasa 6)

## Opis projektu
Uczniowie tworzą interaktywną kartkę z życzeniami, która zawiera animowane elementy, dźwięki i reakcje na kliknięcia.

## Cele edukacyjne
- Poznanie podstawowych bloków Scratch
- Zrozumienie pojęcia animacji
- Nauka obsługi zdarzeń (kliknięcia)
- Wprowadzenie do pętli i warunków

## Elementy projektu

### Sprite'y (postacie)
1. **Główna postać** - kot Scratch lub własny wybór
2. **Elementy dekoracyjne** - balony, confetti, kwiaty
3. **Tekst** - napis z życzeniami

### Tła
- **Tło główne** - kolorowe, świąteczne
- **Opcjonalnie**: przełączanie między tłami

### Animacje
1. **Poruszanie się postaci** - lewa/prawa, góra/dół
2. **Zmiana kostiumów** - efekt animacji
3. **Znikanie i pojawianie** - efekt "ghost"
4. **Obracanie** - kręcenie wokół własnej osi

### Dźwięki
- **Muzyka tła** - wesołe dźwięki
- **Efekty dźwiękowe** - przy kliknięciach
- **Mowa** - nagranie własnego głosu

## Instrukcja krok po kroku

### Krok 1: Przygotowanie tła
```scratch
// Wybierz tło z biblioteki lub narysuj własne
1. Kliknij ikonę "Wybierz tło"
2. Wybierz kolorowe, świąteczne tło
3. Opcjonalnie: dodaj elementy w edytorze graficznym
```

### Krok 2: Dodanie głównej postaci
```scratch
// Sprite kot Scratch
Kiedy kliknięto zieloną flagę
    idź do x: 0 y: 0
    pokaż
    zawsze
        idź o 10 kroków
        jeśli na brzegu, odbij się
    
Kiedy kliknięto ten sprite
    powiedz "Wszystkiego najlepszego!" przez 2 sek
    zagraj dźwięk "pop"
```

### Krok 3: Dodanie elementów dekoracyjnych
```scratch
// Sprite balon
Kiedy kliknięto zieloną flagę
    ukryj
    czekaj 2 sek
    pokaż
    powtarzaj
        zmień y o 5
        czekaj 0.1 sek
        zmień y o -5
        czekaj 0.1 sek
```

### Krok 4: Interakcja z użytkownikiem
```scratch
// Reakcja na kliknięcia
Kiedy kliknięto ten sprite
    zmień efekt kolorowy o 25
    ustaw rozmiar na 120%
    czekaj 0.2 sek
    ustaw rozmiar na 100%
```

## Rozszerzenia dla zdolnych

### Poziom średni
- Dodanie więcej sprite'ów z różnymi animacjami
- Użycie zmiennych do liczenia kliknięć
- Tworzenie prostych warunków if/else

### Poziom zaawansowany
- Komunikacja między sprite'ami (broadcast)
- Tworzenie własnych bloków (funkcji)
- Dodanie prostej gry (np. łapanie spadających obiektów)

## Przykładowe bloki do wykorzystania

### Ruch i wygląd
- `idź o X kroków`
- `obróć się o X stopni`
- `zmień kostium na następny`
- `ustaw efekt kolorowy na X`

### Dźwięk
- `zagraj dźwięk X`
- `zagraj dźwięk X do końca`
- `ustaw głośność na X%`

### Zdarzenia
- `kiedy kliknięto zieloną flagę`
- `kiedy kliknięto ten sprite`
- `kiedy naciśnięto klawisz spacja`

### Kontrola
- `czekaj X sek`
- `powtarzaj X razy`
- `powtarzaj`
- `jeśli X to`

## Ocenianie

### Kryteria podstawowe (dla wszystkich)
- [x] Projekt zawiera animowane sprite'y
- [x] Jest reakcja na kliknięcie
- [x] Użyto dźwięków
- [x] Projekt jest zapisany z odpowiednią nazwą

### Kryteria rozszerzone
- [x] Użyto pętli i warunków
- [x] Projekt jest kreatywny i oryginalny
- [x] Kod jest zorganizowany i czytelny
- [x] Dodano własne elementy graficzne

## Materiały dodatkowe

### Pliki do pobrania
- `szablon-kartka.sb3` - podstawowy szablon do rozpoczęcia
- `dzwieki-example.zip` - zbiór dźwięków do wykorzystania
- `tla-swiateczne.zip` - dodatkowe tła

### Linki przydatne
- [Scratch - oficjalna strona](https://scratch.mit.edu/)
- [Tutoriale Scratch](https://scratch.mit.edu/ideas)
- [Darmowe dźwięki](https://freesound.org/) - tylko z pomocą nauczyciela

## Troubleshooting - częste problemy

### Sprite nie porusza się
- Sprawdź czy jest blok "kiedy kliknięto zieloną flagę"
- Upewnij się, że sprite nie jest ukryty
- Sprawdź czy nie ma konfliktu z innymi skryptami

### Brak dźwięku
- Sprawdź głośność w systemie
- Upewnij się, że dźwięk jest załadowany
- Sprawdź czy blok dźwięku jest w odpowiednim miejscu

### Animacja nie działa płynnie
- Użyj bloków "czekaj" między zmianami
- Zmniejsz wartości w blokach ruchu
- Sprawdź czy nie ma zbyt wielu jednoczesnych animacji

## Dla nauczyciela

### Przygotowanie lekcji
1. Uruchom Scratch na wszystkich komputerach
2. Przygotuj przykłady do demonstracji
3. Sprawdź czy działa dźwięk na wszystkich stanowiskach

### Wsparcie uczniów
- Zachęcaj do eksperymentowania
- Pokaż jak szukać pomocy w dokumentacji Scratch
- Organizuj prezentacje prac między uczniami

### Ocena projektów
- Zwróć uwagę na proces, nie tylko efekt końcowy
- Doceniaj kreatywność i oryginalność
- Pomagaj w debugowaniu, ale pozwól uczniom samodzielnie rozwiązywać problemy