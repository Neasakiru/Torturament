# Tourturament

Aplikacja do organizowania turniejów w piłkarzyki (i nie tylko). Jeden plik `index.html`, czysty HTML, CSS i JS, bez instalacji i bez serwera.

## Uruchomienie

1. Otwórz `index.html` dwuklikiem (najlepiej w Chrome lub Edge).
2. Na górze kliknij **Utwórz nowy db.json** (albo **Otwórz db.json**, jeśli już go masz) i wskaż miejsce zapisu.
3. Od tej chwili każda zmiana zapisuje się automatycznie do pliku.

Po ponownym otwarciu strony przeglądarka poprosi o jedno kliknięcie: **Wznów zapis do pliku**.

## Gdzie są dane

- **Plik `db.json`** to główna baza (Chrome/Edge). Kopia zapasowa to zwykłe skopiowanie tego pliku.
- **Pamięć przeglądarki** to zapasowa kopia zapisywana zawsze, także gdy nie połączysz pliku.
- **Eksport / Import JSON** pozwalają ręcznie zrobić kopię albo przenieść bazę na inny komputer. W Firefoxie i Safari to jedyna droga do pliku, bo nie umieją zapisywać do niego automatycznie.

## Tworzenie turnieju

Przycisk **+ Nowa drabinka**. Poprzednie turnieje zostają w zakładce **Historia**.

| Ustawienie | Opcje |
|---|---|
| Tryb | **Wszyscy na wszystkich** (punkty i bilans) lub **drabinka pucharowa** (przegrany odpada) |
| Format meczu | jedna gra, **best of 3** lub **best of 5** |
| Rozmiar drużyny | 1–6 graczy |
| Punkty | za wygraną i przegraną (tylko w trybie „wszyscy na wszystkich”) |

## Jak grać

1. **Lobby.** Dodaj drużyny ręcznie albo dodaj samych graczy (**+ Dodaj gracza**) i kliknij **🎲 Wylosuj drużyny**. Wylosowane drużyny możesz od razu nazwać po swojemu albo przelosować (**🔄**). Nazwę zmienisz później przyciskiem **✎**.
2. **Start.** Kliknij **Start**. W trybie „wszyscy na wszystkich” drużyny można dodawać także w trakcie gry. W drabince skład zamyka się po starcie.
3. **Wyniki.** Wpisz wynik meczu. W best of 3/5 klikasz **Wpisz wynik** i podajesz wynik każdej gry. Remisów nie ma.
4. **Koniec.** W drabince turniej kończy się sam po finale. W trybie „wszyscy na wszystkich” kończysz go przyciskiem **🏁**.

## Dobrze wiedzieć

- Kolejka meczów jest losowa i układana tak, żeby ta sama drużyna nie grała dwa razy pod rząd. Przy 4 drużynach (i mniej) da się to uniknąć tylko częściowo. Przycisk **🔀** przelosuje kolejkę.
- Tabela sortuje według punktów, potem bilansu (w best of 3/5 najpierw różnicy gier), potem bramek zdobytych.
- W drabince wyniku nie zmienisz, jeśli zwycięzca zmieniłby się po rozegraniu kolejnych meczów. Najpierw wyczyść następny mecz.

## Własne logo

W `index.html` w nagłówku jest zakomentowana linia z `<img class="logo-img" src="logo.png">`. Odkomentuj ją, usuń blok `<svg class="logo-svg">` powyżej i połóż `logo.png` obok `index.html`. Wysokość logo ustawisz w CSS (`.logo-svg`, `.logo-img`).
