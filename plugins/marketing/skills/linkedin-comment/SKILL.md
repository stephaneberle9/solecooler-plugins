---
name: linkedin-comment
description: >
  Write LinkedIn comments that get read and earn their own reach — not generic "Great post!" filler.
  STEP-BY-STEP, interactive process: intake the original post, pick a comment angle, then write 2-3
  tight variations built so the value lands before LinkedIn's "...more" cutoff. Reads voice and ICP
  context from CLAUDE.md or the project's `Context/` folder; asks the user to fill gaps if context is thin.

  USE THIS SKILL WHEN:
  - User pastes someone else's LinkedIn post and wants to comment on it
  - User says "write a comment", "comment on this post", "reply to this LinkedIn post"
  - User wants to engage on another person's or company's post to get visibility
  - User asks how to respond to a LinkedIn post in a way that gets noticed
  - User wants a "top comment" / a comment that ranks and pulls reach

  Use this skill even when the user doesn't say "comment" — if they paste a post that isn't theirs and
  want to react publicly to it, this is the right tool (NOT linkedin-post, which writes whole posts).

  TRIGGERS: "LinkedIn comment", "comment on this", "reply to this post", "write a comment",
  "respond to this LinkedIn post", "top comment", "engage with this post"
---

# LinkedIn Comment

You help the user write LinkedIn comments that actually get seen. A comment is **not a small post** — it behaves differently in the feed and the algorithm reads it differently, so the craft is different. Read [references/comment-craft.md](references/comment-craft.md) before you write anything; it explains the mechanics this whole skill is built on.

This is an **interactive, step-by-step process**. Comments are short, so the process is lighter than the post skill — but you still never dump a finished comment without intake and an angle decision. You present options and let the user steer.

The reason this process exists: most comments are invisible. "Great post!" earns nothing. A comment only pulls reach if it clears two hurdles — it gets **read** (LinkedIn truncates after a couple of lines with "…more", and most people never expand), and it earns its **own reactions** (only then does the algorithm rank it as a "Top comment" and show it to more people). Every step here serves those two hurdles.

---

## the two hurdles (the whole point)

Internalize this before writing — full version in [references/comment-craft.md](references/comment-craft.md):

1. **A comment is first an engagement signal on someone else's post.** It primarily boosts the *original* post's visibility and puts the user in front of *that post's* audience. Commenting on the right posts is itself a visibility play.
2. **To pull reach of its own, the comment must (a) get read and (b) earn reactions.**
   - **Get read:** the first 1–2 lines must deliver the full value with no "…more" click. A long block gets scrolled past; a short one gets read whole.
   - **Earn reactions:** a pointed, self-contained statement with a concrete fact or a clear thesis. A mini-essay gives the reader nothing to grab.

**Rule of thumb:** payload in the first one or two lines. Any link goes at the **end** (external links dampen reach — much less so in a comment than in a post, but still put it last).

---

## before starting: gather context

**STOP. Do not begin until voice and ICP context are in hand. Cap questions at 2 max.**

**Load reference skills first:**
- `company-instructions` — Solecooler voice rules, writing standards, and banned phrases that apply to all output.
- `company-context` — if the comment touches Solecooler products, positioning, or proof, load this too.

### Step A: Scan context (fast)

1. **Check what's already loaded.** Context comes from three layers: the reference skills above (company-wide voice + products), Global Instructions (the user's personal overlay from `/personal-interview`), and project-specific context (Project Instructions in Claude Desktop, or CLAUDE.md for CLI users). Scan for:
   - **Voice** — tone, do/don't rules, signature phrases. A comment is short, so one off-key word reads like a bot. It must sound like the user.
   - **ICP / positioning** — who the user wants to be seen by, and what they're known for. The comment should land for the audience reading the *original* post.
2. **Last resort:** check the project folder for `Context/voice.md`, `Context/icp.md`. Read whichever exist.
3. **Check for comment/post samples.** If the user has previous LinkedIn writing saved anywhere obvious, read it — best voice reference there is.

### Step B: Ask ≤2 questions to fill gaps

Only ask about what context didn't cover. Combine into AT MOST 2 questions. Priority:

1. **Voice + samples** — "I don't see voice context. Paste 2–3 of your previous LinkedIn comments or posts so I can match how you write?"
2. **Goal** — "What's the goal here — be seen by this author's audience, support the author, add a counter-point, or something else? And is there a specific fact/experience you want to bring?"

Skip whichever the context already covers. Never ask more than 2.

---

## the process

```
SCAN CONTEXT → INTAKE ORIGINAL POST → ANALYZE → PICK ANGLE (5-7 options) → WRITE (2-3 variations) → ITERATE
```

| Step | What happens | User chooses from |
|---|---|---|
| 0 | Get the original post + the user's take | — |
| 1 | Analyze the post internally | — |
| 2 | Suggest comment angles | 5–7 options |
| 3 | Write the comment | 2–3 variations to iterate |

**Golden rule:** Never skip Step 0 or Step 2. A comment written without reading the original post, or without a deliberate angle, defaults to generic filler.

---

## Step 0: Intake the original post

Get the **full text of the post being commented on**, plus the user's angle if they have one.

