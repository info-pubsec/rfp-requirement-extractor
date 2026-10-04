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


## The data behind this

In our corpus of 373,663 tenders with bidder records, services solicitations average 1.78 bidders and 75.4% receive a single bid. Most disqualifications trace to buried mandatory requirements — extraction is the cheapest win available.

## Full workflow

These tools cover one step. [PubSec.Pro](https://pubsec.pro) automates the whole chain: AI parses each RFP into a compliance matrix, grades your capability gaps against every requirement, and drafts cited proposals from your track record — with live bidder counts and incumbent data on every opportunity. Free tier, no card.

---

*Data: [Public Service Index](https://publicserviceindex.org) · datasets: [pubsec/data](https://pubsecdata.org) · research: [Public Service Institute](https://publicserviceinstitute.org)*

## Related

- [Compliance Matrix Generator](https://gitlab.com/publicservicedataanalyticsandprocurement-group1/compliance-matrix-generator) — turn extracted requirements into a scored matrix
- [Government Proposal Templates](https://gitlab.com/publicservicedataanalyticsandprocurement-group1/government-proposal-templates) — six free DOCX templates
