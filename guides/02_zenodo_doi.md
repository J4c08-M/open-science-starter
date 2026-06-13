# 📘 Przewodnik 2: Zenodo i DOI
## Jak nadać swojemu projektowi naukowy identyfikator DOI

---

## Czym jest DOI i po co Ci go?

**DOI** (Digital Object Identifier) to stały, unikalny identyfikator Twojego projektu — jak ISBN dla książki. Wygląda tak:

```
https://doi.org/10.5281/zenodo.14523678
```

Dzięki DOI:
- Twój projekt można **cytować w pracach naukowych**
- Jest **trwały** — nawet jeśli zmienisz nazwę repo na GitHub, DOI nadal działa
- Pojawia się w bazach danych: **DataCite, Google Scholar, OpenAIRE**
- Nadaje projektowi **wiarygodność akademicką**

**Zenodo** to bezpłatna platforma archiwizacji naukowej prowadzona przez CERN i Unię Europejską. Automatycznie nadaje DOI po połączeniu z GitHub i opublikowaniu wersji (Release).

---

## Krok 1 — Załóż konto Zenodo

1. Wejdź na [zenodo.org](https://zenodo.org)
2. Kliknij **„Log in"** → wybierz **„Log in with GitHub"**
3. Kliknij **„Authorize zenodo"** — autoryzujesz Zenodo do odczytu Twoich repozytoriów

> ⚠️ Logowanie przez GitHub jest kluczowe — bez tego automatyczna synchronizacja nie zadziała.

---

## Krok 2 — Włącz synchronizację dla repozytorium

1. Po zalogowaniu na Zenodo kliknij swój avatar → **„GitHub"**
   *(lub wejdź bezpośrednio: [zenodo.org/account/settings/github](https://zenodo.org/account/settings/github))*

2. Znajdź swoje repozytorium na liście

3. Przełącz przełącznik na **ON**

> Jeśli repozytorium nie pojawia się na liście — kliknij **„Sync now"** (przycisk w prawym górnym rogu strony). GitHub czasami wymaga chwili na synchronizację.

---

## Krok 3 — Opublikuj pierwsze wydanie (Release) na GitHub

Zenodo **nie monitoruje zwykłych commitów** — nadaje DOI dopiero przy opublikowaniu **Release**.

1. Wejdź na stronę swojego repozytorium na GitHub
2. Po prawej stronie kliknij **„Releases"** → **„Create a new release"**
3. Wypełnij formularz:

| Pole | Wartość |
|---|---|
| **Choose a tag** | Wpisz `v1.0.0` → kliknij **„Create new tag: v1.0.0"** |
| **Target** | `main` (gałąź główna) |
| **Release title** | `v1.0.0 — Initial Release` |
| **Description** | `First public release. [Krótki opis projektu po angielsku]` |
| **Set as latest release** | ✅ Zaznacz |

4. Kliknij **„Publish release"**

> **Konwencja wersjonowania (SemVer):**
> - `v1.0.0` — pierwsze pełne wydanie
> - `v1.1.0` — drobne zmiany / nowe treści
> - `v2.0.0` — duże zmiany struktury projektu

---

## Krok 4 — Odbierz DOI na Zenodo

1. Wróć na [zenodo.org/account/settings/github](https://zenodo.org/account/settings/github)
2. Obok swojego repozytorium powinien pojawić się DOI w formie:
   `10.5281/zenodo.XXXXXXX`
3. Kliknij go — zobaczysz swój rekord na Zenodo z metadanymi projektu

> Przetworzenie zwykle zajmuje **kilka minut**. Jeśli po 10 minutach nic się nie pojawia — odśwież stronę lub sprawdź czy synchronizacja była włączona przed publikacją Release.

---

## Krok 5 — Zaktualizuj projekt o DOI

Po uzyskaniu DOI zaktualizuj dwa miejsca w projekcie:

### W `README.md` — znajdź i zamień:
```markdown
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)
```
Zamień `XXXXXXX` na swój numer (np. `14523678`).

### W `CITATION.cff` — znajdź i zamień:
```yaml
doi: "[FILL IN: assigned by Zenodo after first release]"
```
Na:
```yaml
doi: "10.5281/zenodo.14523678"
```

### Zatwierdź zmiany:
```bash
git add README.md CITATION.cff
git commit -m "Add DOI badge and update citation"
git push
```

---

## Jak działa wersjonowanie DOI?

Zenodo nadaje **dwa rodzaje DOI**:

| Typ | Wygląd | Kiedy używać |
|---|---|---|
| **DOI wersji** | `10.5281/zenodo.14523678` | Cytowanie konkretnej wersji (v1.0.0) |
| **DOI koncepcyjny** | `10.5281/zenodo.14523677` | Zawsze wskazuje na najnowszą wersję |

> W `CITATION.cff` i odznace README używaj **DOI koncepcyjnego** — wtedy cytowanie jest zawsze aktualne, niezależnie od wersji.
>
> DOI koncepcyjny znajdziesz na stronie rekordu Zenodo, w sekcji **„Versions"** po lewej stronie.

---

## Jak zaktualizować projekt w przyszłości?

1. Wprowadź zmiany w plikach i wgraj na GitHub (`git push`)
2. Utwórz nowy Release na GitHub (np. `v1.1.0`)
3. Zenodo automatycznie utworzy nowy rekord z nowym DOI wersji
4. DOI koncepcyjny automatycznie zaktualizuje się na najnowszą wersję

---

## Checklist — Zenodo DOI ✅

- [ ] Konto Zenodo założone przez GitHub
- [ ] Synchronizacja włączona dla repozytorium
- [ ] Release v1.0.0 opublikowany na GitHub
- [ ] DOI uzyskany na Zenodo
- [ ] Odznaka DOI zaktualizowana w `README.md`
- [ ] `CITATION.cff` uzupełniony o DOI koncepcyjny
- [ ] Zmiany zatwierdzone i wgrane na GitHub

---

*Poprzedni krok → [`01_github.md`](./01_github.md)*  
*Następny krok → [`03_orcid.md`](./03_orcid.md)*
