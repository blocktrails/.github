# Blocktrails

**Nostr-native state on Bitcoin.**

Blocktrails are a primitive for anchoring evolving state to Bitcoin using output-key commitments. One P2TR output per state update. No extra tokens. No sidechains.

## Get Started

| Resource | Description |
|----------|-------------|
| [blocktrails.github.io](https://blocktrails.github.io) | Landing page — start here |
| [Specification](https://blocktrails.github.io/spec/) | Full technical spec |
| [Reference Implementation](https://github.com/blocktrails/blocktrails) | JavaScript/Node.js library |

## Quick Example

```javascript
import { Blocktrail } from 'blocktrails';

const trail = new Blocktrail(privateKey);
trail.genesis(JSON.stringify({ balance: 1000 }));
trail.advance(JSON.stringify({ balance: 900 }));

// Each state → unique P2TR address on Bitcoin
```

## Key Properties

- **Nostr-native** — full secp256k1 keys, same as Nostr
- **Minimal** — one output per state, key-path spends only
- **SPV-compatible** — verify with merkle proofs
- **No extra tokens** — just Bitcoin

## Status

- Specification: **draft**
- Reference implementation: **v0.1.0**

## License

Public domain.
