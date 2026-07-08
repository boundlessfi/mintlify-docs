# Boundless Documentation, Rebuild Plan

> A from-scratch information architecture for the Boundless end-user docs, grounded in
> what is **actually live** on `boundless-platform` (not the old/aspirational docs).
> Audience: **Contributors, Backers, Organizers, Judges**: end users, not developers.

---

## 0. Ground truth (what this plan is based on)

Verified against `boundless-platform/src` (the live product) and `notion-docs/` (the
authoritative product spec). The current mintlify docs contain several claims that are
now wrong. **Corrections baked into this plan:**

| Old docs said | Reality (source of truth) | Action |
|---|---|---|
| Payments are in **XLM** | Payments settle in **USDC** on Stellar; wallet shows a USD balance | Replace all XLM references with USDC |
| "**Trustless** escrow" everywhere | Brand is **"on-chain mechanics meet human review"**: escrow enforces, humans decide | Drop "trustless"; use "on-chain escrow + human review" |
| Credits = "**Spark**" / "Power Cells" | Live UI calls it **"Credits"** (internal icon is `SparksIcon`, never shown as "Sparks") | Use **Credits** only |
| Bounties/Grants "**coming soon**"; Hackathons + Crowdfunding live | **All four pillars are live to browse.** Bounties has the fullest flow (apply + submit) | Re-baseline live status (below) |
| **Off-ramping** (XLM→fiat) pages | Off-ramp is **not a platform feature** at v1; users convert USDC via exchanges | Remove off-ramp pages; one short reference note instead |
| KYC via Didit | Confirmed: **Didit**, at `/settings/verification`, gates withdrawals | Keep Didit |

### Live status per pillar (from `boundless-platform`)

| Pillar | Browse/discover | Detail page | Participate on-platform | Notes |
|---|---|---|---|---|
| **Bounties** | ✅ Live | ✅ Full (all tabs) | ✅ **Apply + Submit** live | Reference implementation; six modes |
| **Hackathons** | ✅ Live | ✅ Full (all tabs) | ⚠️ No public apply/submit route | Registration/submission managed server-side / off-platform for now |
| **Grants** | ✅ Live | ✅ Core tabs | ⚠️ Some detail tabs are "coming soon" | Detail wired against backend; advanced tabs pending |
| **Crowdfunding** | ✅ Live | ✅ Core tabs | ✅ Backing live; ⚠️ some tabs pending | Community voting + milestone releases |

**Organizer program-creation is self-serve**: the flows exist, but the UI is still being
designed and rolled out. So "Organizers & Judges" docs describe the real self-serve model and
mark each flow **"UI rolling out"** where the screen is not live yet, rather than framing it as
contact-us-only.

---

## 1. Navigation model, role-first, live-first

Five top-level tabs. Roles mirror the platform's own onboarding role picker
(Contributor / Organizer / Judge) plus Backer. Live surfaces lead; forthcoming surfaces are
badged, never hidden.

| Tab | Who | Job |
|---|---|---|
| **Start Here** | Everyone | Understand Boundless, create an account, learn the shared concepts |
| **For Contributors** | Builders / applicants | Find & win bounties, hackathons, grants; get paid |
| **For Backers** | Crowdfunding supporters | Discover, vote on, and back projects |
| **For Organizers & Judges** | Program runners & judges | How programs & judging work (creation rolling out) |
| **Help & Reference** | Everyone | Troubleshooting, glossary, fees, tokens, security, FAQ, support |

---

## 2. Full page tree

Legend: **[LIVE]** live & self-serve · **[BROWSE]** live to view, participation limited · **[SOON]** documented, marked coming soon · **[NEW]** page to write · **[REUSE]** adapt an existing page.

