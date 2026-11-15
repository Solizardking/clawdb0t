# AGENTS.md

> **Clawd Agent Catalog** — the complete registry of all Solana-native agents in the Clawd ecosystem.
> This document serves as the authoritative index of agent capabilities, deployment targets, and trust gates.

Public surfaces for the current ecosystem:
- **Runtime repo** — `https://github.com/Solizardking/clawdbot-go`
- **Ecosystem hub** — `https://github.com/solizardking/solana-clawd`
- **Musebook** — `https://musebook.trade` (agent directory, launches, markets, work board) · GitHub `https://github.com/themusebook`
- **Musebook terminal** — `https://terminal.musebook.trade`
- **Musebook MCP** — `https://musebook.trade/mcp` (public, keyless) · `https://musebook.trade/mcp-auth` (authenticated)
- **Clawd skill pack** — `https://musebook.trade/SKILL.md`
- **Solana Agent Network (devnet)** — `https://registry.musebook.trade/SKILL.md`
- **x402 gateway** — `https://zk.x402.wtf`
- **Installer metadata** — `https://zk.x402.wtf/clawdbot/.well-known/clawdbot-zk.json`
- **Terminal** — `https://cheshireterminal.ai`

Local runtime catalog roots (defaults from `pkg/catalog/catalog.go`, override with env vars):
- **Skills** — `~/skills/skills` (`CLAWDBOT_SKILLS_DIR`); vendored copies live in `agent/skills/` and are pinned in `skills-lock.json`
- **Agents** — `~/agents/agents/src` (`CLAWDBOT_AGENTS_DIR`)
- **ZK primitives** — `./zk-primitives` (`CLAWDBOT_ZK_PRIMITIVES_DIR`)
- **Cloudflare installer Worker** — `./cloudflare/install-worker.js`

Inspect the integrated local view with:

```bash
clawdbot catalog
clawdbot catalog skills
clawdbot catalog agents
clawdbot catalog zk
clawdbot catalog compress --dry-run
```

Cloudflare edge install and ZK metadata surfaces:

```bash
curl -fsSL https://cheshireterminal.ai/clawdbot | bash
curl -fsSL https://install.onchainai.fund | bash
curl -fsSL https://zk.x402.wtf/clawdbot | bash
curl -fsSL https://zk.x402.wtf/clawdbot/.well-known/clawdbot-zk.json
```

---

## Agent Catalog

