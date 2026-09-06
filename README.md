# Refer & Earn

**Reacher Creator Portal · Feature Case**

A performance-based referral loop: creators invite other creators (and brands) and earn milestone bonuses funded by Reacher, paid only as the people they bring actually perform.

*Written by Aasritha Narayan · 8-hour design challenge, Sept 2026*

**Live links:**
- 🔗 [Full app](https://claude.ai/code/artifact/7730eef0-b30d-40c7-8dc9-d21ff04b3cd0) — the whole Creator Portal (Home, Brands, Campaigns, Ads Studio, Earnings, Profile) with Refer & Earn built in as a native screen
- 🔗 [Refer & Earn screen only](https://claude.ai/code/artifact/fd23cb92-f119-45eb-b1cf-b4b3a47317d5) — just the feature, for a faster look
- 🔗 [This write-up, as a designed page](https://claude.ai/code/artifact/0fb0e4a8-e5bc-40fb-b09f-4265708784fb)

**How to find it in the app:**
1. Open the full app link above — it loads on the Home screen.
2. Tap the avatar, top left (next to your handle and tier).
3. On the Profile screen, tap **Refer & Earn** — the first row under your name, next to your TikTok Shop level and rate settings.

---

## The insight

Creators aren't loyal to affiliate tools the way they're loyal to a brand or a following. They're commercial operators who go where the economics and the deal flow are best, and they multi-home across two or three platforms at once rather than fully switching. That means the fight for Reacher isn't "get creators to delete Trybe." It's **get Reacher into rotation, and make it the app they invest their attention in**.

Two things shape how that happens:

- **Creators trust other creators, not cold outreach.** A creator fielding 20 brand DMs a day tunes most of them out; a personal invite from a peer who's already getting paid on the platform carries real weight. The best acquisition channel for a creator tool is the creators already on it.
- **The creator economy is visibly anxious about anything that smells like MLM recruiting.** "Refer people, get paid" is a mechanic the industry associates with pyramid structures almost by reflex. A referral feature that pays a flat bounty for a signup, or that could plausibly be read as taking a cut of the person you referred, will get side-eyed by exactly the audience it's meant to win over.

Both point the same direction: the referral loop has to be built on *real, ongoing performance*, not a signup bounty, and the trust framing has to be explicit and on-screen, not just in the terms.

## The competitive gap

TikTok Shop already runs its own native creator referral program, which is the clearest evidence this lever works, and the clearest gap to build into. Per TikTok Shop's own seller documentation, the program is an **invite-only pilot**: an invitee has to sign up, post one shoppable video, and land one qualifying sale, and the inviter's reward for all twenty possible invitees is paid **once, in a lump sum, after the whole campaign period ends**. There's no running balance, no visibility mid-cycle, and it can be switched off between pilots.

Euka, the closest creator-facing competitor with a shipping mobile app, already has leaderboard-based contests as a retention hook, so gamified ranking alone is table stakes, not a wedge. Trybe is the platform most often cited as viral in the creator community, but that virality reads as organic word-of-mouth about deal quality; there's no public evidence it has engineered peer referral into the product itself.

| Mechanic | TikTok Shop (native) | Euka | Reacher: Refer & Earn |
|---|---|---|---|
| Availability | Invite-only pilot | Always-on | **Always-on** |
| What triggers a reward | One sale from the invitee | Contest placement | **4 real milestones over time** |
| When it's paid | Lump sum, after campaign ends | Per contest | **As each milestone lands** |
| Visible mid-cycle? | No | Yes (leaderboard) | Yes, live crew progress |
| Funded by | TikTok Shop | Euka / brand pool | Reacher, never the invitee |

## The feature, and why it wins

### Refer & Earn

Creators get a personal link and invite other creators (or brands) into Reacher. Every invite is tracked against a milestone ladder, capped at **$475 per referred creator**:

1. **They join** (tracked, not paid) — signs up with the referrer's link. This step exists so the referrer sees momentum immediately, without implying a signup bounty.
2. **Posts a first video: +$25** — the first real signal the invitee is actually using the platform.
3. **Reaches $1,000 GMV: +$150** — the invitee is now a genuine earner, not a stub account.
4. **Gets ad-funded by a brand: +$300** — the invitee has reached Reacher's highest-trust tier, where a brand pays to run their content as an ad.

A parallel track pays **$500** when a referred brand runs its first campaign, and the top three referrers each cycle (surfaced against the app's existing Climb-tier system) unlock a shared crew bonus, folding the loop into a system creators already check instead of bolting on a new one.

> "Paid by Reacher when a creator you bring hits real milestones. Never a cut of their earnings."
>
> — on-screen trust line, always visible on the Refer & Earn screen

**Why it attracts new creators:** it turns existing creators into the acquisition channel, using the exact skill they already have: convincing an audience to act on a personal recommendation. Because the payout is bigger and more legible than TikTok's own lump-sum pilot, and clearly not a pyramid, a creator has a genuine, defensible reason to tell a peer "you should be on Reacher," something no amount of paid UA or cold outreach can buy at the same trust level.

**Why it converts creators away from other tools:** multi-homing means the win isn't exclusivity, it's attention share. A referrer has a direct financial stake in their invitee's success on Reacher specifically: coaching them to post, to grow GMV, to get ad-funded, which pulls both people deeper into Reacher's own workflows (Upload, Ads Studio, tier progression) rather than a competitor's. It's retention through social investment, not a lock-in wall.

## What I built

Refer & Earn as a fifth screen inside Reacher's actual Creator Portal prototype, not a mockup layered on top. It's pushed from a new row on the Profile screen and built entirely from the app's real design tokens, shared UI kit, icon set, and CSS, so it reads as native rather than appended.

- Hero stat, copyable referral link, black "Invite creators" CTA, and the always-visible anti-pyramid trust card.
- The 4-step milestone ladder, each paid step explicitly tagged "Milestone-paid."
- A Creators / Brands toggle. The Creators pane holds six referred creators at varied real stages: two maxed out and ad-funded, two mid-pipeline awaiting ad review, one early with a $-to-next-milestone nudge, one just joined, each with a four-segment progress track and a plain-language next step.
- A referral leaderboard tied to the app's existing Climb-tier system, with the crew bonus for the top three.
- The Brands pane: the $500 brand-referral explainer and one pending brand under review.

## What I'd do next

Given the 8-hour scope, this stops at a fully designed and interactive front end on mock data. The next real increments, in order:

- **Wire it to real milestone events**: GMV thresholds, video posts, and Ads Studio approvals already exist as state elsewhere in the app; this needs to listen to them instead of hard-coded rows, plus the same eligibility guardrails TikTok's own program uses (invitee must be genuinely new, self-referral blocked).
- **Build the invitee's side.** Everything here is the referrer's view. The next screen is the "you were invited by @alex.rivera" welcome moment for the person joining. That's half the loop and currently missing.
- **Proactive nudges** when a referred creator is one step from a milestone, so referrers actually go coach them. The mentorship dynamic only works if it's pushed, not just visible on pull.
- **Tune the numbers against real data** once live: the $475 cap, the four milestone weights, and whether brand referral needs a lighter first pass before opening past manual review.

## Sources

1. [TikTok Shop Creator Referral Program](https://seller-us.tiktok.com/university/essay?knowledge_id=4068323947153166&lang=en) — seller-us.tiktok.com/university
2. Euka Creator: [App Store listing](https://apps.apple.com/us/app/euka-creator/id6757208879), [G2 reviews](https://www.g2.com/products/euka-ai/reviews)
3. [Reacher's existing brand-side positioning](https://www.reacherapp.com/) — reacherapp.com
4. Creator commercial-operator dynamics and commission ranges: TikTok Shop affiliate marketing research, 2026
5. Creator-economy MLM-structure perception: general creator-economy commentary, 2026
