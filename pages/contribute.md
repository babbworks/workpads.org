---
layout: page
title: Contribute
eyebrow: Open Standard
subtitle: The Workpads Standard grows through real implementation experience. Here is how to participate.
permalink: /contribute
---

<div class="contribute-note">
  The standard is open. You may implement it, extend it, and build proprietary or open-source products on it without permission from Babb.
</div>

## Conformance and Use {#conformance}

### Using the Standard

If your product **generates** workpad URLs (`workpads.me/p#1ag/...`): encode according to §5 so any conformant decoder can read the record.

If your product **decodes** workpad URLs: implement §5 faithfully so records from any conformant encoder are readable.

If your product **extends** the format: use the reserved field slots and template bytes in §5, or register a deviation via BASICS.

### BASICS Conformance

The Workpads Standard conforms to BASICS v0.1.1 at the Core tier. BASICS provides a meta-framework for interoperability claims, deviation registration, and compatibility policy.

If you want a formal conformance claim for your product:

1. Read [§8 — BASICS Conformance Mapping](https://github.com/babbworks/workpads-standard/blob/master/basics-conformance.md)
2. Create a `deviation-registry.md` in your repo following the BASICS pattern
3. Reference `workpads-basicsconform/` as a model for the BASICS evidence artifact format

Formal BASICS conformance is **not required** to implement Workpads. It is a signal to other implementors that your product has a documented interoperability posture.

---

## Ways to Contribute

### Report Implementation Deviations

If you are building on the standard and find that something in the spec doesn't match what works in practice, that is valuable signal. Open a discussion on [GitHub](https://github.com/babbworks/Workpads/discussions) describing:

- Which section(s) are affected
- What your implementation does differently
- Why (constraint, error, or deliberate extension)

Deviations found in practice feed the next version of the standard.

### Extend via Registered Deviations

The preferred path for extensions is a registered deviation in your own repo, not a fork of the standard. This keeps the interoperability surface clean while allowing you to innovate.

### Review and Comment

All normative sections are maintained in [workpads-standard](https://github.com/babbworks/workpads-standard). Open issues or pull requests for:

- Ambiguities in the spec text
- Missing edge cases
- Encoding conflicts discovered in implementation

### Build Reference Implementations

The ecosystem benefits from implementations on additional platforms. If you build a conformant implementation for a platform not currently covered, publish your BASICS conformance claim and link to it from the GitHub Discussions.

---

## Contact

- **Email:** [workpads@babb.tel](mailto:workpads@babb.tel)
- **GitHub Discussions:** [github.com/babbworks/Workpads/discussions](https://github.com/babbworks/Workpads/discussions)
- **Projects:** [github.com/babbworks/Workpads/projects](https://github.com/babbworks/Workpads/projects?query=is%3Aopen)
