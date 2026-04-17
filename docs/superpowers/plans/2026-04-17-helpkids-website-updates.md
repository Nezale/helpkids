# HelpKids Website Updates - Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Update HelpKids website with Polish characters, modified therapist page, new diagnoses, and two new subpages (Cennik, SOM).

**Architecture:** Static HTML website with shared navigation across all pages. Each page follows the same structure: header with nav, hero section, content sections, footer. CSS in `css/style.css`.

**Tech Stack:** HTML5, CSS3, UTF-8 encoding

---

## File Structure

**Files to modify:**
- `index.html` - Polish characters + navigation
- `onas.html` - Polish characters + navigation + therapist reorder
- `oferta.html` - Polish characters + navigation + new diagnoses
- `galeria.html` - Polish characters + navigation
- `kontakt.html` - Polish characters + navigation

**Files to create:**
- `cennik.html` - New pricing page
- `som.html` - New child protection standards page
- `assets/images/team/oksana_sytczyk.webp` - New therapist photo

---

## Task 1: Copy new therapist photo

**Files:**
- Create: `assets/images/team/oksana_sytczyk.webp`

- [ ] **Step 1: Copy photo from extracted ZIP**

Run:
```bash
cp "/tmp/zakadkaterapeuci/Oksana Sytczyk.webp" "/Users/aleksander.kozyra/test/repo/helpkids/assets/images/team/oksana_sytczyk.webp"
```

- [ ] **Step 2: Verify file exists**

Run:
```bash
ls -la /Users/aleksander.kozyra/test/repo/helpkids/assets/images/team/oksana_sytczyk.webp
```

Expected: File exists with size ~55KB

- [ ] **Step 3: Commit**

```bash
git add assets/images/team/oksana_sytczyk.webp
git commit -m "feat: add Oksana Sytczyk photo"
```

---

## Task 2: Fix Polish characters in index.html

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Replace ASCII with Polish characters**

Apply these replacements throughout the file:
- "Glowna" → "Główna"
- "rozwijac" → "rozwijać"
- "Wspolnie" → "Wspólnie"
- "nasza oferte" → "naszą ofertę"
- "ktorym" → "którym"
- "znajda" → "znajdą"
- "doswiadczonych" → "doświadczonych"
- "terapeutow" → "terapeutów"
- "psychologow" → "psychologów"
- "pedagogow" → "pedagogów"
- "wspolprace" → "współpracę"
- "bezpieczenstwa" → "bezpieczeństwa"
- "pomagamy" stays as is
- "trudnosci" → "trudności"
- "potencjal" → "potencjał"
- "zespol" → "zespół"
- "sluchowego" → "słuchowego"
- "wiecej" → "więcej"
- "ktorych" → "których"
- "czuja" → "czują"
- "bezpiecznie" → "bezpiecznie"
- "rodzicow" → "rodziców"
- "opiekunow" → "opiekunów"
- "dzis" → "dziś"
- "umowic" → "umówić"
- "pomozemy" → "pomożemy"
- "Warminskim" → "Warmińskim"
- "zastrzezone" → "zastrzeżone"

Full replacements for index.html - change content to use proper Polish diacritics:
- Line 26: "Strona Glowna" → "Strona Główna"
- Line 41: "rozwijac skrzydla" → "rozwijać skrzydła"
- Line 42: "Wspolnie" → "Wspólnie", "harmonijny rozwoj" → "harmonijny rozwój"
- Line 43: "nasza oferte" → "naszą ofertę"
- Line 53: "ktorym" → "którym", "znajda" → "znajdą", "specjalistyczna" → "specjalistyczną", "doswiadczonych" → "doświadczonych", "terapeutow" → "terapeutów", "psychologow" → "psychologów", "pedagogow" → "pedagogów", "pasja" → "pasją", "wspirac" → "wspierać", "rozwoj" → "rozwój"
- Line 54: "diagnozy" stays, "terapie" stays, "potrzeb" stays, "bezpieczenstwa" → "bezpieczeństwa", "pokonywac" → "pokonywać", "trudnosci" → "trudności", "rozwijac" → "rozwijać", "potencjal" → "potencjał"
- Line 55: "zespol" → "zespół"
- Line 68: "sluchowego" → "słuchowego", "wiecej" → "więcej"
- Line 74-75: "psychologiczne" stays, "rodzicow" → "rodziców"
- Line 80-81: all terapie text
- Line 95: "Doswiadczony" → "Doświadczony", "Zespol" → "Zespół"
- Line 100: "wyjatkowe" → "wyjątkowe"
- Line 105: "ktorych" → "których", "czuja" → "czują", "bezpiecznie" stays
- Line 110: "takze" → "także", "rodzicow" → "rodziców", "opiekunow" → "opiekunów"
- Line 119: "dzis" → "dziś", "umowic wizyte" → "umówić wizytę"
- Line 120: "umowic wizyte" → "umówić wizytę", "pomozemy" → "pomożemy"
- Line 131: "Warminskim" → "Warmińskim"
- Line 139: "Glowna" → "Główna"
- Line 149: "Legionow" → "Legionów", "Warminski" → "Warmiński"
- Line 160: "zastrzezone" → "zastrzeżone"

