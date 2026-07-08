# Boundless documentation: writing guidelines

This doc is for **participants, organizers, and normal users**, not developers. Keep language clear, confident, and human.

---

## 1. Voice & tone

**Voice (consistent everywhere):**

- **Clear, not clever:** Say "You'll receive payment" not "Your wallet will be credited with the corresponding USDC amount."
- **Confident, not condescending:** Assume intelligence; explain complexity when it matters.
- **Human, not robotic:** Use "you" and "your"; avoid passive voice.

**Tone by section:**

| Section           | Tone                | Example                                      |
|-------------------|---------------------|----------------------------------------------|
| Getting Started   | Encouraging, friendly | "Let's get you set up. This takes about 5 minutes." |
| Concepts          | Educational, patient  | "Escrow might sound complex, but it's actually simple..." |
| How-To Guides     | Directive, efficient  | "Click **Create Bounty.** Fill in the title and description." |
| Reference         | Precise, factual     | "Contributor tier: 500–1,999 points. Unlocks more bounties." |
| Troubleshooting   | Reassuring, helpful   | "Don't worry, this is fixable. Here's what to do..." |

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
- Hide important info in long paragraphs; use callouts.

---

## 4. Callouts (Mintlify components)

Use these consistently:

| Intent           | Mintlify component | Use for |
|-----------------|--------------------|--------|
| Success / done  | `<Check>`          | "Your bounty application was submitted!" |
| Important / warning | `<Warning>`     | "Applications cost 1 Credit. Make sure you have at least one." |
| Critical / security | `<Warning>`     | "Never share your password or account recovery details. Boundless support will never ask for them." |
| Pro tip         | `<Tip>`            | "Apply early; competition is often lower." |
| Learn more / concept | `<Info>`       | "New to escrow? Read [Escrow and human review](/concepts/escrow-and-human-review)." |
| Note            | `<Note>`           | Supplementary info, safe to skip. |

Example:

```mdx
<Check title="Done when">
  You can log in and see your profile.
</Check>

<Warning title="Important">
  You'll spend 1 Credit when you apply. Check your balance first.
</Warning>

<Tip title="Pro tip">
  Complete your profile before applying; projects review it.
</Tip>

<Info title="Learn more">
  [Escrow and human review](/concepts/escrow-and-human-review)
</Info>
```

---

## 5. Product alignment

- **Currency:** All payments settle in **USDC** on Stellar. Balances show in USD. Never say XLM.
- **Credits:** The platform currency, used **only for bounties** (to apply and submit). Never say "Spark" or "Power Cell".
- **Bounty modes:** A mode is an **entry type** (Open, Application light, Application full) combined with a **selection** (single claim, competition). Backend: `entryType` (`OPEN`, `APPLICATION_LIGHT`, `APPLICATION_FULL`) and `claimType` (`SINGLE_CLAIM`, `COMPETITION`). A competition with more than one prize tier is "multiple winners". Do not say "Pick" or "Showdown".
- **Crowdfunding in the app:** Called **Projects**; URLs: `/projects`, `/projects/[slug]`.
- **Main site:** [www.boundlessfi.xyz](https://www.boundlessfi.xyz). Support: support@boundlessfi.xyz. Discord: https://discord.gg/cNabHsV7PN.
- **Wallets:** A **Boundless wallet** is managed for the user (platform holds the balance; no seed phrase). An **external wallet** (e.g., Freighter) is self-custody. **Passkey** sign-in is **planned for the future**; don't document it as current.
- **KYC:** Done via [Didit](https://didit.me/). **Withdrawing funds requires KYC** (withdraw to an external wallet, then convert on an exchange).
- **Escrow:** Runs on **Boundless's own Soroban smart contracts** on Stellar. The framing is "on-chain mechanics meet human review", never "trustless".
- **Cashing out:** Converting USDC to local currency is done on an **exchange**, not inside Boundless. Off-ramping is not a platform feature.
- **Live today:** All four pillars are browsable; bounties have the fullest apply/submit flow. Some organizer and detail screens are still rolling out.

---

## 6. Links

- **Internal:** Root-relative, no extension: `/start-here/create-your-account`.
- **External:** Full URL; they open in a new tab.
- **App links:** Use production when possible: `https://www.boundlessfi.xyz/projects`, etc.
- **Platform backlinks:** Include links to the main platform ([Boundless](https://www.boundlessfi.xyz)) in "Need help" sections and where users would go to sign up, browse hackathons, or browse projects. Use `https://www.boundlessfi.xyz`, `https://www.boundlessfi.xyz/hackathons`, `https://www.boundlessfi.xyz/projects` as appropriate.
- **Punctuation:** Do not use em dashes (—). Use commas, colons, or semicolons instead.
