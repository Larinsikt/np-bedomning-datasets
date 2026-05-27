# Exempel på användning av datasetten

## Ladda dataset (JavaScript)

```javascript
const data = require('./matematik/ak9.json');

console.log(`Ämne: ${data.amne}`);
console.log(`Årskurs: ${data.arskurs}`);
console.log(`Ämnesområden: ${data.amnesomraden.map(a => a.namn).join(', ')}`);

// Hämta E-nivå kriterier för ett ämnesområde
const algebra = data.amnesomraden.find(a => a.namn === 'Algebra');
console.log('Algebra E-nivå:', algebra.delomraden[0].kriterier.E);
```

## Ladda dataset (Python)

```python
import json

with open('matematik/ak9.json', 'r', encoding='utf-8') as f:
    data = json.load(f)

print(f"Ämne: {data['amne']}")
print(f"Årskurs: {data['arskurs']}")

# Hämta alla A-nivå kriterier
for area in data['amnesomraden']:
    for sub in area['delomraden']:
        print(f"{area['namn']} > {sub['namn']}: {sub['kriterier'].get('A', 'N/A')}")
```

## Validera mot schema

```bash
# Installera json-schema validator
npm install ajv

# Validera en fil
node -e "
const Ajv = require('ajv');
const schema = require('./schemas/bedomningskriterier.schema.json');
const data = require('./matematik/ak9.json');
const ajv = new Ajv();
const validate = ajv.compile(schema);
const valid = validate(data);
console.log(valid ? 'Valid!' : validate.errors);
"
```

## Filtrera efter betygsnivå

```javascript
// Hämta alla kriterier på C-nivå
const cKriterier = [];
for (const area of data.amnesomraden) {
  for (const sub of area.delomraden) {
    if (sub.kriterier.C) {
      cKriterier.push({
        omrade: area.namn,
        delomrade: sub.namn,
        kriterie: sub.kriterier.C
      });
    }
  }
}
console.log(`Hittade ${cKriterier.length} C-nivå kriterier`);
```

## Hämta provstruktur

```javascript
// Visa vilka delprov som finns och hur långa de är
for (const dp of data.provstruktur.delprov) {
  console.log(`Delprov ${dp.beteckning}: ${dp.typ}, ${dp.tidslangd_minuter} min, tillåtna hjälpmedel: ${dp.hjalpmedel.join(', ')}`);
}
```

---

*Mer exempel kommer när fler dataset läggs till.*