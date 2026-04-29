---
layout: page
title: The Standard
eyebrow: Workpads Standard v0.1
subtitle: Eight numbered sections form the normative core. Each is versioned independently. When implementation and standard conflict, the standard governs.
wide: true
permalink: /standard
---

## Normative Sections

<div class="standard-toc">

  <div class="toc-section">
    <div class="toc-num">01</div>
    <div class="toc-body">
      <div class="toc-title"><a href="https://github.com/babbworks/workpads-standard/blob/master/pads-model.md">PADS Data Model</a></div>
      <div class="toc-desc">The structure of a workpad record — the atomic unit of the format. Defines field names, types, cardinality, and the three-record vocabulary (open, active, complete).</div>
      <div class="toc-meta">pads-model.md &middot; v1 &middot; 2026-04-27</div>
    </div>
  </div>

  <div class="toc-section">
    <div class="toc-num">02</div>
    <div class="toc-body">
      <div class="toc-title"><a href="https://github.com/babbworks/workpads-standard/blob/master/record-schema.md">Record Schema (svc-basic)</a></div>
      <div class="toc-desc">Canonical field definitions for the baseline service record type. The minimum viable record: worker, client, service, status, and optional financial fields.</div>
      <div class="toc-meta">record-schema.md &middot; v1 &middot; 2026-04-27</div>
    </div>
  </div>

  <div class="toc-section">
    <div class="toc-num">03</div>
    <div class="toc-body">
      <div class="toc-title"><a href="https://github.com/babbworks/workpads-standard/blob/master/naming-convention.md">Naming Convention</a></div>
      <div class="toc-desc">How records, fields, record types, and implementations are named. Establishes the slug vocabulary and the URL scheme prefix convention.</div>
      <div class="toc-meta">naming-convention.md &middot; v1 &middot; 2026-04-26</div>
    </div>
  </div>

  <div class="toc-section">
    <div class="toc-num">04</div>
    <div class="toc-body">
      <div class="toc-title"><a href="https://github.com/babbworks/workpads-standard/blob/master/record-service.md">RecordService Interface</a></div>
      <div class="toc-desc">The programmatic surface for creating, reading, updating, and persisting workpad records. Defines the contract that implementations must satisfy.</div>
      <div class="toc-meta">record-service.md &middot; v1 &middot; 2026-04-27</div>
    </div>
  </div>

  <div class="toc-section">
    <div class="toc-num">05</div>
    <div class="toc-body">
      <div class="toc-title"><a href="https://github.com/babbworks/workpads-standard/blob/master/codec.md">Codec &amp; Compact Encoding</a></div>
      <div class="toc-desc">The binary encoding that produces a URL-safe hash fragment small enough to travel over SMS. This is the interoperability core: any conformant encoder and decoder must be compatible.</div>
      <div class="toc-meta">codec.md &middot; v1.1 &middot; 2026-04-28</div>
    </div>
  </div>

  <div class="toc-section">
    <div class="toc-num">06</div>
    <div class="toc-body">
      <div class="toc-title"><a href="https://github.com/babbworks/workpads-standard/blob/master/storage-adapter.md">Storage Adapter Contract</a></div>
      <div class="toc-desc">The interface between record logic and platform-specific storage. Allows the same business logic to run over IndexedDB, file storage, or in-memory backends.</div>
      <div class="toc-meta">storage-adapter.md &middot; v1 &middot; 2026-04-27</div>
    </div>
  </div>

  <div class="toc-section">
    <div class="toc-num">07</div>
    <div class="toc-body">
      <div class="toc-title"><a href="https://github.com/babbworks/workpads-standard/blob/master/build-strategy.md">Two-Build Strategy</a></div>
      <div class="toc-desc">How a single codebase produces both a KaiOS 3.x build (D-pad, feature phone) and a modern web build. Defines the build targets and the split points in the code.</div>
      <div class="toc-meta">build-strategy.md &middot; v1 &middot; 2026-04-27</div>
    </div>
  </div>

  <div class="toc-section">
    <div class="toc-num">08</div>
    <div class="toc-body">
      <div class="toc-title"><a href="https://github.com/babbworks/workpads-standard/blob/master/basics-conformance.md">BASICS Conformance Mapping</a></div>
      <div class="toc-desc">The explicit mapping from Workpads Standard v0.1 to the BASICS Core tier. Enables formal interoperability claims and deviation registration.</div>
      <div class="toc-meta">basics-conformance.md &middot; v1 &middot; 2026-04-27</div>
    </div>
  </div>

</div>

---

## Extended Specifications

These documents are part of the standard and cover features in active implementation or scheduled for v0.2.

| Document | Scope |
|----------|-------|
| [record-philosophy.md](https://github.com/babbworks/workpads-standard/blob/master/record-philosophy.md) | The five properties of a workpad record — foundational rationale for all design decisions |
| [activity-profile.md](https://github.com/babbworks/workpads-standard/blob/master/activity-profile.md) | Activity Profile and Block Registry — sender identity, contact store, location store |
| [chain-protocol.md](https://github.com/babbworks/workpads-standard/blob/master/chain-protocol.md) | Record chain protocol — linked records, ACK mechanism, multi-worker pre-seeding (v0.2) |
| [participants-block.md](https://github.com/babbworks/workpads-standard/blob/master/participants-block.md) | Participants block — typed party list replacing simple worker text field (v0.2) |
| [financial-block.md](https://github.com/babbworks/workpads-standard/blob/master/financial-block.md) | Financial block — amounts, currency, tax, qty×rate, compound invoicing (v0.2) |
| [transaction-classification.md](https://github.com/babbworks/workpads-standard/blob/master/transaction-classification.md) | I>O notation for income/expense direction, time, and settlement state |
| [personal-platform.md](https://github.com/babbworks/workpads-standard/blob/master/personal-platform.md) | Two-engine architecture: Exchange Engine + Learning Engine |
| [panel-access-model.md](https://github.com/babbworks/workpads-standard/blob/master/panel-access-model.md) | Panel navigation model (ArrowLeft/ArrowRight) for platform input adaptation |

---

## Maintenance Documents

| Document | Purpose |
|----------|---------|
| [ECOSYSTEM.md](https://github.com/babbworks/workpads-standard/blob/master/ECOSYSTEM.md) | Map of all repos, tools, and how they connect |
| [implementation-notes.md](https://github.com/babbworks/workpads-standard/blob/master/implementation-notes.md) | Pre-publication scan: deviations and innovations found in v0.1 implementations |
| [codec-sync.md](https://github.com/babbworks/workpads-standard/blob/master/codec-sync.md) | Protocol for keeping codec implementations in sync across products |

---

## Versioning {#roadmap}

Section versions use `v1`, `v2`, etc. A section version increments on **breaking changes** only (field removed, encoding slot reassigned). Additive changes do not increment existing section versions.

### v0.2 Roadmap

The following are settled in design and documented in extended specs, pending implementation:

- Financial block in codec (§`financial-block.md`)
- Chain protocol (§`chain-protocol.md`)
- Participants block (§`participants-block.md`)
- KaiOS 2.5 build target (§`build-strategy.md`)
- URL scheme tag alignment across all implementations
- Block Registry v0.2 schema with typed customers and locations
