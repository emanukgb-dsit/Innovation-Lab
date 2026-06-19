# Data Sharing Observatory v6 - Build Specification

> This is the blueprint for a COMPLETE OVERHAUL, not an enhancement of v3.
> v3 was a tabbed dashboard. v6 is a narrative-driven, multi-surface experience.
> Build in a file-enabled environment as a single self-contained data_sharing_observatory_v6.html, chunked and validated, NEVER one monolithic write.

## Owner & intent
- Owner: Emanuel Silva (emanukgb-dsit / cyberdudeuk). NDL Pan-UK Data Sharing Observatory vision.
- Skin: GDS Internal Design System - GOV.UK components + internal/admin density + darker PMO chrome. NOT the public GOV.UK look.
- Single self-contained HTML file, no external build step, opens in a browser, hostable on GitHub Pages.
- Bar: as real as a front-end prototype gets. Data baked in, sourced, evidence-flagged. NO live API claims.

## Why v6 is NOT v3-with-extras (the overhaul test)
v3 = left-rail tabs over a dashboard. If v6 looks like tabs over a dashboard, it has FAILED. v6 is a JOURNEY: the user is taken from the origin sketch to the future-state architecture and down into the data model, as a narrative they move through - not panels they click between.

## The six surfaces v6 MUST contain

### 1. The Film - napkin to future state (lands FIRST)
Scrubbable five-act transition: I Napkin sketch (make the invisible visible; nobody checks if it worked); II Braindump (raw entities/principles as chips, externalised thinking not delivery); III Vision (organised into three horizons + 16-visual set); IV Future-state architecture board (7-layer EA stack); V KIL lineage (navigate into the data model). Playable AND scrubbable. The spine of the overhaul.

### 2. Observatory working surface (three zones)
Observatory (public), Exchange (professional), Command Centre (PMO). Five rail items: 3 collections + 360 loop + evidence-method. ONE surface among six, not the whole app.

### 3. Three collections (replication triad) - each a full view
Transplant equity (PoC) binds on VISIBILITY; Inactivity & loneliness binds on ATTRIBUTION (may stall at loop stage 6); Births & perinatal binds on CAPTURE (1837 GRO), structural twin of transplant. Each: KPI cards with evidence flags; cohort-coverage rows declaring blind spots (Absent/Partial/Evidenced).

### 4. The 360 loop + Marie journey
11 stages, 3 bands: Signal (1-3) / Return path (4-8, THE innovation) / Hold-the-line (9-11). Stage 10 = flatline alarm (heartbeat-flatline motif, operational). Marie journey: full 11-stage walkthrough of a composite BSL-first Deaf patient whose consent was mis-recorded refused. Evidence boundary at stage 3 (FACTUAL ends, MODELLED begins). Flatline branch at stage 10.

### 5. Vision layer (three horizons overlay)
H1 Evolution (you-are-here) / H2 Reform / H3 Revolution. Built = green live islands; vision = purple, marked not yet built. Sovereignty stack + sequencing roadmap, honestly placing programme early in Phase 1.

### 6. EA portal + navigable KIL / data lineage
7-layer architecture board: presentation / application / KIL semantic / data&integration / storage / infrastructure / security. Navigable KIL: click entity, see relationships. Lineage path: Dataset > measured_by > KPI > affects > PopulationSegment > acts_on > Action > verified_by > Outcome. Lineage MODELLED (designed path), marked NOT a live trace until Supabase provisioned.

## Evidence discipline (non-negotiable)
FACTUAL (green): Black patients wait ~2.5x longer for kidney (30mo vs 12mo, NHSBT); 11/15 equity groups absent/critical; 0/4 nations interoperable API; ~1 in 6 UK deaths inactivity-linked (Sport England); +26% loneliness mortality (Holt-Lunstad 2015); 35%/15% deprivation gradient (OHID); MBRRACE-UK 2023 ethnic disparities. MODELLED (amber): 23:1 ROI (~11.5:1 half benefit); ~120M GBP/yr preventable harm. ILLUSTRATIVE (pink): Health Equity Score 62-90 (unvalidated); composite personas. PARTIAL (blue): 871k global loneliness deaths (WHO modelled); same-6-extensions-apply-to-births. 6 DEIA extensions: ethnicityCoverage, deprivationLinkage, deiaImpactFlag, vulnerabilityMarker, panUKScope, healthEquityScore. NEVER claim live data; provenance banner: real sourced figures, baked in, not yet live-wired. Community with/by/for claims CONTINGENT until ART004 done AND engagement happened.

## KIL data model (canonical)
Entities: Dataset/DataService (hub), KPI, PopulationSegment (equity lens), IntersectionNode, Action, DeploymentEvent, OutcomeEvent, Organisation, Jurisdiction, Policy, Risk, BarometerScore, Evidence, Persona. Edges: measured_by, affects, owned_by, governed_by, located_in, scored_by, exposes (derived - render dashed), acts_on, verified_by. Equity Risk Score: ERS = sum(factor x weight), 0-100. Weights: Gap Magnitude 25, Population 20, Trend 15, Vulnerability 15, Modifiability 15, Strategic 10. Bands: Critical 80-100 / High 60-79 / Medium 40-59 / Low 20-39 / Very Low 0-19.

## Build method (avoids two prior crashes)
1. Scaffold HTML shell + CSS design tokens (GDS Internal) first; validate. 2. Append each surface as its own section; validate syntax between each. 3. All JS in-file, no external deps, no localStorage. 4. Commit to feature/v6-portal; keep main clean. 5. Final file to outputs, presented for download/host.

## Reconciliation inputs (read before building)
NDL_Transplant_Data_Product_Spec.xlsx (real data dictionary + ROI model, supersedes seed). 16 Designer visuals (clean). Visual 13 = KIL ERD (richer than canonical, wins where richer). Visual 14 = Equity Risk Score. Confluence governed record (gds-ogcdo Architecture): 360 loop 44171265; v6 Build Handoff 44138499; ART004 44171291.

## Definition of done
- Lands on the Film, not a dashboard.
- All six surfaces present and navigable.
- GDS Internal skin, visibly distinct from v3.
- Every figure flagged + sourced; provenance banner present.
- Marie journey complete with evidence boundary + flatline branch.
- KIL navigable; lineage marked MODELLED.
- Single self-contained file, opens in browser, hostable.
- A reviewer comparing v3 and v6 says this is a different class of thing, not v3 with extras.
