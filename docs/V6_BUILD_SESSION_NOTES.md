# v6 Build Session - Notes & Connector Reality

Read alongside docs/V6_OBSERVATORY_BAROMETER_SPEC.md (the canonical spec).
This file captures hard-won setup facts so the next session loses no time.

## THE ONE BLOCKER (why no portal exists yet)
The sessions so far were Zapier-only and had NO file-creation tool. That is the
entire reason the portal was never built - not a design problem, a tooling one.
The next build session MUST have the Analysis tool / code execution enabled,
OR use Claude Code directly on this repo. With that on, the build is one pass.

## OPENING MOVE for the build session
"Read docs/V6_OBSERVATORY_BAROMETER_SPEC.md in emanukgb-dsit/Innovation-Lab and
build data_sharing_observatory_v6.html to it - chunked, validated section by section,
GDS Internal skin. Read the existing data_sharing_observatory_v3.html first and exceed it.
NO film, NO narrative spine - it is a DEIA-enabled Observatory & Barometer."

## CONNECTOR REALITY (Zapier)
- GitHub is authed as **emanukgb-dsit** (NOT cyberdudeuk).
  Writable repos: agent-skills, Innovation-Lab, Internal-Sandbox.
  cyberdudeuk/ndl-pubsec-mcp is public but NOT writable via this connection.
- This repo (Innovation-Lab) GitHub connector has NO file-READ action - cannot fetch a
  file SHA, so cannot cleanly UPDATE an existing file. Workaround used: write NEW filenames.
  (That is why the canonical spec is V6_OBSERVATORY_BAROMETER_SPEC.md, superseding
  the earlier V6_PORTAL_BUILD_SPEC.md which wrongly framed it as a film.)
- Linear team: Cyberdudeuk (id 4567e58f-5dbd-4f72-b1c9-ef659f0f23d2).
- Slack / Notion / Figma: enabled but NOT yet authorised.
- One Zapier skill saved: "feature intake" (creates a Linear issue + GitHub branch, cross-linked).

## UPLOADS - WILL BE LOST IF THE CHAT IS DELETED
These lived only in the chat, not in any repo. Save locally and re-upload to the build session:
- NDL_Transplant_Data_Product_Spec.xlsx - NEVER read (no spreadsheet tool this session).
  Likely real data dictionary + ROI model; supersedes the hand-built seed. PRIORITY read.
- 16 Designer vision visuals (clean, no OCR corruption). Visual 13 = KIL ERD (richer than
  canonical - wins where richer). Visual 14 = Equity Risk Score model.
- SSOT PDF; DEIA-INITIATION-PACK.md; Swarm Charter; DEIA_Community_Engagement.pdf (ART004 briefing).

## GOVERNED RECORD (Confluence gds-ogcdo Architecture - survives chat deletion)
44171265 360 loop + KIL (canonical) | 44138499 v6 Build Handoff | 44171291 ART004 |
44531735 intermediary outreach | 44204057 ToC | 44367875 UR scaffold |
44335107 authority boundary | 44531713 vision-led portal milestone |
44302338 Captain's Log | 44302359 Dev Log. (Note: cross-check page IDs in-product;
 some supplements were created in-session.)

## STANDING DISCIPLINES
No fabrication - flag every figure FACTUAL/MODELLED/ILLUSTRATIVE/PARTIAL + source.
System failure not group deficiency. Declare blind spots. Lineage/scores MODELLED until
Supabase provisioned. NO live-data claims. Quantum stays with Office for Quantum.
Chunked builds, validate between sections, never one monolithic write (crashed twice on ~4000 lines).
