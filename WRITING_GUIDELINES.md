# Boundless documentation — writing guidelines

This doc is for **participants, organizers, and normal users**—not developers. Keep language clear, confident, and human.

---

## 1. Voice & tone

**Voice (consistent everywhere):**

- **Clear, not clever:** Say "You'll receive payment" not "Your wallet will be credited with the corresponding XLM amount."
- **Confident, not condescending:** Assume intelligence; explain complexity when it matters.
- **Human, not robotic:** Use "you" and "your"; avoid passive voice.

**Tone by section:**

| Section           | Tone                | Example                                      |
|-------------------|---------------------|----------------------------------------------|
| Getting Started   | Encouraging, friendly | "Let's get you set up. This takes about 5 minutes." |
| Concepts          | Educational, patient  | "Escrow might sound complex, but it's actually simple..." |
| How-To Guides     | Directive, efficient  | "Click **Create Bounty.** Fill in the title and description." |
| Reference         | Precise, factual     | "Contributor tier: 500–1,999 points. Unlocks more bounties." |
| Troubleshooting   | Reassuring, helpful   | "Don't worry—this is fixable. Here's what to do..." |

---

## 2. Page structure

Use this structure on every page:

```markdown
# Page Title

> **TL;DR:** One-sentence summary of what this page covers.

## What You'll Learn
- Bullet 1
- Bullet 2
- Bullet 3

[Main content with clear headings]

## Next Steps
- Link to related page 1
- Link to related page 2

## Need Help?
[Discord] [Support Email] [Relevant FAQ]
```

---

## 3. Writing rules

**Do:**

- Use second person ("you," "your").
- Start with outcomes ("After this, you'll be able to...").
- Use examples.
- Break up text with headings, lists, tables.
- Link to related concepts inline.

**Don't:**

- Use jargon without defining it first.
- Assume technical knowledge (explain blockchain terms when needed).
- Write paragraphs longer than 4 lines.
- Use passive voice when active is clearer ("An admin will review your bounty" not "The bounty will be reviewed").
- Hide important info in long paragraphs—use callouts.

---

## 4. Callouts (Mintlify components)

Use these consistently:

| Intent           | Mintlify component | Use for |
|-----------------|--------------------|--------|
| Success / done  | `<Check>`          | "Your bounty application was submitted!" |
| Important / warning | `<Warning>`     | "Applications cost 1 Power Cell. Make sure you have at least one." |
| Critical / security | `<Warning>`     | "Never share your password or account recovery details. Boundless support will never ask for them." |
| Pro tip         | `<Tip>`            | "Apply during bounty windows—competition is often lower." |
| Learn more / concept | `<Info>`       | "New to escrow? Read [How Trustless Escrow Works](/concepts/trustless-escrow-explained)." |
| Note            | `<Note>`           | Supplementary info, safe to skip. |

Example:

```mdx
<Check title="Done when">
  You can log in and see your profile.
</Check>

<Warning title="Important">
  You'll spend 1 Power Cell when you apply. Check your balance first.
</Warning>

<Tip title="Pro tip">
  Complete your profile before applying—projects review it.
</Tip>

<Info title="Learn more">
  [Trustless escrow explained](/concepts/trustless-escrow-explained)
</Info>
```

---

## 5. Product alignment

- **Bounty types:** Fixed price, competition, milestone-based (backend: `fixed_price`, `competition`, `milestone_based`).
- **Bounty windows:** Upcoming, active, closed (time-limited claiming).
- **Reputation tiers:** Newcomer (0–499), Contributor (500–1,999), Established (2,000–4,999), Expert (5,000–9,999), Legend (10,000+).
- **Crowdfunding in the app:** Called **Projects**; URLs: `/projects`, `/projects/[slug]`, share link `boundlessfi.xyz/campaigns/{id}`.
- **Main site:** [www.boundlessfi.xyz](https://www.boundlessfi.xyz). Support: support@boundlessfi.xyz. Discord: https://discord.gg/cNabHsV7PN.
- **Wallets:** Boundless currently **abstracts wallets** (platform holds user balance; no seed phrase or external wallet). **Passkey** sign-in/signing is **planned for the future**—don't document it as current. Use "account and balance" or "managed wallet" for today.
- **KYC:** Done via [Didit](https://didit.me/). **Withdrawing Stellar assets** from the platform **requires KYC** (withdraw to external wallet or, when available, off-ramp to fiat).
- **Escrow:** Powered by [Trustless Work](https://www.trustlesswork.com/) (non-custodial, milestone-based escrow on Stellar).
- **Upcoming features:** **Bounties**, **grants**, and **off-ramping** (XLM -> fiat) are upcoming. **Live today:** Hackathons, crowdfunding (Projects).

---

## 6. Links

- **Internal:** Root-relative, no extension: `/getting-started/quick-start`.
- **External:** Full URL; they open in a new tab.
- **App links:** Use production when possible: `https://www.boundlessfi.xyz/projects`, etc.
