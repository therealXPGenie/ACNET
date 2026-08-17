# ACNET Acknowledgements and Third-Party Notices

ACNET (Audio Communication Network) is licensed under the **GNU General Public
License v3.0** in its current GitHub repository. Third-party components retain
their own licenses; ACNET's GPL license does not replace their notices.

## A note of thanks

### Georgi Gerganov — ggwave
ACNET sincerely thanks **Georgi Gerganov** for creating and openly sharing
**ggwave**. Its compact data-over-sound engine provides an important acoustic
communications foundation for ACNET and demonstrates how capable audio modem
technology can remain portable and approachable.

### Mike Lubinets — Reed-Solomon code used by ggwave
Thank you to **Mike Lubinets (mersinvald)** for the Reed-Solomon implementation
included in ggwave. Error correction is essential to useful acoustic links in
real conditions, and ACNET appreciates this open contribution.

### Takuya Ooura — FFT routines used by ggwave
Thank you to **Takuya Ooura** for the FFT routines incorporated by ggwave.
This long-standing signal-processing work has supported many technical
projects, and ACNET is grateful that it was published for broad reuse.

### Vitaly Puzrin, Andrei Tuputcyn, and Nodeca — pako
ACNET thanks **Vitaly Puzrin**, **Andrei Tuputcyn**, and the **Nodeca/pako**
contributors for providing a dependable browser-friendly DEFLATE/zlib
implementation. pako makes mature compression practical inside a portable,
single-file browser application.

### Jean-loup Gailly and Mark Adler — zlib
ACNET gratefully acknowledges **Jean-loup Gailly** and **Mark Adler** for
**zlib**, a foundational contribution to modern computing. pako—and therefore
parts of ACNET's compression path—benefit from that work.

### David E. Weekly and the Cyrinx contributors
ACNET thanks **David E. Weekly (dweekly)** and the **Cyrinx** contributors for
publishing the project and documenting its acoustic bulk-PHY architecture.
Cyrinx provided valuable technical reference material for ACNET's independently
implemented CYRINX browser profile, and ACNET appreciates that open engineering
work.

### Emscripten authors and contributors
Thank you to the **Emscripten** authors and contributors for making compiled
C/C++ and WebAssembly software practical in browsers. The ggwave browser build
used by ACNET benefits from that ecosystem.

### Matt McInerney and Orbitron contributors
Thank you to **Matt McInerney**, the original designer of **Orbitron**, and the
contributors who have maintained and expanded it. Orbitron's geometric,
futuristic character helps give ACNET its communications-console appearance.
The formal license notice remains **Copyright 2018 The Orbitron Project
Authors**.

### Ralph du Carrois and Carrois Type Design — Share Tech Mono
Thank you to **Ralph du Carrois** and **Carrois Type Design** for **Share Tech
Mono**. Its clear monospaced design is particularly well suited to packet logs,
telemetry, diagnostics, and technical interfaces.

### Google Fonts
ACNET also thanks the **Google Fonts** team and the wider open-font community
for making openly licensed typography easy to discover and use across browsers
and platforms.

---

## Bundled software and notices

### ggwave
- Upstream: https://github.com/ggerganov/ggwave
- Copyright: Copyright (c) 2020 Georgi Gerganov
- License: MIT
- Notice: `THIRD_PARTY_LICENSES/ggwave-MIT.txt`

The upstream ggwave source also identifies:
- Ooura FFT routines — Copyright Takuya OOURA, 1996-2001
- Reed-Solomon implementation — Copyright © 2015 Mike Lubinets
- browser/WASM build tooling from Emscripten

Corresponding notices are included under `THIRD_PARTY_LICENSES/`.

ACNET's chunking, ACK/NAK, retry logic, callsign handling, UI, relay behavior,
crypto wrappers, and surrounding transport integration are ACNET additions and
should not be represented as upstream ggwave work.

### pako
- Upstream: https://github.com/nodeca/pako
- Copyright: Copyright (C) 2014-2017 by Vitaly Puzrin and Andrei Tuputcyn
- License: MIT; pako's `/src/zlib` content is under the zlib License
- Notices: `pako-MIT.txt` and `zlib-License.txt`

## Cyrinx acknowledgement

- Upstream: https://github.com/dweekly/cyrinx
- Upstream license: Apache License 2.0
- License copy: `THIRD_PARTY_LICENSES/Cyrinx-Apache-2.0.txt`

ACNET's own source describes the CYRINX browser modem as a **clean-room
JavaScript implementation** whose architecture follows documented Cyrinx
bulk-PHY building blocks, and states that it is not bit-for-bit wire compatible
with upstream `cyrinx_bulk`. This acknowledgement therefore credits the
technical reference without claiming that upstream Cyrinx C source is bundled.

The upstream repository contains a `NOTICE` file. See
`Cyrinx-UPSTREAM-NOTICE-REFERENCE.txt`. If future ACNET releases incorporate
copyrightable Cyrinx source, preserve the exact applicable upstream NOTICE from
the version used and comply with Apache-2.0 redistribution requirements.

## Fonts

ACNET currently loads these fonts remotely from Google Fonts:

- **Orbitron** — Copyright 2018 The Orbitron Project Authors; Reserved Font
  Name "Orbitron"; SIL Open Font License 1.1.
- **Share Tech Mono** — Copyright (c) 2012, Carrois Type Design, Ralph du
  Carrois; Reserved Font Name "Share"; SIL Open Font License 1.1.

The full OFL notices are included under `THIRD_PARTY_LICENSES/`.

## External services

Optional proxies, storage services, Google Fonts delivery, and other online
services referenced by ACNET are not bundled software. They have their own
terms, privacy policies, rate limits, and availability. Mention does not imply
sponsorship or endorsement.

## Redistribution

Keep the top-level `LICENSE`, `ACKNOWLEDGEMENTS.md`, `NOTICE`,
`THIRD_PARTY_LICENSES/`, and the license comments embedded in the standalone
ACNET HTML with releases. Re-audit this list whenever bundled dependencies
change.