### Tab 1, Start Here
```
Introduction
  ├─ What is Boundless               [REUSE overview.mdx, rewrite money/trustless]  🎬 A1  🖼 A2
  ├─ How Boundless works             [REUSE how-boundless-works, Fund→Work→Review→Settle]  📊 A3
  └─ Choose your path (role router)  [NEW]  🖼 A4

Get set up
  ├─ Create your account             [REUSE quick-start]  🎬 A5  🖼 A6
  ├─ Onboarding: profile & role      [NEW, 2-step: profile setup + Contributor/Organizer/Judge]  🖼 A7
  └─ Verify your identity (KYC)       [REUSE complete-kyc-verification, Didit]  🎬 A8  🖼 A9

Core concepts
  ├─ Escrow & human review           [REUSE trustless-escrow-explained, RENAME, drop "trustless"; custom Soroban contracts]  📊 A10
  ├─ Reputation (your track record)  [REUSE reputation-system]  📊 A11
  ├─ Credits                         [REUSE power-cells, RENAME to Credits; full model in §4]  🖼 A12
  ├─ Your wallet & balance           [REUSE passkey-wallets + set-up-your-wallet, USDC]  🖼 A13
  └─ Fees                            [REUSE fee-structure, add real numbers]
```

### Tab 2, For Contributors  *(largest live surface)*
```
Overview
  ├─ Ways to earn                    [NEW, routes to the 3 pillars]  🖼 B1
  └─ Find opportunities              [NEW, discover/explore, search & filter]  🖼 B2

Bounties  [LIVE]
  ├─ Overview                        [REUSE bounties/overview]
  ├─ Bounty modes                    [REUSE four-claiming-models, the 6 modes: vetting × selection]  📊 B3
  ├─ Apply to a bounty               [REUSE applying-for-bounties, vetting/proposal]  🖼 B4
  ├─ Submit your work                [NEW, /submit flow, dynamic requirements]  🖼 B5
  └─ How winners are picked & paid   [NEW, reveal moment, tiers, ~30s settle]  📊 B6
  (drop lightning-rounds for now, concept is being revamped, will be revisited later)

Hackathons  [BROWSE]
  ├─ Overview                        [REUSE hackathons/overview]
  ├─ Join & submit                   [REUSE participating, note where registration happens]  🖼 B7
  ├─ Tracks, prizes & judging        [REUSE judging-system, participant view]  📊 B8
  └─ Post-event milestones           [REUSE post-event-milestones]

Grants  [BROWSE]
  ├─ Overview                        [REUSE grants/overview]
  ├─ Grant types & distribution      [REUSE grant-types, positions, % distribution]  📊 B9
  ├─ Apply for a grant               [REUSE application-process]  🖼 B10
  └─ Deliver milestones              [REUSE milestone-delivery + structure-grant-milestones]  📊 B11

Get paid
  ├─ Your wallet & withdrawals       [REUSE withdraw-funds, KYC-gated, USDC]  🎬 B12  🖼 B13
  ├─ Earn & spend Credits            [NEW, earn tasks, tiers, refill timer, ledger]  🖼 B14
  └─ Build your reputation           [REUSE build-your-reputation]
```

### Tab 3, For Backers  *(Crowdfunding)*
```
Overview
  └─ Crowdfunding on Boundless       [REUSE crowdfunding/overview]  🖼 C1

Discover & back
  ├─ Discover projects               [NEW, /crowdfunding listing]  🖼 C2
  ├─ Back a project                  [REUSE backing-campaigns, contribute in USDC]  🎬 C3  🖼 C4
  └─ Vote on campaigns               [REUSE community-validation, quorum 10 / 60% threshold]  📊 C5

How your money is protected
  ├─ Milestones & releases           [REUSE milestone-structure, dynamic math]  📊 C6
  └─ Refunds & cancellation          [NEW, pro-rata, partners refunded first]  📊 C7
```

