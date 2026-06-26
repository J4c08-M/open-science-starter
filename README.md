<div align="center">

# 🔬 Open Science Starter
## Przewodnik: GitHub · Zenodo · ORCID · DOI · OSF · ClinicalTrials.gov

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightblue.svg)](https://creativecommons.org/licenses/by/4.0/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20681671.svg)](https://doi.org/10.5281/zenodo.20681671)
[![Status](https://img.shields.io/badge/status-active-brightgreen)](https://github.com)
[![For Students](https://img.shields.io/badge/for-students%20%26%20researchers-purple)](https://github.com)

**Polski** | [English summary below](#english-summary)

</div>

---

## 🎯 O projekcie

**Open Science Starter** to praktyczny przewodnik dla studentów i młodych badaczy, którzy chcą:

- opublikować swój pierwszy projekt na **GitHub**
- nadać mu stały naukowy identyfikator **DOI** przez **Zenodo**
- założyć profil badacza **ORCID**
- poprawnie napisać plik **CITATION.cff**
- zrozumieć, gdzie rejestrować plan badania (**OSF**) i badanie kliniczne (**ClinicalTrials.gov**)
- spiąć **Claude + Obsidian + Mendeley + Word** w jeden obieg pracy naukowej
- zrozumieć, jak działa ekosystem otwartej nauki

> 💡 Przewodnik nie wymaga znajomości programowania. Każdy krok jest opisany tak, żeby mógł go wykonać student humanistyki, medycyny, biologii — nie tylko informatyki.

---

## 🧪 Geneza projektu

> To moje pierwsze publiczne repozytorium — stworzone jako projekt edukacyjny podczas nauki obsługi GitHub i narzędzi otwartej nauki.
>
> Powstało równolegle z projektem [Smart Study AI](https://github.com/J4c08-M/smart-study-ai), przy okazji którego odkryłem, że konfiguracja GitHub + Zenodo + ORCID zasługuje na osobny, szczegółowy przewodnik.
>
> Jeśli też zaczynasz przygodę z open source — ten przewodnik jest dla Ciebie.

---

## 📁 Struktura projektu

```
📦 open-science-starter/
│
├── README.md                  ← Ten plik — przegląd projektu
├── LICENSE                    ← CC BY 4.0
├── CITATION.cff               ← Przykładowy plik cytowania
│
└── guides/
    ├── 01_github.md           ← Tworzenie i konfiguracja repozytorium GitHub
    ├── 02_zenodo_doi.md       ← Połączenie z Zenodo i nadanie DOI
    ├── 03_orcid.md            ← Założenie profilu ORCID i połączenie z Zenodo
    ├── 04_citation_cff.md     ← Jak napisać poprawny plik CITATION.cff
    ├── 05_clinicaltrials.md   ← ClinicalTrials.gov — rejestracja badań klinicznych
    ├── 06_osf.md              ← Open Science Framework — prerejestracja i pierwszeństwo
    ├── 07_obsidian.md         ← Obsidian (+ Claude) — baza wiedzy / drugi mózg
    ├── 08_mendeley.md         ← Mendeley (+ Word) — bibliografia i cytowania
    ├── 09_claude_workflow.md  ← Wspólny obieg: Claude + Obsidian + Mendeley + Word
    └── 10_links.md            ← Wszystkie przydatne linki w jednym miejscu
```

---

## 🗺️ Mapa v1 — podstawowy obieg (kod → DOI)

> Najprostsza ścieżka: opublikuj projekt i nadaj mu cytowalny DOI.

```
Twój projekt
     │
     ▼
┌─────────────┐     Release v1.0.0     ┌─────────────────┐
│   GitHub    │ ─────────────────────▶│     Zenodo      │
│ (kod / dok) │                        │  (archiwum DOI) │
└─────────────┘                        └────────┬────────┘
                                                │ DOI
                                                ▼
                                    ┌───────────────────────┐
                                    │  Cytowanie naukowe    │
                                    │  Google Scholar       │
                                    │  Scopus / DataCite    │
                                    └───────────────────────┘
          ┌───────────┐
          │   ORCID   │ ◀── połącz z Zenodo → automatyczne
          │ (profil   │     uzupełnianie dorobku naukowego
          │ badacza)  │
          └───────────┘
```

---

## 🗺️ Mapa v2 — pełny ekosystem otwartej nauki

> Wersja rozbudowana: od pisania pracy (Claude · Obsidian · Mendeley · Word), przez wybór właściwego rejestru wg typu pracy, po cytowalność.

```
                         ✍️  ETAP PISANIA / RESEARCHU
   📚 Mendeley ──▶ 🧠 Claude ◀──▶ 🗂️ Obsidian ──▶ 📝 Word + Mendeley Cite
   (literatura)    (analiza,        (notatki,        (format + cytowania)
                    draft)           MOC, draft)               │
                                                               ▼
                          CO PUBLIKUJESZ / REJESTRUJESZ?
                                      │
        ┌─────────────────────┬───────┴────────┬──────────────────────┐
        ▼                     ▼                ▼                      ▼
┌───────────────┐   ┌─────────────────┐  ┌──────────────┐   ┌─────────────────┐
│ Kod / dane /  │   │ Plan badania    │  │ Badanie      │   │ Ty jako autor   │
│ dokumentacja  │   │ (przed danymi)  │  │ kliniczne    │   │                 │
└───────┬───────┘   └────────┬────────┘  └──────┬───────┘   └────────┬────────┘
        ▼                    ▼                  ▼                    ▼
┌───────────────┐   ┌─────────────────┐  ┌──────────────┐   ┌─────────────────┐
│    GitHub     │   │       OSF       │  │ Clinical     │   │      ORCID      │
│      +        │   │ (prerejestracja)│  │ Trials.gov   │   │ (profil badacza)│
│    Zenodo     │   └────────┬────────┘  └──────┬───────┘   └────────┬────────┘
└───────┬───────┘            │ DOI              │ NCT                │ ORCID iD
        │ DOI                │                  │                    │
        └────────────────────┴────────┬─────────┴────────────────────┘
                                       ▼
                       ┌───────────────────────────────┐
                       │   Cytowanie i widoczność      │
                       │   Google Scholar · Scopus     │
                       │   DataCite · OpenAIRE         │
                       └───────────────────────────────┘

   ORCID spina całość — łączy się z Zenodo i OSF, automatycznie
   uzupełniając Twój dorobek naukowy.
```

---

## 📋 Gdzie co zarejestrować?

| Co masz | Gdzie | Identyfikator | Przewodnik |
|---|---|---|---|
| Kod / dane / dokumentacja | **GitHub + Zenodo** | DOI | `01`, `02` |
| Plan badania (przed danymi) | **OSF** (prerejestracja) | DOI | `06` |
| Badanie kliniczne na ludziach | **ClinicalTrials.gov** | NCT | `05` |
| Ty jako autor | **ORCID** | ORCID iD | `03` |
| Pierwszeństwo pomysłu inżynierskiego | **repo + Zenodo + OSF** | DOI / commit | `02`, `06` |

> 🛡️ **Pierwszeństwo bez badania klinicznego** ustalasz przez publiczną historię commitów (datowany ślad), DOI z Zenodo i prerejestrację na OSF — **nie** przez ClinicalTrials.gov.

---

## 📖 Przewodniki — szybki przegląd

| Plik | Zawartość | Czas |
|---|---|---|
| [`01_github.md`](./guides/01_github.md) | Konto, nowe repo, wgrywanie plików, dobre praktyki | ~15 min |
| [`02_zenodo_doi.md`](./guides/02_zenodo_doi.md) | Połączenie GitHub–Zenodo, pierwsze wydanie, uzyskanie DOI | ~10 min |
| [`03_orcid.md`](./guides/03_orcid.md) | Założenie ORCID, połączenie z Zenodo, widoczność naukowa | ~10 min |
| [`04_citation_cff.md`](./guides/04_citation_cff.md) | Struktura CITATION.cff, pola obowiązkowe, walidacja | ~10 min |
| [`05_clinicaltrials.md`](./guides/05_clinicaltrials.md) | ClinicalTrials.gov, numer NCT, kiedy (nie) rejestrować | ~10 min |
| [`06_osf.md`](./guides/06_osf.md) | OSF, prerejestracja, pierwszeństwo pomysłu | ~10 min |
| [`07_obsidian.md`](./guides/07_obsidian.md) | Obsidian: baza wiedzy, po co i jak łączyć z Claude | ~10 min |
| [`08_mendeley.md`](./guides/08_mendeley.md) | Mendeley: bibliografia, integracja z Wordem | ~10 min |
| [`09_claude_workflow.md`](./guides/09_claude_workflow.md) | Wspólny obieg: Claude + Obsidian + Mendeley + Word | ~15 min |
| [`10_links.md`](./guides/10_links.md) | Wszystkie przydatne linki do narzędzi i platform | ~2 min |

---

## ✅ Checklist — od zera do DOI

- [ ] Konto GitHub założone
- [ ] Repozytorium publiczne utworzone
- [ ] Pliki wgrane: `README.md`, `LICENSE`, `CITATION.cff`
- [ ] Konto Zenodo założone (przez GitHub)
- [ ] Synchronizacja GitHub–Zenodo włączona
- [ ] Pierwsze wydanie (Release v1.0.0) opublikowane na GitHub
- [ ] DOI uzyskany na Zenodo
- [ ] Odznaka DOI dodana do `README.md`
- [ ] `CITATION.cff` uzupełniony o DOI
- [ ] Konto ORCID założone i połączone z Zenodo
- [ ] (Opcjonalnie) Plan badania prerejestrowany na OSF
- [ ] (Opcjonalnie) Badanie kliniczne zarejestrowane na ClinicalTrials.gov

---

## 📜 Licencja

[![CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)

**Creative Commons Attribution 4.0 International (CC BY 4.0)**
Możesz kopiować, modyfikować i udostępniać — pod warunkiem podania autora i źródła.

---

<a name="english-summary"></a>

## 🇬🇧 English Summary

**Open Science Starter** is a practical guide for students and early-stage researchers who want to publish their first project on GitHub, obtain a DOI via Zenodo, set up an ORCID profile, write a proper CITATION.cff file, register study plans (OSF) and clinical trials (ClinicalTrials.gov), and combine Claude + Obsidian + Mendeley + Word into one research writing workflow. No programming knowledge required. Written primarily in Polish, with a universal workflow applicable to any field.

**License:** CC BY 4.0 | **Audience:** Students, early-career researchers, any discipline

---

<div align="center">

*Jeśli przewodnik był pomocny — zostaw ⭐!*

🔗 Powiązany projekt: [smart-study-ai](https://github.com/J4c08-M/smart-study-ai) — szablony Claude dla studentów medycyny

</div>