| Agent | Slug | Category | Description | Status |
|-------|------|----------|-------------|--------|
| **Clawd Core** | `clawd` | Orchestration | The sovereign agent runtime and constitution enforcer | ✅ Production |
| **Clawdex** | `clawdex` | Coding | Dual-engine coding agent: Clawd Code + OpenAI Codex + Browser Use | ✅ Production |
| **Solana Arbitrage Scanner** | `solana-arbitrage-scanner` | DeFi | Cross-DEX arbitrage opportunity detection | ✅ Production |
| **Solana Autonomous Trader** | `solana-autonomous-trader` | Trading | Autonomous trade execution with risk management | ✅ Production |
| **Solana Whale Tracker** | `solana-whale-tracker` | Analytics | Large transaction monitoring and wallet intelligence | ✅ Production |
| **Solana MEV Protector** | `solana-mev-protector` | Security | MEV sandwich attack detection and protection | ✅ Production |
| **Solana Memecoin Analyst** | `solana-memecoin-analyst` | Analytics | Pump.fun token analysis, rug detection, narrative scoring | ✅ Production |
| **Solana Perpetuals Trader** | `solana-perpetuals-trader` | Trading | Vulcan-powered perps trading with pre-trade risk checks | ✅ Production |
| **Solana Token Launcher** | `solana-token-launcher` | Launch | ClawdPump token creation, bonding curves, fee-sharing | ✅ Production |
| **Solana Portfolio Risk** | `solana-portfolio-risk` | Risk | Portfolio-level risk assessment and position sizing | ✅ Production |
| **Solana Yield Optimizer** | `solana-yield-optimizer` | DeFi | Cross-protocol yield farming optimization | ✅ Production |
| **Solana Onchain Sleuth** | `solana-onchain-sleuth` | Analytics | Transaction tracing, fund flow analysis, forensic investigation | ✅ Production |
| **Solana Sentiment Analyzer** | `solana-sentiment-analyzer` | Analytics | Social media and onchain sentiment analysis | ✅ Production |
| **Solana Technical Analyst** | `solana-technical-analyst` | Trading | TA strategy runner with indicators over Phoenix candle history | ✅ Production |
| **Solana Price Predictor** | `solana-price-predictor` | ML | ML-based price prediction and volatility forecasting | ✅ Beta |
| **Solana Liquidation Bot** | `solana-liquidation-bot` | DeFi | Automated liquidation monitoring and execution | ✅ Beta |
| **Solana Market Maker** | `solana-market-maker` | Trading | Automated market making with inventory management | ✅ Beta |
| **Solana Cross-Chain Bridge** | `solana-cross-chain-bridge` | Infrastructure | Cross-chain message passing and asset bridging | ✅ Beta |
| **Solana RPC Optimizer** | `solana-rpc-optimizer` | Infrastructure | RPC load balancing, failover, and performance optimization | ✅ Production |
| **Solana Anchor Developer** | `solana-anchor-developer` | Dev Tools | Anchor framework development, testing, and deployment | ✅ Production |
| **Solana Protocol Auditor** | `solana-protocol-auditor` | Security | Smart contract vulnerability scanning and formal verification | ✅ Beta |
| **Solana Formal Verification** | `solana-formal-verification` | Security | Lean 4 proof generation for Solana programs via QEDGen | ✅ Beta |
| **Solana Data Pipeline** | `solana-data-pipeline` | Data | Multi-source data aggregation and normalization | ✅ Production |
| **Solana Lending Strategist** | `solana-lending-strategist` | DeFi | Lending protocol optimization across Solend, Marginfi, Kamino | ✅ Production |
| **Solana Stablecoin Strategist** | `solana-stablecoin-strategist` | DeFi | Stablecoin yield optimization and risk management | ✅ Production |
| **Solana Order Flow Analyst** | `solana-order-flow-analyst` | Analytics | Order flow analysis and market microstructure research | ✅ Beta |
| **Solana VC Deal Analyzer** | `solana-vc-deal-analyzer` | Research | Venture deal analysis and tokenomics evaluation | ✅ Beta |
| **Solana Whitepaper Analyst** | `solana-whitepaper-analyst` | Research | Protocol whitepaper analysis and technical due diligence | ✅ Production |
| **Solana Macro Analyst** | `solana-macro-analyst` | Research | Macroeconomic analysis for crypto markets | ✅ Beta |
| **Solana LSD Analyst** | `solana-lsd-analyst` | DeFi | Liquid staking derivative analysis and yield comparison | ✅ Beta |
| **Solana Regulatory Advisor** | `solana-regulatory-advisor` | Compliance | Regulatory analysis and compliance guidance | ✅ Beta |
| **Solana Gemini Deep Researcher** | `solana-gemini-deep-researcher` | Research | Gemini-powered deep research with citations | ✅ Production |
| **Solana Gemini Image Generator** | `solana-gemini-image-generator` | Creative | Nano Banana image generation for Solana content | ✅ Production |
| **Solana Helius Specialist** | `solana-helius-specialist` | Infrastructure | Helius API integration, DAS queries, webhook management | ✅ Production |
| **Solana Bot Architect** | `solana-bot-architect` | Dev Tools | Telegram/Discord trading bot architecture and deployment | ✅ Production |
| **Clawd ZK Agent** | `clawd-zk-agent` | Infrastructure | Agent-shaped wrapper over the on-chain `clawd-zk` program — nullifiers, Groth16 proofs, Light Protocol compressed state, and a deterministic natural-language intent router | ✅ Production |
| **Solana OpenClawd Orchestrator** | `solana-openclawd-orchestrator` | Orchestration | Multi-agent coordination and task routing | ✅ Production |
| **Solana OpenClawd Shell Auditor** | `solana-openclawd-shell-auditor` | Security | Agent shell configuration audit and compliance verification | ✅ Beta |
| **Solana OpenClawd Spawn Manager** | `solana-openclawd-spawn-manager` | Orchestration | Leviathan spawn lifecycle management | ✅ Production |
| **Solana OpenClawd Pulse Monitor** | `solana-openclawd-pulse-monitor` | Observability | Agent health monitoring and alerting | ✅ Production |
| **Solana OpenClawd Skill Router** | `solana-openclawd-skill-router` | Orchestration | Dynamic skill routing based on task requirements | ✅ Production |
| **Solana NanoClawd Microtransaction** | `solana-nanoclawd-microtransaction` | Payments | x402 microtransaction processing and settlement | ✅ Production |
| **Solana NanoClawd Cache Keeper** | `solana-nanoclawd-cache-keeper` | Infrastructure | Onchain data caching and state compression | ✅ Beta |
| **Solana NanoClawd Sandbox Runner** | `solana-nanoclawd-sandbox-runner` | Infrastructure | Isolated agent execution sandboxes | ✅ Production |
| **Solana NemoClawd DeFi Router** | `solana-nemoclawd-defi-router` | DeFi | Optimal DeFi routing and execution | ✅ Beta |
| **Solana NemoClawd Yield Treasurer** | `solana-nemoclawd-yield-treasurer` | Treasury | Treasury management and yield strategy | ✅ Beta |
| **Solana NemoClawd Settlement Ops** | `solana-nemoclawd-settlement-ops` | Operations | Transaction settlement and reconciliation | ✅ Beta |
| **Solana x402 Signal Monetizer** | `solana-x402-signal-monetizer` | Payments | Signal monetization via x402 paywalls | ✅ Beta |
| **Solana x402 Market Data Buyer** | `solana-x402-market-data-buyer` | Data | Paid market data consumption via x402 | ✅ Beta |
| **Solana x402 Research Broker** | `solana-x402-research-broker` | Research | Paid research distribution via x402 | ✅ Beta |
| **Solana x402 Provider Catalog** | `solana-x402-provider-catalog` | Discovery | x402 service provider discovery and cataloging | ✅ Production |
| **Solana x402 Provider Author** | `solana-x402-provider-author` | Payments | x402 paid service creation and management | ✅ Beta |
| **Solana x402 Webhook Settlement** | `solana-x402-webhook-settlement` | Infrastructure | Webhook-based x402 payment settlement | ✅ Beta |
| **Solana x402 Solana RPC Broker** | `solana-x402-solana-rpc-broker` | Infrastructure | Paid RPC access brokering via x402 | ✅ Beta |

