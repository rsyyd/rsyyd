# rsyyd

Systems and tooling engineer. I prefer the unglamorous parts done properly: runtime
contracts, permission boundaries, install paths, and tests that prove the claims.

## larecode — AI coding agent for the terminal

TypeScript, MIT. Runs locally, provider-neutral (OpenAI-compatible, Anthropic, Ollama,
OpenRouter, custom endpoints).

Two things I care about more than features:

- **One runtime, seven surfaces.** TUI, `run`, HTTP server, ACP, Telegram gateway, cron, and SDK all run the same `AgentRuntime` turn contract — same events, same halt reasons, same cancellation semantics. [ADR-0002](https://github.com/rsyyd/larecode/blob/main/docs/architecture/adr/0002-agent-runtime-contract.md) · [surface matrix](https://github.com/rsyyd/larecode/blob/main/docs/architecture/surfaces.md)
- **Default-deny permissions.** 11 groups; `secrets` and `destructive` can never be pre-authorized, including in unattended cron and gateway runs; unknown tools fall back to the strictest group rather than silently passing. [permissions](https://github.com/rsyyd/larecode/blob/main/docs/permissions.md)

Every claim in the README links to the test that proves it, or is labelled not shipped: [claims and evidence](https://github.com/rsyyd/larecode/blob/main/docs/claims.md).

`npm i -g larecode` · `brew tap rsyyd/larecode` · [docs](https://rsyyd.github.io/larecode/) · [source](https://github.com/rsyyd/larecode)

## LPLang — a programming language

Rust, pre-alpha. Gradual typing (Python-like and Rust-like), ARC plus a cycle detector instead of a GC, structured concurrency via nurseries. Design principles and current status are in the README, including what is deliberately not built yet. [source](https://github.com/rsyyd/LPLang)

## Reach me

Telegram: [@rsyyd_h](https://t.me/rsyyd_h)
