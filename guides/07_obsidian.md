# 🗂️ Przewodnik 07 — Obsidian (+ Claude)

> Twój „drugi mózg": trwała, połączona baza wiedzy. I dlaczego warto wpiąć w nią Claude.

---

## 🎯 Co to jest Obsidian

[Obsidian](https://obsidian.md) to darmowa aplikacja do notatek oparta na **zwykłych plikach Markdown** trzymanych lokalnie na Twoim dysku (tzw. *vault*). Zamiast jednego liniowego dokumentu budujesz **sieć połączonych notatek**.

Kluczowe cechy:
- **Pliki lokalne, `.md`** — Twoje, na zawsze, bez vendor lock-in. Działają nawet bez Obsidiana.
- **Linkowanie `[[wikilink]]`** — łączysz notatki ze sobą; powstaje graf wiedzy.
- **Mapy treści (MOC)** — notatki-huby spinające tematycznie powiązane notatki.
- **Frontmatter YAML** (`typ/status/tagi`) — metadane, po których filtrujesz i wyszukujesz.
- **Wtyczki** — Dataview, Templates, kalendarz, kanban itd.

> 💡 Różnica wobec Worda: Word to **dokument**, Obsidian to **system wiedzy**. W Wordzie piszesz jedną pracę; w Obsidianie gromadzisz wiedzę, z której powstaje wiele prac.

---

## 🧠 Po co Ci Obsidian w pracy naukowej

- **Wiedza nie ulatuje.** Wniosek z artykułu, pomysł na badanie, fragment metodyki — raz zapisany, zostaje i jest połączony z resztą.
- **Widzisz powiązania.** Graf i linki pokazują, że temat z farmakologii łączy się z Twoim projektem druku 3D — czego w liniowych notatkach byś nie zauważył.
- **Jedno źródło prawdy.** Zamiast dziesięciu plików „notatki_final_v3.docx" masz jeden vault, w którym wszystko jest powiązane.
- **Skalowalność.** Im więcej notatek, tym **cenniejsza** sieć — odwrotnie niż w folderach z plikami, gdzie rośnie bałagan.

---

## 🔗 Po co łączyć Claude z Obsidianem

Sam Obsidian **przechowuje** wiedzę, ale jej nie analizuje ani nie pisze. Sam Claude **analizuje i pisze**, ale **nie pamięta** niczego między rozmowami. Razem:

- **Claude czyta Twój vault** → odpowiada w kontekście *Twoich* notatek, nie ogólnej wiedzy.
- **Claude zapisuje do vaulta** → wnioski z rozmowy lądują jako trwałe notatki z linkami, zamiast zniknąć wraz z czatem.
- **Obsidian daje Claude pamięć długoterminową** → vault staje się Twoją bazą, do której Claude sięga.

> ⚙️ Połączenie realizuje się przez **MCP** (Model Context Protocol) / odpowiedni konektor do systemu plików — Claude dostaje dostęp do katalogu vaulta i może czytać oraz tworzyć notatki.

---

## 🛠️ Jak to wykorzystać — konkretnie

- **Eksport rozmów do vaulta.** Po sesji z Claude: „zapisz wnioski jako notatkę w `Rozmowy z Claude/`, z frontmatterem i linkami `[[...]]`". Rozmowa znika, notatka zostaje.
- **Research w kontekście.** „Na podstawie moich notatek w folderze `Projekty/dicom-to-3d-print` zaproponuj strukturę sekcji Metody." Claude pracuje na Twojej wiedzy.
- **Budowa MOC.** Claude tworzy notatkę-hub spinającą rozproszone notatki tematyczne i wpina ją w indeks.
- **Porządkowanie vaulta.** Aktualizacja indeksu, ujednolicenie tagów, wykrywanie duplikatów.
- **Draft w markdownie.** Szkielet manuskryptu powstaje w Obsidianie — łatwo iterować, linkować do źródeł, wersjonować — a dopiero potem trafia do Worda (patrz przewodnik `09`).

---

## ✅ Dobre praktyki

- **Obsidian to baza, nie czat.** Wnioski z rozmów zawsze przeklejaj/eksportuj do trwałych notatek.
- **Konwencja od początku.** Ustal frontmatter (`typ/status/tagi`) i strukturę folderów, zanim vault urośnie.
- **Linkuj, nie kopiuj.** Zamiast powielać treść — `[[linkuj]]` do notatki źródłowej.
- **Jeden vault = jeden kontekst.** Trzymaj projekt naukowy w spójnym vaultcie, żeby Claude widział całość.

---

## 🔗 Powiązane

- Przewodnik `08` — Mendeley (+ Word): bibliografia i finalizacja.
- Przewodnik `09` — wspólny obieg: Claude + Obsidian + Mendeley + Word.
- Projekt [`smart-study-ai`](https://github.com/J4c08-M/smart-study-ai) — szablony promptów Claude.

---

*Część przewodnika [Open Science Starter](../README.md) · CC BY 4.0*
