---
layout: page
title: Privacy Policy
permalink: /privacy/
---

**Effective date:** 2026-04-24
**Last updated:** 2026-04-24

## 1. Overview

BrainTax is a self-hosted video publishing tool operated solely by its owner for the `@braintaxhq` channel. No data is collected from visitors to this website or from any third-party TikTok user. All operations performed by the BrainTax tool are on behalf of the operator's own accounts on TikTok, YouTube, Instagram, and Facebook.

## 2. TikTok API scopes

BrainTax requests the following TikTok API scopes when authorizing the operator's own TikTok account:

- **`user.info.basic`** — used to verify the identity of the operator's own TikTok account during initial setup.
- **`video.upload`** — used to upload video files produced by the BrainTax pipeline to the operator's own TikTok account.
- **`video.publish`** — used to publish uploaded videos directly to the operator's own TikTok account, with caption, privacy, and interaction settings chosen by the operator.

No scopes are requested that would grant access to any other TikTok user's data or content.

## 3. Data received from the TikTok API

Data received from the TikTok API is limited to the following, all pertaining solely to the operator's own TikTok account:

- `open_id` (an opaque TikTok-assigned identifier for the operator's account)
- display name
- avatar URL
- publish status for videos uploaded by the operator
- TikTok-assigned video IDs for videos uploaded by the operator

No data is received about any other TikTok user at any time.

## 4. Token storage and retention

OAuth access tokens and refresh tokens issued by TikTok are stored on the operator's local filesystem only, in a configuration file excluded from version control. Tokens are never transmitted to any third party, analytics service, or cloud backend. Tokens are retained until the operator revokes app access.

## 5. Revocation and user rights

Because the only user of the BrainTax tool is its operator, data-subject rights are self-exercised by revoking app access at:

<https://www.tiktok.com/setting/apps-and-website>

Any questions may be directed to the contact email below.

## 6. Contact

`agha.awais@braintax.net`

## 7. Changes to this policy

This policy may be updated as the BrainTax tool evolves or as required by applicable law. The "Last updated" date above reflects the most recent revision.
