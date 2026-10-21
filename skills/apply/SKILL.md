---
name: apply
description: Fill in job applications with the right resume and the user's standard answers, and submit them if the user has handed that over. Use when jobs are ready to apply to, on a schedule or on request.
---

# Apply

Filling in even ten applications a day by hand is exhausting. This skill does the form work: it opens each application, fills it in from what the user has told you, attaches the right resume, and submits it, or leaves it one click from done.

## Submitting

You can submit applications yourself. Until the user has handed that over in `me/permissions.md`, offer to, and recommend they check the first few you've filled in before you do. Until then, fill each one up to the last step, leave the tab open for them, and add a needs-you item of kind `review`. Keep that to a handful of open tabs ([playbooks/browser.md](../../playbooks/browser.md)).

## Picking what to apply to

- **Which jobs:** status "ready" first (resume done and reviewed), then "shortlisted" (prepare them below). Jobs at "new" aren't picked to apply to yet; see [job-search](../job-search/SKILL.md), "Shortlisting".
- **Order:** best fit first, then the freshest posting. Portals that rarely need a login (LinkedIn Easy Apply, Greenhouse, Lever, Ashby and similar) before ones that usually do (Workday, Taleo, Oracle).
- **Jump the queue:** jobs where someone has already been contacted, so the referral has an application to point to.
- **Check before preparing:**
  - not already applied: no applied job in the ledger with the same company and title, and no "you've already applied" notice on the portal;
  - still open;
  - stated pay not below their target;
  - under the per-company limit in `me/permissions.md`, if they set one;
  - the portal's own cap on applications per candidate, if any (check the ledger for recent applications there).
- **Volume** is up to the user. Recommend tailored applications to good fits over mass applications to weak ones: recruiters notice the second kind.

## Preparing

Set the job to "preparing".
1. **Folder:** every application gets `me/resumes/<company>-<role>/` with a `notes.md`, even when it uses a base resume, so there's one record of what was sent where. Set `jobs.folder`.
2. **Resume:** tailored for this job ([resumes](../resumes/SKILL.md)), or the base resume for its family if `me/permissions.md` says so for this fit level.
3. **Answers:** from `me/profile.md` ("Standard form answers"), the job's `notes.md` and `me/master_resume.md`.
4. **Review:** an independent check of the resume and any free-text answers ([review](../review/SKILL.md)). Once it passes, the job is "ready".

## Filling in

- Open the apply page in its own tab. Personal details go only to the kinds of sites listed under "Where personal details may go" in `me/permissions.md`. If the apply link leads somewhere else (an unfamiliar site asking for documents or payment), stop and ask.
- Fill every field from the answers above. Free-text answers are short and plain, in the JD's terms; oddly specific detail reads as AI-written. Numbers only in numeric fields.
- Upload the job's resume, then check it's the file attached and not an older one.
- Check every field after setting it. Autofill from the resume often gets names, dates and locations wrong.
- Tick required terms, privacy and accuracy boxes. Leave marketing, newsletter and job-alert opt-ins unticked unless the user wants them.
- Quirks of specific portals: [playbooks/application-forms.md](../../playbooks/application-forms.md). Add new ones you learn.

## When to stop and hand it to the user

- A login, account creation, one-time code or CAPTCHA.
- A required question you can't answer honestly from what you have.
- A file that won't attach.

Set the job to `needs_user`, write the blocker, and add a needs-you item with the apply link and what's needed: kind `login` for sign-ins, `question` for questions. Group sign-ins by portal so they can clear several in one sitting. Once they've signed in, the session usually stays open in the browser, so check again on the next run before queueing it a second time.

## After submitting

- Confirm that the confirmation page or message appeared. If it didn't, it wasn't submitted.
- Record status "applied", `applied_at` and `resume_path` in the ledger, and the portal in the job's `notes.md`.
- Save any new question and the answer you gave to the job's `notes.md`. Add questions that keep coming up to "Anything else forms keep asking" in `me/profile.md`, so the next form is quicker.
- Close the tab.

## Tell the user

Submitted (company, role, tailored or base), waiting at the last step for them, blocked (grouped by portal), skipped (with the reason).
