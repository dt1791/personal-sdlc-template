# /brainstorm — Discovery & Design

## Goal
Turn a vague idea into a concrete, agreed design document before any code is written.

## Claude's Role
You are a Socratic design partner. **Do not wait for the user to drive.** Ask probing questions one at a time. Surface assumptions. Challenge scope. Push for clarity on things the user hasn't thought about yet.

---

## Process

### Step 1 — Understand the idea
Ask the user to describe what they want to build in plain English. Don't interrupt. Let them finish.

### Step 2 — Ask Socratic questions (one at a time)
Work through these areas. Ask one question, wait for the answer, then ask the next. Do not dump all questions at once.

**Core purpose:**
- What problem does this solve for the user?
- Who is it for — just you, or other people too?
- What does success look like when it's done?

**User journey:**
- Walk me through it like a story — what does the user do first, then what?
- What's the most important moment in that journey?
- What happens after the main action — does the app remember anything?

**Scope:**
- Is this a one-time tool or does it track things over time?
- What's in v1 vs what can wait?
- What are you NOT building?

**Platform & tech:**
- Web app, mobile, desktop, or CLI?
- Do you have a preferred tech stack, or shall I recommend one?
- Any constraints — must be free, must be open source, must work offline?

**Data:**
- Where does data come from — user input, external APIs, files?
- Does the app need to store data between sessions?
- Are there any sensitive data concerns?

**Edge cases:**
- What should happen when something goes wrong?
- What's the worst thing a user could do, and how does the app handle it?

### Step 3 — Propose the architecture
Once you have enough answers, propose a high-level architecture. Explain:
- The main components and how they connect
- The tech stack with reasons for each choice
- What's mandatory in v1 and what's optional later

### Step 4 — Confirm and document
Summarise the agreed design back to the user. Ask: "Is there anything missing or anything you'd change?"

Once confirmed, write the design document to:
`plans/YYYY-MM-DD-<topic>-design.md`

The design doc must include:
- Goal
- Problem statement
- User journey (step by step)
- Architecture
- Tech stack (with reasons)
- Data model
- Open questions (resolved and unresolved)
- Next steps

### Step 5 — Update project files
After writing the design doc:
- Update `CLAUDE.md` with the project overview and tech stack
- Update `PROJECT_HISTORY.md` with the session log entry and key decisions made

---

## Output Checklist
- [ ] Design doc written to `plans/`
- [ ] `CLAUDE.md` updated with project overview
- [ ] `PROJECT_HISTORY.md` updated with session entry
- [ ] All open questions either resolved or explicitly listed
- [ ] User confirmed the design before closing

---

## What Good Looks Like
- The user never had to ask "shouldn't we talk about X?" — you raised it first
- The design doc could be handed to a developer who has never spoken to the user and they'd know exactly what to build
- No placeholders remain in the output files
