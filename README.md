# Aplikacja do Generowania i Szablonowania Strony HTML na Podstawie Tekstu

## Opis projektu

Aplikacja generuje stronę HTML na podstawie treści zawartej w pliku tekstowym `Zadanie.txt`. Wygenerowany HTML jest zgodny ze szczegółowymi wytycznymi dotyczącymi układu i stylizacji. Aplikacja automatycznie pobiera tytuł, nagłówki oraz główną treść artykułu z pliku, a następnie zapisuje wynik jako `podglad.html`. Dodatkowo aplikacja tworzy szablon `szablon.html` z uniwersalnymi placeholderami w miejsce rzeczywistej treści, co może być użyteczne jako baza do kolejnych projektów.

## Funkcjonalność

1. **Generowanie HTML na podstawie treści z pliku**:
   - Wysyłanie treści z pliku `Zadanie.txt` do API OpenAI w celu wygenerowania HTML zgodnie z wytycznymi.
   - Zapisanie wygenerowanego HTML do pliku `podglad.html`.

2. **Tworzenie szablonu HTML**:
   - Przetwarzanie wygenerowanego pliku HTML w celu zastąpienia rzeczywistej treści placeholderami.
   - Zapis szablonu z placeholderami jako `szablon.html`.

## Wymagania

- **Python 3.7+**
- **Klucz API OpenAI** (niezbędny do generowania treści przez API OpenAI)
- Biblioteki:
  - `openai`
  - `re` (wbudowana w Pythona, nie wymaga instalacji)

## Instalacja

1. **Klonowanie repozytorium**
   ```bash
   git clone <link-do-repozytorium>
   cd <nazwa-repozytorium>

2. **Instalacja wymaganych bibliotek**

   Zainstaluj bibliotekę openai, jeśli nie jest jeszcze zainstalowana:

   ```bash
   pip install openai
   Konfiguracja klucza API
   ```

3. **W pliku Zadanie.py wstaw swój klucz API OpenAI w zmiennej API_KEY:**

   ```python
   API_KEY = 'wstaw-swoj-klucz-api'
   ```
   
4. **Przygotowanie pliku tekstowego**<br>

   Upewnij się, że plik Zadanie.txt zawiera tekst artykułu, który ma być użyty do generowania HTML.

5. **Uruchomienie aplikacji**
      **Uruchom skrypt Python:**
   
   ```bash
   python Zadanie.py
   ```
   
7. **Po uruchomieniu aplikacja:**

      **-Wygeneruje plik podglad.html z pełnym kodem HTML.**<br>
      **-Utworzy plik szablon.html z uniwersalnymi placeholderami.**<br>
      **-Pliki wynikowe podglad.html i szablon.html będą dostępne w katalogu projektu.**<br>

**Struktura plików projektu**<br>
   **-Zadanie.py: Główny skrypt aplikacji.**<br>
   **-Zadanie.txt: Plik tekstowy z treścią artykułu do przetworzenia.**<br>
   **-podglad.html: Wygenerowany kod HTML.**<br>
   **-szablon.html: Szablon HTML z placeholderami.**<br>
