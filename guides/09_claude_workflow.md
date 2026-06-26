# 🔗 Przewodnik 09 — Wspólny obieg: Claude + Obsidian + Mendeley + Word

> Spięcie wszystkiego z przewodników `07` i `08` w jeden pipeline: od pomysłu, przez literaturę i notatki, po gotowy manuskrypt z bibliografią.

> 📌 Ten przewodnik zakłada, że znasz już rolę **Obsidiana** (przewodnik `07`) i **Mendeleya** (przewodnik `08`). Tu pokazujemy, jak działają **razem**.

---

## 🎯 Po co je łączyć

Każde narzędzie robi jedną rzecz świetnie — dopiero razem tworzą pełny pipeline od surowego pomysłu do manuskryptu złożonego do czasopisma. Zamiast przeskakiwać między aplikacjami i przepisywać wszystko ręcznie, prowadzisz pracę w jednym, spójnym przepływie.

| Narzędzie | Rola w obiegu | Szczegóły |
|---|---|---|
| 🧠 **Claude** | Silnik intelektualny | analiza literatury, streszczenia, draftowanie, krytyka, tłumaczenie |
| 🗂️ **Obsidian** | Baza wiedzy | trwałe notatki, MOC, draft w markdownie → *przewodnik `07`* |
| 📚 **Mendeley** | Bibliografia | biblioteka PDF, cytowania, Mendeley Cite → *przewodnik `08`* |
| 📝 **Word** | Finalizacja | format pod czasopismo, śledzenie zmian, eksport |

---

## 🔗 Dlaczego to działa razem (synergia)

Pojedynczo każde narzędzie ma lukę:
- **Claude** pisze świetnie, ale **nie pamięta** Twojej wiedzy i **nie cytuje** wiarygodnie;
- **Obsidian** przechowuje, ale nie analizuje ani nie pisze;
- **Mendeley** trzyma PDF-y, ale nie streści 40 artykułów;
- **Word** sformatuje, ale nie zbuduje argumentacji.

Spięte — luki się znoszą:

> **Mendeley** dostarcza literaturę → **Claude** ją analizuje i drafuje → **Obsidian** przechowuje każdy wniosek trwale i z linkami → **Word + Mendeley Cite** składa manuskrypt z poprawnymi cytowaniami.

Żadna myśl ani źródło nie ginie, a przejście „notatka → akapit manuskryptu" jest płynne zamiast przepisywania od zera.

---

## 🛠️ Obieg pracy — krok po kroku

1. **Literatura (Mendeley + PubMed).** Importujesz PDF-y, porządkujesz w folder projektu, weryfikujesz metadane.
2. **Research i streszczenia (Claude).** Wrzucasz artykuły → streszczenia, porównania metod, luka badawcza. **Zawsze weryfikujesz** w oryginale.
3. **Trwałe notatki (Obsidian).** Wnioski lądują jako notatki z `[[wikilinkami]]` i frontmatterem. Budujesz MOC projektu.
4. **Draft (Claude ↔ Obsidian).** Claude pisze szkielet sekcji na podstawie Twoich notatek; draft trzymasz w markdownie w Obsidianie.
5. **Finalizacja (Word + Mendeley).** Draft → Word (kopiuj-wklej lub `pandoc`). Wtyczką Mendeley Cite wstawiasz cytowania i bibliografię w stylu czasopisma. Włączasz śledzenie zmian.
6. **Publikacja i archiwizacja.** Manuskrypt → czasopismo / preprint. Kod, dane, protokół → GitHub + Zenodo (DOI) + OSF — przewodniki `01`–`06`.

```
POMYSŁ
  │
  ▼
📚 Mendeley (literatura, PDF, DOI)        → przewodnik 08
  │
  ▼
🧠 Claude (analiza, streszczenia, draft)  ◀──┐
  │                                          │ czyta / zapisuje
  ▼                                          │
🗂️ Obsidian (notatki, MOC, draft .md) ──────┘  → przewodnik 07
  │
  ▼
📝 Word + Mendeley Cite (format + cytowania)
  │
  ▼
PUBLIKACJA → czasopismo / preprint + GitHub·Zenodo·OSF (DOI)  → przewodniki 01–06
```

---

## ⚠️ Pułapki i dobre praktyki

- **Claude nie cytuje wiarygodnie.** Bibliografię prowadzi **wyłącznie Mendeley** (przewodnik `08`). Nigdy nie ufaj numerom cytowań od modelu bez sprawdzenia.
- **Jedno źródło prawdy dla referencji = Mendeley.** Obsidian i Word tylko z niego korzystają.
- **Markdown najpierw, formatowanie na końcu.** Nie formatuj w Wordzie, póki treść nie jest skończona.
- **Obsidian to baza, nie czat.** Wnioski z rozmów przeklejaj do trwałych notatek (przewodnik `07`).
- **Pandoc dla czystego przejścia.** `pandoc draft.md -o draft.docx` zachowuje nagłówki i strukturę przy przejściu z Obsidiana do Worda.

---

## 🔗 Powiązane

- Przewodnik `07` — Obsidian (+ Claude).
- Przewodnik `08` — Mendeley (+ Word).
- Przewodniki `01`–`06` — publikacja i rejestracja (GitHub, Zenodo, ORCID, CITATION.cff, ClinicalTrials.gov, OSF).
- Projekt [`smart-study-ai`](https://github.com/J4c08-M/smart-study-ai) — szablony promptów Claude.

---

*Część przewodnika [Open Science Starter](../README.md) · CC BY 4.0*
