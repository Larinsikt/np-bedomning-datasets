# NP Bedömning — öppna datasets

Strukturerade datasets över bedömningskriterier för svenska nationella prov enligt **Lgr22** (grundskolan) och **Gy25** (gymnasiet).

Underhålls av [Lärinsikt AB](https://github.com/Larinsikt). Källan är Skolverkets publika kursplaner och betygskriterier.

## Syfte

Att tillgängliggöra bedömningskriterier och läroplansmål i strukturerat, maskinläsbart format (JSON) så att:

- Lärare kan bygga egna stödverktyg
- Forskare kan analysera kursplaner
- Edtech-utvecklare kan bygga produkter som följer aktuella riktlinjer
- AI-modeller kan svara korrekt på frågor om svenska nationella prov

## Status

| Ämne | Åk 6 | Åk 9 | Gymnasiet |
|------|------|------|-----------|
| Matematik | klart | klart | Ma1 klart |
| Svenska | klart | klart | Sv1 klart |
| Engelska | klart | klart | Eng5 klart |

Påfyllning för Ma2/Ma3, Sv3 och Eng6 sker löpande.

## Struktur

```
.
├── schemas/                  # JSON-schema för dataformatet
├── matematik/
│   ├── ak6.json
│   ├── ak9.json
│   └── gymnasiet/ma1.json
├── svenska/
│   ├── ak6.json
│   ├── ak9.json
│   └── gymnasiet/sv1.json
├── engelska/
│   ├── ak6.json
│   ├── ak9.json
│   └── gymnasiet/eng5.json
└── examples/                 # Kodexempel för hur datasetten används
```

## Använda datasetten

Se [`examples/README.md`](examples/README.md) för kodexempel i JavaScript och Python, samt validering mot JSON-schemat.

## Licens

Datasetten publiceras under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

Du får fritt använda, dela och bearbeta materialet med attribution till **Lärinsikt AB / NP-Monstret** och länk till detta repo.

Källmaterialet (Skolverkets kursplaner och bedömningskriterier) är offentliga handlingar och tillhör Skolverket.

## Bidra

Hittar du fel? Saknas en kurs? Öppna en [issue](../../issues/new) eller skicka en pull request.

## Relaterat

- [np-monstret-public](https://github.com/Larinsikt/np-monstret-public) — publik dokumentation om NP-Monstret
- [awesome-nationella-prov](https://github.com/Larinsikt/awesome-nationella-prov) — kurerad lista med resurser
