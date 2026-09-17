---
title: "Privacy Policy — Personal Agent"
description: "How the personal agent at danlopez.fyi handles data received from Google APIs"
---

*Last updated: 17 September 2026*

This policy covers the personal agent operated at `danlopez.fyi` ("the agent") and how it handles information obtained from Google APIs. The agent is a private, self-hosted assistant with a single user: its operator, Dan Lopez. It is not offered to the public and does not have accounts.

## Data the agent accesses

Only after permission is granted through Google's OAuth consent flow — in practice, only for the operator's own account — the agent may access:

- **Gmail** — read messages, apply labels and filters, modify (archive, mark as read), send and draft mail
- **Google Calendar** — read calendars and events, create and edit events
- **Google Drive, Docs and Sheets** — read and write files and documents
- **Google Contacts** — read contacts

These permissions are requested because the operator's own workflows need them. No other person's Google account is authorized.

## How the data is used

Accessed data is used only to carry out the tasks the operator asks for — for example summarizing an inbox, preparing a daily brief, creating a calendar event, or editing a document. It is not used for advertising, profiling, or any purpose beyond fulfilling those requests.

## How the data is stored

- OAuth tokens are stored on a private server controlled by the operator (an Oracle Cloud virtual machine in Querétaro, Mexico). That server is reachable only over a private network and is not exposed to the public internet.
- Token files and working data are readable only by the operating-system account that runs the agent.
- The agent keeps a small long-term record of durable facts (for example, a standing preference) and the documents and spreadsheets it maintains for the operator. These live on the same private server, are readable only by the operator, and are never shared.
- Mail, calendar entries and files themselves stay in the operator's own Google account; the agent keeps no independent offsite copy.

## Sharing

- No Google user data is sold, rented, or shared with third parties for advertising or any other purpose.
- To generate responses, requests are processed by third-party AI model providers acting as service providers under their API terms. No Google user data received by the agent is used to train or improve foundation models.
- Data would be disclosed only if required by law.

## Limited Use

The agent's use of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the [Limited Use](https://developers.google.com/terms/api-services-user-data-policy#limited-use) requirements.

## Revoking access and deleting data

- Access can be revoked at any time from the Google Account's [third-party connections page](https://myaccount.google.com/permissions). Revocation takes effect immediately and invalidates the stored tokens, after which the agent can no longer reach the account.
- Deleting the corresponding mail, calendar events, or documents in the Google account removes that data everywhere. Working copies the agent created are deleted on the private server when the task completes.
- To request deletion of anything else the agent stores, or to ask a question about this policy, email [hi@danlopez.fyi](mailto:hi@danlopez.fyi).

## Changes

Any change to this policy is published on this page with a new "last updated" date.