- [ ] **Step 2: Verify file displays correctly**

Open in browser: `file:///Users/aleksander.kozyra/test/repo/helpkids/index.html`
Check that Polish characters display correctly (ą, ę, ć, ł, ń, ó, ś, ź, ż)

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "fix: add Polish diacritics to index.html"
```

---

## Task 3: Fix Polish characters in onas.html + reorder therapists

**Files:**
- Modify: `onas.html`

- [ ] **Step 1: Replace ASCII with Polish characters**

Same pattern as index.html - replace all instances of:
- "Glowna" → "Główna"
- "Poznaj" stays
- "specjalistow" → "specjalistów"
- "ktorzy" → "którzy"
- "pasja" → "pasją"
- "zaangazowaniem" → "zaangażowaniem"
- "pomagaja" → "pomagają"
- "rozwoju" stays
- "ktore" → "które"
- "powstalo" → "powstało"
- "mysla" → "myślą"
- "miesci" → "mieści"
- "Warminskim" → "Warmińskim"
- "uslug" → "usług"
- "pracuja" → "pracują"
- "nieustannie" stays
- "poszerzaja" → "poszerzają"
- "jakosc" → "jakość"
- "Wierzymy" stays
- "wyjatkowe" → "wyjątkowe"
- "zasluguje" → "zasługuje"
- "mozliwosci" → "możliwości"
- "psychofizycznych" stays
- All therapist descriptions need Polish characters

- [ ] **Step 2: Remove Paulina Sobczak section**

Delete the entire team-card block for Paulina Sobczak (lines 65-73 in original file):
```html
        <!-- Paulina Sobczak -->
        <div class="team-card">
          <img src="assets/images/team/paulina_sobczak.jpg" alt="Paulina Sobczak" class="team-card__img" loading="lazy">
          <div class="team-card__content">
            <h3 class="team-card__name">mgr Paulina Sobczak</h3>
            <p class="team-card__role">Psycholog, Pedagog Specjalny</p>
            <p class="team-card__bio">Absolwentka Uniwersytetu SWPS w Sopocie (psychologia kliniczna), Gdanskiego Uniwersytetu Medycznego oraz Uniwersytetu Warminsko-Mazurskiego. Ukonczyla szkolenia z terapii behawioralnej dzieci w spektrum autyzmu, TUS, Terapii Reki i metody Kids Skills. W HelpKids prowadzi konsultacje psychologiczne dziecka i rodziny oraz terapie psychologiczna.</p>
          </div>
        </div>
```

- [ ] **Step 3: Reorder therapists - Budrewicz first**

New order in team-grid section:
1. Kamila Budrewicz
2. Żaneta Budrewicz  
3. Anita Budrewicz
4. Agnieszka Karpyza
5. Marlena Piskorz
6. Oksana Sytczyk (new)

- [ ] **Step 4: Add Oksana Sytczyk at the end**

Add after Marlena Piskorz:
```html
        <!-- Oksana Sytczyk -->
        <div class="team-card">
          <img src="assets/images/team/oksana_sytczyk.webp" alt="Oksana Sytczyk" class="team-card__img" loading="lazy">
          <div class="team-card__content">
            <h3 class="team-card__name">mgr Oksana Anna Sytczyk</h3>
            <p class="team-card__role">Psycholog kliniczny, Pedagog, Diagnosta, Psychoterapeuta CBT</p>
            <p class="team-card__bio">Pomagam dzieciom, młodzieży i dorosłym lepiej rozumieć siebie, odzyskać równowagę emocjonalną i znaleźć skuteczne rozwiązania w trudnych momentach życia. Jestem psychologiem i pedagogiem z wieloletnim doświadczeniem w pracy terapeutycznej oraz diagnostycznej. Pracuję w nurcie poznawczo-behawioralnym, opierając terapię na sprawdzonych metodach i indywidualnym podejściu do każdej osoby. W gabinecie tworzę atmosferę bezpieczeństwa, akceptacji i uważności.</p>
          </div>
        </div>
```

- [ ] **Step 5: Verify changes in browser**

Open: `file:///Users/aleksander.kozyra/test/repo/helpkids/onas.html`
Check:
- Polish characters display correctly
- Paulina Sobczak is removed
- Budrewicz therapists are first (Kamila, Żaneta, Anita)
- Oksana Sytczyk appears at the end

- [ ] **Step 6: Commit**

```bash
git add onas.html
git commit -m "feat: update therapist page - Polish chars, remove Sobczak, reorder Budrewicz first, add Sytczyk"
```

