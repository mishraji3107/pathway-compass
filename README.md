# Pathway Compass

Pathway Compass is an interactive educational explainer for the DataForge 2026
Pathway Track. It helps a first-time builder understand long-horizon evolving
state through a small, transparent browser computation.

## Central claim

> A fixed-shape recurrent state can process a sequence of unbounded duration
> without allocating a new memory slot for every token, but it can still forget
> through interference.

The learner varies sequence length and input noise, observes a live state
summary, and compares it with a defined reference signal. The demo is a
teaching model, not a BDH implementation, benchmark reproduction, or deployment
claim.

## Repository layout

- `artifacts/pathway-compass/` — React + Vite application.
- `submission-kit/` — application copy, concept summary, technical blog,
  presentation, sources, licenses, AI disclosure, and demo script.
- `pnpm-workspace.yaml` — workspace package configuration.

## Requirements

- Node.js 20 or newer
- pnpm 10 or newer

## Install and run

```bash
pnpm install
pnpm --filter @workspace/pathway-compass run dev
```

Open the local URL printed by Vite. The app defaults to port `5173` and can
also use Replit's `PORT` and `BASE_PATH` environment variables when present.

## Verify a production build

```bash
pnpm --filter @workspace/pathway-compass run typecheck
pnpm --filter @workspace/pathway-compass run build
```

The production output is written to
`artifacts/pathway-compass/dist/public/`.

## Reproduce the lesson

1. Open the app without signing in.
2. Start with the recommended topic.
3. Scroll to the interactive state demo.
4. Increase sequence length and observe that the state remains fixed-shape.
5. Increase noise and observe how interference makes the summary less reliable.
6. Read the BDH and BDH-CQ sections and compare the case studies with the toy
   mechanism.

## Evidence and provenance

Research references, license notes, and AI assistance disclosure are in
`submission-kit/`. The project cites primary papers and labels synthetic
teaching behavior separately from reported research claims.

## License

This project is released under the MIT License. See `LICENSE`.