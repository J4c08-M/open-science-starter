# 📘 Przewodnik 3: ORCID
## Profil badacza i połączenie z Zenodo

---

## Czym jest ORCID?

**ORCID** (Open Researcher and Contributor ID) to bezpłatny, unikalny identyfikator dla badaczy i autorów — jak PESEL, ale dla nauki. Wygląda tak:

```
https://orcid.org/0000-0002-1825-0097
```

ORCID rozwiązuje problem niejednoznaczności autorstwa — jeśli masz popularne imię i nazwisko, ORCID jednoznacznie identyfikuje Cię jako autora pracy, projektu lub publikacji.

**Dlaczego warto założyć ORCID jako student?**
- Budujesz swój profil naukowy od początku studiów
- Zenodo automatycznie przypisuje Twoje projekty do profilu ORCID
- Wymagany przez coraz więcej wydawców i grantodawców (NCN, Horizon Europe)
- Widoczny w bazach danych: Scopus, Web of Science, PubMed, OpenAIRE

---

## Krok 1 — Załóż konto ORCID

1. Wejdź na [orcid.org](https://orcid.org) → kliknij **„Sign in / Register"**
2. Kliknij **„Register now"**
3. Wypełnij formularz:
   - Imię i nazwisko (używaj wersji, której będziesz używać w publikacjach)
   - Adres e-mail (najlepiej uczelniany)
   - Hasło
4. Wybierz widoczność profilu: **„Everyone"** — publiczny profil jest kluczowy dla widoczności naukowej
5. Potwierdź e-mail

> Twój ORCID iD to 16-cyfrowy numer w formacie: `0000-0000-0000-0000`

---

## Krok 2 — Uzupełnij profil ORCID

Kliknij swoje imię po zalogowaniu → edytuj profil. Uzupełnij:

| Sekcja | Co wpisać | Priorytet |
|---|---|---|
| **Employment** | Uczelnia, rok rozpoczęcia studiów | Wysoki |
| **Education** | Kierunek, uczelnia, rok | Wysoki |
| **Works** | Publikacje, projekty (można importować automatycznie) | Średni |
| **Keywords** | Twoje zainteresowania naukowe | Niski |
| **Websites** | Link do GitHub, ResearchGate | Niski |

---

## Krok 3 — Połącz ORCID z Zenodo

1. Zaloguj się na [zenodo.org](https://zenodo.org)
2. Kliknij swój avatar → **„Linked accounts"** (lub **„Settings"** → **„Linked accounts"**)
3. Znajdź sekcję **ORCID** → kliknij **„Connect"**
4. Zaloguj się na ORCID i kliknij **„Authorize"**

Po połączeniu:
- Twoje rekordy na Zenodo będą automatycznie powiązane z ORCID
- Możesz importować swoje projekty Zenodo do profilu ORCID jako **„Works"**

---

## Krok 4 — Importuj projekt do ORCID (opcjonalnie)

Po uzyskaniu DOI na Zenodo, możesz go dodać do swojego profilu ORCID:

1. Zaloguj się na ORCID → sekcja **„Works"** → **„Add works"**
2. Wybierz **„Search & link"** → znajdź **„DataCite"** (to partner Zenodo)
3. Wyszukaj swój projekt po DOI lub nazwie → kliknij **„Add to ORCID record"**

---

## Krok 5 — Dodaj ORCID do pliku CITATION.cff

W pliku `CITATION.cff` w swoim projekcie:

```yaml
authors:
  - family-names: "Kowalski"
    given-names: "Jan"
    affiliation: "Medical University of Białystok"
    orcid: "https://orcid.org/0000-0000-0000-0000"
```

> Używaj zawsze pełnego URL: `https://orcid.org/XXXX-XXXX-XXXX-XXXX`

---

## Jak ORCID, Zenodo i GitHub współpracują?

```
GitHub (kod / dokumentacja)
    │
    │ Release → automatyczny trigger
    ▼
Zenodo (archiwizacja + DOI)
    │
    │ Import przez DataCite
    ▼
ORCID (profil badacza)
    │
    │ Widoczny w
    ▼
Google Scholar · Scopus · OpenAIRE · PubMed
```

---

## Checklist — ORCID ✅

- [ ] Konto ORCID założone
- [ ] Profil uzupełniony (uczelnia, kierunek)
- [ ] Widoczność ustawiona na „Everyone"
- [ ] ORCID połączony z Zenodo
- [ ] ORCID iD dodany do `CITATION.cff`
- [ ] Projekt zaimportowany do profilu ORCID (opcjonalnie)

---

*Poprzedni krok → [`02_zenodo_doi.md`](./02_zenodo_doi.md)*  
*Następny krok → [`04_citation_cff.md`](./04_citation_cff.md)*