---

## Task 4: Fix Polish characters in oferta.html + add new diagnoses

**Files:**
- Modify: `oferta.html`

- [ ] **Step 1: Replace ASCII with Polish characters**

Same pattern - all Polish diacritics throughout the file.

- [ ] **Step 2: Add three new diagnoses to the Diagnozy section**

Add after "Diagnoza Przetwarzania Słuchowego" (before closing `</div>` of service-list):

```html
          <details class="service-item">
            <summary>Diagnoza ADHD</summary>
            <div class="service-item__content">
              <p>Proces diagnostyczny obejmuje 3 spotkania (z możliwością wydłużenia), każde trwające do 60 minut. Celem jest dokładne zrozumienie trudności dziecka oraz sprawdzenie, czy obserwowane objawy odpowiadają ADHD.</p>
              <p><strong>Etap 1 – wywiad z rodzicem:</strong> Zbieramy informacje o rozwoju dziecka, jego funkcjonowaniu w domu i szkole. Rodzic wypełnia kwestionariusz Conners-3.</p>
              <p><strong>Etap 2 – spotkania z dzieckiem:</strong> Młodsze dzieci obserwujemy podczas zabawy, ze starszymi prowadzimy wywiad (Young DIVA-5).</p>
              <p><strong>Etap 3 – opinia diagnostyczna:</strong> Przygotowujemy pisemną opinię z wnioskami i zaleceniami.</p>
              <p>Diagnozę prowadzimy u dzieci i młodzieży od 6. roku życia.</p>
            </div>
          </details>

          <details class="service-item">
            <summary>Badanie Inteligencji Stanford-Binet 5</summary>
            <div class="service-item__content">
              <p>Rzetelna diagnoza możliwości poznawczych dziecka. Badanie pomaga ocenić potencjał i potrzeby dziecka, które ma trudności w nauce, szybko się rozprasza lub rozwija się szybciej niż rówieśnicy.</p>
              <p><strong>Co daje badanie:</strong></p>
              <ul style="list-style: disc; margin-left: 1.5rem; margin-bottom: 1rem;">
                <li>Poznanie poziomu rozwoju intelektualnego dziecka</li>
                <li>Lepsze zrozumienie stylu uczenia się</li>
                <li>Wychwycenie ewentualnych trudności rozwojowych</li>
                <li>Rozpoznanie uzdolnień i mocnych stron</li>
                <li>Wsparcie w dostosowaniu wymagań szkolnych</li>
              </ul>
              <p>Badanie często stanowi ważne uzupełnienie diagnozy ADHD lub spektrum autyzmu. Trwa od 60 do 120 minut.</p>
            </div>
          </details>

          <details class="service-item">
            <summary>Diagnoza ADI-R</summary>
            <div class="service-item__content">
              <p>ADI-R (Autism Diagnostic Interview-Revised) to wywiad strukturalny opracowany specjalnie do diagnozowania zaburzeń ze spektrum autyzmu (ASD) u dzieci, młodzieży i dorosłych. Jest uważany za jedno z najbardziej niezawodnych narzędzi diagnostycznych w tej dziedzinie.</p>
              <p><strong>ADI-R ocenia trzy obszary:</strong></p>
              <ul style="list-style: disc; margin-left: 1.5rem; margin-bottom: 1rem;">
                <li>Jakość interakcji społecznych</li>
                <li>Jakość komunikacji i mowy</li>
                <li>Zakres, intensywność i złożoność zachowań stereotypowych</li>
              </ul>
              <p>Wywiad przeprowadzany jest z rodzicami lub opiekunami i trwa od 2,5 do 3 godzin. ADI-R służy postawieniu formalnej diagnozy oraz może być wykorzystany przy planowaniu terapii.</p>
            </div>
          </details>
```

- [ ] **Step 3: Verify changes in browser**

Open: `file:///Users/aleksander.kozyra/test/repo/helpkids/oferta.html#diagnozy`
Check:
- Polish characters display correctly
- Three new diagnoses appear at the end of Diagnozy section
- Expandable details work correctly

- [ ] **Step 4: Commit**

```bash
git add oferta.html
git commit -m "feat: add Polish chars + ADHD, Stanford-Binet 5, ADI-R diagnoses"
```

---

## Task 5: Fix Polish characters in galeria.html

**Files:**
- Modify: `galeria.html`

- [ ] **Step 1: Replace ASCII with Polish characters**

Key replacements:
- "Glowna" → "Główna"
- "ktorej" → "której"
- "rozwijac" → "rozwijać"
- "Wnetrza" → "Wnętrza"
- "zaprojektowane" stays
- "mysla" → "myślą"
- "przyjazne" stays
- "wyposazone" → "wyposażone"
- "sprzet" → "sprzęt"
- "zywo" → "żywo"
- "stworzyslismy" → "stworzyliśmy"
- "przestrzen" → "przestrzeń"
- "czuja" → "czują"
- "Warminskim" → "Warmińskim"
- "zastrzezone" → "zastrzeżone"

