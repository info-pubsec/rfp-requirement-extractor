# RFP Requirement Extractor

Paste RFP text, get a numbered requirements table. Extract every "shall", "must", and "will" from Canadian government solicitations into a structured format you can build a compliance matrix from.

## Usage

```python
from extractor import extract_requirements

requirements = extract_requirements(rfp_text)
for req in requirements:
    print(f"{req.number}. [{req.type}] {req.text}")
```

## Why this matters

Most losing proposals miss mandatory requirements — not because the bidder can't deliver, but because the requirement was buried on page 47 of a 200-page RFP. Systematic extraction prevents the most common disqualification.

## Related

- [Compliance Matrix Generator](https://gitlab.com/publicservicedataanalyticsandprocurement-group1/compliance-matrix-generator) — turn extracted requirements into a scored matrix
- [Government Proposal Templates](https://gitlab.com/publicservicedataanalyticsandprocurement-group1/government-proposal-templates) — six free DOCX templates
