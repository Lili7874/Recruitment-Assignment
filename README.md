# AI Article Processor

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
  **-Kod generowany przez API OpenAI zawiera jedynie strukturę HTML przeznaczoną do wstawienia pomiędzy tagami <body> i </body>.**<br>
  **-Tag <img> używa src="image_placeholder.jpg" jako tymczasowego odnośnika oraz zawiera atrybut alt z promptem do wygenerowania odpowiedniej grafiki.**<br>
  
## Uwaga: W kodzie HTML nie ma stylów CSS ani JavaScript.
