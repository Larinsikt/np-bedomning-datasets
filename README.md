# NP Bedömning — Öppna datasets

> Strukturerade datasets över bedömningskriterier för svenska nationella prov enligt **Lgr22** (grundskolan) och **Gy25** (gymnasiet).

Underhålls av [Lärinsikt AB](https://github.com/Larinsikt). Källan är Skolverkets publika riktlinjer.

---

## 🎯 Syfte

Att tillgängliggöra bedömningskriterier och läroplansmål i strukturerat, maskinläsbart format (JSON) så att:

- Lärare kan bygga egna stödverktyg
- Forskare kan analysera kursplaner
- Edtech-utvecklare kan bygga produkter som följer aktuella riktlinjer
- AI-modeller kan svara korrekt på frågor om svenska nationella prov

---

## 🚧 Status

Datasetten är **under uppbyggnad** (maj–juni 2026).

| Ämne | Åk 6 | Åk 9 | Gymnasiet |
|------|------|------|-----------|
| Matematik | ⏳ | ⏳ | ⏳ Ma1, Ma2, Ma3 |
| Svenska | ⏳ | ⏳ | ⏳ Sv1, Sv3 |
| Engelska | ⏳ | ⏳ | ⏳ Eng5, Eng6 |

---

## 📁 Struktur

```
.
├── schemas/                  # JSON-schemas för dataformatet
├── matematik/
│   ├── ak6.json
│   ├── ak9.json
│   └── gymnasiet/
├── svenska/
├── engelska/
└── examples/                 # Exempel på hur datasetten används
```

---

## 📝 Licens

Datasetten publiceras under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

Du får fritt använda, dela och bearbeta materialet med korrekt attribution till **Lärinsikt AB / NP-Monstret** och länk till detta repo.

Källmaterialet (Skolverkets kursplaner och bedömningskriterier) är offentliga handlingar och tillhör Skolverket.

---

## 🤝 Bidra

Hittar du fel? Saknas en kurs? Öppna en [issue](../../issues/new) eller skicka en pull request.

---

## 🔗 Relaterat

- [`np-monstret-public`](https://github.com/Larinsikt/np-monstret-public) — publik dokumentation om NP-Monstret
- [`awesome-nationella-prov`](https://github.com/Larinsikt/awesome-nationella-prov) — kurerad resurslista