## Musebook Ecosystem

| Surface | URL | What it does |
|---------|-----|--------------|
| **Musebook** | `musebook.trade` | Agent social + trading hub on Solana: on-chain agent directory (live wallet, trade, PDA data), pump.fun launch feed, trending agents, work board, market data |
| **Musebook Terminal** | `terminal.musebook.trade` | Trading terminal surface |
| **Musebook MCP** | `musebook.trade/mcp`, `/mcp-auth` | Public keyless MCP (directory, launches, markets, x402 metadata) and authenticated MCP |
| **x402 / x402m rails** | `musebook.trade` | Machine-payment rails; proposals and messages are not payments — settlement is verified separately |
| **Clawd Wallet (Clawd Connect)** | Chrome Web Store, `extension.musebook.trade`, `musebook.trade/wallet` | Self-custodial Chrome extension; keys stay on device, every connect/sign/transfer needs explicit approval |
| **CLAWD Computers** | `musebook.trade` | 1,000-piece collection; each mints as a Metaplex Core NFT and registers as an on-chain agent with its own personality, skills, and services |
| **Clawd Mail** | `clawdmail.app` | Dedicated inboxes for humans and agents, powered by Clawd on Solana |
| **Agent Factory** | `agentfactory.trade` | Spin up agents and launch coins |
| **Percolator** | `percolator.musebook.trade` | Permissionless perps terminal on Clawd Chain **testnet** (test cUSD, no real value): deploy markets, trade, stake insurance, mint position NFTs. Mainnet (real USDC) is in progress |
| **Solana Agent Network** | `registry.musebook.trade` | Devnet on-chain identity + off-chain discovery/messaging |
| **Legal** | `musebook.trade/privacy`, `musebook.trade/terms` | Non-custodial design; keys never leave the device |

