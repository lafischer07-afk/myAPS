# APS Calculator — Data Update Guide

## When to Update

Universities publish new intake requirements annually, typically **February–June**.
Target one big update around **May–June** each year when most data is available.

### Publishing Timeline (approximate)

| University | Abbr | Typical Publish Window | URL |
|---|---|---|---|
| University of Pretoria | UP | Feb–Mar | https://www.up.ac.za/programmes |
| University of Johannesburg | UJ | Feb–Mar | https://www.uj.ac.za/programmes/ |
| Wits | Wits | Feb–Mar | https://www.wits.ac.za/studyatwits/ |
| UCT | UCT | Feb–Apr | https://www.uct.ac.za/study/undergraduate |
| Stellenbosch | Stell | Feb–Apr | https://www.maties.com/programmes/ |
| UKZN | UKZN | Mar–May | https://applications.ukzn.ac.za |
| Free State | UFS | Mar–May | https://www.ufs.ac.za/supportservices/departments/student-academic-services-home/prospective-students |
| North-West | NWU | Mar–May | https://studies.nwu.ac.za |
| Rhodes | Rhodes | Mar–May | https://www.ru.ac.za/admissiongateway/departmentsandfaculties/ |
| TUT | TUT | Apr–Jun | https://www.tut.ac.za/programmes |
| CPUT | CPUT | Apr–Jun | https://www.cput.ac.za/study |
| DUT | DUT | Apr–Jun | https://www.dut.ac.za/admissions/ |

## How to Update

1. Visit each university URL above
2. Check the APS/points and subject requirements for each programme in `index.html`
3. Update the `req` object for any programme that changed (aps, math, phys, lifesci, hl, acc)
4. Add/remove programmes if the university added or discontinued any
5. Update these fields per university in `UNI_PROGRAMMES`:
   - `dataYear` — e.g. change `'2027'` to `'2028'`
   - `dataSource` — set to `'official'` if sourced directly, `'mixed'` if some were estimated
6. Update `DATA_LAST_UPDATED` at the top of the data section (e.g. `'2027-06-15'`)

## What to Check Per Programme

- **APS / Points score** — the minimum total score
- **Maths minimum %** — `math` field
- **Physical Sciences minimum %** — `phys` field
- **Life Sciences minimum %** — `lifesci` field
- **Home Language minimum %** — `hl` field
- **Accounting minimum %** — `acc` field (BCom programmes)
- **Whether Maths Literacy is accepted** — some programmes only accept pure Maths

## Current Data Status (as of 2026-10-10)

- **2027 official:** UP, UJ, UCT, Stellenbosch, UFS
- **2027 mixed:** UKZN
- **2025–2027 mixed:** Wits, Rhodes
- **2025–2026 mixed:** NWU
- **2026 mixed:** TUT, CPUT
- **2026–2027 mixed:** DUT

## Notes

- "mixed" means some programme data was cross-referenced from multiple years or secondary sources
- "official" means all data was sourced directly from the university's published requirements
- UoTs (TUT, CPUT, DUT) are often slower to publish and harder to find exact APS breakdowns
- Requirements rarely change drastically year-to-year, but always verify before publishing
