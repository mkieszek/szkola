# Copilot Instructions - Dokumentacja Informatyki dla Szkoły Podstawowej

## Kontekst Projektu

Ten projekt służy do budowania dokumentacji i przygotowania programu lekcji informatyki dla szkoły podstawowej, klasy 4-8. Dokumentacja jest tworzona przez nauczyciela informatyki pracującego z uczniami o różnych potrzebach edukacyjnych.

## Środowisko Techniczne

### Infrastruktura Szkolna
- **Pracownia komputerowa**: Linux Mint 20.1 uruchamiany przez LTSP
- **Laptopy nauczycieli**: Windows 10 Pro podłączone do domeny Entra ID (Azure AD)
- **Monitorowanie**: System epoptes do nadzorowania pracy uczniów
- **Licencje**: Microsoft A1 dla nauczycieli i uczniów

### Ograniczenia Czasowe
- **Częstotliwość lekcji**: Jedna lekcja tygodniowo
- **Czas lekcji**: 45 minut

## Grupa Docelowa

### Uczniowie
- **Klasy**: 4, 5, 6, 7, 8 szkoły podstawowej
- **Specjalne potrzeby**: W klasach są dzieci z orzeczeniem o specjalnych potrzebach edukacyjnych
- **Różnorodność**: Dostosowanie materiałów do różnych stylów uczenia się i tempa pracy

### Nauczyciele
- Pracują na laptopach z Windows 10 Pro
- Potrzebują materiałów gotowych do użycia w środowisku Linux Mint
- Muszą uwzględniać potrzeby uczniów ze specjalnymi potrzebami edukacyjnymi

## Podstawa Programowa

Realizujemy podstawę programową dla informatyki w szkole podstawowej zgodnie z:
**URL**: https://zpe.gov.pl/podstawa-programowa/szkola-podstawowa/informatyka

### Kluczowe Obszary
- Programowanie i algorytmy
- Technologie informacyjno-komunikacyjne
- Bezpieczeństwo cyfrowe
- Grafika komputerowa i multimedia
- Podstawy sieci i internetu

## Wytyczne dla Tworzenia Dokumentacji

### Format i Struktura
1. **Język**: Polski (wszystkie materiały w języku polskim)
2. **Format plików**: Markdown (.md) jako główny format dokumentacji
3. **Struktura lekcji**: 
   - Cel lekcji
   - Materiały potrzebne
   - Plan lekcji (45 minut)
   - Zadania dla uczniów
   - Ocenianie
   - Materiały dodatkowe

### Dostosowania dla Specjalnych Potrzeb Edukacyjnych
- Uwzględnij różne style uczenia się
- Przygotuj alternatywne metody prezentacji materiału
- Zaproponuj zadania o różnym poziomie trudności
- Uwzględnij potrzeby uczniów z trudnościami w nauce

### Kompatybilność Systemowa
- **Pierwotne środowisko**: Linux Mint 20.1
- **Narzędzia**: Dostępne w repozytoriach Linux Mint
- **Alternatywy**: Jeśli sugerowane oprogramowanie wymaga Windows, zaproponuj alternatywy dla Linux
- **Instrukcje**: Jasne kroki instalacji i konfiguracji dla środowiska LTSP

### Praktyczne Aspekty
- **Epoptes**: Uwzględnij możliwości monitorowania i zarządzania klasą
- **Zarządzanie czasem**: 45-minutowe lekcje wymagają efektywnego planowania
- **Materiały offline**: Przygotuj materiały działające bez stałego dostępu do internetu

## Przykładowa Struktura Lekcji

```markdown
# Lekcja X: [Tytuł]
**Klasa**: [4/5/6/7/8]
**Czas**: 45 minut
**Temat podstawy programowej**: [odniesienie do podstawy]

## Cel lekcji
- [cel główny]
- [cele szczegółowe]

## Materiały i narzędzia
- Linux Mint 20.1
- [konkretne aplikacje]
- [materiały do pobrania]

## Plan lekcji (45 min)
1. **Wprowadzenie** (5 min)
2. **Prezentacja materiału** (15 min)
3. **Ćwiczenia praktyczne** (20 min)
4. **Podsumowanie** (5 min)

## Zadania
### Zadanie podstawowe
[opis dla wszystkich uczniów]

### Zadanie rozszerzone
[dla uczniów szybciej opanowujących materiał]

### Dostosowania dla SNE
[modyfikacje dla uczniów ze specjalnymi potrzebach]

## Ocenianie
[kryteria i metody oceny]

## Materiały dodatkowe
[linki, pliki, zasoby]
```

## Wskazówki dla Copilota

Kiedy pomagasz w tworzeniu lub edytowaniu dokumentacji:

1. **Zawsze używaj języka polskiego** w treści lekcji i dokumentacji
2. **Sprawdzaj zgodność z podstawą programową** - odnosz się do konkretnych wymagań
3. **Uwzględniaj ograniczenia czasowe** - 45 minut to niewiele czasu
4. **Pamiętaj o środowisku Linux Mint** - sugeruj narzędzia dostępne w tym systemie
5. **Myśl o różnorodności uczniów** - przygotuj warianty dla różnych potrzeb
6. **Bądź praktyczny** - każda lekcja musi być wykonalna w rzeczywistych warunkach szkolnych
7. **Uwzględniaj możliwości epoptes** - jak nauczyciel może skutecznie zarządzać klasą

## Struktura Katalogów

Sugerowana organizacja plików w repozytorium:
```
/klasa-4/          # Materiały dla klasy 4
/klasa-5/          # Materiały dla klasy 5
/klasa-6/          # Materiały dla klasy 6
/klasa-7/          # Materiały dla klasy 7
/klasa-8/          # Materiały dla klasy 8
/zasoby/           # Wspólne zasoby, pliki, obrazki
/narzędzia/        # Instrukcje instalacji i konfiguracji narzędzi
/podstawa-programowa/ # Dokumenty odniesienia do podstawy programowej
```

Każdy katalog klasy powinien zawierać:
- `README.md` - przegląd materiałów dla tej klasy
- Pliki poszczególnych lekcji w formacie `lekcja-XX-temat.md`
- Katalog `/materialy/` z plikami do pobrania dla uczniów