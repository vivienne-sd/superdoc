This branch is intended to reproduce the local "SuperDoc Dev" demo UI used for diffing demos.

Use this app:

- `packages/superdoc`

Do not use this app for the demo handoff:

- `examples/features/diffing`

Why:

- `packages/superdoc/src/main.js` mounts the `SuperdocDev` UI
- that is the dark-header app with `Upload file`, `Compare documents`, and tracked-change bubbles on the right

Demo assets:

- `examples/features/diffing/demo-docs/diff-demo-1.docx`
- `examples/features/diffing/demo-docs/diff-demo-2.docx`
- `examples/features/diffing/demo-docs/diff-demo-3.docx`
- `examples/features/diffing/demo-docs/diff-demo-4.docx`

Local run command:

```bash
npx pnpm@10.25.0 --prefix ./packages/superdoc run dev
```

Notes:

- this branch enables `server.allowedHosts = true` in `packages/superdoc/vite.config.js` so tunneled preview hosts work during ad hoc demos
- for Railway, the app Matt wants to deploy is still the `packages/superdoc` app
