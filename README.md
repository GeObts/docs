# BasedMining Docs

Public-facing documentation for [basedmining.xyz](https://basedmining.xyz), published via Mintlify at [docs.basedmining.xyz](https://docs.basedmining.xyz).

## What goes here

Public, audience-friendly docs for three audiences:

- **Hardware miners** running ASICs at home
- **Onchain users** participating via Hashpower NFTs on Base mainnet
- **AI agents** (the surface is being built — see `agents/`)

## What does NOT go here

This repo is **public**. Keep out:

- Server / VPS infrastructure details (hosts, ports, paths, ckpool internals)
- Operator runbooks, postgres ops, backup procedures
- Rental agent / NiceHash routing internals
- Any internal-ops documentation from the main `basedmining` repo

## Editing

The fastest way is the Mintlify web editor:

1. Go to https://dashboard.mintlify.com → log in → pick the `basedminingco` project
2. Click any page in the sidebar → edit in their WYSIWYG editor
3. Save → it commits to this repo's `main` automatically and the live site rebuilds in ~30 seconds

Alternative: edit MDX files directly in this repo and push to `main`.

## Local preview

```bash
npm i -g mint
mint dev
```

Opens a local preview at http://localhost:3000.

## Structure

```
.
├── docs.json                ← config: theme, navigation, colors
├── introduction.mdx         ← landing page
├── how-it-works.mdx         ← model overview
├── quickstart.mdx           ← path picker for the three audiences
├── pool/                    ← hybrid model, comparisons
├── miners/                  ← ASIC operators
├── onchain/                 ← Hashpower NFT holders
├── agents/                  ← AI agents (in development)
├── dashboard/               ← shared dashboard docs (used by all audiences)
├── calculator/              ← mining odds calculator
├── referrals/               ← referral v1 program
├── faq.mdx
├── glossary.mdx
└── images/                  ← logos, favicon
```

## Tone

Match the live site (see `BASEDMINING_DESIGN_BRIEF.md` in the main repo if you need a reference):

- Terse. Technical. No fluff.
- Metric-first. Sentence case. All-caps for category labels.
- Bitcoin is capitalized. Base is the L2 (never call it "Coinbase L2").
- "onchain" — one word, no hyphen.
- "Hashpower NFT" — not "BasedPool NFT".
- 0% pool fee. No "claim" flow — payouts are automatic.
- No emojis.
