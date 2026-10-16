# NIP-332

assumeUTXO Attestations over Nostr.

## Overview

NIP-332 defines a regular Nostr event (`kind 3332`) in which a Bitcoin node attests to the hash of the UTXO set at a block, as used
by assumeUTXO snapshots: that it recomputed the hash itself, or loaded the snapshot and validated the chain behind it. Attestations are
free to make and permanent once made, so a key's history is its reputation. The sibling of [NIP-333](https://nip-333.github.io/),
block headers over Nostr.

## Specification

- [Read the spec](https://nip-332.github.io/spec/)
- [nip-332.md](spec/nip-332.md)

## Implementations

| Where | What |
|-------|------|
| [assumeutxo.com](https://assumeutxo.com/) | the record: every snapshot, its torrents, and who attested it |
| [play-grounds/assumeutxo](https://github.com/play-grounds/assumeutxo) | `sign/`: make an attestation from a node or in the browser; `verify.mjs` |

## Quick Start

```json
["REQ", "attestations", {
  "kinds": [3332],
  "#network": ["tbtc4"],
  "#height": ["150000"]
}]
```

## Links

- [nip-332.github.io](https://nip-332.github.io) — Project homepage
- [NIP-01](https://github.com/nostr-protocol/nips/blob/master/01.md) — Nostr basics
