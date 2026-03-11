# Acme Demo Sandbox

Standalone demo monorepo for manually exercising `agentpack` and related tools.

## Hero Flow

```bash
node ../../bin/agentpack.js skills inspect domains/brand/skills/copywriting
node ../../bin/agentpack.js skills validate domains/brand/skills/copywriting
node ../../bin/agentpack.js skills dev domains/brand/skills/copywriting
```

If this repo is checked out standalone, replace `../../bin/agentpack.js` with the path to your local `agentpack` checkout.

Edit `domains/brand/knowledge/tone-of-voice.md` to trigger stale-state and workbench refresh behavior.

Local workbench skills under `workbenches/website-dev/skills/` require packaged skills under `domains/**/skills/`.
The packaged skills attach source provenance through `metadata.sources` so the workbench DAG can show both dependency and provenance edges.
