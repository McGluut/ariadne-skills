---
name: karteren
description: "Use when the user asks to karteer/map material, zoom on any part, build a shareable evidence map, or designate mapping as an Ariadne skill-adres; keep provenance, privacy, decision relevance and verification explicit."
---

# Ariadne · Karteren (skill-adres) v0.1

## Invocation and aim

The entry address is **`karteren`**. It turns accessible material into a navigable, zoomable evidence map, preserving the distinction between the user's purpose, source claims, interpretation, action and validation. It is a **skill**, not a new MCP tool, search index, hosting service or permission to read absent/private files.

Use for: "karteer dit", "zoom waar ik wil", "maak een kaart voor reviewer X", "karteren als adres", and follow-up requests to inspect a node. Default to Dutch if the user speaks Dutch.

## Adres / operator contract

**Input**: purpose and target decision; source handles and what is actually available; audience and authorization; optional start focus; desired output/host; optional measure family. Never fabricate inaccessible corpus content.

**Transform**: `source → inventory → typed nodes/edges → layered map → inspectable zoom → action/change measure → verification → share gate`.

**Output**: a useful map or export plus a structured manifest, with explicit source boundaries and a reviewer-ready inspection path. If interactive publishing is unavailable, deliver a self-contained artifact with the distinction **artifact ≠ live website** and **skill ≠ tool**.

**Validation**: every factual node can be traced to the exact source location; uncertain edges stay marked provisional; another reading is kept if it changes the next action; share package contains only authorized material.

**Reopen**: when a new source, correction, source inconsistency, changed audience, or action-relevant counterexample appears. Do not reopen merely because more abstraction is possible.

## Workflow

1. **Receive/lock purpose.** Restate what the user wants to learn or decide; do not replace it with comprehensive taxonomy or a benchmark. Identify audience separately from owner and source.
2. **Inventory source coverage.** Inspect the supplied files/accessible repositories/URLs, counting only what is demonstrably present. Classify direct quotes, summaries, data, linked-but-unread files, missing branches, tool outputs, and inaccessible attachments. Label actual source timestamps and relevant selection windows.
3. **Pick regions and zoom levels.** Choose 2–6 major regions (L0). Within each, add L1 concept/claim nodes; L2 context/evidence locations; L3 verbatim source and independent execution proof if authorized and available. If L3 is absent, show a boundary instead of generating a plausible story.
4. **Type each relation.** Minimum classes: `contains`, `derives_from`, `supports`, `contradicts`, `depends_on`, `excludes`, `proposes`, `validated_by`. Use directional arrows and a confidence/verification marker for hypotheses.
5. **Measure action relevance.** For disputed interpretations, ask whether each alternative changes route, action, validation, storage, measure, lock, abstain or reopen. Keep decision-relevant alternatives; mark `NO-TAKE` when no delta follows. Don't turn all links into confident causal claims.
6. **Protect validation.** Preserve original request, historical answer, later correction, independent evidence and reviewer reference in separate layers; a previous answer cannot grade itself. Avoid mixing development and blind test cases or creating leakage across branches of one event.
7. **Render and inspect.** Provide a compact readable overview, selectable nodes, pan/zoom, search, simple controls, keyboard + touch support, status indications and accessible text view. A static site may run offline. Do not claim a deployment until a host returns a working URL.
8. **Sharing gate.** Separate owner-only full map from a shareable review projection. Remove raw conversations, credentials, personal data, sensitive attachments, index dumps and hidden local links unless sharing is explicitly authorized and technically access-controlled. Prevent embedded outbound analytics. Make clear what the reviewer can and cannot inspect.
9. **Validate + hand off.** Confirm representative node → exact source, negative source case, counter-reading that changes action, touch/desktop behavior if rendered, privacy boundary, and review export if provided. Name what remains unvalidated, the next action and reopening condition.

## Output contract

Generate a structured manifest per [map-spec](references/map-spec.md). For the user's request, give (a) navigation-ready map, (b) visible provenance and access limits, (c) optional shareable inspection surface and reviewer notes, and (d) a small validation ledger. Avoid lists of every extract when that would defeat usability.

### Minimal invocation examples

- `Karteer deze projectnotitie. Welke uitspraken hebben een aanwijsbare bron en waar ontbreekt bewijs?`
- `Zoom in op de voorgestelde meting en laat zien welke uitkomst ons besluit zou veranderen.`
- `Maak een deelbare kaart voor de reviewer met alleen de documenten die deze mag inzien.`

## Worked example

[Projectnotitie over een energiemeting](references/example-projectbrief.md) contains the complete fictional source. It illustrates how a proposal, a missing attachment and a decision can appear together on one map.
