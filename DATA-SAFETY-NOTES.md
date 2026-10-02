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
| App info and performance | Crash logs, diagnostics | Yes | No | Analytics | Required, Sentry crash reports, no name, email or account id attached |
| Location | Approximate location | Yes | Yes | Advertising | Free tier only, derived by Google from IP |

## Answers to the standard questions

- Is all data encrypted in transit? **Yes.**
- Do you provide a way for users to request data deletion? **Yes**, in-app deletion plus
  play@lootpick.quest. Deletion URL is the privacy page.
- Data collected for advertising is only collected from free tier users. The AdMob SDK is
  started by `AdsBootstrap` in `app/_layout.tsx` only once the tier has resolved to `free`, so
  it does not start for ad_free or premium accounts when the app opens. (Before 2 October 2026
  it started for everyone and only the banner was hidden. The policy now matches the code.)
- Calendar: the app requests READ_CALENDAR and WRITE_CALENDAR to add release-date reminders to
  a calendar on the device. Nothing is sent to our servers, so no Data Safety category is
  declared, but the permission is disclosed in the policy. Re-check this answer if reminders
  ever sync to a server.

## Loose ends before submitting the form

- Verified in code on 2 October 2026: the delete account flow exists (Profile, then Delete
  Account, with an emailed code) and the Google UMP consent form is wired in `src/lib/ads.ts`.
- The policy no longer states a PostHog retention figure or a 30-day backup clear. If you want
  to state either, check the PostHog and Supabase settings first and then add it back.
- Confirm in the Stripe dashboard which billing details you can see (name, email, country,
  postcode), since the policy describes what Stripe collects and may show us.
- Confirm whether Stripe Tax is switched on for website sales. The Terms say tax is applied at
  checkout where the law requires it.
- If Steam sync ships at launch, no extra Data Safety category is needed. The Steam ID
  falls under User IDs, already declared.
