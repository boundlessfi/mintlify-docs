# Boundless docs audit: gaps and media opportunities

This audit summarizes what is lacking in the current documentation and where video guides, images, and other media would add the most value.

---

## Part 1: What is lacking

### 1. Content gaps

| Gap | Location | Recommendation |
|-----|----------|----------------|
| **API documentation** | Reference | The original structure had "API Documentation (future)". It is not in the current nav. Either add a placeholder page under Reference ("API documentation – coming soon") or leave until the API is ready. |
| **Supported countries list** | reference/supported-countries.mdx | Page says "check the app" but does not list countries. Add either a link to Didit's supported documents/countries, or a note that "A list of supported countries is available in the [Boundless app](https://www.boundlessfi.xyz) under account or verification settings." |
| **Fee structure numbers** | reference/fee-structure.mdx | No concrete amounts (e.g. "Creation fees: X Sparks or Y XLM"). Either add placeholder ranges when known or keep "check in-app" but add a sentence like "Typical fee types are listed above; exact amounts appear in the app before you confirm." |
| **Withdrawal flow** | How-to / Concepts | There is no dedicated "How to withdraw your Stellar assets" page. Users who want to withdraw (not off-ramp) may look for steps. Add a short how-to that points to KYC first, then in-app withdraw flow, or fold into "Complete KYC" + one paragraph in off-ramping. |
| **Troubleshooting** | Site-wide | No dedicated troubleshooting page. Consider adding one (e.g. "Troubleshooting" under How-To or Support) with: payment delayed, KYC rejected, can't submit, dispute not resolved, account access. |
| **Privacy policy / Terms links** | reference/security-and-privacy.mdx | Text mentions "privacy policy" and "applicable law" but there are no links. Add links to boundlessfi.xyz privacy and terms if they exist (e.g. /privacy, /terms). |
| **Organizer quick path** | Getting started | "I want to hire or run events" is only in overview/quick-start. Consider a short "Organizer quick start" (hackathon + future bounties) that links to Organizing and Creating bounties. |

### 2. Consistency and copy

| Issue | Examples | Fix |
|-------|----------|-----|
| **Missing punctuation** | quick-start: "No blockchain experience required Boundless"; set-up-your-wallet: "for you no wallet"; complete-kyc: "compliance check the program"; faq/general: "the rest Boundless manages" | Add period or comma so sentences read correctly. |
| **Fee structure / reference** | reference/fee-structure.mdx: "**Creation fees** Fees for..." (no colon) | Use colons after bold labels where it improves scanability (e.g. "**Creation fees:** Fees for..."). |
| **"Set up your wallet" vs "Set up your account"** | Some module pages still say "Set up your wallet" in prerequisites | Prefer "Set up your account" and link to /how-to-guides/set-up-your-wallet (page title is "Set up your account and balance"). |
| **"Need help" vs "Related"** | Some pages have both, some only "Related" | Prefer "Need help?" when you want to surface Platform/Discord/Support; keep "Related" for doc links. Add "Need help?" to pages that only have "Related" where it fits. |

### 3. Depth and examples

- **Real-world examples:** Docs are mostly conceptual. Where helpful, add one-line examples (e.g. "Example: a campaign with three milestones: 30% at alpha, 40% at beta, 30% at launch"). Not every page needs this.
- **Screenshots and UI names:** No references to specific button labels or screens (e.g. "Click **Create project** in the dashboard"). Adding a few concrete UI references in the main flows (sign up, create campaign, back campaign, KYC) would help.
- **Judging / organizing:** Judging system and Organizing are clear but high-level. If the app has specific steps (e.g. "Add criteria in the Judging tab"), one or two concrete references would reduce guesswork.

### 4. Navigation and discovery

- **Overview vs index:** Home is `overview.mdx`. Ensure docs.json and any internal links use the same slug so the home page is discoverable and consistent.
- **Bounties/Grants (coming soon):** Nav and cards already label these. No change needed unless you want to collapse or de-emphasize them until launch.

---

## Part 2: Where to add video guides, images, and other media

### Video guides (high impact)