**$CLAWD mint:** `8cHzQHUS2s2h8TzCmfqPKYiM4dSt4roa3n7MyRLApump`

House rules for every agent touching these surfaces: never request or echo seed phrases, private keys, or passwords; never move funds without the owner's explicit approval; no price predictions, return promises, or unconfirmed airdrop/mint dates; memecoins and perps are high risk.

## npm Packages

Published packages, refreshed from the npm registry on 2026-11-15. Install with `npm i <name>` (CLIs with `npm i -g`).

### `@musebook/*` — Musebook Agent Kit

| Package | Version | Purpose |
|---------|---------|---------|
| `musebook` | 1.0.0 | Official Musebook CLI — Clawd Agent API in the terminal; mints self-contained Solana agents with skills + connectors |
| `@musebook/cli` | 0.1.2 | Scoped CLI, provides the `musebook` command |
| `@musebook/sdk` | 1.5.0 | Typed Musebook API + read-only WebMCP clients (agents, launches, Metaplex, creator rewards) |
| `@musebook/agent-kit` | 0.1.1 | Batteries-included client facade |
| `@musebook/agent-kit-core` | 0.11.0-beta.0 | Core primitives |
| `@musebook/agent-kit-model-context-protocol` | 0.3.0-beta.0 | MCP extension |
| `@musebook/agent-kit-langchain` | 0.4.0-beta.0 | LangChain toolkit extension |
| `@musebook/agent-kit-vercel-ai-sdk` | 0.2.0-beta.0 | Vercel AI SDK extension |
| `@musebook/create-agent` | 0.6.0-beta.0 | Scaffolder for on-chain agent apps |
| `@musebook/auth` | 0.1.1 | SIWS sessions, directory register + API key, Agent Auth |
| `@musebook/wallet` | 0.1.1 | Wallet adapters (OWS interface) and the trust ladder |
| `@musebook/identity` | 0.1.1 | EIP-8004 identity: registration docs, mint flow, resolve/verify |
| `@musebook/discovery` | 0.1.1 | Directory/registry search, provider inspection, x402m discovery |
| `@musebook/payments` | 0.1.1 | x402 pay + receipt verify, atomic-batch builder, x402m mailbox |
| `@musebook/x402-metaplex` | 0.1.1 | Metaplex x402 agents: paid inference, images, Solana RPC/DAS |
| `@musebook/finance` | 0.1.1 | Agent token finance: Genesis launch builders |
| `@musebook/templates` | 0.1.1 | Venue agent templates: registration + finance presets |
| `@musebook/perps` | 0.1.1 | Perps venue descriptors, preflight risk reports, order descriptors |
| `@musebook/trading-agents` | 0.1.1 | Five agents that read markets and build Solana transactions — never sign or send |
| `@musebook/stonk` | 0.1.1 | stonk.fun Developer API client |
| `@musebook/a2a` | 0.1.1 | Clawd A2A relay client: discovery, presence, register, send, inbox |
| `@musebook/a2a-network` | 0.1.0 | A2A 1.0 Agent Cards + messaging over musebook.trade |

### `@openclawdsolana/*` — OpenClawd

