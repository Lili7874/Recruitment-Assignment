# 1. AI Article Processor

## Opis projektu

To jest prosta aplikacja w Pythonie, która:
1. Łączy się z **API OpenAI**.
2. Wczytuje treść artykułu z pliku tekstowego.
3. Przekazuje artykuł do API OpenAI, prosząc o wygenerowanie kodu HTML zgodnego z wytycznymi.
4. Zapisuje wygenerowany kod HTML do pliku `artykul.html`.

Kod HTML generowany przez AI zawiera strukturę artykułu z użyciem odpowiednich tagów HTML, miejsc na obrazy z odpowiednimi atrybutami `alt` oraz podpisami pod grafikami.

## Funkcjonalność

- **Łączenie z OpenAI API:** Aplikacja łączy się z API OpenAI, używając klucza API dostarczonego przez użytkownika.
- **Przetwarzanie tekstu artykułu:** Artykuł jest wczytywany z pliku `Zadanie.txt`.
- **Generowanie HTML:** Aplikacja przesyła treść artykułu wraz z promptem do OpenAI, prosząc o przekształcenie artykułu do formatu HTML zgodnego z zadaniem.
- **Zapis wyniku:** Wygenerowany kod HTML jest zapisywany w pliku `artykul.html`.

## Instalacja

1. **Klonowanie repozytorium:**
   ```bash
   git clone https://github.com/TwojeRepozytorium/AI-Article-Processor.git
   ```
2. **Przejście do katalogu projektu:**
  ```bash
  cd AI-Article-Processor
  ```
3. **Instalacja zależności:**
  Upewnij się, że masz zainstalowanego Pythona w wersji 3.8 lub wyższej.

4. **Zainstaluj wymagane pakiety:**
  ```bash
  pip install -r requirements.txt
  ```
## Użycie

1.**Dodanie klucza API OpenAI:**
  Utwórz plik .env w katalogu projektu i dodaj klucz API:
  ```bash
  OPENAI_API_KEY="YOUR_API_KEY"
  ```
2. **Uruchomienie aplikacji:**
  ```bash
  python Zadanie_testowe.py
  ```
## Efekt działania:
  Aplikacja odczyta plik Zadanie.txt, przetworzy treść artykułu z wykorzystaniem OpenAI API i zapisze wygenerowany HTML do artykul.html.

### Przykładowy Plik Wejściowy
  Plik Zadanie.txt powinien zawierać artykuł o sztucznej inteligencji, który zostanie przetworzony przez API OpenAI.

## Wymagania
  **-Python 3.8 lub nowszy**<br>
  **-Konto OpenAI z ważnym kluczem API**<br>

## Uwagi
  **-Kod generowany przez API OpenAI zawiera jedynie strukturę HTML przeznaczoną do wstawienia pomiędzy tagami 'body'.**<br>
  **-Tag <img> używa src="image_placeholder.jpg" jako tymczasowego odnośnika oraz zawiera atrybut alt z promptem do wygenerowania odpowiedniej grafiki.**<br>
  **-Tag img używa src="image_placeholder.jpg" jako tymczasowego odnośnika oraz zawiera atrybut alt z promptem do wygenerowania odpowiedniej grafiki.**<br>

## Uwaga: W kodzie HTML nie ma stylów CSS ani JavaScript.

# 2. Aplikacja do Generowania i Szablonowania Strony HTML na Podstawie Tekstu

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