| Page / topic | Suggested video | Purpose |
|--------------|-----------------|--------|
| **Home (overview)** | "What is Boundless?" (1–2 min) | Platform overview: escrow, reputation, four modules, who it’s for. |
| **Quick start** or **Set up your account** | "Sign up and get started" (2–3 min) | Walk through sign-up, first login, where to find hackathons and projects. |
| **Complete KYC verification** | "Completing KYC with Didit" (2–3 min) | What to have ready (ID, selfie), what the flow looks like, what to do if something fails. |
| **Your first hackathon / Participating** | "How to join and submit to a hackathon" (3–4 min) | Find event, register, build, submit before deadline; optional team formation. |
| **Creating campaigns** | "How to create a crowdfunding campaign" (3–4 min) | Create project, set goal and milestones, launch; where funds go (escrow). |
| **Backing campaigns** | "How to back a campaign" (1–2 min) | Browse projects, choose amount, contribute; how to track milestones. |
| **Trustless escrow** or **How Boundless works** | "How escrow works" (1–2 min, can be animated) | Lock → verify → release; why it’s trustless; optional: Trustless Work in one sentence. |
| **FAQ (general)** | Short clips for top 3–5 questions | Optional: "What is Boundless?", "Do I need crypto?", "How do I get paid?" as 30–60 sec answers. |

### Images and screenshots (high impact)

| Page / topic | Suggested asset | Purpose |
|--------------|-----------------|--------|
| **Quick start / Set up your account** | Sign-up or welcome screen | Shows where to start and what "done" looks like. |
| **Set up your account** or **Wallets and accounts** | Dashboard or balance view (blurred if needed) | Shows "your balance" and where payouts appear. |
| **Complete KYC verification** | KYC flow (e.g. "Upload ID" or "Selfie" step, anonymized) | Sets expectations for Didit flow. |
| **Hackathons overview** or **Participating** | Hackathons list or event card | Where to find and choose events. |
| **Crowdfunding overview** or **Creating campaigns** | Projects/campaign list or single campaign page | What a live campaign looks like. |
| **Creating campaigns** | Create campaign form (goal, milestones) | Where to set goal and milestones. |
| **Organizing** or **Judging system** | Organizer view (e.g. submissions or judging tab) | What organizers see when managing events. |
| **Handle disputes** | Dispute or support flow (optional) | Where to open a dispute or find help. |
| **Off-ramping** / **Convert XLM to fiat** | Withdraw or off-ramp screen (when live) | Where to request withdrawal; reinforce KYC requirement. |

### Diagrams and illustrations (medium impact)

| Page / topic | Suggested asset | Purpose |
|--------------|-----------------|--------|
| **How Boundless works** or **Trustless escrow** | Escrow flow diagram | Visual: Lock → Verify → Release (you have ASCII; a simple diagram would be clearer). |
| **Reputation system** or **Reputation formula** | Reputation tier ladder | Newcomer → Contributor → Established → Expert → Legend with score ranges. |
| **How Boundless works** | Four modules (Bounties, Grants, Hackathons, Crowdfunding) | One diagram showing four pillars and "one account, one reputation". |
| **Crowdfunding / Milestone structure** | Milestone timeline | Example campaign: milestones on a timeline with % release. |

### Other media

| Type | Where | Purpose |
|------|--------|--------|
| **Callout with video embed** | Top of Quick start or Set up your account | Embed "Sign up and get started" so users see it immediately. |
| **Mintlify Video component** | KYC, Participating, Creating campaigns, Backing campaigns | Use Mintlify’s video component where available so videos are inline and not only linked. |
| **GIFs or short clips** | Key flows (e.g. "Click Create project → Set goal → Add milestones") | Optional: short screen recordings for power users. |

---

## Part 3: Priority summary

**Fix first (low effort)**  
- Punctuation and small copy fixes (quick-start, set-up-your-wallet, complete-kyc, faq/general).  
- Colons in reference/fee-structure.mdx.  
- Add privacy/terms links in Security & privacy if URLs exist.  
- Standardize "Set up your account" in prerequisites across modules.

**Add when possible (medium effort)**  
- Supported countries: link to Didit or clear "see in-app" note.  
- One "How to withdraw" section or short page (KYC + in-app steps).  
- Troubleshooting page with 5–10 common issues.  
- API documentation placeholder under Reference if you want it in nav.

**High impact (larger effort)**  
- One "What is Boundless?" video on the home/overview page.  
- One "Sign up and get started" video for Quick start or Set up your account.  
- One "KYC with Didit" video for Complete KYC verification.  
- One "Join a hackathon" and one "Create a campaign" video.  
- Screenshots for sign-up, dashboard/balance, hackathons list, campaign page, create campaign form.  
- One escrow flow diagram and one reputation-tier diagram.

Use this audit to plan content and media backlog; adjust priorities based on launch plans (e.g. bounties, grants, off-ramp) and support volume.
