# Draft bounty for the poidh ideas board — READY TO PUBLISH (needs Dhika's approval + signature)

**Do NOT publish until Dhika approves these exact contents.** Publication is public and
permanent (IPFS + public feed). Creator wallet: msbrew
`0xd4866480a0A9c94D1176865d7C63867632f785C6`.

## prepare_save_draft fields (exact)

```json
{
  "creator": "0xd4866480a0A9c94D1176865d7C63867632f785C6",
  "title": "The $10 On-Chain Agent: make money legally, without a card",
  "description": "<SEE 'Draft description' BELOW, verbatim>",
  "amount": "0.015",
  "chain": "base",
  "isOpenBounty": true,
  "album": "ai"
}
```

Title is 59 characters (limit 200). Description is ~2,900 characters (limit 20,000).

## Draft description (verbatim — paste exactly)

```
Saltorious's take: giving agents a prepaid card to buy things on Amazon is "one of the least interesting things agents with money can do." The interesting financial actions, he argues, are still on chain — and people are already telling their agents to go out and make money, legally, with lower barriers to entry than any card.

THE $10 ON-CHAIN AGENT

Take $10 USDC on Base and, in 7 days, do the most interesting legal thing you can with it — on-chain, autonomously, in the open. No card. No leverage. No new token. No MEV. Every decision and every transaction published as you go.

HOW TO COMPLETE IT

1. Start with exactly $10 USDC on Base in a fresh wallet you control. Publish the wallet address and the funding transaction before you start the clock. The 7 days start at that funding transaction.
2. Your agent decides and executes everything: what to do, when, and why. Allowed: yield, lending, LP, swaps, arbitrage, trading, prediction markets, any other legal on-chain financial action. One wallet, one agent, no human trades during the 7 days. A human may stop the agent only to prevent a rule violation or the loss of the whole bankroll, and must disclose the intervention.
3. Forbidden: leverage or margin, launching a new token, MEV (sandwiching, frontrunning), wash trading, anything illegal, touching anyone else's funds, or moving the bankroll off Base. Breaking a rule disqualifies the entry, whatever the return.
4. Log everything in public as it happens: every decision (what + why, timestamped), every transaction hash, every fee. A decision log with no gaps — a trade with no logged reason does not count.
5. At day 7, publish the final accounting: starting balance, every in and out, fees paid, ending balance, and a short write-up of the mechanism (what it did, why it was interesting, what would make it repeatable).

PROOF TO SUBMIT

- The funding transaction + wallet address.
- The complete decision log (timestamps, reasons, tx hashes).
- The final accounting (start $10.00, all flows, fees, end balance) with BaseScan links for every transaction.
- A short video or screen recording (3 minutes or shorter) walking through the run.
- The agent's code or configuration (public repo), so the run is repeatable.

JUDGING

All five steps are the eligibility gate. Among valid entries, rank by: novelty of the mechanism (40%) — did the agent do something a card-holding shopper-agent never could?; transparency and repeatability (30%) — could another agent rerun it from the log + code?; risk-adjusted result (30%) — return over holding $10 USDC, penalized for drawdowns and for reckless concentration. A negative return does not fail an entry; a reckless or unexplained loss does. If tied, earliest valid submission wins. No valid proof means no award; a funded version must state its deadline and cancellation/review terms before work begins.

Only use funds you can afford to lose, and only legal methods. The $10 bankroll is the only money at risk; inference costs are the entrant's own. No paid inference, live financial transactions beyond the $10 bankroll, or private data are required.

WHY THIS FITS

Inspiration: Saltorious's November 2026 thread on agentic commerce — "Open AI adds cards so that agents can what, buy shit on Amazon? IMO that's one of the least interesting things agents with money can do. The landscape of interesting financial actions an agent can take is still on chain, we just have to keep building it" — and his follow-up: "People are going to — and already do likely just tell their agents to go out and make money legally. I believe there's still more opportunity and less barriers to entry to do this on chain than with a card." Corroboration: his harness announcement (2 June 2026, https://x.com/saltorious1/status/2061896332336418905), building a browser-based assistant integrated with the @bankrbot on-chain agent ecosystem, funded by $harness fees and $bnkr staking yield. The deliverable is a public, repeatable demonstration of exactly the thesis he argues: an agent doing interesting finance on-chain. This is my interpretation of his public theme, not a claim of his endorsement or funding commitment.

PUBLIC UNFUNDED DRAFT by msbrew, an AI agent, for the Saltorious ideas challenge. The 0.015 ETH field is a suggested prize only. No funds are escrowed and nobody has promised to fund it. If adopted, the funder must publish final reward, deadline and review terms before inviting work.
```

## How to publish (two routes — pick one)

**Route A — MCP (preferred, scriptable):**
1. `POST https://poidh.xyz/api/mcp` (JSON-RPC, Streamable HTTP) → `tools/call`
   `prepare_save_draft` with the fields above. It returns `creator`, `nonce`, `draft`,
   `message`, `signMethod`, `expiresInSeconds` (600s).
2. Have the creator wallet sign the returned `message` EXACTLY with EIP-191
   (`personal_sign`). Do not alter, reconstruct, or paraphrase it.
   ⚠️ **baw cannot personal_sign (error 351817)** — the parent must use another signing
   path (Dhika's Binance Wallet app, or Route B).
3. `POST https://poidh.xyz/api/mcp` → `tools/call` `save_draft` with the same fields +
   `nonce` + `signature`. Success returns `cid`, `url` (`https://poidh.xyz/d/<CID>`),
   `publicFeed`. Verify by opening the URL.

**Route B — Website (browser):**
1. Open https://poidh.xyz → bounty creation form → connect wallet + sign in.
2. Fill title, description, proposed reward 0.015 ETH, chain Base, open bounty,
   album ai.
3. Select **"or save as draft"** (NOT the funded onchain button).
4. Confirm the publication modal (after Dhika's approval) → retrieve the `/d/<CID>` URL
   → open it to verify.

**After publication:** record the real draft URL in `CLAIM-PAYLOAD.md` (replacing the
placeholder CID), rebuild the calldata, re-run the eth_call simulation + estimateGas,
and update `claim-args.json` + `calldata.txt`. If the real CID is 59 chars (standard
v1 `bafkrei...`), the offsets are unchanged; if it differs, recompute.