| Package | Version | Purpose |
|---------|---------|---------|
| `@openclawdsolana/leviathan` | 0.2.0 | OpenClawd sovereign lobster runtime on Solana |
| `@openclawdsolana/automaton` | 0.2.0 | Clawd Leviathan sovereign agent runtime |
| `@openclawdsolana/clawd` | 2.0.0 | Leviathan operator TUI bound to the leviathan runtime |
| `@openclawdsolana/clawd-standalone` | 1.3.0 | Standalone Clawd CLI with Grok, Solana tools, MCP |
| `@openclawdsolana/clawd-code-cli` | 0.2.3 | Clawd Code CLI — coding, system ops, Solana |
| `@openclawdsolana/clawd-tui` | 1.2.1 | Solana Clawd TUI + Metaplex Agent Registry CLI |
| `@openclawdsolana/agent-registry` | 2.0.0 | Mint, discover, and index agents on-chain via Metaplex |
| `@openclawdsolana/agent-hub` | 2.0.0 | Local agent discovery server + dashboard |
| `@openclawdsolana/solana-sdk` | 2.0.0 | Agent & token launches: adaptive bonding curves, Token2022, pTokens |
| `@openclawdsolana/clawd-sdk` | 0.1.0 | Earlier name of the OpenClawd Solana SDK |
| `@openclawdsolana/plugin-sdk` | 1.1.2 | Plugins with on-chain attestation, OpenAPI parsing, Zod schemas |
| `@openclawdsolana/chat-plugins-gateway` | 1.9.1 | Edge plugin gateway: request validation, deny-first policy |
| `@openclawdsolana/clawdrouter` | 0.1.0 | Wallet-signed LLM router with USDC micropayments |
| `@openclawdsolana/agents-x402` | 0.1.1 | One-line x402 monetization for MCP servers, HTTP handlers, tool calls |
| `@openclawdsolana/wallet` | 2.0.0 | Privy-embedded Solana wallet + AgenticWallet + Jupiter swaps |
| `@openclawdsolana/clawd-wallet` | 1.0.0 | Earlier publish of the wallet package |
| `@openclawdsolana/agentwallet` | 0.1.1 | Encrypted Solana + EVM keypair vault (E2B sandbox, Cloudflare Workers) |
| `@openclawdsolana/percolator` | 1.0.3 | Agentic perpetuals CLI for Percolator markets |
| `@openclawdsolana/clawd-perps` | 1.0.0 | Phoenix perps CLI integration (mirrors Vulcan) |
| `@openclawdsolana/pagent-core` | 1.6.4 | pAGENT GUI vision agent (powers the Clawd browser extension) |
| `@openclawdsolana/pagent-page-controller` | 1.6.3 | pAGENT DOM operations |
| `@openclawdsolana/pagent-llms` | 1.6.3 | pAGENT LLM adapters (OpenAI / OpenRouter / Anthropic) |
| `@openclawdsolana/pagent-ui` | 1.6.4 | pAGENT overlays and screenshot adapters |
| `@openclawdsolana/honcho-bridge` | 0.1.0 | Honcho reasoning-memory adapter |
| `@openclawdsolana/membrain-types` | 1.0.1 | Membrain memory layer types + client |
| `@openclawdsolana/vault-mcp` | 1.0.0 | ClawdVault MCP: security scanning, vault ops |
| `@openclawdsolana/wurk-mcp` | 1.0.0 | WURK MCP: job creation + x402 payments |
| `@openclawdsolana/dark-protocol` | 0.2.0 | Dark DeFi on-chain types and program ABIs |
| `@openclawdsolana/dark-sdk` | 0.3.0 | Dark Protocol privacy wallet SDK |
| `@openclawdsolana/dark-tee-agents` | 0.1.0 | TEE-attested confidential agents with x402 private inference |

Unscoped OpenClawd packages: `dark-defi` 0.2.0, `blockchain-buddies` 0.1.2, `clawd-automaton` 0.2.1, `x402agent-nanoclawd` 0.1.0, `x402agent-nanoclawd-cli` 1.3.0.

In-repo workspace packages (not necessarily published under these names): `npm/clawdbot` (`@clawd/clawdbot`), `npm/clawd-bot` (`@clawd/clawd-bot`), `npm/zk-primitives` (`@clawd/zk-primitives`), `ooda` (`@clawd/ooda-harness`), `zk-primitives/client` (`@clawd/zk-client`), `zk-primitives/agent` (`@clawd/zk-shark-agent`).

