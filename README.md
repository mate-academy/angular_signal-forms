# Moonbase Control: Tworzenie formularza z Signal Forms

Zadanie z modułu Angular. Repozytorium zawiera kod startowy aplikacji Moonbase Control dla tej lekcji.

## Zadanie

Utwórz formularz zgłaszania incydentu w przygotowanym wcześniej komponencie `ReportIncident`.

Formularz powinien umożliwiać operatorowi wprowadzenie:

- tytułu incydentu,
- opisu incydentu,
- poziomu zagrożenia.

#### 1. Przygotuj model danych formularza
W pliku `report-incident.ts`:

- utwórz interfejs `IncidentFormData`,
- dodaj do niego pola `title`, `description` oraz `severity`,
- dla `severity` wykorzystaj istniejący `IncidentSeverity`,
- uwzględnij możliwość pustej wartości przed wybraniem poziomu zagrożenia.

#### 2. Utwórz stan formularza
- Utwórz `incidentModel` za pomocą `signal()`.
- Ustaw początkowe wartości wszystkich pól formularza.
- Na podstawie `incidentModel` utwórz `incidentForm` za pomocą `form()`.

#### 3. Przygotuj pola formularza
W pliku `report-incident.html`:

- utwórz pole `Title` przy użyciu `mat-form-field` i `matInput`,
- utwórz pole `Description` przy użyciu `mat-form-field`, `textarea` i `matInput`,
- połącz oba pola z odpowiednimi polami `incidentForm` za pomocą `[formField]`.

#### 4. Dodaj wybór poziomu zagrożenia
W pliku `report-incident.ts`:

- pobierz dostępne wartości `IncidentSeverity` i zapisz je w komponencie.
W pliku `report-incident.html`:

- utwórz pole `Severity` za pomocą `mat-select`,
- połącz je z `incidentForm.severity`,
- wygeneruj dostępne poziomy zagrożenia za pomocą `@for`,
- dodaj pustą opcję reprezentującą brak wybranego poziomu zagrożenia.

#### 5. Sprawdź działanie formularza
- Wyświetl tymczasowo aktualne wartości `incidentModel`.
- Wprowadź dane we wszystkich polach.
- Sprawdź, czy zmiana wartości kontrolek automatycznie aktualizuje model formularza.
💡 `incidentModel` przechowuje dane formularza, `form()` tworzy na jego podstawie strukturę pól, a `[formField]` łączy te pola z kontrolkami w interfejsie.

## Jak zacząć

1. Zrób fork tego repozytorium na swoje konto GitHub.
2. Sklonuj swój fork na komputer.
3. Zainstaluj zależności: `npm install`.
4. Uruchom aplikację: `npm start`.
5. Jeśli zadanie korzysta z danych z API, uruchom w drugim terminalu mock API: `npm run api`.

## Jak oddać zadanie

1. Zapisz zmiany w commicie i wypchnij je do swojego forka.
2. Otwórz Pull Request z forka do repozytorium `mate-academy/angular_signal-forms`, do brancha `main`.
3. Platforma uruchomi review Twojego Pull Requesta.
