# Hodnotící list – CSS animace (sluneční soustava)

Max. **25 bodů** (22 b základ + 3 b bonus). Čas 25 minut.
Vzorové řešení: `reseni/style.css`, část B.

**Žák:** ............................................  **Datum:** ..................

---

## Úloha 1 – Přechody a transformace (7 b)

| # | Kritérium | Body | Získáno |
|---|---|---|---|
| 1a | `transition` je na `.karta` (základní stav), ne v `:hover` | 1,5 | |
| 1b | `transform: translateY(-12px) scale(1.05)` v `.karta:hover` | 2 | |
| 1c | zesílený `box-shadow` v `:hover` a je zahrnutý v přechodu | 1,5 | |
| 1d | `.karta:hover .karta__kule` s `rotate(18deg) scale(1.12)` | 1,5 | |
| 1e | správná trvání a `ease-out` (0,35 s karta / 0,45 s kulička) | 0,5 | |

**Uznává se také:** `transition: all .35s ease-out` (plný počet – chování je
správné, při ústní části lze doplnit otázkou, proč je výčet vlastností lepší).
`translate: 0 -12px` + `scale: 1.05` jako samostatné vlastnosti rovněž uznat.

**Typické chyby:** `transition` zapsaný do `:hover` (−1,5 b); dvě samostatná
pravidla `transform: translateY()` a `transform: scale()` v jednom bloku, kdy
se druhé přepíše (−1 b); `transition` na kuličce chybí, takže se otáčí skokem
(−0,5 b).

## Úloha 2 – Oběh planet (6 b)

| # | Kritérium | Body | Získáno |
|---|---|---|---|
| 2a | `@keyframes obeh` s `rotate(0deg)` → `rotate(360deg)` | 2 | |
| 2b | animace přiřazena `.obeh` (ne `.telo`, ne `.draha`) | 1,5 | |
| 2c | `infinite` | 1 | |
| 2d | `linear` | 0,5 | |
| 2e | čtyři různá `animation-duration` se správnými hodnotami | 1 | |

**Uznává se také:** `0% / 100%` místo `from / to`; `rotate: 0turn → 1turn`;
rozepsané `animation-name`, `animation-duration`, … místo zkratky;
zapsání celé animace čtyřikrát zvlášť pro každou dráhu (−0,5 b za duplicitu,
pokud bylo v zadání výslovně žádáno jedno společné pravidlo).

**Typické chyby:** animace na `.telo` – planeta se otáčí na místě a neobíhá
(−1,5 b); chybí `infinite`, animace proběhne jednou (−1 b); `linear` neuvedeno,
planety se trhaně zpomalují (−0,5 b).

## Úloha 3 – Pulzující Slunce (5 b)

| # | Kritérium | Body | Získáno |
|---|---|---|---|
| 3a | `@keyframes puls` se dvěma snímky (`from` / `to`) | 1 | |
| 3b | mění se `transform: scale()` 1 → 1.12 | 1,5 | |
| 3c | mění se `box-shadow` na uvedené hodnoty | 1 | |
| 3d | `3s` + `ease-in-out` + `infinite` | 1 | |
| 3e | `alternate` (návrat pozpátku, ne skok na začátek) | 0,5 | |

**Typické chyby:** řešení přes tři snímky `0 % / 50 % / 100 %` – funguje, ale
zadání žádalo dva snímky + `alternate` (−0,5 b za 3e); `alternate` chybí,
Slunce skokem splaskne (−0,5 b).

## Úloha 4 – Blikající hvězdy (4 b)

| # | Kritérium | Body | Získáno |
|---|---|---|---|
| 4a | `@keyframes blikani` – `opacity` .15 → 1 | 1 | |
| 4b | `transform: scale()` .7 → 1.1 | 1 | |
| 4c | `2s` + `infinite` + `ease-in-out` + `alternate` | 1 | |
| 4d | `animation-delay: var(--d)` – hvězdy blikají rozfázovaně | 1 | |

**Pozor:** `animation-delay` musí být **samostatná vlastnost** *za* zkratkou
`animation`, nebo musí být zpoždění uvnitř zkratky jako druhá časová hodnota
(`animation: blikani 2s var(--d) ease-in-out infinite alternate`) – obojí
uznat. Pokud žák napíše `animation-delay` **před** zkratku `animation`,
zkratka ho přepíše na `0s` a hvězdy blikají unisono → bod 4d neudělovat.

## Bonus – Přelet rakety (3 b)

| # | Kritérium | Body | Získáno |
|---|---|---|---|
| B1 | `@keyframes prelet` se snímky 0 %, 50 %, 100 % | 1 | |
| B2 | koncový `translateX(calc(100vw + 160px))` | 1 | |
| B3 | `translateY(-40px)` v 50 % a `rotate(12deg)` ve všech snímcích | 0,5 | |
| B4 | `9s linear infinite` | 0,5 | |

**Typická chyba:** `rotate(12deg)` uvedené jen v jednom snímku – raketa se
místo naklonění otáčí tam a zpět (−0,5 b).

---

## Součet

| Úloha | 1 | 2 | 3 | 4 | Bonus | Celkem |
|---|---|---|---|---|---|---|
| Body | /7 | /6 | /5 | /4 | /3 | **/25** |

### Doporučená klasifikace

| Body | Známka |
|---|---|
| 23–25 | 1 |
| 19–22 | 2 |
| 14–18 | 3 |
| 9–13 | 4 |
| 0–8 | 5 |

Pro známku 1 **není** nutný bonus – 23 b lze získat i bez něj pouze při
bezchybném zpracování úloh 1–4 (22 b) … tj. pro 1 bez bonusu stanovte
hranici 22 b, případně bonus hodnoťte jako plus k výsledné známce.

---

## Doplňující otázky k ústní obhajobě

1. Jaký je rozdíl mezi `transition` a `animation`? Kdy použiješ co?
2. Proč se `transition` píše do základního stavu prvku a ne do `:hover`?
3. Co dělá `animation-fill-mode: forwards` a proč ho v těchto úlohách
   nepotřebujeme?
4. Proč se u `.obeh` animuje obal a ne samotná planeta `.telo`?
5. Které CSS vlastnosti jsou pro animaci „levné“ (prohlížeč je zvládá
   plynule) a které nutí prohlížeč přepočítávat rozvržení stránky?
   *(Očekávaná odpověď: `transform` a `opacity` ano; `width`, `height`,
   `top`, `left`, `margin` způsobují reflow.)*
6. Jak bys animace vypnul uživateli, který má v systému zapnuté omezení
   pohybu? *(Očekávaná odpověď: `@media (prefers-reduced-motion: reduce)`
   a v něm `animation: none` / `transition: none`.)*
