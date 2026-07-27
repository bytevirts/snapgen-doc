# SnapGen documentation

Mintlify documentation published at `https://docs.snapgen.org` for the SnapGen
API at `https://api.snapgen.org`.

This repository mirrors the page structure of `bytevirts/freemodel-doc` so
shared API changes can be compared and ported by path without mixing brands in
the published content.

The public information architecture has four top-level tabs:

- **API Manual**: overview, individual text/image/video model pages, endpoint references, and task management
- **Integrations**: development tools and OpenAI SDKs
- **Guides**: quickstart, authentication, video workflow, billing, rate limits, and errors
- **FAQs**: connection, billing, security, and model capability questions

## Local development

Validate the complete Mintlify build:

```bash
npx -y mintlify@4.2.715 validate
```

Start the local preview:

```bash
npx -y mintlify@4.2.715 dev --port 3000
```

Open `http://localhost:3000`.

## Content rules

- Keep `docs.json` navigation synchronized with every visible page.
- Give every live model its own page under `api-manual/{text,image,video}`.
- Copy model IDs, prices, and availability from the live SnapGen catalog.
- Keep Portal-only values such as `familySlug` out of public API payloads.
- Use individual model pages for model-specific duration, resolution, reference, and billing rules.

## Publishing

Mintlify deploys the documentation from the repository's default branch. Validate locally before pushing changes to that branch.
