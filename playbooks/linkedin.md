# LinkedIn

Field notes. LinkedIn changes its limits and pages often. When what it shows differs from this file, trust the page and update the file.

## Limits and terms
- LinkedIn's user agreement prohibits bots and automated activity, so any sending done for the user breaks its terms and can get the account restricted at any volume. The user should know this before they hand over any sending.
- **Invitations:** LinkedIn publishes no limit, and it varies by account. Trouble is most often reported once they pass roughly 100–150 a week. There's no fixed cap here: start moderate, spread sends through the day, and speed up while LinkedIn shows nothing. At any "too many invitations" warning, verification prompt or CAPTCHA, stop sending invitations for the run, set `linkedin_invite_limit_hit_at` in the ledger's `state` table, cool off for several days, and write what happened under Pace in the user's `me/permissions.md`. Later runs pace themselves from that.
- **Notes on invitations:** up to 300 characters on Premium. Free accounts have had a shorter limit and only a few personalised notes a month. Check what the user's account allows. Without notes, send the invitation bare and write the message once they accept.
- Messages to existing connections and follow-ups don't count towards the invitation limit, but a burst of near-identical messages still looks automated. Vary them and spread them out.
- Pending invitations can't be nudged. Withdrawing ones that are weeks old keeps the pending list short.

## Before every send
- Open the profile. "Pending" means the invitation already went. For a 1st-degree connection, read the whole thread first.
- Text left over in a message box proves nothing. Check the sent thread.

## Reading messages
- The messaging list renders rows lazily: rows outside the viewport can come back empty in the page text. Scroll in small steps and record every row's text after each step (dedupe by name) until you pass the last check's date. Never treat an empty row as a separator. Look for unread badges too.
- Typing into the messaging search box doesn't always register through automation. Don't rely on it.
- **Acceptances:** the sent-invitations page (My Network → Manage → Sent) lists who is still pending. For anyone no longer there, confirm on their profile that they're now a 1st-degree connection.

## Searching for jobs
- Job search URLs take filters, for example `f_TPR=r86400` (posted in the last 24 hours; `r604800` for a week), `f_WT=2` (remote) and `f_AL=true` (Easy Apply). Check they still work on the user's account.
- Fetch tools often get only a summary of a LinkedIn posting. Read the full JD in the browser.
- "Easy Apply" stays on LinkedIn. External "Apply" links often end at a portal that needs an account (Workday, Taleo, Oracle); in one user's runs it was about half.

## Making the profile work for them
- A headline in their target role's terms, and "Open to work" (they can show it to recruiters only).
- Saving jobs, following target companies, and liking or commenting on posts in their field shape the job recommendations and the feed.
- Job alerts for saved searches arrive by email, where the inbox routine can pick them up.
