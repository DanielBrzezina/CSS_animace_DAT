# Maturitní úloha – CSS animace

**Téma:** transformace, přechody, animace klíčových snímků (keyframes)
**Čas na vypracování:** 25 minut
**Maximální počet bodů:** 25 (22 b základní úlohy + 3 b bonus)

---

## Zadání

Dostáváš rozpracovaný web **Průzkumník sluneční soustavy**. Stránka je kompletně
hotová po stránce obsahu, rozvržení i barev – jen je úplně **nehybná**.
Tvým úkolem je ji rozpohybovat pomocí CSS.

### Soubory

| Soubor | Co s ním |
|---|---|
| `index.html` | **Neupravuj.** Pouze si v něm najdi názvy tříd. |
| `style.css` – ČÁST A | **Neupravuj.** Hotové rozvržení, barvy a tvary. |
| `style.css` – ČÁST B | **Zde pracuj.** U každé úlohy je připravené místo. |

Stránku si otevři v prohlížeči a po každé změně ji obnov (F5), abys průběžně
viděl výsledek.

### Pravidla

- Používej **pouze CSS**, žádný JavaScript.
- Nepřidávej do HTML nové prvky ani třídy.
- Vše piš do části B v souboru `style.css`.
- Kód odsazuj a formátuj tak, jak je to v části A.

### Prvky, se kterými budeš pracovat

| Selektor | Co to je |
|---|---|
| `.karta` | karta jedné planety (4× na stránce) |
| `.karta__kule` | barevná kulička planety uvnitř karty |
| `.slunce` | Slunce v modelu soustavy |
| `.obeh` | neviditelný obal, jehož otáčením objede planeta svou dráhu |
| `.draha--merkur`, `.draha--venuse`, `.draha--zeme`, `.draha--mars` | jednotlivé oběžné dráhy |
| `.hvezda` | jedna hvězda v pozadí (18× na stránce) |
| `.raketa` | raketa v levém horním rohu |

---

## Úloha 1 – Přechody a transformace na kartách planet (7 bodů)

Zajisti, aby karta planety reagovala na **najetí myší** (`:hover`):

1. karta se posune o **12 px nahoru** a zvětší se na **105 %**,
2. stín karty zesílí na `0 18px 38px rgba(0, 0, 0, .5)`,
3. kulička planety v kartě (`.karta__kule`) se otočí o **18°** a zvětší se na **112 %**,
4. všechny tyto změny jsou **plynulé, ne skokové** – karta **0,35 s**,
   kulička **0,45 s**, obojí s náběhem `ease-out`.

> **Nápověda:** přechod (`transition`) se zapisuje do základního stavu prvku,
> nikoli do stavu `:hover`. Jinak se prvek plynule vrací, ale skokem se mění.

## Úloha 2 – Oběh planet kolem Slunce (6 bodů)

Vytvoř animaci klíčových snímků s názvem **`obeh`**, která prvek otočí
z **0°** na **360°**, a přiřaď ji **všem** prvkům `.obeh` tak, aby:

- běžela **nekonečně** dokola,
- měla **rovnoměrnou** rychlost (bez zpomalení na začátku a na konci),
- každá planeta měla **jinou dobu oběhu**:

| Planeta | Doba oběhu |
|---|---|
| Merkur | 4 s |
| Venuše | 7 s |
| Země | 11 s |
| Mars | 16 s |

Samotnou animaci přiřaď jen **jednou** (společně pro všechny `.obeh`),
rozdílné doby oběhu dořeš přes jednotlivé dráhy.

## Úloha 3 – Pulzující Slunce (5 bodů)

Vytvoř animaci **`puls`** pro Slunce (`.slunce`), která:

- plynule mění velikost ze **100 %** na **112 %**,
- zároveň mění vnější záři z `0 0 40px rgba(255, 183, 3, .5)`
  na `0 0 70px rgba(255, 183, 3, .85)`,
- trvá **3 s**, běží **nekonečně**, zrychluje i zpomaluje (**`ease-in-out`**),
- po dojetí na konec se přehraje **pozpátku zpět** – Slunce tedy nesmí
  skokem „splasknout“ a začít znovu.

Použij **pouze dva klíčové snímky** (`from` a `to`).

## Úloha 4 – Blikající hvězdy (4 body)

Vytvoř animaci **`blikani`** pro hvězdy (`.hvezda`):

- průhlednost se mění z **0.15** na **1**,
- velikost se mění ze **70 %** na **110 %**,
- trvání **2 s**, **nekonečně**, `ease-in-out`, přehrávání **tam a zpět**,
- hvězdy **nesmí blikat všechny současně**. Každá hvězda má v HTML
  připravenou vlastní proměnnou `--d` se svým zpožděním
  (např. `style="--d: 1.1s"`). Tuto proměnnou ve své animaci využij.

## Bonus – Raketa přelétá obrazovku (3 body)

Rozhýbej raketu (`.raketa`) animací **`prelet`**, která:

- ji posune od levého okraje až za pravý okraj obrazovky –
  koncová vodorovná pozice je `calc(100vw + 160px)`,
- v **polovině** cesty ji nadzvedne o **40 px** výš,
- po celou dobu ji drží naklopenou o **12°**,
- trvá **9 s**, probíhá **rovnoměrně** a **nekonečně**.

Použij klíčové snímky **0 %, 50 % a 100 %**.

---

## Jak bude práce hodnocena

| Část | Body |
|---|---|
| Úloha 1 – přechody a transformace (hover) | 7 |
| Úloha 2 – keyframes: oběh planet | 6 |
| Úloha 3 – keyframes: pulzující Slunce | 5 |
| Úloha 4 – keyframes: blikající hvězdy | 4 |
| Bonus – keyframes: přelet rakety | 3 |
| **Celkem** | **25** |

Body se udělují za **funkční výsledek v prohlížeči** i za **správný zápis CSS**.
Pokud se ti nějaká úloha nepovede celá, odevzdej i částečné řešení –
dílčí body se započítávají.
