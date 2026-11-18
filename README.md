# Maturitní úloha – CSS animace (sluneční soustava)

Praktická úloha na **25 minut** k tématu *transformace, přechody a animace
klíčových snímků*. Žák dostane hotovou, ale nehybnou stránku o planetách
a rozpohybuje ji pomocí CSS.

## Obsah

| Cesta | Určeno pro | Popis |
|---|---|---|
| [ZADANI.md](ZADANI.md) | žák | Zadání k vytištění nebo zobrazení. |
| [zadani/](zadani/) | žák | Pracovní soubory – `index.html` + `style.css` s částí B k doplnění. |
| [reseni/](reseni/) | učitel | Vzorové řešení. **Nedávat žákovi.** |
| [HODNOCENI.md](HODNOCENI.md) | učitel | Bodový rozpis, uznávané varianty, typické chyby, otázky k obhajobě. |

## Příprava před zkouškou

1. Zkopíruj žákovi **pouze** složku `zadani/` a soubor `ZADANI.md`.
2. Ověř, že se `zadani/index.html` otevře v prohlížeči – stránka musí být
   vidět barevně a kompletně, jen bez jakéhokoli pohybu.
3. Rozhodni o povolených pomůckách. Doporučení: povolit prohlížeč s
   dokumentací MDN (úloha testuje porozumění, ne memorování zápisu),
   nebo vydat jednostránkový tahák se syntaxí `transition`, `@keyframes`
   a `animation`.

## Co úloha ověřuje

- `transition` – správné umístění do základního stavu, výběr vlastností, trvání, náběh
- `transform` – `translateY`, `scale`, `rotate` a jejich skládání do jedné vlastnosti
- `@keyframes` – zápis snímků (`from`/`to` i procenta)
- `animation` – `duration`, `timing-function`, `iteration-count`, `direction`, `delay`
- práce s vlastní CSS proměnnou (`var(--d)`) a pořadí zápisu vůči zkratce
- pochopení struktury: co se musí animovat, aby planeta obíhala, a ne se otáčela na místě

## Technické poznámky

- Žádné externí obrázky, fonty ani JS – planety i Slunce jsou CSS gradienty,
  raketa je emoji. Funguje offline a bez internetu.
- Vše běží v současných prohlížečích bez prefixů.
- Rychlá kontrola: po doplnění části B musí planety obíhat Slunce, Slunce
  pulzovat, hvězdy blikat rozfázovaně a karty reagovat na `:hover`.
