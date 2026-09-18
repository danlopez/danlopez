---
title: "Privacy Policy — Personal Agent"
description: "How the Personal Agent handles data received from Google APIs"
# Reachable by direct URL only: no menu or in-page links point here, the page is kept
# out of the sitemap, and search engines are asked not to index it.
sitemap:
  disable: true
_build:
  list: never
noindex: true
---

*Last updated: 17 September 2026*

This policy describes how the **Personal Agent** — a private, self-hosted assistant operated by the owner of this site for their own use — handles information obtained from Google APIs. The assistant is not a public service, has no accounts, and has a single user: its operator.

## Data the assistant accesses

Only after permission is granted through Google's OAuth consent flow, and only for the Google account that grants it, the assistant may access:

- **Gmail** — read messages, apply labels and filters, modify (archive, mark as read), send and draft mail
- **Google Calendar** — read calendars and events, create and edit events
- **Google Drive, Docs and Sheets** — read and write files and documents
- **Google Contacts** — read contacts

These permissions are requested because the operator's own workflows need them. No other person's Google account is authorized.

## How the data is used

Accessed data is used only to carry out tasks the operator asks for — for example summarizing an inbox, preparing a daily brief, creating a calendar event, or editing a document. It is not used for advertising, profiling, or any purpose beyond fulfilling those requests.

## How the data is stored

- OAuth tokens and working files are stored on a private server controlled by the operator. That server is reachable only over a private network and is not exposed to the public internet.
- Tokens and working data are readable only by the operating-system account that runs the assistant.
- The assistant keeps a small long-term record of durable facts (for example, a standing preference) and the documents and spreadsheets it maintains for the operator. These stay on the same private server and are never shared.
- Mail, calendar entries and files themselves remain in the operator's own Google account; the assistant keeps no independent offsite copy.

## Sharing

- No Google user data is sold, rented, or shared with third parties for advertising or any other purpose.
- To generate responses, requests are processed by third-party AI model providers acting as service providers under their API terms. No Google user data received by the assistant is used to train or improve foundation models.
- Data would be disclosed only if required by law.

## Limited Use

The assistant's use of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the [Limited Use](https://developers.google.com/terms/api-services-user-data-policy#limited-use) requirements.

## Revoking access and deleting data

- Access can be revoked at any time from the Google Account's [third-party connections page](https://myaccount.google.com/permissions). Revocation takes effect immediately and invalidates the stored tokens, after which the assistant can no longer reach the account.
- Deleting the corresponding mail, calendar events, or documents in the Google account removes that data everywhere. Working copies the assistant created are deleted on the private server when the task completes.
- To request deletion of anything else the assistant stores, or to ask a question about this policy, email [hi@danlopez.fyi](mailto:hi@danlopez.fyi).

## Changes

Any change to this policy is published on this page with a new "last updated" date.
