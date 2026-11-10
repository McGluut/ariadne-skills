# Karteren map specification v0.1

The manifest expresses what has been learned **and** what is not known. Consumers may represent it in HTML/JSON/SVG or prose. This is a data contract, not a promise of an implemented software API.

```json
{
  "schema": "ariadne.karteren.v0.1",
  "map_id": "string",
  "purpose": "concrete user purpose or decision",
  "audience": "owner | reviewer | public",
  "source_inventory": [{"id":"s1","locator":"source pointer","available":true,"scope":"summary","timestamp":null}],
  "excluded_or_missing": ["raw documents not supplied"],
  "regions": [{"id":"r1","name":"source"}],
  "nodes": [{"id":"n1","region_id":"r1","level":"L1","kind":"observation | interpretation | question | action | boundary | validation","statement":"...","source_refs":["s1#L18"],"verification":"direct | derived | proposed | missing","visibility":"owner | reviewer | public"}],
  "edges": [{"from":"n1","to":"n2","relation":"supports","verification":"direct | derived | proposed"}],
  "action_measure": [{"node_id":"n1","alternative":"...","delta":"route | action | validation | storage | measure | lock | abstain | reopen | NO-TAKE","test":"..."}],
  "validation": {"source_trace_checked":false,"counter_reading_checked":false,"privacy_checked":false,"mobile_checked":false},
  "reopen_when": ["new sources materially change the map"]
}
```

Rules:
- L0: broad region; L1: claim/concept; L2: evidence/context; L3: exact primary source, when available.
- A node without an exact source must say `proposed` or `missing`, never `direct`.
- Negative hits in an incomplete index mean **not found in indexed scope**, not absent globally.
- Source quotation, source interpretation, external verification, execution proof and review reference must remain distinct.
- Sharing cannot expose `owner` nodes to reviewer/public. Regenerate review-specific manifests from an allowlist. Do not merely hide restricted nodes in CSS.
- Map coverage is measured against the declared input, not against an imaginary complete corpus.
- Zoom is meaningful only when it reveals deeper evidence or a relevant decision distinction; visual magnification alone is not epistemic zoom.