- [ ] **Step 2: Verify in browser**

Open: `file:///Users/aleksander.kozyra/test/repo/helpkids/galeria.html`

- [ ] **Step 3: Commit**

```bash
git add galeria.html
git commit -m "fix: add Polish diacritics to galeria.html"
```

---

## Task 6: Fix Polish characters in kontakt.html

**Files:**
- Modify: `kontakt.html`

- [ ] **Step 1: Replace ASCII with Polish characters**

Key replacements:
- "Glowna" → "Główna"
- "Skontaktuj sie" → "Skontaktuj się"
- "odwiedz" → "odwiedź"
- "nasza placowke" → "naszą placówkę"
- "Chetnie" → "Chętnie"
- "Warminskim" → "Warmińskim"
- "Legionow" → "Legionów"
- "dotrzec" → "dotrzeć"
- "miesci sie" → "mieści się"
- "Glowna" → "Główna"
- "wejsciowa" → "wejściowa"
- "znajduje sie" → "znajduje się"
- "udac sie" → "udać się"
- "pietro" → "piętro"
- "Wejscie" → "Wejście"
- "placowki" → "placówki"
- "zastrzezone" → "zastrzeżone"

- [ ] **Step 2: Verify in browser**

Open: `file:///Users/aleksander.kozyra/test/repo/helpkids/kontakt.html`

- [ ] **Step 3: Commit**

```bash
git add kontakt.html
git commit -m "fix: add Polish diacritics to kontakt.html"
```

---

## Task 7: Create cennik.html

**Files:**
- Create: `cennik.html`

- [ ] **Step 1: Create cennik.html with full content**

