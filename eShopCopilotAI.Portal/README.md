# eShop Copilot AI — Dashboard

Ten plik HTML jest **produkcyjną wersją dashboardu** dla systemu eShop Copilot AI.

## Funkcje

- **Asystent AI** — okno czatu, w którym użytkownik może zadawać pytania, otrzymywać rekomendacje i interpretacje danych.
- **Rekomendacje** — lista dynamicznych rekomendacji (karty), renderowanych w trybie DEMO ze stałymi danymi.
- **Alerty** — lista alertów z kolorowaniem według poziomu ważności (info, warning, critical).
- **KPI** — sekcja kluczowych wskaźników (sprzedaż, marża, liczba alertów i rekomendacji).
- **Toolbar** — filtry kategorii rekomendacji (Ceny, Zakupy, Anomalie, Info).

## Layout

- Układ oparty o CSS Grid (`grid-template-columns: 480px 1fr`), co daje szerszy panel czatu.
- Zawiera niewielki padding po lewej i prawej stronie, aby zawartość nie przylegała do krawędzi ekranu.
- Panel rekomendacji i alertów podzielony w proporcji ok. 60/40 wysokości.

## Tryb DEMO

- Wbudowane dane przykładowe:
  - 3 rekomendacje (karty)
  - 3 alerty
  - przykładowa rozmowa w oknie czatu
- Brak połączenia z API — funkcje `loadRecs()` i `loadAlerts()` wstrzykują dane statyczne.
- Można łatwo podpiąć prawdziwe API przez podmianę funkcji `loadRecs` i `loadAlerts`.

## Dalszy rozwój

- Podpięcie REST API lub WebSocket / SSE do pobierania rekomendacji i alertów w czasie rzeczywistym.
- Integracja z backendem w .NET (np. Azure Functions + Azure Service Bus).
- Obsługa logowania użytkownika (obecnie przycisk **Wyloguj** kieruje na `/logout`).

## Uruchomienie

Plik jest **samowystarczalny** — wystarczy otworzyć w przeglądarce:

```bash
open dashboard-production.html
```

Lub w systemie Windows:

```bash
start dashboard-production.html
```

