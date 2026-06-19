---
layout: page
title: How It Works
eyebrow: The Lifecycle
subtitle: A record that travels without a server. Here's the full path.
permalink: /how-it-works
---

<div class="step-block">
  <div class="step-num">01</div>
  <div class="step-body">
    <h3>You create a record</h3>
    <p>Open the app. Fill in the details — who, what, how much. A service record. An invoice. A job note. Whatever your work needs.</p>
  </div>
</div>

<div class="step-block">
  <div class="step-num">02</div>
  <div class="step-body">
    <h3>It encodes into a URL</h3>
    <p>The entire record compresses into a compact binary string. That string becomes the fragment of a URL. The data IS the link. Nothing is stored anywhere else.</p>
  </div>
</div>

<div class="step-block">
  <div class="step-num">03</div>
  <div class="step-body">
    <h3>You send it</h3>
    <p>SMS. WhatsApp. Telegram. Email. QR code printed on paper. Any channel that can carry a URL can carry your record. No app install required to receive.</p>
  </div>
</div>

<div class="step-block">
  <div class="step-num">04</div>
  <div class="step-body">
    <h3>The other person opens it</h3>
    <p>They click the link. The app decodes the URL fragment. The record appears. No server was contacted. No database was queried. The data travelled peer-to-peer, inside the message itself.</p>
  </div>
</div>

<div class="step-block">
  <div class="step-num">05</div>
  <div class="step-body">
    <h3>Both parties have the record</h3>
    <p>Stored locally on each device. Offline-first. Works on feature phones. Works without WiFi. Works without a cloud account. Works without permission from anyone.</p>
  </div>
</div>

---

## What this means

> The record IS the message. There is no copy on a server. There is no sync service. There is no company in the middle.

**No account** — you don't register. You just use it.

**No server** — the URL carries the data. Opening the link decodes it locally.

**No breach** — there's nothing to hack. The data only exists on the devices of the people involved.

**No lock-in** — the format is an open standard. Anyone can build a compatible app.

---

## Technical detail

The encoding uses a compact binary codec (§5 of the standard). A full service record — worker, client, service type, status, financial fields — fits in under 2KB of URL fragment. Small enough for SMS. Small enough for a QR code.

The codec is deterministic: the same record always produces the same URL. Different conformant encoders produce identical output. Different conformant decoders read it identically.

<p class="structural" style="margin-top:2rem;">
  <a href="/standard">Read the full standard →</a>
</p>
