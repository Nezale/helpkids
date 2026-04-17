# HelpKids Website Updates - Design Specification

**Date:** 2026-04-17  
**Status:** Approved

## Overview

Aktualizacja strony internetowej HelpKids obejmująca: naprawienie polskich znaków, modyfikację zakładki terapeutów, dodanie nowych diagnoz oraz utworzenie dwóch nowych podstron (Cennik, SOM).

## Scope

### 1. Polskie znaki

**Problem:** Wszystkie polskie znaki (ą, ę, ć, ł, ń, ó, ś, ź, ż) są zastąpione ASCII odpowiednikami.

**Rozwiązanie:**
- Zamiana wszystkich wystąpień w 5 plikach HTML: index.html, onas.html, oferta.html, galeria.html, kontakt.html
- Pliki mają już `<meta charset="UTF-8">` - kodowanie jest poprawne
- Przykłady zamian: "Glowna" → "Główna", "wiecej" → "więcej", "terapeutow" → "terapeutów"

### 2. Modyfikacja zakładki terapeutów (onas.html)

**Zmiany:**
1. **Usunięcie:** Paulina Sobczak (cały blok team-card)
2. **Nowa kolejność:**
   - Kamila Budrewicz (pierwsza)
   - Żaneta Budrewicz (druga)
   - Anita Budrewicz (trzecia)
   - Agnieszka Karpyza (czwarta)
   - Marlena Piskorz (piąta)
   - Oksana Sytczyk (szósta - nowa)

**Nowa terapeutka:**
- Źródło: `/Users/aleksander.kozyra/test/repo/assets/zakadkaterapeuci.zip`
- Zdjęcie: Oksana Sytczyk.webp → skopiować do `assets/images/team/oksana_sytczyk.webp`
- Opis: mgr Oksana Anna Sytczyk.docx

### 3. Nowe diagnozy w ofercie (oferta.html)

**Źródło:** `/Users/aleksander.kozyra/test/repo/assets/plikinastron.zip`

**Dodanie do sekcji "Diagnozy Specjalistyczne" - 3 nowe pozycje:**

1. **Diagnoza ADHD**
   - Treść z pliku ADHD + BINET.docx (część dotycząca ADHD)
   - Format: element `<details>` z summary i content

2. **Skala Inteligencji Stanford-Binet 5**
   - Treść z pliku ADHD + BINET.docx (część dotycząca Stanford-Binet)
   - Format: element `<details>` z summary i content

3. **Diagnoza ADI-R**
   - Treść z pliku ADI-R.docx
   - Format: element `<details>` z summary i content

**Lokalizacja:** Na końcu listy diagnoz (po "Diagnoza Przetwarzania Słuchowego")

### 4. Nowe podstrony

#### cennik.html
- Treść z pliku: `/Users/aleksander.kozyra/test/repo/assets/CENNIK HelpKids.docx`
- Styl spójny z resztą strony (header, footer, hero section)
- Tabelaryczne przedstawienie cen usług
- Hero image: wykorzystanie istniejącego zdjęcia z galerii

#### som.html (Standardy Ochrony Małoletnich)
- Treść z pliku: `/Users/aleksander.kozyra/test/repo/assets/Standardy Ochrony Małoletnich w HelpKids Żaneta Budrewicz.docx`
- Styl spójny z resztą strony
- Dokument prawny/informacyjny - czytelny układ z sekcjami
- Hero image: wykorzystanie istniejącego zdjęcia z galerii

### 5. Aktualizacja nawigacji

**Menu główne - nowa kolejność (wszystkie 7 plików HTML):**
1. Strona Główna (index.html)
2. O Nas (onas.html)
3. Oferta (oferta.html)
4. Cennik (cennik.html) ← nowa pozycja
5. Galeria (galeria.html)
6. SOM (som.html) ← nowa pozycja
7. Kontakt (kontakt.html)

**Stopka (footer) - sekcja "Szybkie Linki":**
- Dodanie tych samych dwóch nowych linków (Cennik, SOM)

**Pliki do edycji:**
- index.html, onas.html, oferta.html, galeria.html, kontakt.html (istniejące)
- cennik.html, som.html (nowe - już z poprawną nawigacją)

## Implementation Order

1. Naprawienie polskich znaków we wszystkich 5 plikach HTML
2. Modyfikacja zakładki terapeutów (onas.html)
3. Dodanie nowych diagnoz do oferta.html
4. Utworzenie nowych podstron: cennik.html, som.html
5. Aktualizacja nawigacji we wszystkich plikach

## Verification

Po zakończeniu implementacji, otwórz w przeglądarce:

```
file:///Users/aleksander.kozyra/test/repo/helpkids/index.html
```

Bezpośrednie linki do weryfikacji:
- **Polskie znaki:** `file:///Users/aleksander.kozyra/test/repo/helpkids/index.html`
- **Terapeuci:** `file:///Users/aleksander.kozyra/test/repo/helpkids/onas.html`
- **Nowe diagnozy:** `file:///Users/aleksander.kozyra/test/repo/helpkids/oferta.html#diagnozy`
- **Cennik:** `file:///Users/aleksander.kozyra/test/repo/helpkids/cennik.html`
- **SOM:** `file:///Users/aleksander.kozyra/test/repo/helpkids/som.html`

## Source Files

External assets folder: `/Users/aleksander.kozyra/test/repo/assets/`

| File | Purpose |
|------|---------|
| CENNIK HelpKids.docx | Treść strony cennik.html |
| Standardy Ochrony Małoletnich w HelpKids Żaneta Budrewicz.docx | Treść strony som.html |
| plikinastron.zip | ADHD + BINET.docx, ADI-R.docx (nowe diagnozy) |
| zakadkaterapeuci.zip | Oksana Sytczyk.webp, mgr Oksana Anna Sytczyk.docx (nowa terapeutka) |