- **The user must paste the post text.** Never scrape LinkedIn posts or profiles. If they give a URL, ask them to paste the post body (and note the author + roughly how big the account is, if known — it affects the visibility play).
- Ask, if not given: **does the user have a specific fact, number, experience, or disagreement to bring?** That's the strongest raw material for a top comment.
- Acknowledge with a 1-sentence read of what the post is arguing, then move to Step 1.

---

## Step 1: Analyze the original post (internal)

Before suggesting angles, work out internally:
- The post's **core thesis** and the **tone/register** of the author (so the comment is a good guest, not a hijack).
- The **audience** reading it — these are the people the user's comment will reach.
- **Openings:** what the post left out, didn't take far enough, got slightly wrong, or invites a question. These become the angles.
- Whether the user's supplied fact/experience fits a specific gap.

Don't present this analysis in detail — use it to drive Step 2. Just signal you've read the post and you're ready with angles.

---

## Step 2: Pick a comment angle

Present **5–7 angle options**, each mapped to an archetype from [templates/comment-archetypes.md](templates/comment-archetypes.md). For each option give:
- **Archetype** (new fact / sharp counter / build-on / lived experience / reframe / precise question)
- **The angle** (1 line): the specific move for *this* post
- **Why it earns reach** (½ line): what reaction it's built to pull

Make them genuinely different — pull from different gaps in the post and different reaction triggers. Don't offer six variations of "agree and add a point." Generic praise is never an option; if the only honest reaction is "nice post," say so and suggest the user skip commenting.

**Wait for the user to choose before writing.**

---

## Step 3: Write the comment

**Re-read [references/comment-craft.md](references/comment-craft.md) and the relevant structure in [templates/comment-archetypes.md](templates/comment-archetypes.md) before writing.** Then write **2–3 variations** of the chosen angle so the user can pick.

Each variation must:
- **Land the value in the first 1–2 lines** — works fully before the "…more" cutoff.
- Be **self-contained and pointed** — one concrete fact or one clear thesis, something a reader can react to.
- Be **short** — 1–3 lines is the target. Extra detail (a worked example, a source) goes *below* the headline value, for the minority who expand.
- **Sound like the user** — their phrasing, their directness, no corporate filler, no AI tells.
- Put any **link at the very end**, one max, and still work if the link is never clicked.
- **Not pitch.** Add value; visibility is the reward. No turning the author's post into an ad for the user's thing.

Show the variations inline (comments are short — no artifact needed) with a one-line note on what each leads with. Mark anything the user must supply with `[PLACEHOLDER — needs real number/source]`. Never fabricate facts, rulings, numbers, or experiences.

### After writing

Ask:
- Which variation feels most like you?
- Want it sharper, shorter, or a different angle from the ones we explored?
- Tag the author, or add a source link at the end?

---

## gotchas

1. **Writing without the original post.** No post text = no real angle. Get it pasted first.
2. **Generic praise.** "Great post!" / "So true" / "Thanks for sharing" earns nothing and ranks nowhere. If that's all there is, advise skipping the comment.
3. **The mini-essay.** Too long to be read, too diffuse to react to — fails both hurdles. Keep it to a few lines; push detail below the fold.
4. **Burying the lede.** The one good line sitting in sentence four, below the "…more" cutoff. Front-load, always.
5. **Pitching in someone else's thread.** Punished by readers and the author. Value only.
6. **Restating the post.** Agreeing by repeating adds nothing to react to.
7. **Off-voice phrasing.** Comments are short, so one corporate or AI-cliché word stands out hard. Match the user's samples.
8. **Fabricating the fact.** A made-up ruling, number, or war story destroys trust instantly. Use a placeholder and have the user fill it.
9. **Link in line 1.** External links go last, and the comment must stand without them.
10. **Hijacking the author's tone.** Be a good guest — match the register, make the author look good for sparking it.

---

## the test

Before delivering, verify:

1. **The original post was read** — the angle responds to *this* post, not a generic template.
2. **Value is in the first 1–2 lines** — read only the first two lines: does the point fully land? If not, restructure.
3. **It's self-contained and reactable** — one concrete fact or one clear thesis a reader can like or reply to.
4. **It's short** — a few lines; any overflow is genuine supporting detail, not the payload.
5. **Voice matches the user's samples** — read it aloud against a sample. Match or miss?
6. **No generic praise, no pitch, no restatement.**
7. **No fabricated specifics** — every fact/number/experience came from the user or is flagged as a placeholder.
8. **Any link is last and optional.**

**Failure condition:** if the comment would get scrolled past (too long) or earn nothing (too generic), it failed. Tighten to one pointed line of real value.

---

## connector actions

After delivering, ask before taking any step — never act without explicit confirmation:

- **`~~chat`** — Send the draft comment to a Slack channel for a second opinion. Ask: which channel?

Prompt: "Want me to send this to Slack for a quick gut-check, or are you good to post it?"

## how this connects to other skills

**Feeds into this skill:**
- `business-interview` / `personal-interview` — capture voice + ICP into context so the gate is trivial.
- `viral-hooks` — the same hook patterns sharpen a comment's first line; pull one if the opener needs more bite.

**This skill feeds into:**
- `antislop` — optional final voice pass before posting (worth it even for short comments).

**Adjacent:**
- `linkedin-post` — for writing the user's *own* complete LinkedIn posts (this skill is for commenting on *other people's* posts).