### Tab 4, For Organizers & Judges
```
Overview
  └─ Running programs on Boundless   [NEW, the model; badge creation "Rolling out, contact us"]  🖼 D1

Run a program  [self-serve, some UI still rolling out]
  ├─ Host a hackathon                [REUSE hackathons/organizing, 7-step wizard model]  🖼 D2
  ├─ Post a bounty                   [REUSE creating-bounties, choosing a mode, setting credit cost]  📊 D3
  └─ Run a grant program             [REUSE grant-programs, distribution, milestones]  🖼 D4

Judging  [LIVE role]
  ├─ How judging works               [NEW, rubric, weighted criteria, AI Judging Assist]  📊 D5
  └─ Score submissions               [NEW, judge dashboard walkthrough]  🖼 D6
```

### Tab 5, Help & Reference
```
Get help
  ├─ Troubleshooting                 [NEW, payment delayed, KYC declined, can't submit, access]
  ├─ Disputes & moderation           [REUSE handle-disputes, rejection taxonomy, pause/flag]
  └─ Report a bug                    [REUSE report-a-bug]

Reference
  ├─ Glossary                        [REUSE glossary, align to canonical terms below]
  ├─ Fees                            [REUSE fee-structure, real numbers per pillar]
  ├─ Reputation formula              [REUSE reputation-formula]
  ├─ Tokens & wallets                [NEW, USDC, G-address, trustline, Boundless vs external wallet]  📊 E1
  ├─ Converting USDC to local currency [NEW, short: use exchanges; not a platform feature]
  ├─ Supported countries             [REUSE supported-countries, real list or Didit link]
  └─ Security & privacy              [REUSE security-and-privacy, add privacy/terms links]

FAQ
  ├─ General                         [REUSE faq/general]
  ├─ Payments & KYC                  [NEW]
  ├─ Bounties / Hackathons / Grants / Crowdfunding  [REUSE faq/*, correct XLM→USDC]

Support & community
  ├─ Contact us                      [REUSE support/contact-us]
  └─ Community                       [REUSE support/community]
```

---

## 3. Content to DELETE (starter-template boilerplate + wrong pages)

- `essentials/` (markdown, code, images, navigation, settings, reusable-snippets), Mintlify demo
- `ai-tools/` (cursor, claude-code, windsurf), Mintlify demo
- `api-reference/` (create, get, delete, webhook, introduction), placeholder CRUD, no public API
- `development.mdx`, `quickstart.mdx` (superseded), `snippets/snippet-intro.mdx`
- `concepts/off-ramping.mdx` + `how-to-guides/convert-xlm-to-fiat.mdx`, off-ramp isn't a v1 feature (replace with the one short reference note)

---

## 4. Terminology standard (use these canonical names everywhere)

| Use | Not |
|---|---|
| **Credits** | Spark, Power Cell, Sparks |
| **USDC** (payments/balances) | XLM |
| **On-chain escrow + human review** | Trustless, trustless escrow |
| **Opportunity** (bounty/hackathon/grant listing) · **Project** (crowdfunding listing) | mixing the two |
| **Mode** (vetting × selection), **Showdown**, **Pick**, **Reveal**, **Shortlist** | claiming models (rework) |
| **Track record / Reputation** | trust score, rating |
| **Settle / Settlement** (~30s payout) | payout processing |
| **Delegated Reviewer**, **Voter**, **Quorum** (10), **Threshold** (60%) | validator, moderator |
| **G-address**, **trustline**, **Boundless wallet** vs **external wallet** (Freighter) | wallet/seed-phrase talk |

**Confirmed fees** (penetration pricing, verify current before publish): Bounty **2.5%** (min $2), Hackathon **1.5%**, Grant **1.5%**/milestone, Crowdfunding **2.5%**/milestone (free under $1,000). Organizer pays for bounty/hackathon/grant; **builder pays** for crowdfunding.

### Credits model (verified in `boundless-nestjs/src/modules/credits`)

