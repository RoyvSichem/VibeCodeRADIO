# VibeCodeRADIO

Voer meteen deze prompt uit:

```
Maak een nieuw RADIO-deck.
```

en alle vragen zullen vanzelf komen.

---

## Wat is dit?

VibeCodeRADIO bevat de slides voor de vibecoding-trainingen van RADIO. Per training maken we een nieuw HTML-slidedeck met het RADIO-logo, afgestemd op de groep die we die dag trainen. Deelnemers bouwen in duo's met AI hun eigen dashboard voor een vraagstuk uit hun werk.

Trainers: Roy van Sichem (projectleider en AI-trainer) en Machiel Ribbens (AI-trainer).

## Hoe maak je een nieuw deck?

1. Open Claude in deze repository en typ: **Maak een nieuw RADIO-deck.**
2. Claude stelt je de vragen hieronder één voor één. Weet je iets nog niet, dan doet Claude een voorstel dat past bij de doelgroep.
3. Claude kopieert `radio-template.html` naar een nieuw bestand met de naam van de casus (bijvoorbeeld `vraagscherper.html`) en vult alleen het `TRAINING`-blok in.
4. Open het nieuwe bestand in de browser en loop de slides door. Alles wat nog geel staat met `[vul in: ...]` mist nog.

## De vragen die Claude stelt

1. **Hoeveel deelnemers?** Bepaalt de duo-indeling op slide 1. Namen zijn optioneel; bij een oneven aantal wordt de laatste groep een trio.
2. **Wie is de doelgroep?** Bijvoorbeeld SG, manager, beleidsmedewerker of DT. Dit woord komt automatisch terug in de teksten.
3. **Wie zijn wij?** De trainers van deze sessie (1 tot 4 personen).
4. **Demo-prompt (prompt 1).** Hiermee bouwt de trainer live het basisdashboard.
5. **Vervolgprompt (prompt 2).** Een aanpassing op de demo-prompt die de trainer daarna laat zien.
6. **Prompt 3 voor de doelgroep.** Specifiek afgestemd op de groep.
7. **Use-case prompt.** Een concrete casus voor de doelgroep, die iedereen zelf intypt.
8. **Menukaart.** 2 of 3 dashboard-opties die helpen bij het vraagstuk van de doelgroep.
9. **Bouwtijd in minuten.** De timer op het spiekbriefje loopt hierop af.
10. **Titel, ondertitel en datum** voor de titelslide.
11. **Naam van de casus.** Dat wordt de bestandsnaam.

## Bestanden

| Bestand | Wat het is |
|---|---|
| `radio-template.html` | Het herbruikbare template. Niet zelf in een training gebruiken, alleen kopiëren. |
| `vraagscherper.html` | Voorbeelddeck (DT van RADIO, 4 november 2026). |
| `INSTRUCTIES.md` | Uitgebreide handleiding, inclusief het volledige `TRAINING`-blok en alle tips. |
| `skills/radio-slidedeck/SKILL.md` | De Claude-skill die de vragen stelt en het deck invult. |

## Slides (15)

1. Duo's
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
13. Spiekbriefje met timer
14. Presenteren
15. Bedankt

## Tijdens de presentatie

- Volgende slide: pijl rechts, pijl omlaag, spatie of Page Down. Vorige: pijl links, pijl omhoog of Page Up.
- Home en End springen naar de eerste en laatste slide.
- `F` zet volledig scherm aan of uit.
- Klik op een promptvenster om de prompt naar het klembord te kopiëren.
- De timer start vanzelf zodra je op het spiekbriefje komt.

Zelf aanpassen zonder Claude? Zie [INSTRUCTIES.md](INSTRUCTIES.md).
