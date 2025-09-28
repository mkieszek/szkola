# Narzędzia i Konfiguracja

Instrukcje instalacji i konfiguracji narzędzi potrzebnych do realizacji lekcji informatyki w środowisku Linux Mint 20.1.

## Podstawowe narzędzia systemowe

### Już zainstalowane w Linux Mint 20.1
- **LibreOffice** - pakiet biurowy (Writer, Calc, Impress)
- **Firefox** - przeglądarka internetowa
- **GIMP** - edycja grafiki rastrowej
- **Inkscape** - grafika wektorowa (może wymagać doinstalowania)
- **Audacity** - edycja dźwięku (może wymagać doinstalowania)

### Instalacja dodatkowych narzędzi

#### Scratch dla programowania
```bash
sudo apt update
sudo apt install scratch
```

#### Programowanie Python
```bash
sudo apt install python3 python3-pip idle3
pip3 install turtle
```

#### Narzędzia graficzne
```bash
sudo apt install inkscape audacity kdenlive
```

## Konfiguracja epoptes

### Dla administratora
Instrukcje konfiguracji systemu monitorowania epoptes na serwerze LTSP.

### Dla nauczyciela
Podstawowe komendy i funkcje dostępne podczas lekcji:
- Monitorowanie ekranów uczniów
- Blokowanie dostępu do aplikacji
- Wysyłanie wiadomości do klasy
- Zdalne sterowanie komputerami uczniów

## Zarządzanie środowiskiem LTSP

### Aktualizacja oprogramowania
Procedury aktualizacji aplikacji dostępnych dla uczniów.

### Instalacja nowego oprogramowania
Kroki instalacji dodatkowego oprogramowania w środowisku LTSP.

### Backup i restore
Procedury tworzenia kopii zapasowych ważnych plików i ustawień.

## Rozwiązywanie problemów

### Typowe problemy
- Problemy z dźwiękiem
- Problemy z siecią
- Awarie aplikacji
- Problemy z drukowaniem

### Kontakt z administratorem IT
Procedury zgłaszania problemów technicznych.

## Materiały dla Microsoft A1

### Wykorzystanie licencji
Jak korzystać z narzędzi Microsoft w środowisku Linux:
- Office 365 przez przeglądarkę
- OneDrive
- Microsoft Teams (jeśli potrzeba)

### Integracja z Windows (dla nauczycieli)
Synchronizacja materiałów między laptopem nauczyciela (Windows) a środowiskiem lekcyjnym (Linux).