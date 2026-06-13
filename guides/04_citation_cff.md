# 📘 Przewodnik 4: CITATION.cff
## Jak napisać poprawny plik cytowania

---

## Czym jest CITATION.cff?

`CITATION.cff` to plik tekstowy w formacie YAML, który mówi innym **jak cytować Twój projekt**. GitHub automatycznie go wykrywa i wyświetla przycisk **„Cite this repository"** na stronie repozytorium.

Obsługują go: GitHub, Zenodo, Zotero, Mendeley, DOI resolver.

---

## Minimalna, poprawna struktura

```yaml
cff-version: 1.2.0
message: "If you use this project, please cite it as below."
type: software
title: "Tytuł Twojego Projektu"
authors:
  - family-names: "Kowalski"
    given-names: "Jan"
    affiliation: "Medical University of Białystok, Poland"
    orcid: "https://orcid.org/0000-0000-0000-0000"
version: "1.0.0"
date-released: "2025-05-24"
license: CC-BY-4.0
repository-code: "https://github.com/jan-kowalski/nazwa-repo"
doi: "10.5281/zenodo.14523678"
```

---

## Wszystkie ważne pola — objaśnienie

| Pole | Opis | Obowiązkowe? |
|---|---|---|
| `cff-version` | Zawsze `1.2.0` (aktualna wersja standardu) | ✅ Tak |
| `message` | Instrukcja dla czytelnika, jak cytować | ✅ Tak |
| `type` | `software` (kod/szablony) lub `dataset` (dane) | ✅ Tak |
| `title` | Pełna nazwa projektu | ✅ Tak |
| `authors` | Lista autorów (min. jeden) | ✅ Tak |
| `family-names` | Nazwisko | ✅ Tak |
| `given-names` | Imię | ✅ Tak |
| `affiliation` | Uczelnia / instytucja | Zalecane |
| `orcid` | Pełny URL ORCID | Zalecane |
| `version` | Wersja projektu (zgodna z Release) | Zalecane |
| `date-released` | Data wydania w formacie `YYYY-MM-DD` | Zalecane |
| `license` | Identyfikator licencji (np. `CC-BY-4.0`, `MIT`) | Zalecane |
| `repository-code` | URL repozytorium GitHub | Zalecane |
| `doi` | DOI z Zenodo (po uzyskaniu) | Zalecane |
| `abstract` | Krótki opis projektu | Opcjonalne |
| `keywords` | Lista słów kluczowych | Opcjonalne |
| `url` | Strona projektu (jeśli inna niż GitHub) | Opcjonalne |

---

## Pełny przykład z komentarzami

```yaml
# Wersja standardu CFF — zawsze 1.2.0
cff-version: 1.2.0

# Wiadomość wyświetlana przez GitHub w przycisku "Cite this repository"
message: "If you use this project, please cite it as below."

# Typ projektu: software (kod, szablony, narzędzia) lub dataset (zbiory danych)
type: software

# Pełna nazwa projektu — taka sama jak tytuł README
title: "Study Smarter with AI: Claude Prompt Templates for Medical Students"

# Krótki opis (opcjonalnie, ale dobra praktyka)
abstract: >
  An open-source collection of Claude AI prompt templates for medical
  students, supporting structured learning and exam preparation.

# Lista autorów
authors:
  - family-names: "Kowalski"
    given-names: "Jan"
    affiliation: "Medical University of Białystok, Poland"
    orcid: "https://orcid.org/0000-0002-1825-0097"

# Wersja — powinna być zgodna z numerem Release na GitHub
version: "1.0.0"

# Data wydania pierwszego Release
date-released: "2025-05-24"

# Identyfikator licencji — lista: https://spdx.org/licenses/
license: CC-BY-4.0

# Pełny URL repozytorium GitHub
repository-code: "https://github.com/jan-kowalski/study-smarter-ai"

# DOI z Zenodo — uzupełnij po uzyskaniu
doi: "10.5281/zenodo.14523678"

# Słowa kluczowe (opcjonalnie)
keywords:
  - Claude AI
  - prompt engineering
  - medical education
  - open education
```

---

## Częste błędy i jak ich unikać

| Błąd | Skutek | Poprawka |
|---|---|---|
| Brak wcięć (spacje vs tabulatory) | Plik nie parsuje się | Używaj zawsze 2 spacji, nigdy Tab |
| ORCID bez `https://` | Nie wykrywany przez GitHub | `"https://orcid.org/0000-..."` |
| Data w złym formacie | Błąd walidacji | Zawsze `YYYY-MM-DD` (np. `2025-05-24`) |
| `license: CC BY 4.0` (z spacjami) | Nieznana licencja | Używaj identyfikatora SPDX: `CC-BY-4.0` |
| `doi` bez cudzysłowu | Może być traktowany jako liczba | Zawsze w cudzysłowach: `"10.5281/..."` |
| Brak `cff-version` | Plik ignorowany | Pierwsze pole, zawsze `1.2.0` |

---

## Jak zwalidować plik?

Przed wgraniem na GitHub sprawdź poprawność pliku:

1. **Online:** Wejdź na [citation-file-format.github.io](https://citation-file-format.github.io/cff-initializer-javascript/) — kreator i walidator CITATION.cff
2. **GitHub:** Po wgraniu, wejdź na stronę repo → po prawej stronie pojawi się sekcja **„Cite this repository"** — jeśli jej nie ma, plik ma błąd

---

## Lista identyfikatorów licencji (SPDX)

Najczęściej używane w projektach edukacyjnych i open-source:

| Licencja | Identyfikator SPDX | Kiedy używać |
|---|---|---|
| Creative Commons BY 4.0 | `CC-BY-4.0` | Dokumentacja, szablony, treści edukacyjne |
| Creative Commons BY-SA 4.0 | `CC-BY-SA-4.0` | Jak CC BY, ale dzieła pochodne też muszą być CC |
| Creative Commons Zero | `CC0-1.0` | Dane, gdy chcesz zrzec się praw autorskich |
| MIT | `MIT` | Kod programistyczny |
| Apache 2.0 | `Apache-2.0` | Kod programistyczny z patentami |

> Pełna lista: [spdx.org/licenses](https://spdx.org/licenses/)

---

## Checklist — CITATION.cff ✅

- [ ] Plik nazwany dokładnie `CITATION.cff`
- [ ] `cff-version: 1.2.0` jest pierwszym polem
- [ ] Imię, nazwisko i afiliacja autora są poprawne
- [ ] ORCID wpisany jako pełny URL z `https://`
- [ ] Data w formacie `YYYY-MM-DD`
- [ ] Licencja jako identyfikator SPDX (np. `CC-BY-4.0`)
- [ ] DOI uzupełniony po uzyskaniu z Zenodo
- [ ] Plik zwalidowany (kreator online lub przycisk GitHub)

---

*Poprzedni krok → [`03_orcid.md`](./03_orcid.md)*  
*Wróć do początku → [`README.md`](../README.md)*
