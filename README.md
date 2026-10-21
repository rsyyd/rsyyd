# rsyyd

Systems and tooling engineer. I build developer tools in TypeScript and Rust — currently an AI coding agent for the terminal, and a programming language.

## larecode

An AI coding agent for the terminal. Provider-neutral, runs locally, MIT.

- **One runtime, seven surfaces.** The TUI, `run`, the HTTP server, ACP, the Telegram gateway, cron, and the SDK all drive the same `AgentRuntime` turn — same events, same halt reasons, same cancellation semantics. One matrix test runs all seven against a single fake runtime.
- **Default-deny permissions.** Every tool call is checked against one of 11 groups before it runs. `secrets` and `destructive` can never be pre-authorized, including in unattended cron and gateway runs. Unknown tools fall back to the strictest group rather than passing silently.

Every claim in its README maps to the test that proves it, or is labelled *not shipped*.

```bash
npm install -g larecode
brew tap rsyyd/larecode && brew install larecode
```

<p>
  <a href="https://rsyyd.github.io/larecode/"><img src="https://img.shields.io/badge/docs-1f6feb?style=flat-square&logo=readthedocs&logoColor=white" alt="Documentation"></a>
  <a href="https://www.npmjs.com/package/larecode"><img src="https://img.shields.io/npm/v/larecode?style=flat-square&logo=npm&label=npm&color=cb3837" alt="npm version"></a>
  <a href="https://github.com/rsyyd/larecode/blob/main/LICENSE"><img src="https://img.shields.io/github/license/rsyyd/larecode?style=flat-square&label=license&color=2ea043" alt="License"></a>
  <a href="https://t.me/rsyyd_h"><img src="https://img.shields.io/badge/telegram-26a5e4?style=flat-square&logo=telegram&logoColor=white" alt="Telegram"></a>
</p>

## LPLang

A programming language: gradual typing, ARC with a cycle detector instead of a GC, structured concurrency via nurseries. Pre-alpha, Rust. Its README lists what is deliberately not built yet.

[Source](https://github.com/rsyyd/LPLang)
