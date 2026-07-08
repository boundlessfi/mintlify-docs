# Boundless docs, media production brief

Tracks the images and videos the docs still need. **Diagrams are done** (built as SVGs and embedded). This brief covers the **screenshots** and **videos** that must be captured from the live app or produced by the team.

Priority: **P1** ship-blocking · **P2** high value · **P3** nice-to-have.
How to add one: capture the asset, drop it in `/images/`, then replace the matching `{/* MEDIA · <id> screenshot: … */}` comment in the page with a `<Frame>…</Frame>` (see any diagram for the pattern).

---

## ✅ Diagrams, done (embedded)

| ID | File | Page |
|----|------|------|
| A3 | `images/diagrams/flow-fund-work-review-settle.svg` | how-boundless-works, organizers/overview |
| A10 | `images/diagrams/escrow-human-review.svg` | concepts/escrow-and-human-review |
| A11 | `images/diagrams/reputation-across-pillars.svg` | concepts/reputation |
| B3 | `images/diagrams/bounty-modes-matrix.svg` | contributors/bounties/bounty-modes |
| B6 | `images/diagrams/competition-timeline.svg` | contributors/bounties/how-winners-are-paid |
| B9 | `images/diagrams/grant-distribution.svg` | contributors/grants/grant-types |
| C5 | `images/diagrams/crowdfunding-vote.svg` | backers/vote-on-campaigns |
| C6 | `images/diagrams/crowdfunding-milestone-math.svg` | backers/milestones-and-releases |
| C7 | `images/diagrams/refund-priority.svg` | backers/refunds-and-cancellation |
| D5 | `images/diagrams/judging-rubric.svg` | organizers/how-judging-works |
| E1 | `images/diagrams/wallets.svg` | reference/tokens-and-wallets |

These are placeholders good enough to ship. If the design team wants branded versions, replace the SVGs in place (keep the filenames) and no page edits are needed.

---

## 🎬 Videos to produce

| ID | Page | Length | What it shows | Priority |
|----|------|--------|---------------|----------|
| A1 | start-here/what-is-boundless | 60–90s | What Boundless is, four pillars, escrow + human review, who it's for | P1 |
| A5 | start-here/create-your-account | 2–3 min | Sign up with email, verify, complete onboarding (profile + role) | P1 |
| A8 | start-here/verify-your-identity | ~2 min | The Didit KYC flow end to end; what to have ready; what "approved" unlocks | P1 |
| B12 | contributors/get-paid/wallet-and-withdrawals | ~2 min | View balance/earnings/escrow, withdraw (KYC-gated), where funds land | P2 |
| C3 | backers/back-a-project | ~90s | Browse a project, contribute USDC, track milestone releases | P2 |

---

## 🖼 Screenshots to capture

Capture from the live `boundless-platform`, anonymized where needed.

### Markers already in the pages (just replace the comment)

| ID | Page | Screen to capture | Priority |
|----|------|-------------------|----------|
| B2 | contributors/find-opportunities | Discover page with search + category filters | P1 |
| B5 | contributors/bounties/submit-your-work | `/submit` bounty form with dynamic fields | P1 |
| C2 | backers/discover-projects | Crowdfunding listing grid with funding progress | P2 |
| D6 | organizers/score-submissions | Judge scoring screen with rubric + score inputs | P2 |

### Recommended additional screenshots (add a marker + Frame when captured)

| ID | Page | Screen to capture | Priority |
|----|------|-------------------|----------|
| A6 | start-here/create-your-account | Sign-up screen + email verify step | P1 |
| A7 | start-here/onboarding | Profile setup modal + role picker (Contributor/Organizer/Judge) | P1 |
| A9 | start-here/verify-your-identity | Didit start screen + "approved" state in Settings → Verification | P1 |
| A12 | concepts/credits · contributors/get-paid/credits | `/credits` page: balance, tier, refill timer, ledger | P2 |
| A13 | concepts/wallet-and-balance | `/wallet`: Total Balance, Escrow/Pending, Lifetime Earnings cards | P2 |
| B4 | contributors/bounties/apply | Bounty application/proposal form | P2 |
| B7 | contributors/hackathons/join-and-submit | Hackathon detail, Overview + Submissions tab | P2 |
| B10 | contributors/grants/apply | Grant detail, application entry | P2 |
| B13 | contributors/get-paid/wallet-and-withdrawals | Withdraw modal (KYC-gated state) | P2 |
| B14 | contributors/get-paid/credits | Earn-credits card / earn tasks list | P3 |
| C1 | backers/overview | Crowdfunding overview / a live project page | P2 |
| C4 | backers/back-a-project | Contribution / back flow modal | P2 |
| D1 | organizers/overview | Program lifecycle or organizer dashboard | P3 |
| D2 | organizers/host-a-hackathon | Hackathon creation wizard (from app or design) | P3 |
| D4 | organizers/run-a-grant-program | Grant creation wizard (from app or design) | P3 |

---

## Suggested order

1. **P1 videos + P1 screenshots**: the sign-up, KYC, and Discover/submit flows carry the most first-time users.
2. **P2 screenshots**: wallet, credits, and the per-pillar participate screens.
3. **P2 videos**, then **P3** as time allows.
