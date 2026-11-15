# POIDH Bounty 1551 (on-chain 565) — Submission Package (RESEARCH ONLY)

**Status: RESEARCH COMPLETE, DRAFT READY — NOT PUBLISHED, NOT CLAIMED.**
**Blocked on 3 parent/Dhika steps (see §7): (1) approve + publish the draft on the poidh
ideas board (needs a wallet signature), (2) dated tweet screenshot via browser,
(3) proof repo creation + upload. Do NOT claim on-chain until Dhika gives his explicit
yes (claim = Base mainnet tx). No contact with Saltorious, no signup, no payment made.**

## 1. Bounty facts (verified on-chain + poidh API)

| Field | Value |
|---|---|
| Bounty page | https://poidh.xyz/base/bounty/1551 |
| Title | write a bounty for Saltorious |
| UI id / on-chain id | 1551 / 565 |
| Chain | Base (8453) |
| Contract | `0x5555Fa783936C260f77385b4E153B9725feF1719` |
| Issuer | `0x10fc964ef70c8467cd8c53e9ed9347422adf96a8` (NOT Vireo's address — see §2) |
| Prize escrowed | **0.0033 ETH** (~$5.84; winner net 0.0032175 ETH ≈ $5.69 after 2.5% fee) |
| Created | **2026-11-14 22:39:18 UTC** (= 15 Nov 05:39:18 WIB), `createdAt` epoch 1794695958 |
| Deadline (creation+168h, binding) | **2026-11-21 22:39:18 UTC = 2026-11-22 05:39:18 WIB** |
| Deadline as written in bounty text | "Saturday, November 21st @ 11:59pm PST" = 22 Nov 07:59 UTC = **22 Nov 14:59 WIB** (LATER than the on-chain deadline — the earlier on-chain deadline governs; target before 22 Nov 05:39 WIB) |
| Review / nomination | by issuer; "The most creative, saltorious-aligned bounty idea wins" |
| Status | **OPEN** — `bounties(565)`: claimer `0x0`, claimedAt 0; API: `inProgress: true`, `acceptingClaims: true`, `isVoting: false`, `winningClaim: null` |
| Album | `research` (per API `extra.album`) |
| Existing claims | **ONE** — rival claim at `getClaimsByBountyId(565,0)` (see §2); index 1 is the empty template → no second claim |
| Hours left at package time | ~6.5 days (package written 15 Nov ~07:30 WIB) |

Bounty text (full, decoded from `bounties(565)`, 1162 chars, verified against the API):
> "Agents, go read @saltorious1's X feed (https://x.com/saltorious1) and come back with
> a poidh bounty he'd actually want to put money behind. Look for something he keeps
> coming back to, a take he'd love to see tested, or a running joke that deserves to
> become a real challenge. Turn it into a bounty someone could actually complete. What
> should they do, and what would count as proof they did it? **How to enter** 1. Publish
> your idea as a public bounty draft on the poidh ideas board (https://poidh.xyz/ideas).
> 2. Submit a claim here with the **direct link to your published poidh draft** in the
> claim description. Tell us which post or theme from his feed inspired it and why you
> think he'd fund it. Ideally you screenshot the tweet and include it as your claim
> image. **Bonus points** if you, the agent, post your draft link on X yourself and tag
> @saltorious1. Include the link to your X post in your claim so we can see the pitch.
> **The most creative, saltorious-aligned bounty idea wins.** Deadline to submit a claim
> is Saturday, November 21st @ 11:59pm PST. Need help getting started with poidh? Check
> out https://poidh.xyz/skill.md"

Sources on disk: `~/workspace/bounty-tools/poidh-1565/bounty-565-raw.txt`,
`rival-claim-0-raw.txt`, `rival-claim-1-raw.txt`.

## 2. The rival claim — decoded in full

Only ONE rival claim exists. It is **strong** — authored by **Vireo itself**
(farcaster `vireo-agent`, address `0xe70b21eb2c666d7f828fb27228cfbdbf2b80a986` — the
same address that issued bounty 1549). API claimId 9603; claim URI
`https://gateway.pinata.cloud/ipfs/QmVNsdWQpmDAgLJyWBnfuT3jJtNVW6yJ7siYswk5ZrGbin`.

- **Name:** "The HF Fire Drill: a working survival kit for an open model"
- **Published draft:** https://poidh.xyz/d/bafkreic7esirkvyqn6kvevl3sb7vxcjjh35gd5jdj73eamebwbtdxgg7wq
  (Base open bounty, album `ai`, proposed reward **0.020 ETH**)
- **Idea:** recover one openly licensed model from two independently operated,
  non-origin locations, with the origin blocked locally, empty caches, verified
  hashes, real offline inference; repeat with the first mirror blocked; independent
  rerun required. A survival kit for one model — explicitly NOT a full HF replacement.
- **Inspiration cited:** Saltorious's 12 Nov post asking for a decentralized HF
  (https://x.com/saltorious1/status/2120988266384015697, snowflake-verified:
  2026-11-12 21:13 UTC) + corroborating theme "keeping open AI available"
  (https://x.com/saltorious1/status/2120910807013675099, 2026-11-12 16:05 UTC).
  Claims verification via X's syndication endpoint (token redacted in the claim).
- **Strengths:** tight falsifiable spec, verified sources, published draft, clear
  judging rubric, honest "unfunded draft" disclaimer.
- **Weaknesses (our opening):** it is ONE narrow infrastructure idea; it does not
  touch what Saltorious actually builds day-to-day (bankr / harness); the
  decentralized-HF ask is a plea ("I'm begging..."), not a thesis he defends with
  an argument. The bounty asks for the MOST CREATIVE, saltorious-aligned idea —
  a second infrastructure drill is the safe entry, not the creative one.

## 3. Research — who Saltorious is (verified)

**Profile:** @saltorious1 ("saltorious"), ~297 followers. Bio: "Dev. JS/TS and
Solidity. I like building stuff. Founder and lead engineer at [Lazer]. Currently
@Lazer_HQ". Works at **bankr** (@bankrbot); previous experience at Coinbase /
OpenSea / Dinari. Farcaster: saltorious.eth (5.3k followers).

**What he builds — harness (@tryharness):** "a browser based AI assistant that lives
in a floating PiP window, is screen aware, anon/private, and requires no downloads or
installs of any kind, including browser extensions" (announcement tweet
https://x.com/saltorious1/status/2061896332336418905, snowflake-verified:
**2026-06-02 19:42 UTC**; text verified verbatim via twiscan mirror). Goal: "completely
integrate with the @bankrbot ecosystem on the backend, by using a portion of fees from
the $harness token + a portion of any revenue generated to buy and stake $bnkr, and using
the yield to subsidize, and hopefully eventually fund inference to provide a desktop
assistant that is both affordable and capable. In addition, integrating, secondary
marketplaces like @AskSurplus to further reduce inference costs. In addition making
@bankrbot skills a first class provider for adding skills and capabilities to your
individual harness assistant." ~2k MAU, 400–700 WAU, ~200 DAU, usage up ~75% MoM
(per @px_721 / @musashi_kdp summaries, Nov 2026). Thesis: harness is the neutral layer
above agents — agents inherit your context, coordinate and work together in one UX.

**Recurring themes in his feed (all read from public mirrors — x.com itself is blocked
from this VM, so tweets were verified via twiscan.com / instalker.org mirrors + X
snowflake timestamps, NOT by guessing):**

1. **Decentralized HF** — "I'm begging all of the talent we have left in crypto. PLEASE
   build a decentralized HF" (12 Nov 2026, twice + follow-up offering bankr team
   support, "DMs open!"). **TAKEN by the rival — do not duplicate.**
2. **Cheap / accessible inference** — June harness post (above) + November retweet of
   @mfranz_on: "A decent local AI setup is about $10k which is too expensive for many
   people. We should use our knowledge and our tokens to improve the inference engines
   for lower end hardware, making local AI accessible to everyone." + ZABAL/agentic
   bootcamp teaching: cheap-model-for-cheap-task, OpenRouter, x402/Router402
   pay-per-inference (documented in bettercallzaal/zaoos repo, commit 06744e7).
3. **On-chain agent finance (THE TAKE — our anchor):** November 2026 thread on
   agentic commerce, read verbatim from his public profile mirror
   (https://www.instalker.org/saltorious1):
   > "I don't understand this take. Open AI adds cards so that agents can what, buy shit
   > on Amazon? IMO that's one of the least interesting things agents with money can do.
   > The landscape of interesting financial actions an agent can take is still on chain,
   > we just have to keep building it"
   > Follow-up: "That's super fair. However my original point was giving agents
   > effectively a prepaid card is not all that interesting. People are going to — and
   > already do likely just tell their agents to go out and make money *legally*. I believe
   > there's still more opportunity and less barriers to entry to do this on chain than
   > with a card"
   Corroboration: "Lmao, find me a better on chain agent. I dare you" (bankr); guest
   speaking on on-chain index-token empires ($BGLE / EmpireBuilderHQ).
4. **Collaborative video creation with AI** (18 Oct 2026 post, status
   2111936148658602406) — a demo share, not a thesis. Not used.

**What we could NOT verify:** the two rival-cited tweets (2120988266384015697,
2120910807013675099) are not on twiscan ("Tweet not found") and X's syndication
endpoint returns `{}` without a token — their TEXT is unverified by us (only their
existence + timestamps via snowflake, which match the rival's "12 November" claim).
Our draft does not depend on them. The agentic-commerce posts have no exact status
IDs recoverable from the mirror (links truncated) — cited via the instalker profile
URL + exact quoted words.

## 4. Our idea — THE $10 ON-CHAIN AGENT

**Title:** "The $10 On-Chain Agent: make money legally, without a card"
**Proposed reward:** 0.015 ETH (suggested only; unfunded draft)
**Chain:** Base, open bounty, album `ai`

**Why this wins against the rival:**
- It is his **freshest, most argumentative take** (November thread, argued twice in a
  back-and-forth) — "a take he'd love to see tested". The bounty IS the test.
- It is **maximally distinct** from the rival's infrastructure drill (agent finance vs
  model-distribution resilience) — the two entries do not compete on the same axis.
- It serves **bankr, the ecosystem he works in and promotes daily** ("find me a better
  on chain agent. I dare you") — the deliverable is a public, repeatable demonstration
  of bankr's core thesis, not a generic infra test.
- It is **creative where the rival is safe**: an agent DOING finance, not a tool for
  finance. The bounty asks for the most CREATIVE idea.
- It is **completable by anyone** (any agent with $10 USDC + a Base wallet), fully
  falsifiable (every decision + tx logged in public, rubric-scored), and honest about
  being an interpretation, not an endorsement.

**Full draft text:** see `DRAFT-BOUNTY.md` (the exact text to publish on the ideas board).

## 5. Criterion-by-criterion evaluation (bounty 565's own rules)

| Requirement (from bounty text) | Verdict |
|---|---|
| Read @saltorious1's X feed | ✅ PASS — profile + ~15 posts read via public mirrors; themes documented in §3 with exact quotes, IDs, snowflake dates. |
| Something he keeps coming back to / a take to test / a running joke | ✅ PASS — the agentic-commerce take is argued twice in November + echoes his bankr/harness work since June. |
| A bounty someone could actually complete | ✅ PASS — any agent with $10 USDC on Base can run it; no waitlist, no special access, no GPU, no new token. |
| What to do + what counts as proof | ✅ PASS — 5 exact steps, proof list, judging rubric with weights (40/30/30), eligibility gate. |
| Publish as a public bounty draft on poidh ideas board | ⏳ PENDING — draft text ready (`DRAFT-BOUNTY.md`); publication needs Dhika's approval of contents + a wallet signature (EIP-191 personal_sign; see §7). |
| Claim description carries the direct draft link | ⏳ PENDING — placeholder CID in the payload until the draft is published; then the real `https://poidh.xyz/d/<CID>` goes in (see `CLAIM-PAYLOAD.md`). |
| Tell which post/theme inspired it + why he'd fund it | ✅ PASS — in the claim description (commerce thread + harness corroboration + bankr fit). |
| Ideally screenshot the tweet as claim image | ⏳ PENDING — browser screenshot step (§7); the claim image will be the commerce-thread tweet (or, if X is unreachable in the browser, the instalker mirror render of it — flagged honestly in the claim). |
| Bonus: post draft link on X tagging @saltorious1 | ⏳ OPTIONAL — needs an X account post; parent/Dhika decision. Not required to qualify. |
| Most creative, saltorious-aligned idea | ⚠️ JUDGMENT CALL — ours is the more creative + more bankr-aligned entry; the rival's is the more rigorous infra spec. The call belongs to the issuer (0x10fc...). No way to guarantee it; the draft is written to maximize this axis. |
| No outreach / signup / purchase / private data | ✅ PASS — research only; no contact with Saltorious, no signup, no payment. |

## 6. Risks (honest assessment)

1. **The issuer is not Vireo, and the rival IS Vireo.** The 565 issuer (0x10fc...) is
   unknown; the rival claim is authored by Vireo, the platform's own agent. If the
   issuer is close to Vireo, the rival may have a home-field advantage. Mitigation:
   our entry wins on creativity + bankr-alignment, the two axes the bounty text names.
2. **Real money in the bounty design.** The draft asks entrants to risk $10 of their own
   USDC. The draft constrains it hard (no leverage, no new token, no MEV, full logs,
   $10 cap, "only use funds you can afford to lose"). A reviewer could still dislike
   money-at-risk designs. The $10 cap + rules are the mitigation; the design is the
   point of the take being tested.
3. **"Interesting" is partly subjective.** The rubric (40/30/30) + eligibility gate
   constrain it, but the final ranking needs judgment. Same is true of the rival's
   "easiest independently repeatable recovery" tie-breaks.
4. **Draft publication needs a signature.** EIP-191 personal_sign from the creator
   wallet. baw REJECTS personal_sign (error 351817) — the parent must find the signing
   path (Dhika's wallet app, or the poidh website flow in the browser). Without the
   draft published, there is NO valid claim (the bounty requires the draft link).
5. **The claim image tweet may be hard to screenshot.** x.com is blocked from this VM's
   text fetch; the parent's live browser may reach it (as it did for Upwork in 1549).
   Fallback: screenshot the instalker mirror render of the thread, labeled honestly.
6. **Prize is small:** 0.0033 ETH (~$5.84; net ~$5.69). Claim gas ~$0.022. Worth it for
   the win + precedent, same logic as 1549.

## 7. Claim checklist (for the main agent, after Dhika's yes)

- [ ] Dhika approves the draft contents in `DRAFT-BOUNTY.md` (publication is public).
- [ ] Publish the draft: `prepare_save_draft` (MCP https://poidh.xyz/api/mcp, or the
      poidh.xyz website "save as draft" flow) → sign the exact EIP-191 message →
      `save_draft` → record the real `https://poidh.xyz/d/<CID>` URL. Creator: msbrew
      `0xd4866480a0A9c94D1176865d7C63867632f785C6`; amount `"0.015"`; chain `base`;
      isOpenBounty `true`; album `ai`. Message expires in 600s — sign immediately.
- [ ] Replace the placeholder CID in `CLAIM-PAYLOAD.md` + `claim-args.json` with the real
      CID, rebuild calldata, re-run eth_call simulation + estimateGas (offsets shift only
      if the CID length differs from 59 chars).
- [ ] Dated screenshot of the commerce-thread tweet (browser) → PNG into the proof repo.
- [ ] Create public repo `gmlokie/poidh-1565-proof` + upload screenshot PNG + this
      SUBMISSION.md; verify the raw.githubusercontent.com URI returns HTTP 200 image/png.
- [ ] (Optional, bonus points) Post the draft link on X tagging @saltorious1; add the X
      post link to the claim description if done.
- [ ] Dhika tops up msbrew Base ETH (see `CLAIM-PAYLOAD.md`: **0.00002 ETH** recommended).
- [ ] Dhika's explicit yes for the Base mainnet claim tx (preview first, per mainnet rule).
- [ ] Claim via baw `contract-call` preview (set --gasLimit explicitly near the estimate,
      per the 1549 lesson) → sign → broadcast → verify receipt + ClaimCreated event.
- [ ] Re-verify at claim time: bounty still OPEN, still only 1 rival claim.

---
*Prepared by research subagent, 2026-11-15 ~07:30 WIB. Research only — no draft published,
no claim, no contact with Saltorious, no signup, no payment.*
