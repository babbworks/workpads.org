---
layout: post
title: "Built for Feature Phones"
date: 2026-04-27 10:00:00 -0500
categories: [technical, ecosystem]
---

KaiOS runs on feature phones selling for under $25. The global installed base is in the hundreds of millions. It is the dominant computing platform in several African markets and across South Asia.

Workpads launched first on KaiOS. This was not a pragmatic choice. It was a design constraint.

## Why KaiOS first

Building for the most constrained platform first forces decisions that remain correct as you move to richer environments. The KaiOS Workpads app must:

- Navigate entirely via D-pad (ArrowUp, ArrowDown, ArrowLeft, ArrowRight, Enter)
- Fit within tight memory limits
- Produce URLs short enough for SMS
- Work without assuming background sync or push notifications

Every one of these constraints is a good constraint for any commercial record format. D-pad navigation produces a clear information hierarchy. Memory limits prevent scope creep. SMS-length URLs enforce encoding discipline. No background sync means records must be self-contained.

The [Two-Build Strategy (§7)](/standard) describes how a single codebase produces both the KaiOS 3.x build and the modern web build. The split is at the platform adapter layer — the record logic, codec, and storage contract are shared. Only the navigation model and rendering layer diverge.

## The codec constraint

The KaiOS use case gave us the codec's core constraint: a complete business record must encode to under 300 characters to be reliably SMS-transmissible. The [§5 codec](/standard) achieves this through:

- **Bitfield packing** for status and flags
- **Sparse encoding** — absent optional fields are not written
- **Base64url output** — URL-safe, no percent-encoding overhead
- **No schema envelope** — the codec is versioned at the URL prefix, not embedded in the payload

The result: a complete svc-basic record with all optional fields populated encodes to approximately 180-220 characters. With only required fields, it's under 80.

## The panel navigation model

KaiOS apps navigate using softkeys and D-pad. The [panel access model (§ panel-access-model.md)](/standard) defines how ArrowLeft and ArrowRight navigate between record panels, and how the softkey bar maps to record actions (Save, Share, New).

This model transfers cleanly to touch and mouse: swipe or click to move between panels, with the softkey actions becoming persistent footer buttons. The same mental model works across both platforms.

---

The KaiOS app is available on the [KaiOS Store](https://www.kaiostech.com/store/apps/?bundle_id=com.babbworks.workpads) and as a [demo at workpads.app](https://workpads.app).
