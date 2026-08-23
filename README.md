# Project Preview Generator

A single-file web app that turns any team's project into a polished, consulting-deck-style
preview, live, in the browser. Generic version of the Capstone Preview Generator — same wizard,
same formatting, no roster-doc upload, and no wording tied to a specific course or cohort. Any
team fills in their own names and content, no coding or GitHub account needed.

This tool doesn't call any AI model itself — it just formats what the team already wrote.

## How it's organized

The wizard is one step per real deliverable. Each team member works through their own step — the
fields map to a real project deliverable — then pastes or types their answers in and uploads their
own slide images if they built them. Everything combines into one HTML presentation automatically.

| Step | Whose deliverable | What's in it |
|---|---|---|
| 1. Upload Your Document | Whole team | Upload the project brief (.docx/.txt/.md); auto-fills what it can |
| 2. Team & Project Basics | Whole team | Team number, 6 names/roles, client, objective, logo |
| 3. Business Problem | Team Member 3 | Problem summary, key challenges, baseline metrics, current vs. proposed workflow, before/after — plus their slides |
| 4. Proposed Solution | Team Member 2 | Solution name/description, 5 solution components — plus their slides |
| 5. Recommendation & Follow-Up | Team Member 4 | Recommendation, 3-message follow-up, quality review, risks/safeguards, human review — plus their slides |
| 6. Testing & Measurement | Team Member 5 | Testing criteria (rubric), test results & revisions, 3 success measures — plus their slides |
| 7. Implementation Plan | Team Member 6 | Pilot, training, handoff points, adoption risks, feedback process, measure & improve, scale decision, final recommendation — plus their slides |
| 8. Review & Export | Whole team | Save & Get Link, Export HTML |

Team Member 1 (Team Lead / Project Manager) doesn't get their own content section — that role is
pure coordination (meetings, schedule, tracking deliverables), not a content deliverable.

Names, roles, and responsibilities for all 6 team members are entered by hand on Step 2 — there is
no document-upload shortcut for the roster in this version (the original Capstone Preview
Generator has that feature if you need it).

## Saving and sharing — no files to pass around

Click **Save & Get Link** on Step 8 (or any time) and the tool saves the whole project — every
field, the logo, and everyone's slide images — to the cloud and shows a link. Send that link to a
teammate; opening it loads the project exactly as it was left, ready to keep editing. No JSON file,
no email attachment, no GitHub account on their end.

Saving again reuses the same link and just updates it in place — the link never changes for a given
project. Anyone with the link can open and edit it; there's no login and no passcode, so only share
the link with your own team.

Work also **autosaves in this browser** as a safety net against an accidental refresh or closed tab
— that's separate from Save & Get Link and doesn't carry across computers or browsers on its own.

**Export HTML** downloads a finished, standalone HTML copy of the preview — for sharing with
stakeholders. It's not editable back into the form; use Save & Get Link for that.

## What it does