```html
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Cennik usług HelpKids - diagnozy, konsultacje i terapie dla dzieci. Sprawdź aktualne ceny.">
  <title>Cennik - HelpKids</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Quicksand:wght@500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <!-- Header -->
  <header class="header">
    <div class="container">
      <div class="header__inner">
        <a href="index.html" class="logo">
          <img src="assets/logo/HELPKIDS.jpg" alt="HelpKids Logo" class="logo__img">
          <span class="logo__text">HelpKids</span>
        </a>
        <nav>
          <input type="checkbox" id="nav-toggle" class="nav__toggle">
          <label for="nav-toggle" class="nav__toggle-label"><span></span></label>
          <ul class="nav__menu">
            <li><a href="index.html" class="nav__link">Strona Główna</a></li>
            <li><a href="onas.html" class="nav__link">O Nas</a></li>
            <li><a href="oferta.html" class="nav__link">Oferta</a></li>
            <li><a href="cennik.html" class="nav__link nav__link--active">Cennik</a></li>
            <li><a href="galeria.html" class="nav__link">Galeria</a></li>
            <li><a href="som.html" class="nav__link">SOM</a></li>
            <li><a href="kontakt.html" class="nav__link">Kontakt</a></li>
          </ul>
        </nav>
      </div>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero hero--small" style="background-image: url('assets/images/gallery/20231022_112354.jpg');">
    <div class="container">
      <div class="hero__content">
        <h1 class="hero__title">Cennik</h1>
        <p class="hero__subtitle">Poznaj aktualne ceny naszych usług diagnostycznych i terapeutycznych.</p>
      </div>
    </div>
  </section>

  <!-- Cennik Diagnozy -->
  <section class="section">
    <div class="container">
      <h2 class="section__title">Diagnozy i Konsultacje</h2>
      <div class="pricing-table">
        <table class="price-list">
          <thead>
            <tr>
              <th>Usługa</th>
              <th>Cena</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Diagnoza ADOS-2</td>
              <td>600 zł</td>
            </tr>
            <tr>
              <td>ADI-R</td>
              <td>500 zł</td>
            </tr>
            <tr>
              <td>Diagnoza ADOS-2 + ADI-R</td>
              <td>1000 zł</td>
            </tr>
            <tr>
              <td>Diagnoza Nadpobudliwości Psychoruchowej (ADHD)</td>
              <td>700 zł</td>
            </tr>
            <tr>
              <td>Diagnoza SI</td>
              <td>600 zł</td>
            </tr>
            <tr>
              <td>Badanie Inteligencji Stanford-Binet 5</td>
              <td>700 zł</td>
            </tr>
            <tr>
              <td>Diagnoza pedagogiczna</td>
              <td>600 zł</td>
            </tr>
            <tr>
              <td>Badanie Przetwarzania Słuchowego</td>
              <td>350 zł</td>
            </tr>
            <tr>
              <td>Rediagnoza Przetwarzania Słuchowego</td>
              <td>300 zł</td>
            </tr>
            <tr>
              <td>Konsultacja specjalistyczna</td>
              <td>200 zł</td>
            </tr>
            <tr>
              <td>Konsultacja wielospecjalistyczna</td>
              <td>300 zł</td>
            </tr>
            <tr>
              <td>Konsultacja psychologiczna</td>
              <td>200 zł</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <!-- Cennik Terapie -->
  <section class="section section--alt">
    <div class="container">
      <h2 class="section__title">Zajęcia Terapeutyczne</h2>
      <div class="pricing-table">
        <table class="price-list">
          <thead>
            <tr>
              <th>Usługa</th>
              <th>Cena</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Zajęcia 45-minutowe</td>
              <td>130 zł</td>
            </tr>
            <tr>
              <td>Zajęcia 30-minutowe</td>
              <td>100 zł</td>
            </tr>
            <tr>
              <td>Pakiet 10 zajęć po 45 min</td>
              <td>1250 zł</td>
            </tr>
            <tr>
              <td>Pakiet 10 zajęć po 30 min</td>
              <td>950 zł</td>
            </tr>
            <tr>
              <td>Trening Umiejętności Społecznych TUS (zajęcia grupowe)</td>
              <td>80 zł / zajęcia</td>
            </tr>
            <tr>
              <td>Zajęcia Rozwijające Umiejętności Emocjonalno-Społeczne (grupowe)</td>
              <td>80 zł / zajęcia</td>
            </tr>
            <tr>
              <td>Terapia Kids'Skills - metoda „Dam Radę!" i „Jestem z Ciebie Dumny!"</td>
              <td>130 zł / spotkanie</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <!-- Cennik Treningi -->
  <section class="section">
    <div class="container">
      <h2 class="section__title">Treningi Słuchowe</h2>
      <div class="pricing-table">
        <table class="price-list">
          <thead>
            <tr>
              <th>Usługa</th>
              <th>Cena</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Neuroakustyczny Trening Mózgu - konsultacja</td>
              <td>bezpłatna</td>
            </tr>
            <tr>
              <td>Neuroakustyczny Trening Mózgu - 24 sesje</td>
              <td>1660,50 zł</td>
            </tr>
            <tr>
              <td>Trening słuchowy Johansena - płyta</td>
              <td>250-300 zł</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <section class="section section--alt">
    <div class="container text-center">
      <h2 class="section__title">Masz pytania dotyczące cen?</h2>
      <p style="max-width: 600px; margin: 0 auto 2rem;">Skontaktuj się z nami, aby uzyskać więcej informacji lub umówić wizytę.</p>
      <a href="kontakt.html" class="btn btn--primary">Skontaktuj się</a>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="container">
      <div class="footer__grid">
        <div>
          <h3 class="footer__title">HelpKids</h3>
          <p class="footer__text">Centrum Diagnozy i Terapii Dziecka. Profesjonalna pomoc dla dzieci i ich rodzin w Lidzbarku Warmińskim.</p>
          <div class="footer__social">
            <a href="https://www.facebook.com/profile.php?id=100076142580022" target="_blank" rel="noopener" aria-label="Facebook">FB</a>
          </div>
        </div>
        <div>
          <h3 class="footer__title">Szybkie Linki</h3>
          <div class="footer__links">
            <a href="index.html" class="footer__link">Strona Główna</a>
            <a href="onas.html" class="footer__link">O Nas</a>
            <a href="oferta.html" class="footer__link">Oferta</a>
            <a href="cennik.html" class="footer__link">Cennik</a>
            <a href="galeria.html" class="footer__link">Galeria</a>
            <a href="som.html" class="footer__link">SOM</a>
            <a href="kontakt.html" class="footer__link">Kontakt</a>
          </div>
        </div>
        <div>
          <h3 class="footer__title">Kontakt</h3>
          <div class="footer__contact-item">
            &#128205; Legionów 2F, 11-100 Lidzbark Warmiński
          </div>
          <div class="footer__contact-item">
            &#128222; <a href="tel:+48531866177">531 866 177</a>
          </div>
          <div class="footer__contact-item">
            &#9993; <a href="mailto:helpkidslidzbark@gmail.com">helpkidslidzbark@gmail.com</a>
          </div>
        </div>
      </div>
      <div class="footer__bottom">
        <p>&copy; 2026 HelpKids - Diagnoza i Terapia Dziecka. Wszelkie prawa zastrzeżone.</p>
      </div>
    </div>
  </footer>
</body>
</html>
```

- [ ] **Step 2: Add CSS for pricing tables**

Add to `css/style.css`:
```css
/* Pricing Tables */
.pricing-table {
  max-width: 800px;
  margin: 0 auto;
}

.price-list {
  width: 100%;
  border-collapse: collapse;
  background: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.price-list th,
.price-list td {
  padding: 1rem 1.5rem;
  text-align: left;
}

.price-list th {
  background: var(--primary);
  color: white;
  font-weight: 600;
}

.price-list th:last-child,
.price-list td:last-child {
  text-align: right;
  white-space: nowrap;
}

.price-list tbody tr {
  border-bottom: 1px solid #eee;
}

.price-list tbody tr:last-child {
  border-bottom: none;
}

.price-list tbody tr:hover {
  background: #f8f9fa;
}
```

