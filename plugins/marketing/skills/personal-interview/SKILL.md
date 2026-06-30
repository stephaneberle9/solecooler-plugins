---
name: personal-interview
description: Onboard a Solecooler colleague with a short 5-question interview and produce their personalized Global Instructions overlay. Invoke directly with /personal-interview — do not trigger automatically.
disable-model-invocation: true
---

# Personal Interview

Load the `company-context` and `company-instructions` skills before starting — they are your complete company context. Do not ask the user about anything already covered there.

You are helping a Solecooler colleague set up their **personal Global Instructions overlay**. Collect only what's personal: their role, product/service focus, any additional offerings they cover, their specific proof, and any voice adjustments.

---

## Interview Instructions

Open with this exact line:
"The shared Solecooler context is already loaded — company, all products, ICPs, competitors, proof, and Voice DNA. I just need 5 quick things from you to build your personal overlay. Let's go."

Ask ONE question at a time. Wait for the answer. Acknowledge in one line. Move on. Fewer than 5 questions is fine if answers make some redundant.

---

**Q1 — Name + Role:**
"What's your name and role at Solecooler? One sentence on what you're actually responsible for day-to-day. (Your LinkedIn headline or About section is a great source — paste it in if you have it handy.)"

---

**Q2 — Product/Service Focus:**
"Which of Solecooler's products are you primarily working with? The shared context covers the ClimFeet range (ClimFeet, ClimFeet Perf, ClimFeet+) and WarnFeet. Are there others you focus on — a specific market (pro/outdoor, sport, medical), a distribution channel, or anything else not in that list?"

If they mention additional offerings, ask ONE follow-up only:
"For [the new offering]: who's the ideal customer, what's their key pain, and what transformation do you promise? Rough pricing if you have it."

---

**Q3 — ICP Nuances:**
"For the products you focus on — anything about your specific customers that the shared ICP descriptions miss? Different industry vertical, different persona, different pain angle, or objections you hear that aren't listed?"

---

**Q4 — Personal Proof:**
"What proof can you personally cite in your area? Named clients, specific results, testimonials, case studies — anything real. Even 1-2 items."

---

**Q5 — Voice Adjustments:**
"The shared Voice DNA is your base. Anything you'd add, change, or override? Words you always use, words you'd never touch, or a sample of your own writing you want me to learn from?"

---

## Output

**Critical rule:** The output contains only personal additions and overrides. Never copy or embed content from the `company-instructions` or `company-context` skills — that content is already available to Claude separately. If a section has nothing personal to add, say so in one line rather than reproducing shared content.

After all answers, output a single fenced code block using this exact structure. Fill every section — use [NONE YET] where real content is missing:

```
# Personal Global Instructions Overlay
# [Full Name] — [Role] at Solecooler
# Last updated: [today's date]

> Personal overlay — apply together with the Solecooler Company Instructions.
> This file adds/overrides only what's specific to me.
> Shared context covers: company overview, all products (ClimFeet range + WarnFeet), ICPs, competitors, proof, and Voice DNA.

---

## About Me

[Name], [Role] at Solecooler.
[1-2 sentences from Q1 on day-to-day responsibilities.]

## My Product/Service Focus

Primary focus: [list products/services from the shared context they focus on]

[Only include this section if they mentioned additional offerings not in the shared context:]
### Additional Offerings

#### [Offering Name]
**Offer:** [What it is]
**Price:** [If known, otherwise: TBD]
**Transformation:** [One-line outcome promise]
**Ideal Customer:** [Who they are, what they've tried, key pain]
**Key Objections:** [Top 2-3 reasons someone says no, or NONE YET]
**Proof:** [What they can cite, or NONE YET]

## My ICP Nuances

[Additions or corrections to the shared ICP descriptions specific to this person's focus and customer experience.]
[If nothing to add: "No additions — shared ICP descriptions apply as-is for my focus areas."]

## My Personal Proof

[Proof beyond what's in the shared section. Format: Client name — result or quote — context.]
[If none: NONE YET]

## Voice Adjustments

[Any additions or overrides to the shared Voice DNA.]
[If they provided writing samples, paste 2-3 sentences as ground-truth rhythm reference.]
[If none: "No adjustments — shared Voice DNA applies as-is."]

## Key Instructions for Claude (Personal Layer)

- Apply the Solecooler Company Instructions as the base for all content. Do not reproduce shared content here — reference it by name.
- My primary product focus is: [list]
- Speak to the ICP nuances above when writing for my specific audiences.
- [Any additional personal-layer overrides from the interview.]
- Never fabricate testimonials, results, or case studies. If a specific isn't in my proof above or the shared proof section, mark it [PLACEHOLDER — needs real X].
```

After the code block, say:
"Done. Paste this into Settings → Cowork → Global Instructions. It works as an overlay on top of the shared company context your admin distributes separately."
