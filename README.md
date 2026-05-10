# BasedMining Docs (Mintlify)

This folder contains the **public-facing** documentation for BasedMining, published to Mintlify.

## What goes here

Public-friendly docs for three audiences:

- **Miners** running ASICs at home
- **On-chain users** participating via BasedPool NFTs on Base
- **AI agents** (planned, not live yet)

## What does NOT go here

This folder is **public**. Do not put any of the following in it:

- Server / VPS infrastructure details (Apollo, Vultr, NY VPS, ports, paths)
- Internal ckpool config or operator runbooks
- Rental agent / NiceHash routing internals
- Database schemas, backup procedures, postgres configs
- Anything from the existing `/docs` folder at the repo root

Internal ops docs stay in the repo-root `/docs` folder. They are separate intentionally.

## Local preview

```bash
npm i -g mint
cd mintlify-docs
mint dev
```

Opens a local preview at http://localhost:3000.

## Deploy

The site is hosted by Mintlify. Deployment is one of:

1. **GitHub-connected deploy.** If the Mintlify project is connected to a GitHub repo, push to the configured branch — Mintlify auto-deploys. Recommended.
2. **Manual trigger via API.** After content is in the connected repo, call:
   ```bash
   curl -X POST https://api.mintlify.com/v1/project/update/<projectId> \
     -H "Authorization: Bearer mint_<admin_api_key>"
   ```

## Structure

```
mintlify-docs/
├── docs.json              ← config: theme, navigation, colors
├── introduction.mdx       ← landing page
├── how-it-works.mdx       ← model overview
├── quickstart.mdx         ← path picker for the three audiences
├── miners/                ← ASIC operators
├── onchain/               ← NFT holders
├── agents/                ← AI agents (coming soon)
├── faq.mdx
├── glossary.mdx
└── images/                ← logos, favicon
```

## Editing tone

Match the existing site's voice (see `BASEDMINING_DESIGN_BRIEF.md` at repo root):

- Terse. Technical. No fluff.
- Metric-first. Sentence case. All-caps for category labels.
- Bitcoin is always capitalized. Base is the L2.
- No emojis.