Credits are an off-chain currency used **only for Bounties**: you spend them to take part in a
bounty (applying to a bounty that requires an application, and submitting). They do not apply to
hackathons, grants, or crowdfunding.

- **Cost:** base **1 credit** per bounty action; an organizer can set a higher cost on their own bounty.
- **Balance cap:** **12** credits maximum, you can never hold more than this.
- **Welcome grant:** new users get **6** credits on first use, so a beginner can start right away.
- **Refill:** a **monthly reset** (not a top-up, no rollover) on the 1st of each month (UTC). Your
  balance is set back to your tier's refill amount. The wallet/credits page shows the next refill date.
- **Earn extra credits** (one-time, still capped at 12):
  - Complete your profile (name + bio + at least one skill) → **+2**
  - Connect GitHub → **+3**
  - Complete your first opportunity (a won/accepted bounty or hackathon, or an approved grant) → **+5**

**Tiers** are set by your on-chain reputation score and decide your monthly refill:

| Tier | Reputation | Monthly refill |
|---|---|---|
| Bronze | 0+ | 3 |
| Silver | 100+ | 5 |
| Gold | 400+ | 8 |
| Platinum | 1,000+ | 12 |

> These numbers are policy knobs in `credit-policy.ts` and may be tuned. Cite the behaviour, and
> note in the docs that exact amounts can change.

### Escrow (custom Soroban contracts)

Escrow runs on **Boundless's own Soroban smart contracts on Stellar**: not Trustless Work.
Reference contract addresses (for the escrow/reference page, not for step-by-step user tasks):

- `profile_contract`: `CD3KH4OE7HDHHHUYFX3U4L7NLIILMXAY6HM5FEH2UH6UBOKX4HDNE3PC`
- `events_contract`: `CCFVEGOQJEM47LRAJU2LHEK4KTL5VYN7AOGZ2HH2GNHAMXTILNMMJGQZ`

---

## 5. Media & asset plan

Every asset the docs need, so the design/video team can produce them. Priority: **P1** = ship-blocking for a good first release, **P2** = high value, **P3** = nice-to-have. Type: 🎬 video · 🖼 screenshot · 📊 diagram/illustration.

### Videos 🎬
| ID | Page | What it shows | Priority |
|---|---|---|---|
| A1 | What is Boundless | 60–90s: what Boundless is, four pillars, escrow + human review, who it's for | P1 |
| A5 | Create your account | 2–3 min: sign up with email, verify, complete onboarding (profile + role) | P1 |
| A8 | Verify your identity | 2 min: the Didit KYC flow end-to-end; what to have ready; what "approved" unlocks | P1 |
| B12 | Wallet & withdrawals | 2 min: view balance/earnings/escrow, withdraw (KYC-gated), where funds land | P2 |
| C3 | Back a project | 90s: browse a project, contribute USDC, track milestone releases | P2 |

### Screenshots 🖼 (capture from live `boundless-platform`, anonymized)
| ID | Page | Screen to capture |
|---|---|---|
| A2 | What is Boundless | Discover/explore page showing all four pillars |
| A4 | Choose your path | (illustration, not screenshot) role router cards |
| A6 | Create your account | Sign-up screen + email verify step |
| A7 | Onboarding | Profile setup modal + role picker (Contributor/Organizer/Judge) |
| A9 | KYC | Didit verification start screen + "approved" state in settings/verification |
| A12 | Credits | `/credits` page: balance, tier, refill timer, ledger |
| A13 | Wallet | `/wallet`: Total Balance, Escrow/Pending, Lifetime Earnings cards |
| B1 | Ways to earn | (illustration) three-pillar earn router |
| B2 | Find opportunities | `/discover` with search + category filters |
| B4 | Apply to a bounty | `/apply/bounties/[slug]` proposal form |
| B5 | Submit your work | `/submit/bounties/[slug]` dynamic submission form |
| B7 | Join & submit (hackathon) | Hackathon detail, Overview + Submissions tab |
| B10 | Apply for a grant | Grant detail, application entry |
| B13 | Wallet & withdrawals | Withdraw modal (KYC-gated state) |
| B14 | Credits | Earn-credits card / earn tasks list |
| C1 | Crowdfunding overview | Crowdfunding listing page |
| C2 | Discover projects | `/crowdfunding` grid with funding progress |
| C4 | Back a project | Contribution/back flow modal |
| D1 | Organizer overview | (illustration) program lifecycle |
| D2 | Host a hackathon | Hackathon organizer wizard (from admin/design if not public) |
| D4 | Run a grant program | Grant creation wizard (from admin/design) |
| D6 | Score submissions | Judge dashboard / scoring screen |
| E-misc | KYC/settings | settings/verification states |

