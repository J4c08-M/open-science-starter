# 📘 Przewodnik 1: GitHub
## Tworzenie i konfiguracja repozytorium

---

## Czym jest GitHub?

GitHub to platforma do przechowywania i udostępniania projektów — plików tekstowych, kodu, dokumentacji, szablonów. Działa jak chmura dla projektów, z historią wszystkich zmian i możliwością współpracy.

Dla studenta bez doświadczenia programistycznego GitHub to przede wszystkim:
- bezpłatne, publiczne miejsce na Twój projekt
- warunek konieczny do uzyskania DOI przez Zenodo
- portfolio projektów widoczne dla innych

---

## Krok 1 — Załóż konto

1. Wejdź na [github.com](https://github.com) → kliknij **Sign up**
2. Wybierz darmowy plan **Free**
3. Potwierdź adres e-mail

> **Wskazówka dot. nazwy użytkownika:**  
> Wybierz coś profesjonalnego — ta nazwa będzie widoczna w linku do Twojego profilu i repozytorium (np. `github.com/jan-kowalski`). Unikaj pseudonimów, które mogą wyglądać nieprofesjonalnie.

---

## Krok 2 — Utwórz nowe repozytorium

1. Zaloguj się → kliknij **„+"** (prawy górny róg) → **„New repository"**
   lub wejdź na [github.com/new](https://github.com/new)

2. Wypełnij formularz:

| Pole | Zalecana wartość i wskazówka |
|---|---|
| **Repository name** | Krótka, opisowa nazwa z myślnikami: `smart-study-ai`, `open-science-starter`. Bez spacji, bez polskich znaków. |
| **Description** | Jedno zdanie opisujące projekt po angielsku (widoczne w wyszukiwarce GitHub i Google). |
| **Visibility** | ✅ **Public** — wymagane dla Zenodo DOI i widoczności naukowej |
| **Initialize with README** | ❌ **Nie zaznaczaj** — wgrasz własny plik README.md |
| **Add .gitignore** | None |
| **Choose a license** | None — wgrasz własny plik LICENSE |

3. Kliknij **„Create repository"**

---

## Krok 3 — Wgraj pliki

### Opcja A — przez przeglądarkę (zalecane na start)

1. Na stronie nowego repozytorium kliknij **„uploading an existing file"**
2. Przeciągnij lub kliknij **„choose your files"** i wybierz wszystkie pliki projektu
3. W polu **„Commit message"** wpisz: `Initial commit: add project files`
4. Kliknij **„Commit changes"**

### Opcja B — przez terminal (dla zaawansowanych)

```bash
git init
git add .
git commit -m "Initial commit: add project files"
git branch -M main
git remote add origin https://github.com/TWOJA_NAZWA/NAZWA_REPO.git
git push -u origin main
```

---

## Krok 4 — Uzupełnij informacje o repozytorium

Na stronie repozytorium, po prawej stronie przy sekcji **„About"**, kliknij ⚙️:

- **Description** — krótki opis (jeśli nie dodałeś wcześniej)
- **Website** — możesz zostawić puste lub wpisać link do powiązanego projektu
- **Topics (tagi)** — bardzo ważne dla widoczności! Dodaj kilka słów kluczowych, np.:
  - `claude-ai` `prompt-engineering` `medical-education` `open-education` `students`

> Tagi pomagają innym znaleźć Twój projekt przez wyszukiwarkę GitHub.

---

## Krok 5 — Sprawdź poprawność wyświetlania

Po wgraniu plików zweryfikuj:

- [ ] `README.md` renderuje się automatycznie na stronie głównej repo
- [ ] Odznaki (badges) są widoczne pod tytułem
- [ ] Plik `LICENSE` jest wykryty przez GitHub — przy nazwie repo pojawi się etykieta z nazwą licencji
- [ ] Wszystkie pliki i foldery są widoczne w liście
- [ ] Opis i tagi są ustawione w sekcji **About**

---

## Dobre praktyki nazewnictwa plików

| ✅ Dobrze | ❌ Unikaj |
|---|---|
| `README.md` | `readme.md`, `Readme.MD` |
| `LICENSE` (bez rozszerzenia) | `license.txt`, `LICENCJA.md` |
| `CITATION.cff` | `citation.yaml`, `cytowanie.cff` |
| `guides/01_github.md` | `Przewodnik 1 Github.md` |

> GitHub rozróżnia wielkość liter w nazwach plików. `README.md` jest automatycznie renderowany — `readme.md` już nie na wszystkich widokach.

---

## Struktura plików — co jest obowiązkowe, co opcjonalne?

| Plik | Rola | Obowiązkowy? |
|---|---|---|
| `README.md` | Strona główna projektu | ✅ Tak |
| `LICENSE` | Określa warunki użycia | ✅ Tak (dla Zenodo) |
| `CITATION.cff` | Informacje do cytowania | ✅ Tak (dla DOI) |
| `CITATION.cff` | Informacje do cytowania | ✅ Tak (dla DOI) |
| Pliki projektu (`.md`, `.pdf`...) | Właściwa treść | ✅ Tak |
| `guides/` lub `docs/` | Podstrony / dokumentacja | Opcjonalnie |
| `.gitignore` | Ignorowanie plików lokalnych | Opcjonalnie |

---

*Następny krok → [`02_zenodo_doi.md`](./02_zenodo_doi.md)*
