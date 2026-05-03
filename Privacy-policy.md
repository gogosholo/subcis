# Subcis Privacy Policy

**Last updated:** 3 May 2026

Subcis is a voice app for small Quran memorization circles. We're an
independent Muslim project run on a tight budget, so the privacy
trade-offs here are simple and conservative: we collect as little as we
can possibly get away with, and we never sell or share your data.

## Who we are

- **Operator:** Oogle ("we", "us"), reachable at `subcis@oogle.tech`.
- **App:** Subcis, available on the App Store and Google Play.
- **Region:** Operated from Sweden using third-party infrastructure
  providers where necessary to deliver the service.

## What we collect — and why

### 1. Quran.com account (required)

To use Subcis you sign in with your **Quran.com** account using
OAuth 2.0. Quran.com is operated by **Quran.Foundation**, a separate
organization with its own privacy policy. We never see your Quran.com
password.

What we receive from Quran.com after you authenticate:

| Data point         | Why we need it                                          |
| ------------------ | ------------------------------------------------------- |
| First / last name  | Show your name on your Me tab                           |
| Quran.com username | Show in your Subcis profile and (when reported) help us |
|                    | identify abusive accounts                               |
| Avatar URL         | Display your Quran.com profile picture                  |
| Bookmarks          | Sync ayat you've bookmarked (read + write)              |
| Reading sessions   | Update your "continue reading" position on Quran.com    |

We **do not** receive your email password, payment information, or
private messages. The OAuth access token + refresh token are stored
**only** on your device, in iOS / Android system-level secure
preferences. They never leave the device except to call Quran.com's
own API.

### 2. Subcis profile (local to your device)

When you onboard you set:

- A **display name** (visible to others in your circles).
- A **gender** (used to gender-segregate "Open Circle" matchmaking).

This data lives only in **SharedPreferences** on your device. We have
no backend database — there is no central record of your Subcis
profile.

### 3. Voice during a circle

Voice in a circle is relayed through our real-time communications
infrastructure. Voice is **not recorded**, **not transcribed**, and
**not retained** by Subcis. Audio is processed in real time and
discarded when the connection ends.

### 4. Reading-session pings

When you open a verse — either inside a circle or via the standalone
Quran tab — Subcis sends a `{chapterNumber, verseNumber}` ping to
Quran.com so your "continue reading" position is up to date there.
The ping does not include duration, audio, or any other content.

### 5. Local-only state

Stored on your device, never sent to a server we control:

- Your last 10 recent room codes
- Your blocked-users list (Quran.com handle + display name)
- A count of warnings you've received from other users
- Your scheduled groups (codes + start times you set or were invited to)
- Your accepted EULA flag, your selected verse-of-the-day cache

## What we **don't** collect

- We don't run analytics. No Firebase, Mixpanel, Amplitude, etc.
- We don't have ads or ad tracking SDKs. No IDFA / GAID collection.
- We don't ship a crash reporter that uploads stack traces.
- We don't track your location.
- We don't read your contacts.
- We don't see your microphone audio outside an active circle.

## Authentication and connection services

We operate a secure backend service solely for authentication and
connection setup. Its responsibilities include exchanging OAuth codes
for Quran.com tokens and issuing short-lived connection credentials
required for joining voice circles.

This service does **not** store authentication tokens or identifying
data. Requests are handled statelessly and credentials are never
persisted server-side.

## How long we keep things

- **On-device data** lives until you sign out of Subcis or delete the
  app.
- **Quran.com tokens** are kept on-device until they expire or you
  sign out — at which point they are removed.
- **Voice traffic** is not retained.
- **Reports you submit** travel by email to `subcis@oogle.tech`. We
  hold those emails until the reported behaviour is resolved or three
  months have passed, whichever comes first, then they're deleted.

## Permissions we request

| Permission        | Purpose                                                |
| ----------------- | ------------------------------------------------------ |
| Microphone        | Required to speak in a circle.                         |
| Notifications     | Optional — used for "doors open" matchmaking reminders |
|                   | and 5-minute "circle starting soon" pings.             |
| Calendar (write)  | Optional — used by the "Add to calendar" button on a   |
|                   | scheduled invite.                                      |
| Bluetooth (iOS)   | Optional — for routing voice to AirPods / car audio.   |

You can revoke any of these in your device's system settings without
losing access to the app.

## Children

Subcis is not directed to children under 13. We don't knowingly
collect data from anyone under 13. If you believe a child has signed
in to Subcis, contact us and we'll work with you to delete what we
can (mainly: their email reports to us, since everything else is
on-device).

## Your rights (GDPR, CCPA, etc.)

Because almost all your Subcis data lives on your own device, your
rights are mostly self-serve:

- **Access:** open the Me / Settings tabs to see everything we know.
- **Delete:** sign out (clears Quran.com tokens) and uninstall the app
  (clears the rest).
- **Quran.com data:** for anything stored on Quran.Foundation's side,
  contact them via [quran.com](https://quran.com).
- **Email reports:** to remove a report you submitted, email
  `subcis@oogle.tech` with the reported user's code or your reporter ID.

## Sharing

We don't sell or share your data with third parties for marketing.

We share data only with service providers strictly as necessary to
operate Subcis, such as:

- Authentication and Quran sync providers
- Infrastructure providers that power live voice communication
- Hosting / networking providers that deliver backend services

Each processes data only as needed to deliver the service.

## Changes

If we change this policy in a way that affects how we handle your
data, we'll bump the "Last updated" date at the top and surface a
notice in-app on next launch.

## Contact

Questions, requests, or reports: **`subcis@oogle.tech`**.
