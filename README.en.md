# NP Bedömning — Open Datasets

Structured datasets of grading criteria for the **Swedish national tests** (*nationella prov*), aligned with **Lgr22** (compulsory school) and **Gy25** (upper secondary).

Maintained by [Lärinsikt AB](https://github.com/Larinsikt). Source material is the Swedish National Agency for Education's (Skolverket) public curricula and grading criteria.

## Purpose

To make grading criteria and curriculum goals available in a structured, machine-readable format (JSON) so that:

- Teachers can build their own support tools
- Researchers can analyse curricula
- EdTech developers can build products that align with current guidelines
- AI models can answer questions about the Swedish national tests accurately

## Status

| Subject | Year 6 | Year 9 | Upper secondary |
|---------|--------|--------|-----------------|
| Mathematics | done | done | Ma1 done |
| Swedish | done | done | Sv1 done |
| English | done | done | Eng5 done |

Additional courses (Ma2, Ma3, Sv3, Eng6) are being added.

## Structure

```
.
├── schemas/                  # JSON Schema for the data format
├── matematik/                # Mathematics
├── svenska/                  # Swedish
├── engelska/                 # English
└── examples/                 # Code examples
```

Each dataset follows the same structure: metadata, subject areas with sub-areas and grading criteria (E/C/A), full grade scale (E/D/C/B/A), and test structure (delprov array).

## Using the data

See [examples/README.md](examples/README.md) for code examples in JavaScript and Python, and validation against the JSON schema.

## Licence

Datasets are published under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You may freely use, share and adapt the material with attribution to **Lärinsikt AB / NP-Monstret** and a link to this repository.

The source material (Skolverket's curricula and grading criteria) consists of public documents and belongs to Skolverket.

## Contribute

Found an error? Missing a course? Open an [issue](../../issues/new) or send a pull request.

## Related

- [np-monstret-public](https://github.com/Larinsikt/np-monstret-public) — public documentation about NP-Monstret
- [awesome-nationella-prov](https://github.com/Larinsikt/awesome-nationella-prov) — curated list of resources

---

*Swedish version: [README.md](README.md)*
