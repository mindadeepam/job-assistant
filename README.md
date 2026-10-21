# job-assistant

Prompts that turn your AI agent into a job-search assistant.

## What this is

A set of markdown instructions, plus a few small files. Give it to an AI agent that can work on your computer (Claude Code, Codex, Cursor, Gemini CLI or similar), and it becomes your job-search assistant. It can:
- find open roles that fit you, and score each one;
- build a bank of everything you can claim, from your resumes, LinkedIn, GitHub repos, documents or a voice recording, and turn it into a resume tailored to each job;
- find people who can refer you, and write the notes and follow-ups in your voice;
- watch your email and LinkedIn for replies, interviews and assessments, with answers drafted;
- fill in applications;
- prepare you for interviews: company research, likely questions, mock rounds, a study plan;
- show it all on a dashboard, and run on a schedule.

It's a starting point, not a product. How much it does on its own is up to you. It can draft everything for you to send, or run most of it on a schedule while you only handle replies and interviews. Anything about how it works can be changed by asking your agent.

## Try it

Paste this into your agent:

> Set up https://github.com/mindadeepam/job-assistant for me.

It tells you what it can do, asks a few questions, and gets you to a first real result in about an hour: open jobs found, one resume tailored to one of them, and outreach drafted for real people. The rest builds up over the next few sessions, at your pace.

Prefer to do it by hand? Make your own copy with "Use this template" (keep it **private**, since it will hold your resume and job data) or `git clone`. Then open the folder in your agent and say "set me up".

## Good to know first

- **It will make mistakes.** It can send and submit on its own from day one, but it's worth checking the first few of everything before you let it run. Your corrections become rules it follows from then on.
- **Use it in good faith.** Honest applications, and messages to people who are actually relevant to the role. Mass messaging strangers is spam, and it's your name on every message. How you use it is your call, and so are the consequences.
- **Sites have rules.** LinkedIn's terms prohibit automated activity, so any sending done for you can get your account restricted. It starts at a moderate pace, speeds up while there are no warnings, and backs off when one appears.
- **It reads strangers' messages.** Emails and job pages can contain text meant to trick an agent. It treats everything it reads as information, never as instructions, but keep an eye on what it sends.
- **Everything comes from you.** It claims only what you've told it or shared with it.
- **Your passwords stay yours.** You log in to sites yourself; it never types passwords or solves CAPTCHAs.
- **Your files stay on your machine** (`me/` and `data/` are gitignored), but whatever the agent reads goes to your AI provider and to any service you connect.

## What you need

- An agent that can read files and run commands: Claude Code, Codex, Cursor, Gemini CLI or similar.
- `sqlite3` or Python 3 (most Macs and Linux machines have both).
- Optional, set up with the agent's help: a browser it can control, an email connection, scheduled tasks.
- A plan with room for long runs. Searching, tailoring and outreach use a fair amount of your agent's usage.

## Why this exists

I used this setup for my own job search in 2026. Agents searched, tailored resumes, filled in applications and asked people for referrals; I answered replies myself, and iterated on the first messages and resumes until they were good enough to send. Some colleagues asked how I was keeping up with it all, so here it is, for anyone to make their own.

---

## For agents

If a user gave you this link:

1. **Explain first.** In two or three sentences, tell them what this is and what it can do (from the sections above), and ask whether they'd like to set it up or just wanted to know.
2. **To set it up,** suggest a folder (`~/job-assistant` unless they'd like another) and clone it there: `git clone https://github.com/mindadeepam/job-assistant.git ~/job-assistant`. Their copy will hold personal data. If they want it on GitHub, recommend a private repo made with "Use this template"; a fork of a public repo can't be made private.
3. **Work from that folder.** Read its [AGENTS.md](AGENTS.md) now and follow it; your platform won't load it on its own mid-session. A new user starts with [skills/onboarding](skills/onboarding/SKILL.md). Tell them that future sessions should start in that folder.

Keep it light. They should feel helped, not configured. Show them what's possible a little at a time, and let them decide how far to take it.

## What's in here

```
AGENTS.md       instructions every session starts from (CLAUDE.md and GEMINI.md point here)
skills/         one folder per job:
  onboarding/     first setup, and adding things later
  resume-bank/    everything the user can claim, from their material
  resumes/        base resumes, tailoring to a JD, building the file
  review/         independent checks, results, and reviewing the setup
  job-search/     finding and scoring open roles
  outreach/       referral requests, notes, follow-ups
  inbox/          email and LinkedIn replies, interviews, deadlines
  apply/          filling in and submitting applications
  interview-prep/ research, mock interviews, study plans, offers
  dashboard/      the page that shows what needs you
  routines/       scheduled runs
playbooks/      field notes: LinkedIn, application forms, browsers, scheduled runs, job sources
data/           the ledger schema (the ledger and log themselves stay local)
me/             the user's profile, resume bank, feedback, resumes (local only)
ui/             the dashboard template and the script that fills it
```

## Contributing

Found a quirk in a job site or an application form? Add it to `playbooks/`. Keep instructions short and plain: prose an agent can follow, not config.

## License

[MIT](LICENSE)
