# Segmenting Singapore Neighbourhoods for Targeted Senior Digital Inclusion

**Using geospatial analytics and unsupervised learning to inform neighbourhood-specific outreach for older adults.**

## Why this project?

Neighbourhoods with similarly large senior populations may have very different access to potential digital-inclusion touchpoints. A one-size-fits-all outreach approach may overlook these differences.

This project asks:

> What distinct neighbourhood profiles exist, and how could these profiles inform more targeted senior digital-inclusion outreach?

The analysis is intended to help policy and community stakeholders consider **where and how outreach could be delivered**, rather than merely ranking areas by the number of seniors.

## Data and scope

Combined **five publicly available datasets** at the **232 URA subzone** level in Singapore:

| Dataset | Why it matters |
| --- | --- |
| Census 2020 population | Number and share of residents aged 65+ |
| URA subzone boundaries | Common geographic unit for comparison |
| Wireless@SG hotspots | Potential public Wi-Fi access points |
| Community Clubs | Community outreach and learning touchpoints |
| Public libraries | Public learning and digital-resource access |

Sources: Singapore open data, including SingStat, URA, IMDA, People's Association and National Library Board datasets.

## Method

1. Integrated demographic, infrastructure and spatial information into a subzone-level dataset.
2. Engineered **eight features**: senior count and percentage; counts of Wi-Fi hotspots, Community Clubs and libraries; and proximity to the nearest facility of each type.
3. Explored variation in senior population and public-infrastructure accessibility.
4. Standardised the features, applied principal component analysis (PCA) and retained **four components explaining approximately 85% of variance**.
5. Used **K-Means clustering** to identify **four interpretable neighbourhood profiles**, considering elbow, silhouette and practical interpretability criteria.
6. Translated the profiles into differentiated outreach considerations.

The four-cluster solution achieved a **silhouette score of approximately 0.358**. Another cluster count had a slightly higher score, so interpretability was a deliberate model-selection consideration rather than a claim of a mathematically unique solution.

## What emerged?

- A high number of seniors does **not** necessarily imply poor access to public infrastructure.
- Neighbourhoods with similar senior populations can have markedly different combinations of Wi-Fi, Community Club and library availability.
- Four broad profiles provided a more nuanced starting point for outreach planning than senior counts alone.
- The profiles were geographically dispersed, underscoring the value of **subzone-level analysis** over simple regional assumptions.

### Illustrative policy responses

| Neighbourhood context | Possible response |
| --- | --- |
| High senior presence with existing Wi-Fi and Community Club touchpoints | Leverage these venues for targeted support |
| Areas with comparatively limited infrastructure | Investigate local barriers and validate demand |
| Areas with reasonable provision | Maintain coverage and monitor changing needs |
| Areas with accessible infrastructure but unknown usage | Examine whether seniors actually use available services |

These are planning hypotheses, **not evaluated interventions**.

## Why this matters for policy

The project demonstrates how demographic and geospatial evidence can help translate a broad inclusion objective into more differentiated area-level strategies. The intended users are public agencies and community organisations allocating limited outreach resources.

## Limitations

- **Infrastructure accessibility is not the same as digital inclusion.** Physical facilities do not directly measure digital literacy, device ownership, internet use or programme participation.
- Centroid-based proximity is an approximation, not a door-to-door travel-time measurement.
- Subzone averages may obscure individual circumstances and accessibility constraints.
- Results depend on available data and modelling choices; local validation is needed before interventions.

## Tools

Python · pandas · Geospatial Analysis · Feature Engineering · StandardScaler · PCA · K-Means · Data Visualisation

## Reproducibility

Add the final analysis notebook, documentation, official data links and (where redistribution is permitted) data or instructions to reproduce the prepared dataset. If maps or charts are included, label their geographic granularity and data vintage.

## Project context

Independent applied data science mini project, completed **September 2026**. Recommendations are exploratory and not official agency policy.
