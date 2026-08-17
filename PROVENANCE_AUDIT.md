# ACNET Source Provenance and License Audit

**Audit date:** 2026-08-17  
**Artifact:** `ACNET_R70_CYRINX_GGWAVE_LICENSED.html`

## Result

**PASS — no additional unidentified bundled software package was found by this static provenance scan.**

Expected bundled/referenced components were found and accounted for: ggwave
(including its Reed-Solomon/Ooura FFT/browser-build provenance), pako/zlib,
the clean-room Cyrinx technical reference, and the two remotely loaded fonts.
Other hits were ACNET code, standard browser APIs, protocol/algorithm names,
or optional external service endpoints.

## Integrity checks

- Original renamed ACNET SHA-256: `55d12abbbf4b49e17609af693f3aec906612df555ccca922f474c1575c8dc0d7`
- Licensed ACNET SHA-256: `1a2aaa59c5f927076b255757b2445ce6be3f96424c322785a8f733af25e7cc4c`
- Licensing patch verified as comment-only: **YES**
- Executable inline scripts: **24**
- Non-executable script/data blocks: **5**
- Executable JavaScript syntax: **PASS**
- Absolute URL strings inventoried: **32**
- Remaining `Gibberlink` text: **NO**
- `GGwave (best)` present: **YES**

## Component disposition

| Component | Disposition | License / basis |
|---|---|---|
| ACNET original/integration code | PASS | GPL-3.0 project license |
| ggwave | PASS | MIT |
| ggwave Reed-Solomon subcomponent | PASS | MIT |
| Ooura FFT routines used by ggwave | PASS | Ooura FFT permission notice |
| Emscripten-generated ggwave browser runtime | PASS | MIT / University of Illinois-NCSA |
| pako | PASS | MIT |
| zlib-derived pako source | PASS | zlib License |
| Cyrinx technical reference | PASS / REFERENCE | Upstream Apache-2.0; ACNET states clean-room JS |
| Orbitron | PASS | SIL OFL 1.1 |
| Share Tech Mono | PASS | SIL OFL 1.1 |
| Web Crypto/modem algorithms/protocols | PASS / NOT BUNDLED LIBRARY | Browser APIs and ACNET implementations |
| Optional CORS/storage/network services | PASS / EXTERNAL SERVICE | Not bundled software |

## Cyrinx

ACNET's own source describes its CYRINX browser modem as a **clean-room
JavaScript implementation** following documented Cyrinx bulk-PHY building
blocks and explicitly says it is not bit-for-bit wire-compatible with upstream
`cyrinx_bulk`. The release therefore credits Cyrinx and includes Apache-2.0
without falsely claiming upstream C source is bundled.

If future ACNET code copies or adapts copyrightable Cyrinx source, obtain the
exact upstream `NOTICE` from that version/commit and preserve the applicable
notice material as required by Apache-2.0.

## External services

The source contains optional endpoints for Google Fonts, CORS proxies, Filebin,
JSONBlob/jsonstorage and normal example/browsing URLs. These are external
services, not redistributed software dependencies.

## Scope and limitation

The full HTML was searched for copyright/license/author strings, source URLs,
common package fingerprints, cryptographic-library fingerprints, modem/DSP/FEC
identifiers, every script block, embedded pako/ggwave, Cyrinx comments, fonts
and network endpoints. `PROVENANCE_AUDIT.json` contains the detailed inventory.

This is a strong technical release-hygiene audit, not a legal opinion, and it
does not include a commercial/global snippet-similarity database scan.