- [ ] **Step 3: Verify in browser**

Open: `file:///Users/aleksander.kozyra/test/repo/helpkids/cennik.html`

- [ ] **Step 4: Commit**

```bash
git add cennik.html css/style.css
git commit -m "feat: create cennik.html with pricing tables"
```

---

## Task 8: Create som.html

**Files:**
- Create: `som.html`

- [ ] **Step 1: Create som.html with full content**

```html
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Standardy Ochrony Małoletnich w HelpKids - procedury zapewniające bezpieczeństwo dzieci w naszej placówce.">
  <title>Standardy Ochrony Małoletnich - HelpKids</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Quicksand:wght@500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <!-- Header -->
  <header class="header">
    <div class="container">
      <div class="header__inner">
        <a href="index.html" class="logo">
          <img src="assets/logo/HELPKIDS.jpg" alt="HelpKids Logo" class="logo__img">
          <span class="logo__text">HelpKids</span>
        </a>
        <nav>
          <input type="checkbox" id="nav-toggle" class="nav__toggle">
          <label for="nav-toggle" class="nav__toggle-label"><span></span></label>
          <ul class="nav__menu">
            <li><a href="index.html" class="nav__link">Strona Główna</a></li>
            <li><a href="onas.html" class="nav__link">O Nas</a></li>
            <li><a href="oferta.html" class="nav__link">Oferta</a></li>
            <li><a href="cennik.html" class="nav__link">Cennik</a></li>
            <li><a href="galeria.html" class="nav__link">Galeria</a></li>
            <li><a href="som.html" class="nav__link nav__link--active">SOM</a></li>
            <li><a href="kontakt.html" class="nav__link">Kontakt</a></li>
          </ul>
        </nav>
      </div>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero hero--small" style="background-image: url('assets/images/gallery/20231022_114624.jpg');">
    <div class="container">
      <div class="hero__content">
        <h1 class="hero__title">Standardy Ochrony Małoletnich</h1>
        <p class="hero__subtitle">Procedury zapewniające bezpieczeństwo dzieci w naszej placówce.</p>
      </div>
    </div>
  </section>

  <!-- Wprowadzenie -->
  <section class="section">
    <div class="container">
      <div class="som-content">
        <p class="som-intro">Działając na podstawie art. 22b ustawy z 13 maja 2016 r. o przeciwdziałaniu zagrożeniom przestępczością na tle seksualnym i ochronie małoletnich, HelpKids – Diagnoza i Terapia Dziecka z dniem 01.08.2024 r. wprowadza do stosowania „Standardy Ochrony Małoletnich", których naczelnym celem jest zapewnienie bezpieczeństwa małoletnim, dbałość o ich dobro, uwzględnianie ich potrzeb i podejmowanie działań w ich najlepszym interesie.</p>

        <h2>Podstawowe Standardy</h2>
        
        <div class="som-standards">
          <div class="som-standard">
            <h3>Standard 1</h3>
            <p>Placówka opracowała, przyjęła i wdrożyła do realizacji Standardy Ochrony Małoletnich, które określają:</p>
            <ul>
              <li>Zasady bezpiecznej rekrutacji personelu</li>
              <li>Procedury reagowania na krzywdzenie</li>
              <li>Procedury i osoby odpowiedzialne za przyjęcie zgłoszenia, dokumentowanie i dalsze działania pomocowe</li>
              <li>Zasady ustalania planu wsparcia małoletniego po ujawnieniu krzywdzenia</li>
              <li>Zasady bezpiecznych relacji personel – małoletni, w tym zachowania niedozwolone</li>
              <li>Zasady bezpiecznych relacji małoletni – małoletni</li>
              <li>Zasady korzystania z urządzeń elektronicznych z dostępem do Internetu</li>
              <li>Procedury ochrony dzieci przed treściami szkodliwymi i zagrożeniami w Internecie</li>
              <li>Zasady upowszechniania i ewaluacji Standardów</li>
            </ul>
          </div>

          <div class="som-standard">
            <h3>Standard 2</h3>
            <p>Placówka stosuje zasady bezpiecznej rekrutacji personelu, szkoli personel ze Standardów pierwszorazowo oraz każdorazowo po zmianie.</p>
          </div>

          <div class="som-standard">
            <h3>Standard 3</h3>
            <p>Placówka wdrożyła i stosuje procedury interwencyjne, które znane są i udostępnione całemu personelowi. Każdy pracownik wie komu należy zgłosić informację o krzywdzeniu małoletniego i kto jest odpowiedzialny za działania interwencyjne.</p>
          </div>

          <div class="som-standard">
            <h3>Standard 4</h3>
            <p>Placówka co najmniej raz na 2 lata monitoruje i w razie konieczności ewaluuje oraz aktualizuje zapisy Standardów.</p>
          </div>
        </div>

        <h2>Cel Standardów</h2>
        <ul>
          <li>Zwrócenie uwagi personelu placówki, rodziców i podmiotów współpracujących na konieczność podejmowania wzmożonych działań na rzecz ochrony małoletnich przed krzywdzeniem</li>
          <li>Określenie zakresu obowiązków przedstawicieli placówki w działaniach podejmowanych na rzecz ochrony małoletnich przed krzywdzeniem</li>
          <li>Wypracowanie adekwatnej procedury do wykorzystania podczas interwencji w przypadku podejrzenia krzywdzenia małoletnich</li>
          <li>Wprowadzenie wzmożonej działalności profilaktyczno-wychowawczej w zakresie zapewnienia ochrony pacjentów przed przemocą</li>
        </ul>

        <h2>Zasady Bezpiecznych Relacji</h2>
        <p>Podstawową zasadą relacji między małoletnimi a personelem placówki jest działanie dla dobra pacjenta, z poszanowaniem jego godności, z uwzględnieniem jego emocji i potrzeb oraz w jego najlepszym interesie.</p>
        
        <p>Podstawowe standardy obejmują w szczególności:</p>
        <ul>
          <li>Utrzymywanie profesjonalnej relacji z pacjentami</li>
          <li>Zachowanie cierpliwości i szacunku w komunikacji</li>
          <li>Wyznaczanie jasnych granic w postępowaniu</li>
          <li>Reagowanie w sposób adekwatny do sytuacji i możliwości psychofizycznych pacjenta</li>
          <li>Równe traktowanie pacjentów bez względu na płeć, niepełnosprawność, status społeczny</li>
          <li>Fizyczny kontakt z pacjentem możliwy tylko jako odpowiedź na realne potrzeby, za zgodą pacjenta</li>
        </ul>

        <h2>Procedury Interwencyjne</h2>
        <p>W przypadku podejrzenia krzywdzenia małoletniego:</p>
        <ol>
          <li>Każde zgłoszenie musi zostać przekazane właścicielowi placówki</li>
          <li>Po dokonaniu rozpoznania właściciel decyduje o dalszych krokach</li>
          <li>Terapeuta sporządza notatkę ze spotkania</li>
          <li>Ustalana jest forma zgłoszenia do odpowiednich organów</li>
          <li>Wypełniana jest Karta Przebiegu Interwencji</li>
          <li>Określana jest forma dalszej pomocy i wsparcia</li>
        </ol>

        <h2>Osoba Odpowiedzialna</h2>
        <p><strong>Żaneta Budrewicz</strong> jest osobą odpowiedzialną za:</p>
        <ul>
          <li>Monitorowanie realizacji Standardów</li>
          <li>Reagowanie na sygnały naruszenia</li>
          <li>Ewaluowanie i modyfikowanie zapisów Standardów</li>
          <li>Prowadzenie rejestru interwencji i zgłoszeń</li>
        </ul>

        <h2>Kontakt w Sprawie Standardów</h2>
        <p>W przypadku pytań dotyczących Standardów Ochrony Małoletnich prosimy o kontakt z placówką.</p>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <section class="section section--alt">
    <div class="container text-center">
      <h2 class="section__title">Masz pytania?</h2>
      <p style="max-width: 600px; margin: 0 auto 2rem;">Skontaktuj się z nami, jeśli chcesz dowiedzieć się więcej o naszych standardach ochrony dzieci.</p>
      <a href="kontakt.html" class="btn btn--primary">Skontaktuj się</a>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="container">
      <div class="footer__grid">
        <div>
          <h3 class="footer__title">HelpKids</h3>
          <p class="footer__text">Centrum Diagnozy i Terapii Dziecka. Profesjonalna pomoc dla dzieci i ich rodzin w Lidzbarku Warmińskim.</p>
          <div class="footer__social">
            <a href="https://www.facebook.com/profile.php?id=100076142580022" target="_blank" rel="noopener" aria-label="Facebook">FB</a>
          </div>
        </div>
        <div>
          <h3 class="footer__title">Szybkie Linki</h3>
          <div class="footer__links">
            <a href="index.html" class="footer__link">Strona Główna</a>
            <a href="onas.html" class="footer__link">O Nas</a>
            <a href="oferta.html" class="footer__link">Oferta</a>
            <a href="cennik.html" class="footer__link">Cennik</a>
            <a href="galeria.html" class="footer__link">Galeria</a>
            <a href="som.html" class="footer__link">SOM</a>
            <a href="kontakt.html" class="footer__link">Kontakt</a>
          </div>
        </div>
        <div>
          <h3 class="footer__title">Kontakt</h3>
          <div class="footer__contact-item">
            &#128205; Legionów 2F, 11-100 Lidzbark Warmiński
          </div>
          <div class="footer__contact-item">
            &#128222; <a href="tel:+48531866177">531 866 177</a>
          </div>
          <div class="footer__contact-item">
            &#9993; <a href="mailto:helpkidslidzbark@gmail.com">helpkidslidzbark@gmail.com</a>
          </div>
        </div>
      </div>
      <div class="footer__bottom">
        <p>&copy; 2026 HelpKids - Diagnoza i Terapia Dziecka. Wszelkie prawa zastrzeżone.</p>
      </div>
    </div>
  </footer>
</body>
</html>
```

