# Przykład programu Python - "Gra w zgadywanie" (Klasa 7)

## Opis projektu
Prosta gra tekstowa, w której komputer wybiera losową liczbę, a gracz próbuje ją odgadnąć. Program wykorzystuje podstawowe konstrukcje języka Python.

## Cele edukacyjne
- Praktyczne zastosowanie zmiennych, pętli i warunków
- Obsługa wejścia użytkownika
- Generowanie liczb losowych
- Strukturyzacja programu

## Kod programu

### Wersja podstawowa
```python
import random

# Generowanie losowej liczby
liczba_do_odgadniecia = random.randint(1, 100)
liczba_prob = 0
max_prob = 7

print("=== GRA W ZGADYWANIE ===")
print("Zgadnij liczbę od 1 do 100!")
print(f"Masz {max_prob} prób.")
print()

# Główna pętla gry
while liczba_prob < max_prob:
    # Pobranie liczby od gracza
    try:
        propozycja = int(input("Podaj swoją propozycję: "))
    except ValueError:
        print("To nie jest liczba! Spróbuj jeszcze raz.")
        continue
    
    liczba_prob += 1
    pozostalo_prob = max_prob - liczba_prob
    
    # Sprawdzenie propozycji
    if propozycja == liczba_do_odgadniecia:
        print(f"🎉 BRAWO! Odgadłeś za {liczba_prob} razem!")
        break
    elif propozycja < liczba_do_odgadniecia:
        if pozostalo_prob > 0:
            print(f"Za mało! Pozostało prób: {pozostalo_prob}")
        else:
            print("Za mało!")
    else:
        if pozostalo_prob > 0:
            print(f"Za dużo! Pozostało prób: {pozostalo_prob}")
        else:
            print("Za dużo!")

# Koniec gry
if liczba_prob >= max_prob:
    print(f"Koniec prób! Liczba to: {liczba_do_odgadniecia}")

print("Dzięki za grę!")
```

### Wersja rozszerzona (dla zdolnych)
```python
import random
import time

def wyswietl_tytul():
    """Wyświetla tytuł gry"""
    print("=" * 30)
    print("    GRA W ZGADYWANIE")
    print("=" * 30)
    print()

def pobierz_poziom_trudnosci():
    """Pozwala graczowi wybrać poziom trudności"""
    print("Wybierz poziom trudności:")
    print("1. Łatwy (1-50, 10 prób)")
    print("2. Średni (1-100, 7 prób)")
    print("3. Trudny (1-200, 5 prób)")
    
    while True:
        try:
            wybor = int(input("Twój wybór (1-3): "))
            if wybor == 1:
                return 50, 10
            elif wybor == 2:
                return 100, 7
            elif wybor == 3:
                return 200, 5
            else:
                print("Wybierz 1, 2 lub 3!")
        except ValueError:
            print("Podaj liczbę 1, 2 lub 3!")

def graj_gre():
    """Główna funkcja gry"""
    wyswietl_tytul()
    
    # Wybór poziomu
    max_liczba, max_prob = pobierz_poziom_trudnosci()
    liczba_do_odgadniecia = random.randint(1, max_liczba)
    
    print(f"\nZgadnij liczbę od 1 do {max_liczba}!")
    print(f"Masz {max_prob} prób.")
    print()
    
    liczba_prob = 0
    historia_prob = []
    
    # Główna pętla gry
    while liczba_prob < max_prob:
        # Pobranie liczby od gracza
        try:
            propozycja = int(input(f"Próba {liczba_prob + 1}/{max_prob}: "))
            
            # Sprawdzenie czy liczba jest w zakresie
            if propozycja < 1 or propozycja > max_liczba:
                print(f"Liczba musi być od 1 do {max_liczba}!")
                continue
                
        except ValueError:
            print("To nie jest liczba! Spróbuj jeszcze raz.")
            continue
        
        liczba_prob += 1
        historia_prob.append(propozycja)
        pozostalo_prob = max_prob - liczba_prob
        
        # Sprawdzenie propozycji
        if propozycja == liczba_do_odgadniecia:
            print(f"🎉 BRAWO! Odgadłeś za {liczba_prob} razem!")
            print(f"Twoje próby: {historia_prob}")
            return True
        elif propozycja < liczba_do_odgadniecia:
            if pozostalo_prob > 0:
                roznica = liczba_do_odgadniecia - propozycja
                if roznica <= 5:
                    print(f"Bardzo blisko! Za mało. Pozostało: {pozostalo_prob}")
                elif roznica <= 15:
                    print(f"Blisko! Za mało. Pozostało: {pozostalo_prob}")
                else:
                    print(f"Za mało! Pozostało: {pozostalo_prob}")
            else:
                print("Za mało!")
        else:
            if pozostalo_prob > 0:
                roznica = propozycja - liczba_do_odgadniecia
                if roznica <= 5:
                    print(f"Bardzo blisko! Za dużo. Pozostało: {pozostalo_prob}")
                elif roznica <= 15:
                    print(f"Blisko! Za dużo. Pozostało: {pozostalo_prob}")
                else:
                    print(f"Za dużo! Pozostało: {pozostalo_prob}")
            else:
                print("Za dużo!")
        
        # Pokazanie historii prób
        if len(historia_prob) > 1:
            print(f"Dotychczasowe próby: {historia_prob}")
        
        print()

    # Koniec gry - brak wygranych
    print(f"Koniec prób! Liczba to: {liczba_do_odgadniecia}")
    print(f"Twoje próby: {historia_prob}")
    return False

def main():
    """Funkcja główna z opcją powtarzania gry"""
    while True:
        if graj_gre():
            print("\n🎊 GRATULACJE! 🎊")
        else:
            print("\n😔 Może następnym razem!")
        
        print("\nCzy chcesz zagrać jeszcze raz?")
        odpowiedz = input("Tak (t) / Nie (n): ").lower()
        
        if odpowiedz != 't' and odpowiedz != 'tak':
            break
    
    print("Dzięki za grę! Do zobaczenia! 👋")

# Uruchomienie gry
if __name__ == "__main__":
    main()
```

