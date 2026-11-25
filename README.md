# B2B Demo Page Prompt Kit

A free kit for briefing an AI website builder to draft a B2B "book a demo" or "request a walkthrough" page: v0, Lovable, Bolt, Cursor, Windsurf, Claude, ChatGPT, Gemini, Replit, GitHub Copilot, Framer AI, Google Stitch, Readdy, Aura.build or OpenAI Codex.

This is not a pack of finished marketing pages, and it is not a generic homepage template. It is the fact sheet, constraints and review list that usually decide whether the first draft is a usable demo request page, or a SaaS cliché with invented logos and a `#` calendar link.

> **Disclosure:** this repo is maintained by people who work on VibUI, a paid website prompt library. Everything in this repo is free to use under CC0 (public domain). The paid library is mentioned once, in [Other resources](#other-resources).

**Short answer:** before you prompt an AI builder for a demo page, write down who the demo is for, what happens after the form is submitted, which calendar or form you actually use, and which claims you can defend. Forbid invented customer logos, metrics and quotes. Then review the draft on a phone and complete a test submission. This kit still works if you never open a commercial catalogue.

## Contents

- [How to use this repo](#how-to-use-this-repo)
- [1. Fact sheet](#1-fact-sheet)
- [2. Reusable constraint blocks](#2-reusable-constraint-blocks)
- [3. Page checklist](#3-page-checklist)
- [4. Starter prompt](#4-starter-prompt)
- [5. After-generation review](#5-after-generation-review)
- [6. Where to paste the prompt](#6-where-to-paste-the-prompt)
- [Other resources](#other-resources)
- [FAQ](#faq)
- [License](#license)

## How to use this repo

1. Copy the [fact sheet](#1-fact-sheet) into a document and fill every row you can. Leave the rest marked `[PLACEHOLDER]`.
2. Tick the [page checklist](#3-page-checklist).
3. Paste the [constraint blocks](#2-reusable-constraint-blocks) you need under your brief.
4. Drop the facts and constraints into the [starter prompt](#4-starter-prompt).
5. Generate once, then run the [review](#5-after-generation-review), including a real test submission, before you share the URL.

If a fact is missing, do not let the model invent it. A blank placeholder is cheaper than a logo you have to take down, or a calendar that emails nobody.

## 1. Fact sheet

| Fact | Your notes |
|---|---|
| Product name and one-line description in plain language | |
| Who a demo is for (role, company type, situation) | |
| Who a demo is *not* for (so the wrong lead can leave) | |
| What the visitor is booking (a product walkthrough, a scoping call, a technical deep-dive) | |
| Length of the meeting, and who from your side attends, if you will say this | |
| What happens after they submit (calendar invite, email from a person, a form in a queue) | |
| The real booking URL, calendar embed, or form endpoint you have tested | |
| Timezones you will honour, and any limits (weekdays, no same-day, specific regions) | |
| Form fields you actually need, and why (name, work email, company, role, anything else) | |
| Fields you will *not* require on the first step (do not copy a twelve-field "lead gen" pattern by habit) | |
| Pricing you are willing to publish, or "pricing is discussed on the call" if that is true | |
| Proof you have permission to use (named customers, quotes, logos, screenshots) | |
| Security, compliance or residency facts you will stand behind, with a link to the real page if any | |
| Integrations you actually support, not a hoped-for list | |
| Facts that must not appear (user counts, "trusted by" logos, awards, invented case studies) | |
| Visual tokens, or "keep it calm, do not invent a loud campaign identity" | |
| Existing nav or footer the page must match, if any | |

The prompt is only as good as this sheet. If you do not yet have a working booking path, build that first. A handsome page with a dead form is not a demo page.

## 2. Reusable constraint blocks

Append the blocks you need. Delete the ones that do not apply.

**Do not invent proof**

```text
Use only the customer names, logos, quotes, metrics and awards I paste.
If I have not provided a piece of proof, omit that element. Do not add a logo wall, a testimonial slider, a "trusted by N teams" line, or a made-up case study.
```

**Booking path**

```text
The primary action is [Book a demo / Request a walkthrough] and must use this destination: [URL or embed instructions].
Do not invent a second calendar, a chatbot, or a "we'll call you tomorrow" promise I did not write.
If the destination is a placeholder, label the button clearly as inactive and do not pretend it books a meeting.
```

**Form fields**

```text
The form may only include these fields: [list].
Every field has a visible label. Required fields are marked. Do not add hidden questions, a budget field, or a "how did you hear about us" dropdown unless I listed them.
The form must be completable with a keyboard, and usable on a phone.
Say next to the submit button what happens after they send it, using my wording: [ ].
```

**Who it is for**

```text
Include a short "this demo is for / this demo is not for" pair, using only my text.
Do not replace it with vague language like "teams of all sizes" unless I wrote that.
```

**Security and compliance**

```text
If a security, privacy, residency or certification line appears, use only the wording and links I paste.
Do not invent SOC / ISO / "bank-grade" / "GDPR compliant" claims, or a trust badge I did not supply.
```

**Accessibility and tone**

```text
One h1, logical heading order, 4.5:1 contrast for text, visible focus styles, labelled controls, a skip link to main.
No autoplay video, no countdown, no exit-intent popup.
Voice: plain and specific. Do not use "synergy," "unlock," or "transform your workflow" unless I pasted those words.
```

## 3. Page checklist

Use this as a section list, not as a requirement to fill the whole viewport.

- [ ] Header with product name and a way back to the main site, if one exists
- [ ] One-sentence explanation of the product
- [ ] Who the demo is for, and who it is not for
- [ ] What the demo covers, and how long it is, if you will say so
- [ ] The primary action, above the fold and again near the end
- [ ] The form or calendar, with the fields you actually need
- [ ] What happens after they submit
- [ ] Optional: a short, permissioned customer note or screenshot
- [ ] Optional: a link to pricing, security, or docs — only if those pages exist
- [ ] FAQ you have written (scheduling, who should attend, recording, language)
- [ ] Footer with legal links you already have

If you also need a homepage or a pricing page, brief those separately. A "book a demo" prompt that tries to rebuild the entire marketing site usually produces a generic kit with a form at the bottom.

## 4. Starter prompt

```text
Build a single "book a demo" page for [PRODUCT], a [one-line description] for [AUDIENCE].
Page job: help a qualifying visitor decide whether to request a walkthrough, and complete that request.
Primary action: [Book a demo] using [TESTED URL OR EMBED]. Do not invent a second CTA.

Who it is for: [ ]. Who it is not for: [ ].
What the demo is: [length, format, who attends], in my wording.
What happens after they submit: [ ].

Form fields (only these): [list].
Pricing I will publish: [paste, or "do not show prices; say that pricing is discussed on the call"].
Proof I have permission to use: [paste, or "no proof section"].
Security or compliance lines I will stand behind: [paste, or "omit this section"].

Sections in this order: [header; hero with the one-line description and the primary action; this-is / this-is-not; what the demo covers; booking form or calendar; optional proof; FAQ I paste; footer].

Visual system: [tokens, or "calm, readable, no gradient hero, no stock office photography"].
Use only the copy I paste. Mark gaps as [PLACEHOLDER].

Constraints:
[paste the blocks you need from section 2]

Accessibility: one h1, logical headings, 4.5:1 contrast, visible focus, labelled fields, usable on a phone.
Do not add autoplay video, a chatbot, a countdown, or a logo wall I did not supply.
```

## 5. After-generation review

- [ ] Every customer name, logo, metric and quote is on the fact sheet, or the section is absent
- [ ] The button or form goes to the tested destination, not a `#` link
- [ ] You completed a test submission, and the result was what the page promised (invite, email, queue)
- [ ] Form labels are visible; required fields are honest; the form works on a phone and with a keyboard
- [ ] "Who it is for / not for" is still your wording
- [ ] No invented security badge, user count, or "used by leading companies" line
- [ ] Pricing language matches what sales will actually say
- [ ] Contrast, heading order and focus styles pass a quick pass
- [ ] There is a way to reach a person if the calendar fails
- [ ] Someone who did not write the prompt has read the page once

If several items fail, fix the brief and regenerate the section. Do not hand-patch invented logos into "good enough."

## 6. Where to paste the prompt

This brief is tool-agnostic. Paste it into v0, Lovable, Bolt, Cursor, Windsurf, Claude, ChatGPT, Gemini, Replit, GitHub Copilot, Framer AI, Google Stitch, Readdy, Aura.build or OpenAI Codex. If the tool accepts images, attach real screenshots *after* the written facts, and say that the written facts win when the two disagree.

## Other resources

- Keep a private `prompts.md` of briefs that already worked for you. A short personal file beats a large catalogue you have not read.
- If you also need a general pre-flight checklist for other page types, use a checklist you already trust. This repo is only the demo-page kit.
- If you want a larger commercial catalogue of starting briefs, [VibUI](https://vibui.dev) has 2,852 website prompt templates: 775 full pages, 1,100 sections, 817 components and 160 animated backgrounds, with about 1,000 also including source code. Yearly and lifetime plans also include 2,407 AI video prompts. Pricing is one-time with no auto-renewal: $48 quarterly, $99 yearly, $179 lifetime (shown as reduced from $384). There are 60 free samples, and a free account can copy 2 prompts, which is enough to run one brief through this kit before you decide to pay. Skip it if the fact sheet and prompt above already cover the page you need.

## FAQ

**Can I use this commercially?**

Yes. It is CC0. No attribution needed.

**Should the form be long, so sales can qualify the lead?**

Only require fields you will actually use before the meeting. Extra questions you ignore in the inbox waste a visitor's time and often reduce completions. You can ask follow-ups after the booking, in the confirmation email, if you need them.

**What if we do not have a calendar tool yet?**

Stand up a real path first: even a monitored form that sends you an email, plus a sentence about when you will reply. Then brief the page. Do not ship a decorative "pick a time" widget that does not book anything.

**Will a better demo page book more qualified meetings?**

This kit will not promise that. It can help you ship a clearer page, with a working request path and claims you can defend. Outcomes still depend on the product, the audience and the follow-up after the form is submitted.

**Can I contribute?**

Yes. Open a pull request that adds a constraint block, a fact-sheet row, or a review tick, and that does not introduce invented example metrics.

## License

[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/). Use, modify and share without restriction.