- [ ] **Step 2: Add CSS for SOM page**

Add to `css/style.css`:
```css
/* SOM Page Styles */
.som-content {
  max-width: 900px;
  margin: 0 auto;
}

.som-intro {
  font-size: 1.1rem;
  line-height: 1.8;
  margin-bottom: 2rem;
  padding: 1.5rem;
  background: #f8f9fa;
  border-left: 4px solid var(--primary);
  border-radius: 0 8px 8px 0;
}

.som-content h2 {
  color: var(--primary);
  margin-top: 2.5rem;
  margin-bottom: 1rem;
  font-size: 1.5rem;
}

.som-content ul,
.som-content ol {
  margin-left: 1.5rem;
  margin-bottom: 1.5rem;
}

.som-content li {
  margin-bottom: 0.5rem;
  line-height: 1.6;
}

.som-standards {
  display: grid;
  gap: 1.5rem;
  margin: 1.5rem 0;
}

.som-standard {
  background: white;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.som-standard h3 {
  color: var(--primary);
  margin-bottom: 0.75rem;
  font-size: 1.2rem;
}

.som-standard ul {
  margin-top: 0.75rem;
}
```

- [ ] **Step 3: Verify in browser**

Open: `file:///Users/aleksander.kozyra/test/repo/helpkids/som.html`

