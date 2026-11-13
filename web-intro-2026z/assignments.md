# Zadania, rubryki i przykładowa struktura plików

## Zasady wspólne
- Jedno repozytorium studenta zawierające niezależne katalogi zad1, zad2, zad3, zad4. Każdy katalog ma własny index.html i działa jako osobna wersja CV.
- Można używać fikcyjnych danych do CV; prawdziwe dane osobowe nie są potrzebne.
- Każda kolejna wersja rozwija poprzednią. Gotowe działające strony należy udostępnić na GitHub Pages.
- Zgłoszenie przez PR zawiera link do repozytorium oraz link do zad4 i wskazanie docelowej oceny. Nie zawiera numeru indeksu, nazwiska ani wrażliwych danych.
- Do oceny 3,0 nie wymaga się obrony. Dla wyższych ocen w ścieżce projektowej wymagana jest prezentacja i zmiany na żywo.
- Standardowy termin oddania pakietu 1–4: koniec L4; można oddać wcześniej.

## Zadanie 1 — CV HTML
Plik zad1/index.html. Wymagane: poprawny dokument HTML5, h1, opis, co najmniej trzy sekcje (np. edukacja, doświadczenie, umiejętności), lista ul/ol, link a, sensowne znaczniki nagłówków i section/main. Wersja działa bez CSS i JavaScript.

## Zadanie 2 — CSS
Katalog zad2 z index.html i style.css. Wymagane: osobny arkusz, czytelny układ, własna typografia i kolory, układ oparty o Flexbox lub Grid, rozwiązanie działające na mobilnych ekranach, sensowny kontrast.

## Zadanie 3 — JavaScript
Katalog zad3 z index.html, style.css i script.js. Wymagane: co najmniej dwa działania po stronie klienta reagujące na użytkownika, np. przycisk motywu, rozwijanie sekcji, filtrowanie umiejętności, pokazanie/ukrycie dodatkowych szczegółów. Obsługa zdarzeń przez addEventListener; bez błędów JS w konsoli.

## Zadanie 4 — JSON + fetch + DOM
Katalog zad4 z index.html, style.css, script.js, cv.json. Wymagane:
1. Dane opisujące przynajmniej trzy sekcje CV znajdują się w cv.json, a nie w HTML.
2. JavaScript wywołuje fetch('./cv.json'), przetwarza JSON i generuje elementy DOM.
3. Zmiana cv.json skutkuje zmianą treści strony bez ręcznej edycji HTML.
4. Widoczny jest stan ładowania i komunikat w przypadku błędu sieci.
5. Strona jest uruchamiana przez GitHub Pages (otwieranie pliku jako file:// nie jest zalecane).
6. Nie używaj innerHTML dla niezweryfikowanego tekstu; bezpieczniejsze są createElement i textContent.
W katalogu examples/ znajduje się przykładowy format JSON; student może go rozbudować.

## Ścieżka na 4,0 A — kurs
Ukończ zaakceptowany kurs z zakresu technologii webowych. Preferowane: IBM HTML/CSS/JS, University of Michigan JavaScript/PHP, SkillUp Spring (dla osób znających Javę). Dokumentacja: certyfikat, osiągnięcia na platformie, zrzuty pokazujące ukończone moduły/ćwiczenia; bez konieczności publicznego publikowania dokumentacji z danymi osobowymi. Możliwa jest równoważna bezpłatna ścieżka MDN/freeCodeCamp i dokumentacja wykonanych ćwiczeń.

## Ścieżka na 4,0 B — projekt
Rozbuduj zad4 o formularz edycji pól CV, walidację (co najmniej dwa warunki), zapis zmienionych danych w localStorage i przywracanie przy kolejnym otwarciu strony. Przedstaw działające rozwiązanie i wykonaj jedną niewielką zmianę na żywo (np. nowe pole lub regułę walidacji). Oczekiwana wiedza: DOM, zdarzenia, JSON, fetch, localStorage, walidacja, rola serwera.

## Ścieżka na 5,0 — Biblioteka
Frontend HTML/CSS/JS na GitHub Pages. Backend preferowany: Supabase Data API oraz PostgreSQL; alternatywnie równoważny REST backend w PHP, Javie albo Node.js po uzgodnieniu.
Model:
- authors: id, name
- books: id, title, publication_year, author_id (klucz obcy do authors)
Wymagane:
- CRUD autorów i książek przez formularze
- widok listy z nazwiskiem autora przy każdej książce
- filtrowanie/wyszukiwanie oraz walidacja danych
- async/await, obsługa loading i błędów API
- poprawny związek 1:N i integralność referencyjna
- uwierzytelnianie do zapisu, prawidłowe RLS / równoważna autoryzacja
- tylko klucz publishable/anon w frontendzie; nigdy secret/service_role
- README z opisem architektury i uruchomienia; działające demo
- kurs lub równoważny program nauki oraz obrona
Na obronie: prezentacja, wyjaśnienie przepływu HTTP/REST i relacji SQL, dwie drobne zmiany, np. nowe pole books.genre oraz filtr po autorze.

## Przykłady pytań na obronie
- Jak działa fetch i co oznacza asynchroniczność?
- Co robi textContent? Jak działa DOM?
- Jakie statusy HTTP zwraca API przy błędzie?
- Czym jest żądanie GET, POST, PATCH i DELETE?
- Na czym polega klucz obcy i relacja jeden-do-wielu?
- Czym różni się klucz publishable od secret w Supabase?
- Czym jest RLS i dlaczego nie wolno dawać publicznego nieograniczonego dostępu do zapisu?

## Co jest oceniane
3,0: kompletność zadań, działające linki i podstawowe kryteria funkcjonalne.
4,0 A: potwierdzona realizacja zaakceptowanej ścieżki nauki.
4,0 B: działające rozszerzenie i zrozumienie rozwiązania na rozmowie.
5,0: działająca aplikacja i baza danych, bezpieczeństwo, jakość implementacji oraz zrozumienie i modyfikacje podczas rozmowy.
