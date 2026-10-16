---
name: radio-slidedeck
description: "Maak een nieuw RADIO-trainingsdeck (HTML-slides) voor een vibecoding-sessie: vraag de trainingsgegevens uit en vul de RADIO-template in."
---

# RADIO-slidedeck maken

Gebruik deze skill wanneer iemand een nieuw RADIO-trainingsdeck wil. Werk in het Nederlands.

Template: `radio-template.html` in de root van deze repository. Het is al ingevuld met een voorbeeld (de casus Vraagscherper) en voorbeeldnamen; vervang die door de gegevens van de training.

## Werkwijze

1. Stel eerst de vragen hieronder. Vraag alleen wat nog niet bekend is; doe bij ontbrekende details een voorstel dat past bij de doelgroep.
2. Kopieer `radio-template.html` naar `<naam-casus>.html` in de root (kleine letters, streepjes, geen spaties). De bestandsnaam is de naam van het projectje of de casus, bijvoorbeeld `vraagscherper.html`.
3. Pas in het nieuwe bestand alleen het blok `var TRAINING = { ... }` aan. Laat opmaak, logo, slides en scripts ongemoeid.
4. Controleer dat er geen `""` lege velden meer zijn (die verschijnen geel als `[vul in: ...]`) en dat aanhalingstekens in teksten geëscaped zijn.
5. Overschrijf nooit een bestaand deck zonder te vragen.

## De vragen die je elke keer stelt

1. **Hoeveel deelnemers zijn er?** Dit bepaalt de duo-indeling op slide 1. Vraag ook of je de namen hebt, en of ze op volgorde of willekeurig verdeeld moeten worden.
2. **Wie is de doelgroep?** Bijvoorbeeld SG, manager, beleidsmedewerker of DT. Dit woord komt automatisch terug in de teksten.
3. **Wie zijn wij?** De trainers voor deze sessie: naam, rol en organisatie (1 tot 4 personen).
4. **Wat is de demo-prompt (prompt 1)?** Hiermee bouwt de trainer live het basisdashboard op slide 3.
5. **Wat is de vervolgprompt (prompt 2)?** Een aanpassing op de demo-prompt die de trainer daarna laat zien. Zonder demo-prompt is er geen vervolgprompt, dus die twee horen bij elkaar.
6. **Wat is prompt 3 voor deze doelgroep?** Een prompt die specifiek op de groep is afgestemd, zoals "wat kan ik als {doelgroep} nu het beste doen?".
7. **Wat is de use-case prompt?** Een concrete casus die past bij de doelgroep. Iedereen typt deze zelf in ("Jullie beurt").
8. **Welke dashboards komen op de menukaart?** 2 of 3 opties, het liefst afgestemd op de doelgroep: tooling die helpt bij hun vraagstuk. Per optie een titel, korte uitleg, label en eventueel een volledige prompt.
9. **Hoe lang hebben ze om te bouwen?** In minuten. De timer op het spiekbriefje loopt hierop af.
10. **Titel, ondertitel en datum** van de training voor de titelslide.
11. **Hoe heet het projectje of de casus?** Dat wordt de bestandsnaam.

## Het TRAINING-blok invullen

```js
var TRAINING = {
  /* Titelslide */
  titel: "In een stroomversnelling",
  ondertitel: "{doelgroep} bouwt met AI",
  datum: "4 november 2026",

  /* Doelgroep: komt terug op elke plek waar {doelgroep} staat */
  doelgroep: "DT",

  /* Duo's */
  deelnemers: 5,
  namen: ["Deelnemer 1","Deelnemer 2","Deelnemer 3","Deelnemer 4","Deelnemer 5"],  /* optioneel, mag [] zijn */
  husselen: false,   /* true = willekeurig verdelen */

  /* Slide 3: demo door de trainer */
  prompt1: { titel: "Prompt 1 · ...", tekst: "..." },

  /* Wie wij zijn: initialen worden automatisch gemaakt */
  team: [
    { naam: "Roy van Sichem",  rol: "Projectleider en AI-trainer", org: "RADIO" },
    { naam: "Machiel Ribbens", rol: "AI-trainer",                  org: "RADIO" }
  ],

  /* Vervolg op de demo */
  prompt2: { titel: "Prompt 2 · ...", tekst: "..." },

  /* Specifiek voor de doelgroep */
  prompt3: { titel: "Prompt 3 · ...", tekst: "..." },

  /* Jullie beurt */
  usecase: { titel: "Prompt · ...", tekst: "..." },

  /* Menukaart: 2 of 3 opties */
  menukaart: {
    ondertitel: "Dashboards voor het vraagstuk van de {doelgroep}",
    opties: [
      { titel: "...", tekst: "...", label: "...", prompt: "..." },
      { titel: "...", tekst: "...", label: "..." }
    ]
  },

  /* Bouwtijd in minuten */
  bouwtijd: 45
};
```

Handig om te weten:

- `{doelgroep}` en `{bouwtijd}` mag je in elke tekst gebruiken. Ze worden automatisch ingevuld.
- Een leeg veld (`""`) verschijnt geel op de slide als `[vul in: ...]`, zodat je ziet wat nog mist.
- Bij een oneven aantal deelnemers wordt de laatste groep een trio.
- Zijn er geen namen, dan toont slide 1 de duo's met puntjes (…) in plaats van namen.
- Heeft een menu-optie een `prompt`, dan kopieert een klik op de kaart die volledige prompt naar het klembord.
- De bouwtijd stuurt zowel de timer op het spiekbriefje als de regel op de slide "Duo vs. duo".
- Let op aanhalingstekens: gebruik je `"` in een tekst, zet er dan een `\` voor (`\"`), of gebruik `'` of „…".

## Het RADIO-logo

Het logo is geen plaatje maar het getypte woord **RADIO** met een rode verticale balk links (kleur `--rood`, `#D52B1E`). Het staat klein linksboven op elke slide en groot op de titelslide. Je hoeft er niets aan te doen; het zit in het template.

## Volgorde van de slides (15)

1. Duo's (automatisch uit deelnemers en namen)
2. Titel met RADIO-logo
3. Prompt 1: demo, de trainer bouwt live het basisdashboard
4. Wie wij zijn
5. Prompt 2: vervolg op de demo
6. Prompt 3: voor de doelgroep
7. Waarom dit zelf doen
8. Jullie beurt
9. Use-case prompt
10. Tussenstap: sluit de terminal
11. Duo vs. duo
12. Menukaart (2 of 3 dashboards)
13. Spiekbriefje met timer (start vanzelf als je op deze slide komt)
14. Presenteren
15. Bedankt

De oude slide over ons werk en onze loopbaan is eruit gehaald; daar gaan we niet dieper op in.

## Tijdens de presentatie

- Volgende slide: pijl rechts, pijl omlaag, spatie of Page Down. Vorige: pijl links, pijl omhoog of Page Up.
- Home en End springen naar de eerste en laatste slide.
- `F` zet volledig scherm aan of uit.
- Klik op een promptvenster om de prompt naar het klembord te kopiëren.
- De slide staat in de URL, dus herladen houdt je op dezelfde slide.

