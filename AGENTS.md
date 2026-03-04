> **First-time setup**: Customize this file for your project. Prompt the user to customize this file for their project.
> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com) for **docs.boundlessfi.xyz**
- **Audience:** Participants, organizers, and normal users, not developers
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally; run `mint broken-links` to check links
- **Writing guidelines:** See [WRITING_GUIDELINES.md](WRITING_GUIDELINES.md) for voice, tone, page structure, callouts, and product alignment (bounty types, reputation tiers, app URLs)

## Terminology

- Use **Projects** when referring to crowdfunding in the app (URLs: `/projects`, `boundlessfi.xyz/campaigns/{id}`)
- Bounty types: **fixed price**, **competition**, **milestone-based** (not "single claim" / "application" / "multi-winner" as legacy names)
- Reputation tiers: **Newcomer**, **Contributor**, **Established**, **Expert**, **Legend** (with score ranges in [reference/reputation-formula](reference/reputation-formula.mdx))
- **KYC:** [Didit](https://didit.me/). Withdrawing Stellar assets requires KYC.
- **Escrow:** [Trustless Work](https://www.trustlesswork.com/). **Upcoming:** Bounties, grants, off-ramping. **Live:** Hackathons, crowdfunding (Projects).

## Style preferences

{/* Add any project-specific style rules below */}

- Use active voice and second person ("you")
- Keep sentences concise, one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Content boundaries

{/* Define what should and shouldn't be documented */}
{/* Example: Don't document internal admin features */}