### Diagrams & illustrations 📊
| ID | Page | What to illustrate |
|---|---|---|
| A3 | How Boundless works | **Fund → Work → Review → Settle** flow (the shared 4-step spine) |
| A10 | Escrow & human review | Lock in escrow → human gate (organizer/panel/reviewer/vote) → on-chain release |
| A11 | Reputation | One identity, four pillars, reputation compounds across surfaces |
| B3 | Bounty modes | 2×3 matrix: vetting (none/light/heavy) × selection (Pick/Showdown) |
| B6 | Winners picked & paid | Showdown timeline: submit (blind) → reveal → tiers → settle |
| B8 | Tracks, prizes & judging | Hackathon: tracks → weighted rubric → prize tiers |
| B9 | Grant distribution | Positions (1/2/3) with % split summing to 100%, per-milestone amounts |
| B11 | Deliver milestones (grant) | Fixed milestone math: total × % / n; org signs each release |
| C5 | Vote on campaigns | Voting gate: quorum (10) + threshold (60%) → launch |
| C6 | Milestones & releases | Crowdfunding dynamic math: remaining escrow / remaining milestones |
| C7 | Refunds | Refund priority: partners first → builder residual last |
| D3 | Post a bounty | Decision tree: pick a mode for your work type |
| D5 | How judging works | Rubric → weighted criteria → scores → winners (AI Judging Assist summarizes) |
| E1 | Tokens & wallets | Boundless wallet vs external (Freighter); G-address + trustline for USDC |

---

## 6. Rollout phases

1. **Phase 1, Restructure & correct (ship fast).** New `docs.json` (5 role tabs), move/rename existing `.mdx` into the tree, delete boilerplate, global find-replace: XLM→USDC, drop "trustless", Spark/Power Cell→Credits. Ships with corrected existing content.
2. **Phase 2, Fill gaps.** Write the ~15 [NEW] pages; apply real fee numbers; add troubleshooting + Payments/KYC FAQ; confirm the ⚠️ open questions.
3. **Phase 3, Media.** Produce P1 videos + screenshots first (A1, A5, A8; core screenshots), then diagrams, then P2/P3.

---

## 7. Open questions, RESOLVED

1. **Credits mechanics**: ✅ Resolved. Spent only on Bounties (apply + submit), base 1 credit,
   cap 12, monthly reset by tier, welcome grant 6, earn tasks +2/+3/+5. Full model in §4.
2. **Organizer self-serve**: ✅ Self-serve. The flows exist; the UI is still being designed and
   rolled out. Tab 4 documents the real model and marks screens "UI rolling out" where not yet live.
3. **Escrow provider**: ✅ Custom Boundless Soroban contracts on Stellar (not Trustless Work).
   Contract addresses recorded in §4.
4. **Lightning rounds**: ✅ Parked. The concept is being refined and revamped; leave it out of the
   docs for now and revisit later.

### Still worth confirming during writing

- **Hackathon/grant participation**: the public platform has no apply/submit route for these two
  yet (only browse + detail). Confirm where a user registers/submits today so the participant pages
  point to the right place (or badge them "UI rolling out" like the organizer flows).
