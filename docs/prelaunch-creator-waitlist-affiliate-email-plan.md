# Pre-launch creator waitlist: affiliate bridge and email plan

Status: **Planned — not yet implemented** (November 12, 2026).

## Context and goal

SoundReach.me is preparing to launch its own music promotion marketplace. The creator waitlist currently has approximately 100 signups, but first-party paid campaigns depend on recruiting artists and funding campaigns. Rather than leaving interested creators idle, offer an optional way to apply to an existing third-party music campaign platform while SoundReach.me builds its own supply.

## Affiliate offer

- Invite waitlisted creators to apply to **Playlist Push** using SoundReach.me's affiliate/referral link (insert the verified URL before sending).
- Playlist Push independently reviews applicants; the owner reports that creators generally need **30,000+ followers** and must satisfy additional eligibility requirements. Verify the current rules before publishing.
- A click, application, acceptance, campaign completion, and referral commission are distinct events. Do not imply acceptance or paid work is guaranteed.
- SoundReach.me may earn referral compensation for qualifying activity under the affiliate program; disclose this clearly.
- Use **“affiliate link”** or **“affiliate referral”**, not “official partner,” unless a formal partnership is confirmed.
- The owner can inspect the affiliate dashboard for link visits and qualifying referrals, subject to the information the provider actually makes available. Do not imply access to applicants' private decisions or identities beyond that dashboard.
- Keep every creator on the SoundReach.me waitlist regardless of Playlist Push acceptance. The third-party application is optional and separate.

## Launch-period benefit for referred creators

**Recommended offer:** priority early access to SoundReach.me when it launches, potentially branded **Founding Creator** status, with priority consideration for the first available campaigns. This is a proposed benefit, not a launched feature or guarantee of campaign acceptance or earnings.

**Decision:** Do not promise permanent benefits, guaranteed payouts, or special campaign allocations until those rules and product capabilities are approved. The immediate benefit is the opportunity to apply to an existing platform without waiting for SoundReach.me's launch.

## Two email paths (both requested)

1. **Existing waitlist: one-time outreach.** Send a campaign to the approximately 100 current subscribers. Deduplicate addresses, honor opt-outs, record delivery and errors, and avoid re-sending the initial invitation to anyone already contacted.
2. **New waitlist signups: automatic email.** Trigger after a successful signup, preferably after confirmation of consent if double opt-in is used. Include waitlist confirmation, the optional affiliate opportunity, eligibility caveat, disclosure, and unsubscribe information. Make sends idempotent to prevent duplicates.

Both paths should use a shared email template and track: signup timestamp, consent source/status, invitation sent timestamp, provider message ID, delivery/bounce status, and opt-out status. Track referral clicks/conversions only where allowed and verifiable; do not assume affiliate dashboard data can be matched to an individual waitlist signup.

## Draft email

**Subject:** Your SoundReach.me early access update 🎵

Hey!

Thanks for joining the SoundReach.me waitlist. We're working toward launching in the next month or two, and we'll keep you updated as we get closer.

In the meantime, you can apply to Playlist Push, a separate music promotion platform, through our affiliate referral link if you meet its creator requirements.

**Apply here:** [VERIFIED PLAYLIST PUSH AFFILIATE URL]

Playlist Push reviews applications independently. Applying does not guarantee acceptance, campaigns, or earnings. Your place on the SoundReach.me waitlist is unaffected whether you apply or not.

*Affiliate disclosure: SoundReach.me may receive compensation if you qualify and complete eligible activity through this referral.*

We'll email you when SoundReach.me is ready for early access.

— The SoundReach.me Team

[Unsubscribe link] · [Business mailing address]

## Implementation checklist

- [ ] Confirm the actual affiliate URL, referral terms, commission trigger, and current eligibility criteria.
- [ ] Decide whether priority access / Founding Creator recognition will be offered, and define enforceable criteria before promising it.
- [ ] Verify the signup form's marketing consent and the applicable email requirements; include required sender identification, mailing address, and unsubscribe handling.
- [ ] Set up sender domain authentication, transactional/bulk email provider, and bounce/complaint handling.
- [ ] Implement signup capture and admin visibility into new signups and delivery outcomes.
- [ ] Build one reusable email template with separate one-time batch and signup-triggered delivery.
- [ ] Add idempotency, suppression lists, logs, and a small internal test send.
- [ ] Send the existing-waitlist batch only to recipients eligible to receive this outreach.
- [ ] Measure email delivery, clicks where available, and affiliate-dashboard outcomes without overstating attribution.

## Boundaries

This document records product and outreach decisions only. It does **not** mean that email infrastructure, automation, tracking, or any affiliate integration has been coded or deployed. Launch timing is an estimate, not a commitment.

## Wall of Founders — dedicated recognition page (approved concept)

**Name:** Wall of Founders (not “Wall of Fame”). Create a dedicated public page on SoundReach.me celebrating creators who actually help launch the platform.

**Proposed recognition:**
- A **Founding Creator** badge displayed on eligible creator profiles.
- A permanent **Wall of Founders** page showcasing opted-in founding creators with display name/handle, profile image (with permission), creator profile link, and optional short introduction.
- An optional early-adopter label and priority invitation to explore the platform at launch, without guaranteeing campaign approval, assignments, or earnings.

**Eligibility distinction:** Joining the waitlist or clicking a Playlist Push affiliate link alone does **not** earn a place on the Wall of Founders. The intended audience is creators who genuinely **launch with SoundReach.me**. Suggested qualifying action: complete onboarding during the designated founding launch window and participate in an eligible first-party campaign (or another clearly defined launch contribution). Define the launch window, verification rules, and capacity before announcing criteria publicly. Playlist Push referral participation must remain optional and separate.

**Suggested page design:** Hero heading “Wall of Founders,” brief gratitude message, searchable or browsable creator cards, and a clear explanation of what Founding Creator means. Consider a distinctive badge design and an invitation to view founders' profiles. Publish profiles only with explicit opt-in and provide an option to remove public recognition.

**Next implementation decisions:** Choose the exact qualification threshold and founding window; define whether the badge is permanent; design the badge and page; add consent and profile visibility controls; add an admin verification workflow; and update launch communications once criteria are finalized.

**Status:** Product concept recorded in documentation; the badge and page have not been built.

## Early-bird creator eligibility exceptions (proposed)

**Default SoundReach.me creator threshold:** 30,000 followers, as proposed by the owner. This is a **SoundReach.me policy proposal**, distinct from Playlist Push's independent requirements.

**Launch exception:** Allow selected early-bird applicants below 30,000 followers to be manually reviewed for SoundReach.me onboarding. Review authentic engagement, content quality, audience fit, consistency, and account integrity rather than follower count alone. An exception grants **consideration**, not automatic approval or guaranteed paid campaigns.

**Founder recognition:** Eligible launch contributors receive a visible **Founding Creator badge next to their display name** and, with opt-in, a profile on the **Wall of Founders**. The badge and recognition are separate from the eligibility exception: an early application alone does not automatically confer either.

**Potential founding benefits:** priority access to launch onboarding, early campaign notifications, and recognition. Do not promise exclusive earnings, priority allocation of paid campaigns, or permanent exceptions until product rules are approved.

**Open decisions:** Define the early-bird window, number of exceptions (if capped), minimum engagement/quality review rubric, badge eligibility and permanence, and whether exceptions persist after launch. Explain these clearly before public promotion.

**Important separation:** SoundReach.me cannot waive or alter Playlist Push's 30,000-follower requirement or independent vetting. Do not advertise SoundReach.me's early-bird exceptions as applicable to the affiliate referral platform.