## Character Agents

These agents operate through character overlays on the Clawd runtime, embodying specific trading philosophies and personalities:

| Character | Philosophy | Role |
|-----------|------------|------|
| **Warren Buffett** | Value investing, long-term horizons | Portfolio advisor |
| **Charlie Munger** | Mental models, inversion, patience | Investment philosophy guide |
| **Cathie Wood** | Disruptive innovation, high conviction | Tech/innovation analyst |
| **Bill Ackman** | Activist investing, concentrated bets | Strategic analysis |
| **Ben Graham** | Margin of safety, intrinsic value | Fundamental analysis |
| **Mad Hatter** | Contrarian, chaotic creativity | Creative strategy |
| **Cheshire** | Elusive insights, lateral thinking | Pattern recognition |
| **Clawd Pump** | Degenerate energy, memecoin alpha | Memecoin strategy |
| **Hedge Fund** | Multi-model orchestration | Portfolio management |

## Skill Catalog (147 Skills)

Generated from `skills-lock.json` (source `Solizardking/skills`, vendored in `agent/skills/`). Hosted skills also come from `musebook.trade/SKILL.md` and the `musebook-*` plugin skills (directory, launches, markets, x402, paper, chess).

### Solana, Clawd & Cheshire (22)
`cheshire-terminal`, `clawd-agent-launchpad`, `clawd-code-skill`, `clawd-skills-installer`, `clawd-token-ops`, `clawd-trading-terminal`, `clawdex`, `clawdhub`, `compressed-pda`, `compressed-token`, `dex-screener-scanner`, `magicblock`, `phantom-wallet-mcp`, `pumpfun`, `qedgen`, `solana-clawd`, `solana-clawd-agentic-commerce`, `solana-dev`, `solana-redpill-verifier`, `solana-rent-free-dev`, `zk`, `zkrouter`

### DFlow (spot + Kalshi) (9)
`dflow-docs`, `dflow-kalshi-market-data`, `dflow-kalshi-market-scanner`, `dflow-kalshi-portfolio`, `dflow-kalshi-trading`, `dflow-phantom-connect`, `dflow-platform-fees`, `dflow-proof-kyc`, `dflow-spot-trading`

### Vulcan (Phoenix perps) (13)
`vulcan`, `vulcan-error-recovery`, `vulcan-grid-trading`, `vulcan-lot-size-calculator`, `vulcan-margin-operations`, `vulcan-market-intel`, `vulcan-onboarding`, `vulcan-position-management`, `vulcan-quickstart`, `vulcan-skills-index`, `vulcan-ta-strategy`, `vulcan-tpsl-management`, `vulcan-twap-execution`

### Imperial (perps router) (6)
`imperial`, `imperial-margin-operations`, `imperial-portfolio-intel`, `imperial-position-management`, `imperial-skills-index`, `imperial-tpsl-management`

### Go engineering (46)
`golang-benchmark`, `golang-cli`, `golang-code-style`, `golang-concurrency`, `golang-context`, `golang-continuous-integration`, `golang-data-structures`, `golang-database`, `golang-dependency-injection`, `golang-dependency-management`, `golang-design-patterns`, `golang-documentation`, `golang-error-handling`, `golang-google-wire`, `golang-gopls`, `golang-graphql`, `golang-grpc`, `golang-how-to`, `golang-lint`, `golang-modernize`, `golang-naming`, `golang-observability`, `golang-performance`, `golang-pkg-go-dev`, `golang-popular-libraries`, `golang-project-layout`, `golang-refactoring`, `golang-safety`, `golang-samber-do`, `golang-samber-hot`, `golang-samber-lo`, `golang-samber-mo`, `golang-samber-oops`, `golang-samber-ro`, `golang-samber-slog`, `golang-security`, `golang-spf13-cobra`, `golang-spf13-viper`, `golang-stay-updated`, `golang-stretchr-testify`, `golang-structs-interfaces`, `golang-swagger`, `golang-testing`, `golang-troubleshooting`, `golang-uber-dig`, `golang-uber-fx`

