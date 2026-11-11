# Kushtha Roga Database: Ayurvedic Dermatology

An open, structured database of **Kushtha Roga** (classical Ayurvedic skin disorders): classification, nidana (etiology), samprapti (pathogenesis), lakshana (clinical features), upashaya, chikitsa (management), and tentative modern-dermatology correlations, each tied to classical source references.

> **Status: v0.1 (draft).** The seed data lists the 18 classical types with placeholder fields. Every record carries a `verification_status` and must be checked against the primary text before being cited. Nothing here is clinical advice.

## Why this exists

Classical descriptions of Kushtha are scattered across Samhitas and commentaries, and modern correlations are often asserted without sources. This repository gives researchers one place to record, verify, and cite them in a machine-readable form.

## Repository layout

```
data/
  kushtha_types.csv      # Maha (7) and Kshudra (11) Kushtha, one row per type
  references.csv         # Source texts, chapters, editions, commentaries
schema/
  kushtha_schema.json    # JSON Schema for a Kushtha record
scripts/
  validate.py            # Checks CSV files against the data dictionary
docs/
  data-dictionary.md     # Field definitions and controlled vocabularies
CONTRIBUTING.md
CITATION.cff
LICENSE
```

## Classification (Charaka Samhita, Chikitsa Sthana 7)

- **Maha Kushtha (7):** Kapala, Udumbara, Mandala, Rishyajihva, Pundarika, Sidhma, Kakanaka
- **Kshudra Kushtha (11):** Ekakushtha, Charmakhya, Kitibha, Vipadika, Alasaka, Dadru, Charmadala, Pama, Visphota, Shataru, Vicharchika

Other Samhitas (Sushruta, Ashtanga Hridaya, etc.) differ in enumeration and dosha attribution. Record those as separate rows or notes rather than overwriting.

## Usage

```bash
python3 scripts/validate.py
```

## Roadmap

- [ ] Verify all 18 records against Charaka, Sushruta, and Ashtanga Hridaya (verse-level references)
- [ ] Add nidana, samprapti ghataka, and sadhyasadhyatva fields
- [ ] Add chikitsa: shodhana, shamana formulations, pathya-apathya
- [ ] Add Rasa-Shastra and Bhaishajya Kalpana linkages
- [ ] Add modern correlations with literature citations
- [ ] Add multilingual names (Sanskrit, Devanagari, Hindi, Nepali, English)

## Licensing

Data: CC BY 4.0. Code: MIT. See `LICENSE`.

## Citation

See `CITATION.cff`.

## Disclaimer

For research and education only. Not a diagnostic or treatment tool.