## Instrukcja dla uczniów

### Krok 1: Przygotowanie środowiska
1. Uruchom IDLE lub inny edytor Python
2. Utwórz nowy plik i zapisz jako `gra_zgadywanie.py`

### Krok 2: Import bibliotek
```python
import random  # do generowania losowych liczb
```

### Krok 3: Podstawowe zmienne
```python
liczba_do_odgadniecia = random.randint(1, 100)  # liczba do odgadnięcia
liczba_prob = 0  # licznik prób
max_prob = 7     # maksymalna liczba prób
```

### Krok 4: Główna pętla
- Użyj `while` do powtarzania prób
- Pobierz liczbę od użytkownika używając `input()`
- Porównaj z wylosowaną liczbą
- Wyświetl odpowiednią informację

### Krok 5: Testowanie
1. Uruchom program (F5 w IDLE)
2. Przetestuj różne scenariusze
3. Sprawdź czy program reaguje na błędne dane

## Możliwe rozszerzenia

### Poziom podstawowy
- Dodanie licznika prób
- Informacja o pozostałych próbach
- Lepsze komunikaty dla użytkownika

### Poziom średni
- Obsługa błędów (try/except)
- Historia poprzednich prób
- Różne poziomy trudności

### Poziom zaawansowany
- System punktacji
- Zapisywanie najlepszych wyników do pliku
- Graficzny interfejs użytkownika (tkinter)

## Pojęcia do omówienia

### Podstawowe
- **Zmienne** - przechowywanie danych
- **Pętle while** - powtarzanie kodu
- **Instrukcje warunkowe** - podejmowanie decyzji
- **Input/Output** - komunikacja z użytkownikiem

### Zaawansowane
- **Funkcje** - organizacja kodu
- **Obsługa wyjątków** - reakcja na błędy
- **Moduły** - wykorzystanie gotowych bibliotek

## Ocenianie

### Kryteria podstawowe
- [x] Program generuje losową liczbę
- [x] Pobiera dane od użytkownika
- [x] Porównuje liczby i wyświetla rezultat
- [x] Program kończy się po osiągnięciu celu lub wyczerpaniu prób

### Kryteria rozszerzone
- [x] Obsługa błędnych danych wejściowych
- [x] Czytelny i skomentowany kod
- [x] Dodatkowe funkcjonalności (historia, poziomy)
- [x] Estetyczne formatowanie komunikatów

## Dla nauczyciela

### Przygotowanie
1. Sprawdź czy Python działa na wszystkich komputerach
2. Przygotuj przykłady do demonstracji
3. Zaplanuj czas na debugowanie z uczniami

### Częste problemy i rozwiązania

#### Problem: "NameError: name 'random' is not defined"
**Rozwiązanie**: Brakuje `import random` na początku

#### Problem: Program nie reaguje na wprowadzanie danych
**Rozwiązanie**: Sprawdź czy jest `input()` w pętli

#### Problem: Pętla działa w nieskończoność
**Rozwiązanie**: Sprawdź warunek pętli i czy zmienna licznika jest modyfikowana

### Wskazówki metodyczne
- Pozwól uczniom eksperymentować z kodem
- Zachęcaj do dodawania własnych pomysłów
- Organizuj sesje code review
- Pokazuj różne sposoby rozwiązania tego samego problemu