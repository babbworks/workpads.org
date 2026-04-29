---
layout: post
title: "An Open Door, Not a Protected Territory"
date: 2026-04-28 09:00:00 -0500
categories: [community, standard]
---

Babb created the Workpads Standard to grow a format that serves workers. Not to own a market.

This distinction matters in how the standard is structured, what it asks of implementors, and what it does not ask.

## What the standard asks

If your product generates workpad URLs — the `workpads.me/p#...` format — encode according to §5 so that any conformant decoder can read the record. If your product decodes workpad URLs, implement §5 faithfully so that records from any conformant encoder are readable.

That's the full obligation. **Interoperability is the standard's core value, not exclusivity.**

## What the standard does not ask

The standard does not ask:
- For a license fee or royalty
- For permission before building
- For proprietary products to open-source their code
- For extensions to be submitted back to the standard

You may build a commercial product on Workpads and keep that product entirely proprietary. You may extend the format for your use case using the reserved field slots in §5 without registering anything. The standard does not police what you build on top of it.

## BASICS as a signal, not a gate

The Workpads Standard conforms to BASICS v0.1.1 at the Core tier. BASICS provides a meta-framework for interoperability claims and deviation registration.

Formal BASICS conformance for your product is **not required** to implement Workpads. It is a signal — to other implementors, to your users, to the ecosystem — that your product has a documented interoperability posture. It says: here is what we implement, here is what we deviate from, here is why.

If your product generates workpad URLs and you want that signal, [read §8 and create a deviation registry](/standard). If you don't need the signal, build and ship.

## How the ecosystem grows

The standard grows through real implementation experience. We learn more from a conformant product built by an independent team than from months of internal spec work.

If you find that something in the spec doesn't match what works in practice, that is valuable. Open a [GitHub Discussion](https://github.com/babbworks/Workpads/discussions). Describe what you're building, what the spec says, and what you found. Deviations documented in practice feed the next version.

The goal is a format that is actually interoperable in the wild — not one that is theoretically interoperable on paper. Every independent implementation makes that goal more achievable.

[How to Contribute →](/contribute)
