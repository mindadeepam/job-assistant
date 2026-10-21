# Application forms

Field notes on applicant tracking systems. Add what you learn.

## Everywhere
- Check every field after setting it. Autofill from the resume often gets names, dates and locations wrong.
- Numbers only in numeric fields ("25", not "25 LPA").
- After uploading the resume, check that the attached file is this job's resume, not an older one.
- Tick required terms, privacy and accuracy boxes only. Leave marketing, newsletter and job-alert opt-ins unticked.
- Submitted means you saw the confirmation page or message.

## Workday
- Dropdowns open with a real click. Then click the option inside `[role=listbox] [role=option]` (a script click on the option works). Typing and pressing Enter sometimes picks the wrong value, so check it.
- Most Workday sites want an account, which is the user's job. Some offer a guest application ("Apply manually" or similar). Look before calling it a login blocker, and decline any offer to create an account afterwards.

## Others
- **Greenhouse, Lever, Phenom, Freshteam, Oracle:** setting text fields directly usually works.
- **Ashby:** text fields need real typing; values set directly don't register. Some companies cap applications per candidate (for example two in 60 days), so check the ledger for recent applications there first.
- **amazon.jobs:** needs real typing.
- **Oracle-based pages** scroll inside a container. Find the element and scroll it into view rather than scrolling the page.

## Upload buttons with no file input
LinkedIn Easy Apply and SmartRecruiters sometimes show only an "Upload" button. One trick that worked with a Chrome automation extension: patch `HTMLInputElement.prototype.click` so the hidden file input gets attached to the page instead of opening the file picker, click the button, then upload into the captured input. With other tools, use their own file-upload method.

## Background tabs
Forms in a background tab may not react until the tab is brought forward or screenshotted. Timers (`setTimeout`) in page scripts can hang there, so don't wait on them.
