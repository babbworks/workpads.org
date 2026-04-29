---
layout: page
title: Ecosystem
eyebrow: Reference Products
subtitle: The Workpads Standard is supported by a set of reference products maintained by Babb. These are the canonical implementations — not the only valid ones.
wide: true
permalink: /ecosystem
---

## Reference Implementations

<div class="eco-table" markdown="1">

| Repo | Role | Status |
|------|------|--------|
| `workpads-standard` | Normative specification (this site) | <span class="eco-status live">v0.1 live</span> |
| `workpads-codec` | `@workpads/codec` npm package — implements §5 | <span class="eco-status live">v0.1</span> |
| `workpads-cli` | CLI reference implementation — implements §4 surface, used for integration testing | <span class="eco-status active">v0.x</span> |
| `workpadsdev-cli` | Developer toolchain — build, packaging, softkey validation, conformance checks | <span class="eco-status live">v0.1</span> |
| `workpadskaios` | KaiOS 3.x reference app — full implementation, D-pad navigation | <span class="eco-status live">v0.1</span> |
| `workpadsdotme` | Web reference app (`workpads.me`) — three-column layout, mouse + keyboard | <span class="eco-status active">active</span> |
| `workpads-basicsconform` | Research control plane — quiz rounds, decision log, deviation registry | <span class="eco-status internal">internal</span> |
| `workpads` | Original architecture documents (pre-2026). Historical reference. | <span class="eco-status archived">archived</span> |

</div>

---

## Products

| Site | Purpose |
|------|---------|
| [workpads.org](https://workpads.org) | Main project site — app overview, onboarding, KaiOS launch |
| [workpads.app](https://workpads.app) | Web app |
| [workpads.me](https://workpads.me) | Web reference app (three-column layout) |
| [standard.workpads.org](https://standard.workpads.org) | This site — normative standard documentation |

---

## How the Ecosystem Connects

The codec (`workpads-codec`) is the shared library. Both `workpadskaios` and `workpadsdotme` depend on it for §5 encoding and decoding. The CLI uses the same codec for integration testing.

`workpads-standard` (this repository) is the authority. When any implementation conflicts with the standard, the standard governs. Implementations document deviations rather than silently diverging.

See [ECOSYSTEM.md](https://github.com/babbworks/workpads-standard/blob/master/ECOSYSTEM.md) in the standard repo for a detailed description of each repo's role and interconnections.

---

## Build Your Own

The standard is open. Independent implementations — experimental apps, open-source tools, proprietary products — are welcome. The standard defines what a workpad record is and how it is encoded. What you build with that is yours.

[Read the contribution guide →](/contribute)