- **Upload your project brief** (Step 1) and it automatically pulls in Client Name, Problem
  Summary, Objective, and Risk topics — only what's actually written in the document, nothing
  invented. It also finds the specific numbers inside the problem statement (e.g. "14 hours", "more
  than five days") and pre-fills them into Baseline Metrics, and starts the Before/After Comparison
  with a "Before:" line for each one.
- **Team & Project Basics (Step 2)** is where you type in your own 6 names, roles, and
  responsibilities. Team Members 2-6 each own one of the 5 fixed deliverable steps — the hint next
  to each name field says which step.
- **Every deliverable step shows its real owner.** Whatever name is typed into that member's Step 2
  field shows up as the **Owner: [Name]** tag on the matching slide(s) — live, as you type.
- **Each person's step has its own slide upload.** If someone already built their own slide(s)
  elsewhere (Google Slides, PowerPoint, Canva), export as PNG/JPG and upload it right in their own
  section — it's embedded directly into the deck immediately after their own content, not lumped
  into one dump at the end. Skip it and Export HTML still generates the full deck automatically from
  the text fields.
- **Testing is split into rubric + results.** Testing Criteria (the rubric — what outputs were
  scored against) and Test Results & Revisions (what was found and changed) render as two labeled
  parts of the same slide.
- **Implementation is a real phased plan, not a vague "next steps" list.** Days 1-30 Pilot,
  Training Requirements, Human Handoff Points, Adoption Risks, Feedback Process, Days 31-60
  Measure & Improve, Days 61-90 Scale Decision, then a Final Recommendation — each is its own
  field, walking through building an actual rollout plan one piece at a time.
- **Every step shows the actual question your brief asks.** If the uploaded brief has a section
  like "Answer these questions...", the exact questions are pulled out and shown, in quotes, next
  to the field that answers each one.
- **Before / After Comparison automatically becomes a bar chart** when every line has a real,
  comparable number (it understands common units like hours/minutes/days). If anything doesn't
  cleanly compare, it falls back to a plain list instead of showing something misleading.
- **Need help with this?** buttons on content fields open guiding questions and a worked example —
  static, built-in guidance, not an AI call.
- **Team / Company Logo** (Step 2, optional) — embedded directly, travels with Save & Get Link and
  Export HTML.
- The preview is styled like a minimal MBB/Big-Four consulting deck — a cover slide with logo and
  confidentiality line, an **Agenda** listing only the sections actually filled in, an
  **Executive Summary**, and a numbered slide for every section, each with a page number and
  confidentiality footer.
- **Headlines, not labels.** Where a section has a clear point to make, its slide title is the
  actual first sentence of what was written — pulled and trimmed, never rewritten or invented.
- Sections and fields left blank never show up in the preview — no empty placeholders.
- A workflow line like `Sales Notes -> Opportunity Brief -> Proposal Draft -> Human Review` turns
  into connected workflow boxes automatically.
- **Clear** wipes the form and browser autosave (asks to confirm first).

## How to open it

Just open the published link (see "Where to find it" below) — no install, no account, nothing to
download. It also still works as a plain local file: double-click `index.html` and it opens in your
default browser, with everything except Save & Get Link working fully offline.

## How to use it

1. Open the link (or `index.html`).
2. **Step 1 — Upload Your Document.** Upload your project brief (`.docx`, `.txt`, or `.md`, or
   paste the text). No document handy? Click **Skip — I'll fill this in myself**.
3. **Step 2 — Team & Project Basics.** Type in your team number, all 6 names, and check the roles —
   edit if your team splits work differently. Fill in your team name, the client, the objective,
   and a logo (optional).
4. **Step 3** — Problem Summary, Key Challenges, Baseline Metrics, Current Workflow, Proposed
   Workflow (both `Step 1 -> Step 2 -> Step 3`, arrows), Before/After Comparison (`Before: ...` /
   `After: ...`, one per line). Upload slides if that person built any.
5. **Step 4** — Solution Name/Description, then the 5 numbered solution components (Purpose +
   Details each). Upload slides if built.
6. **Step 5** — Recommendation, the 3 Follow-Up Messages, Quality Review, Risks and Safeguards,
   Human Review / Handoff. Upload slides if built.
7. **Step 6** — Testing Criteria (the rubric, one per line), Test Results & Revisions, Three Success
   Measures (pick 3, one per line). Upload slides if built.
8. **Step 7** — Days 1-30 Pilot, Training Requirements, Human Handoff Points, Adoption Risks,
   Feedback Process, Days 31-60 Measure & Improve, Days 61-90 Scale Decision, Final Recommendation.
   Upload slides if built.
9. **Step 8 — Review & Export.** Check the live preview on the right at any point. Click
   **Save & Get Link** for a shareable cloud checkpoint — send the link to a teammate to hand off.
   Click **Export HTML** for the finished, standalone copy to share.

You can move Back and Next between steps at any time — nothing is locked in until export. Special
characters, long paragraphs, and multi-line text are all safe to paste in — the tool escapes
everything so it can't break the page.

### About the document upload

Reads `.docx`, `.txt`, and `.md` files, or pasted text — never guesses or invents content, only
what's actually in the document gets filled in. `.docx` support loads a small unzip library
(JSZip) from a CDN, so it needs an internet connection the first time; `.txt`/`.md` uploads and
pasted text always work fully offline. An older `.doc` (Word 97-2003) file isn't supported — save
it as `.docx` first. `.pdf` isn't supported either — a PDF's text has no headings/tables left in
it to read, so copy the text out and paste it in instead.

### About slide uploads

Each step has its own upload widget — up to 10 images, 3MB each, 10MB total per step. Export slides
as PNG or JPG from Google Slides, PowerPoint, or Canva, then upload them in order in that step.
They're embedded directly into the preview, Export HTML output, and Save & Get Link, right after
that step's own content — so flipping through the final deck reads as one continuous flow.

### About the logo and design

The logo is embedded directly. Keep it under ~500KB so it doesn't bloat Save & Get Link or autosave.

The layout is styled after the minimal house style shared by MBB and Big Four consulting decks —
not a copy of any specific firm's proprietary template: a cover slide, an Agenda, one idea per
slide with a page number and confidentiality line, and headline titles that state a conclusion
instead of just naming a topic. The **Executive Summary** appears once a Problem Summary, a
Solution, or Success Measures are entered — it doesn't invent anything, it re-displays those three
pieces together. The Agenda and the numbered slides that follow are always built from the same
underlying list, so they can never drift out of sync, and blank sections are skipped so numbering
stays consecutive.

### A note on autosave vs. Save & Get Link

Autosave only remembers work in the one browser, on the one computer, where it was typed — it's a
safety net against an accidental refresh or closed tab, not a substitute for **Save & Get Link**.
Click **Save & Get Link** after your section so the next teammate can open the link and continue —
autosave alone won't carry across machines or browsers.

## Where to find it

Deployed on Vercel so anyone can open it with just a link — no account, no install.

The tool runs entirely in the visitor's browser. Only **Save & Get Link** talks to a server (the
Supabase project below) — everything else stays local to the tab.

