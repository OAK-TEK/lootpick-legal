# Play Data Safety, mapped to the privacy policy

Keep this file and the policy in step. If one changes, change both, then update the
Data Safety form in Play Console. Mismatches between the form and the policy are a
common rejection reason.

Policy URL to enter in Play Console:
https://oak-tek.github.io/lootpick-legal/privacy/

## Data collected

| Play category | Type | Collected | Shared | Purpose | Optional |
|---|---|---|---|---|---|
| Personal info | Email address | Yes | No | Account management | Required |
| Personal info | Name | Yes | No | Account management | Optional, Google sign-in only |
| Personal info | User IDs | Yes | No | Account management, analytics | Required |
| Photos | Profile picture | Yes | No | Account management | Optional, Google sign-in only |
| App activity | App interactions | Yes | No | Analytics, app functionality | Required |
| App activity | Other user-generated content | Yes | No | App functionality | Required, wishlist, backlog, alerts, bio, handles |
| Financial info | Purchase history | Yes | No | App functionality | Required, logged purchases and subscription status |
| Device or other IDs | Device or other IDs | Yes | Yes | Advertising, analytics | Required for free tier |
| App info and performance | Crash logs, diagnostics | Yes | No | Analytics | Required |
| Location | Approximate location | Yes | Yes | Advertising | Free tier only, derived by Google from IP |

## Answers to the standard questions

- Is all data encrypted in transit? **Yes.**
- Do you provide a way for users to request data deletion? **Yes**, in-app deletion plus
  play@lootpick.quest. Deletion URL is the privacy page.
- Data collected for advertising is only collected from free tier users. AdMob does not
  initialise for ad_free or premium entitlements.

## Loose ends before submitting the form

- Confirm the in-app delete account flow actually exists and works. The policy promises
  Profile, then Settings, then Delete account.
- Confirm the EEA consent prompt is wired through Google UMP before enabling
  personalised ads.
- Confirm PostHog retention is set to 12 months in the project settings, since the policy
  states that figure.
- If Steam sync ships at launch, no extra Data Safety category is needed. The Steam ID
  falls under User IDs, already declared.
