# DEIA-Enabled Data Sharing Observatory & Barometer v6 - Build Specification (CANONICAL)

> Supersedes docs/V6_PORTAL_BUILD_SPEC.md (which framed it as a film - WRONG).
> This is the correct brief: a direct OVERHAUL and UPGRADE of the existing v3
> (data_sharing_observatory_v3.html). Same product, materially better:
> a DEIA-enabled Data Sharing Observatory AND Barometer.
> NO film. NO narrative spine. The Observatory and Barometer ARE the product.
> Build as a single self-contained data_sharing_observatory_v6.html, chunked and
> validated section by section, NEVER one monolithic write.

## Owner & intent
- Owner: Emanuel Silva (emanukgb-dsit). NDL Pan-UK Data Sharing Observatory & Barometer.
- v3 done properly: keep what v3 had, upgrade it, make it genuinely DEIA-enabled throughout.
- Skin: GDS Internal Design System = GOV.UK Design System components + internal/admin density + darker PMO chrome. NOT the public GOV.UK marketing look.
- Single self-contained HTML file, no external build step, opens in a browser, hostable on GitHub Pages.
- Bar: as real as a front-end prototype gets. Data baked in, sourced, evidence-flagged. NO live API claims.

## The four upgrades over v3
v3 was a tabbed observatory dashboard. v6 keeps that shape and upgrades on four axes:
1. DEIA enabled throughout - every dataset/service carries DEIA metadata; every view disaggregates by population; blind spots declared, not hidden.
2. Barometer made real - a proper scored measurement model, not just display tiles.
3. Evidence discipline - every figure flagged FACTUAL / MODELLED / ILLUSTRATIVE / PARTIAL with named source.
4. The 360 accountability loop - the return path (did the action work, for the cohort) that v3 lacked.

## CORE SURFACES (the product)

### A. Observatory (system-in-context)
- Three zones / audiences: Observatory (public/transparent), Exchange (professional), Command Centre (PMO).
- Left rail: collections + loop + evidence/method.
- National overview, trends over time, equity heatmap, early-warning signals.
- Every view disaggregable by the DEIA population dimensions.

### B. Barometer (measurement engine)
- 10-dimension model: discoverability, ownership/stewardship, identity resolution, interoperability, data quality, legal/policy environment, use & reuse maturity, AI readiness, DEIA coverage, equity.
- RAG score + confidence + trend per dimension.
- Scores disaggregated by geography, demographics, socio-economic factors, accessibility needs.
- Equity Risk Score (ERS) = sum(factor x weight), 0-100. Weights: Gap Magnitude 25, Population Size 20, Trend 15, Vulnerability 15, Modifiability 15, Strategic Alignment 10. Bands: Critical 80-100 / High 60-79 / Medium 40-59 / Low 20-39 / Very Low 0-19.

### C. DEIA layer (the differentiator)
- Population dimensions to disaggregate everywhere: Geography, Socio-economic status, Disability & accessibility, Age & life stage, Gender identity, Ethnicity & race, Language & communication, Household & living situation, Digital inclusion & access.
- 6 DEIA metadata extensions on every dataset: ethnicityCoverage, deprivationLinkage, deiaImpactFlag, vulnerabilityMarker, panUKScope, healthEquityScore.
- Intersectional view: where multiple factors overlap (compound disadvantage).
- Cohort coverage rows on every collection: Absent / Partial / Evidenced. Observe absence, do not hide it. Framing: system failure, not group deficiency.

### D. Collections (worked use cases)
- Transplant equity (PoC) - binds on VISIBILITY.
- Inactivity & loneliness - binds on ATTRIBUTION (may stall at loop stage 6).
- Births & perinatal - binds on CAPTURE (1837 GRO); structural twin of transplant.
- Each: KPI cards with evidence flags + cohort-coverage blind-spot rows.

### E. 360 accountability loop (the upgrade v3 most lacked)
- 11 stages, 3 bands: Signal (1-3) / Return path (4-8, THE innovation: Confirm shipped / Verify results / Assess vs expected / Fix / Re-run) / Hold-the-line (9-11: Monitor / Escalate / Reassess).
- Stage 10 = flatline alarm (a cohort's signal dropping to zero escalates to a named owner).
- One full worked cohort journey (composite BSL-first Deaf transplant patient, consent mis-recorded refused), all 11 stages, with an explicit evidence boundary where FACTUAL ends and MODELLED/projected begins.

## Evidence discipline (non-negotiable, every figure)
FACTUAL (green): kidney wait ~2.5x (30 vs 12mo, NHSBT); 11/15 equity groups absent/critical; 0/4 nations interoperable API; ~1 in 6 UK deaths inactivity-linked (Sport England); +26% loneliness mortality (Holt-Lunstad 2015); 35%/15% deprivation gradient (OHID); MBRRACE-UK 2023 ethnic disparities.
MODELLED (amber): 23:1 ROI (~11.5:1 at half benefit); ~120M GBP/yr preventable harm.
ILLUSTRATIVE (pink): Health Equity Score 62-90 (unvalidated); composite personas.
PARTIAL (blue): 871k global loneliness deaths (WHO modelled); same-6-extensions-apply-to-births.
NEVER claim live data. Provenance banner: real sourced figures, baked in, not yet live-wired to source APIs (that is the next build). Community with/by/for claims CONTINGENT until duty-of-care protocol (ART004) done AND engagement happened.

## KIL data model (underpins the observatory; navigable view, NOT a film)
Entities: Dataset/DataService (hub), KPI, PopulationSegment (equity lens), IntersectionNode, Action, DeploymentEvent, OutcomeEvent, Organisation, Jurisdiction, Policy, Risk, BarometerScore, Evidence, Persona.
Edges: measured_by, affects, owned_by, governed_by, located_in, scored_by, exposes (derived - render dashed), acts_on, verified_by.
Lineage path (modelled, not live): Dataset > measured_by > KPI > affects > PopulationSegment > acts_on > Action > verified_by > Outcome. Mark MODELLED until Supabase provisioned.

## Build method (avoids the two prior crashes)
1. Scaffold HTML shell + CSS design tokens (GDS Internal) first; validate.
2. Append each surface (Observatory, Barometer, DEIA layer, each collection, loop, KIL view) as its own section; validate syntax between each.
3. All JS in-file, no external deps, no localStorage.
4. Commit to feature/v6-portal; keep main clean.
5. Final file presented for download/host.

## Reconciliation inputs (read before building when tools allow)
Existing data_sharing_observatory_v3.html (the thing being overhauled - match and exceed). NDL_Transplant_Data_Product_Spec.xlsx (real data dictionary + ROI model, supersedes seed). 16 Designer visuals (clean): Visual 2 SSOT+KIL, Visual 3 Intersectional layer, Visual 14 Equity Risk Score, Visual 16 technical architecture. Confluence governed record (gds-ogcdo Architecture): 360 loop 44171265; v6 Build Handoff 44138499; ART004 44171291.

## Definition of done
- Recognisably v3, overhauled and upgraded - same Observatory + Barometer product, materially better.
- DEIA enabled throughout: disaggregation everywhere, 6 metadata extensions, intersectional view, blind spots declared.
- Barometer is a real scored measurement model, not display-only tiles.
- Every figure flagged + sourced; provenance banner present; NO live-data claim.
- 360 loop present with the return path and the flatline alarm.
- KIL navigable view present (lineage MODELLED). NO film, NO narrative spine.
- GDS Internal skin. Single self-contained file, opens in a browser, hostable.
