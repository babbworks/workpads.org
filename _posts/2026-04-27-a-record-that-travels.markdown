---
layout: post
title: "A Record That Travels"
date: 2026-04-27 09:00:00 -0500
categories: [standard, technical]
---

Most record formats are built for storage. A workpad record is built for travel.

The distinction matters. When a format is built for storage, it assumes a server will receive it, a database will hold it, and a client will retrieve it on demand. Connectivity is a given. The record is a description of state that lives somewhere else.

A workpad record assumes none of that. The record *is* the transmission. It encodes a complete business transaction — service description, parties, status, financial terms — into a URL hash fragment small enough to fit in an SMS message. When the URL travels, the record travels with it.

## Why this matters for emerging markets

In much of the world, reliable internet connectivity is intermittent or expensive. A feature phone with a data plan may get SMS reliably but not HTTP. A QR code scanned at a market stall doesn't require a working server at the other end.

The Workpads codec (§5) is designed with these constraints in mind:

- **Binary packing** over text serialization — no JSON, no XML bloat
- **Sparse field encoding** — absent fields cost nothing
- **URL-safe output** — the hash fragment survives copy-paste across SMS, WhatsApp, and QR codes
- **No server round-trip** required to decode

A record generated on a KaiOS phone in Lagos can be decoded on a web browser in Louisville without either party having an account, a server, or an internet connection at the moment of transfer.

## The atomic record

The atomic unit of the format is the **workpad record**: a single document capturing one piece of work. By design, it is:

- **Complete** — enough information to understand the transaction without external lookup
- **Compact** — small enough to travel as a URL fragment over any channel
- **Honest** — the record's status field (open, active, complete) reflects its actual state
- **Sovereign** — it belongs to its creator, not to a platform

These four properties, defined in [§1 — PADS Data Model](/standard), are not aspirational. They are enforced by the encoding: a workpad URL that omits the service description is malformed. A workpad URL that requires a server lookup to decode violates the sovereign property.

## Building on the standard

The record format is open. The [Workpads Standard v0.1](/standard) defines what a workpad record is and how it is encoded. What you build with that is yours.

[Read the Standard →](/standard)