## The Supabase project behind Save & Get Link

This version reuses the same Supabase project as the Capstone Preview Generator, in its own table
and storage bucket so the two tools' saved projects never mix.

- **Table `team_projects`** — `code` (share code, primary key), `data` (jsonb — every field plus
  image URLs), `updated_at`.
- **Storage bucket `team-slides`** — logo and slide images, uploaded under `<code>/...` paths.
- Cloud save/load goes through two `SECURITY DEFINER` RPC functions, `save_team_project` and
  `load_team_project`, so the anon key can never read or write the table directly.

Setup SQL (run once in the Supabase SQL editor — this project's table/functions don't exist until
you do):

```sql
create table team_projects (
  code text primary key,
  data jsonb not null,
  updated_at timestamptz not null default now()
);
alter table team_projects enable row level security;

create or replace function save_team_project(p_code text, p_data jsonb)
returns void
language plpgsql
security definer
set search_path = public
as $$
begin
  insert into team_projects (code, data, updated_at)
  values (p_code, p_data, now())
  on conflict (code) do update set data = excluded.data, updated_at = now();
end;
$$;

create or replace function load_team_project(p_code text)
returns jsonb
language sql
security definer
set search_path = public
as $$
  select data from team_projects where code = p_code;
$$;

grant execute on function save_team_project(text, jsonb) to anon;
grant execute on function load_team_project(text) to anon;
```

Then create the `team-slides` Storage bucket (public), with public insert/select/update storage
policies for that bucket.

The project URL and its public "anon" key are embedded directly in `index.html` (the anon key is
meant to be public — Supabase's real access control is the RPC functions and row-level security,
not key secrecy).
