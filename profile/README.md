# Gravit Open Network Foundation

Open protocols and reference code for **verifiable decisions**: a claim, by a person, a
system or an autonomous AI agent, is accepted only with evidence that anyone can re-check,
and every decision is a reproducible artefact.

Swiss non-profit association (Verein), Zurich · Foundation: [gon.foundation](https://gon.foundation/) ·
Network, docs and SDKs: [gravitopennetwork.org](https://gravitopennetwork.org/) ·
Hosted verifier: [gravitverifier.space](https://gravitverifier.space/)

**Status (27 Nov 2026):** reference verifier v0.7.0; all published registry keys are test keys;
the root key ceremony and mainnet are planned for December 2026
([status](https://gravitopennetwork.org/mainnet/)). No production deployment at a customer yet.

## Reproduce our results

```bash
git clone https://github.com/gon-foundation/gravit-eval-pack
cd gravit-eval-pack && make eval
```

Every published number is computed by code and checked in CI.

## Specifications (IETF Internet-Drafts)

- [draft-gravit-gevp-12](https://datatracker.ietf.org/doc/draft-gravit-gevp/12/): GEVP, the mechanism, how evidence is verified (built on SCITT, RFC 9943, and COSE Receipts, RFC 9942)
- [draft-gravit-verifiable-epistemic-decision-00](https://datatracker.ietf.org/doc/draft-gravit-verifiable-epistemic-decision/00/): VEDS, the policy, what a verified decision must guarantee
- [draft-gravit-graviteron-00](https://datatracker.ietf.org/doc/draft-gravit-graviteron/00/): the Graviteron, a unit for the weight of evidence in decibans (experimental)

Internet-Drafts are individual submissions; they are not endorsed by the IETF.

## Test vectors, by version

| Where | Golden vectors |
|---|---|
| Release v0.7.0 (25 Oct 2026) | 54 |
| Implementation status in GEVP-12 (2 Nov 2026) | 56 |
| `verifier` main (27 Nov 2026) | 60 (3 canonical-JSON vectors proposed in PR #13) |

Python reference and Rust port decide all of them identically, and 200,000,000 generated cases in two
public runs, 10,000,000 of them repeated on a second machine
([reports](https://github.com/gon-foundation/verifier/tree/main/reports)). This is our own testing,
not an independent audit.

## Repositories

| Kind | Repositories |
|---|---|
| Specification | [gravit-research](https://github.com/gon-foundation/gravit-research) (IETF draft sources; formerly `gravitnet`), [gravit-canon](https://github.com/gon-foundation/gravit-canon) |
| Reference implementation | [verifier](https://github.com/gon-foundation/verifier), [gravit-eval-pack](https://github.com/gon-foundation/gravit-eval-pack) |
| Service and SDKs | [gravit-verifier-service](https://github.com/gon-foundation/gravit-verifier-service) (hosted API; Python and TypeScript clients) |
| Governance components | [capability-gate](https://github.com/gon-foundation/capability-gate), [history-keeper](https://github.com/gon-foundation/history-keeper) |
| Profiles and adapters | [gevp-agentic-finance-profile](https://github.com/gon-foundation/gevp-agentic-finance-profile), [gravit-safr-adapter](https://github.com/gon-foundation/gravit-safr-adapter) (SAFR v1.1, MAS BuildFin.ai) |
| Applications | [gravit-path](https://github.com/gon-foundation/gravit-path) |
| Public checks (read-only, public data, not audits) | [gravit-chainlink-verification](https://github.com/gon-foundation/gravit-chainlink-verification) (CL-01), [gravit-coffer-verification](https://github.com/gon-foundation/gravit-coffer-verification) (C-01), [gravit-ton-verification](https://github.com/gon-foundation/gravit-ton-verification) (TN-01) |
| Proofs of concept (simulated, test keys, not partnerships) | [allunity](https://github.com/gon-foundation/gravit-allunity-poc), [sygnum](https://github.com/gon-foundation/gravit-sygnum-poc), [dwf](https://github.com/gon-foundation/gravit-dwf-poc), [easymm](https://github.com/gon-foundation/gravit-easymm-poc) |
| Research and experiments | [graviteron](https://github.com/gon-foundation/graviteron), [gravit-grover](https://github.com/gon-foundation/gravit-grover), [gravit-truth-consensus](https://github.com/gon-foundation/gravit-truth-consensus), [gravit-epistemic-verifier](https://github.com/gon-foundation/gravit-epistemic-verifier) |
| Historical (kept, superseded) | [gravit-core](https://github.com/gon-foundation/gravit-core), [gravit-system](https://github.com/gon-foundation/gravit-system), [gravit-spec](https://github.com/gon-foundation/gravit-spec), [gravit-yumi-poc](https://github.com/gon-foundation/gravit-yumi-poc), [gravitnet-grok-poc](https://github.com/gon-foundation/gravitnet-grok-poc) |
| Websites and docs | [gravit-world](https://github.com/gon-foundation/gravit-world) (gon.foundation), [gravit-docs](https://github.com/gon-foundation/gravit-docs) (docs.gravit.world) |

Until 8 Nov 2026 the repositories were in the organisation `gravit-open-network-foundation`;
they were transferred with full history, and old links redirect.

## How we work

- Every change is reviewed and approved by a second person who is not its author.
- Every number in a README must be reproduced by code.
- History is never rewritten: corrections are added, not erased.
- Keys in public repositories are test keys until the root key ceremony.

Code is Apache-2.0 unless stated otherwise.