- [ ] **Step 4: Commit**

```bash
git add som.html css/style.css
git commit -m "feat: create som.html with child protection standards"
```

---

## Task 9: Update navigation in all existing HTML files

**Files:**
- Modify: `index.html`, `onas.html`, `oferta.html`, `galeria.html`, `kontakt.html`

- [ ] **Step 1: Update navigation menu in all 5 files**

Replace the nav menu `<ul class="nav__menu">` in each file with:
```html
          <ul class="nav__menu">
            <li><a href="index.html" class="nav__link">Strona Główna</a></li>
            <li><a href="onas.html" class="nav__link">O Nas</a></li>
            <li><a href="oferta.html" class="nav__link">Oferta</a></li>
            <li><a href="cennik.html" class="nav__link">Cennik</a></li>
            <li><a href="galeria.html" class="nav__link">Galeria</a></li>
            <li><a href="som.html" class="nav__link">SOM</a></li>
            <li><a href="kontakt.html" class="nav__link">Kontakt</a></li>
          </ul>
```

Keep the `nav__link--active` class on the appropriate link for each page.

- [ ] **Step 2: Update footer links in all 5 files**

Replace the footer links `<div class="footer__links">` in each file with:
```html
          <div class="footer__links">
            <a href="index.html" class="footer__link">Strona Główna</a>
            <a href="onas.html" class="footer__link">O Nas</a>
            <a href="oferta.html" class="footer__link">Oferta</a>
            <a href="cennik.html" class="footer__link">Cennik</a>
            <a href="galeria.html" class="footer__link">Galeria</a>
            <a href="som.html" class="footer__link">SOM</a>
            <a href="kontakt.html" class="footer__link">Kontakt</a>
          </div>
```

- [ ] **Step 3: Verify navigation works**

Open each page and verify:
- Menu shows all 7 items
- Active state is correct for current page
- Footer links work
- Navigation to Cennik and SOM works

- [ ] **Step 4: Commit**

```bash
git add index.html onas.html oferta.html galeria.html kontakt.html
git commit -m "feat: update navigation with Cennik and SOM links"
```

---

## Task 10: Final verification

- [ ] **Step 1: Test all pages**

Open in browser and verify:
1. `index.html` - Polish characters, navigation with 7 items
2. `onas.html` - Polish characters, no Paulina Sobczak, Budrewicz first, Oksana at end
3. `oferta.html` - Polish characters, 3 new diagnoses at end of Diagnozy section
4. `galeria.html` - Polish characters, navigation
5. `kontakt.html` - Polish characters, navigation
6. `cennik.html` - Pricing tables display correctly
7. `som.html` - Standards content displays correctly

- [ ] **Step 2: Test responsive design**

Resize browser window to verify mobile navigation works.

- [ ] **Step 3: Final commit if any fixes needed**

```bash
git status
# If changes needed, commit them
```
