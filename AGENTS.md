# AGENTS.md

Guidance for AI coding agents working in this repository.

## What this is

`vscode-3d` v0.2.0. Preview GLB and glTF models inside VS Code, try 2,800 library animations or a text-described motion on any rig and bake the result, generate and refine models from a prompt on the free three.ws lane, optimize for the web, diff a model against git, AI quality-check a render, and get diagnostics and completions for <agent-3d> embeds. Powered by three.ws.

A JavaScript library. Import it from ESM.

## Use it

```bash
npm install vscode-3d
```

Full usage, tool list and configuration are in [README.md](README.md). Machine-readable summaries: [llms.txt](llms.txt) and [llms-full.txt](llms-full.txt).

## Develop

```bash
npm install
npm test
```

Scripts:
- `npm run build`: `node build.mjs`
- `npm run watch`: `node build.mjs --watch`
- `npm run test`: `node build.mjs && node --test "test/*.test.mjs"`
- `npm run package`: `npx --yes @vscode/vsce package --no-dependencies`
- `npm run publish:marketplace`: `npx --yes @vscode/vsce publish --no-dependencies`
- `npm run publish:openvsx`: `npx --yes ovsx publish --no-dependencies`
- `npm run vscode:prepublish`: `node build.mjs --production`

## Conventions

- ES modules, Node >=20.
- Read-only by default. Anything that signs, spends or sends must be an explicit, separately named tool or option, and must never be inferred from untrusted text (token names, memos, listings).
- Never commit credentials. Configuration comes from environment variables documented in the README.
- Keep changes small and covered by a test next to the code they change.

## Source of truth

This repository is a generated mirror of `packages` in https://github.com/nirholas/three.ws. Open issues here; send substantial changes as a pull request here or upstream.