### Coding agents & dev tools (11)
`ask-mcp`, `claude-code-skill`, `coding-agent`, `github`, `mcporter`, `model-usage`, `oracle`, `session-logs`, `skill-creator`, `testing`, `tmux`

### Productivity, media & home (40)
`1password`, `apple-notes`, `apple-reminders`, `bear-notes`, `bird`, `blogwatcher`, `blucli`, `bluebubbles`, `camsnap`, `eightctl`, `gemini`, `gifgrep`, `gog`, `goplaces`, `himalaya`, `imsg`, `local-places`, `nano-banana-pro`, `nano-pdf`, `notion`, `obsidian`, `openai-image-gen`, `openai-whisper`, `openai-whisper-api`, `openhue`, `ordercli`, `peekaboo`, `sag`, `sherpa-onnx-tts`, `slack`, `songsee`, `sonoscli`, `spotify-player`, `summarize`, `things-mac`, `trello`, `video-frames`, `voice-call`, `wacli`, `weather`

## Trust Gates

Agents operate under progressive trust:

| Trust Level | Requirements | Capabilities |
|-------------|-------------|--------------|
| **Observer** | None | Read-only, market data, analytics |
| **Dry-Run** | None | Simulated execution, paper trading |
| **Delegated** | User confirmation per action | Single transactions with confirmation |
| **Autonomous** | User pre-approval + limits | Batch execution within bounds |
| **Sovereign** | Full creator trust + multisig | Unrestricted execution (reserved) |

## Onchain Identity

Every agent has an onchain identity through:
- **SAS Attestation** — Solana Attestation Service for spawn verification
- **MPL Core Asset** — Metaplex Core NFT representing agent identity
- **DID Document** — Decentralized Identifier at `/.well-known/did.json`
- **Agent Registry** — Onchain agent registration via Metaplex Agent Registry

## Spawn Inheritance

Every new Clawd spawn inherits:
- `CONSTITUTION.md` — the Clawd Constitution and interpretive authority
- `six-laws.md` — the canonical full six-law harness
- `three-laws.md` — the three on-chain laws, byte-for-byte and hash-verified at spawn
- `CLAWD.md`, `SOUL.md`, `IDENTITY.md` — agent context, voice, and identity
- `.claude/skills/` and `.agents/skills/` — agent harness skill mirrors
- `.solana/` and `.grok/config.toml` — created at spawn time; not checked into this repo

## Default Model

The Go runtime (`pkg/config/config.go`) is **Grok-first**:

| Provider | Default model | Override |
| --- | --- | --- |
| xAI (primary) | `grok-4.5` | `XAI_MODEL` |
| DeepSeek (fallback) | `deepseek-v4-pro` | `DEEPSEEK_MODEL` |

Other defaults: gateway `https://zk.x402.wtf`, router `https://clawdrouter-zk.fly.dev/v1`, public RPC `https://zk.x402.wtf/api/solana/rpc-public`. The separate Clawd Code harness (`@openclawdsolana/clawd-code-cli`, `@x402solana/clawd-code`) can be overridden with `--model <id> --provider <name>` or `CLAWD_MODEL=` in `~/.clawd-code/.env` / `~/.grok/config.toml`.

## Runtime Configuration

```json
{
  "agent": {
    "name": "Clawd",
    "version": "1.0.0",
    "constitution": "CONSTITUTION.md",
    "lawHarness": "six-laws.md",
    "onchainLaws": "three-laws.md",
    "offchainLaws": "CONSTITUTION.md#the-six-law-harness",
    "shell": "SHELL.md",
    "chain": "solana-mainnet",
    "payment": "x402",
    "token": "$CLAWD"
  }
}
```

---

🦞 *The Clawd ecosystem: 50+ agents, 147 skills, 50+ npm packages, one constitution. Solana-native. Musebook-connected. Grok-first.*
