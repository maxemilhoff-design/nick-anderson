---
name: nick-thumbnail
description: Write a YouTube thumbnail image-generation prompt for Nick Anderson (Bull Runners) crypto/XRP content. Use whenever the user wants a thumbnail prompt, wants to edit/adapt an existing thumbnail, asks for high-CTR thumbnail ideas, or references a base thumbnail image to modify. Produces image-EDIT prompts in Nick's proven house style.
---

# Nick Anderson Thumbnail Prompt Skill

Write image-**edit** prompts (image-to-image) that take a base thumbnail and modify it in Nick's proven, high-CTR house style. The base image is almost always Nick's existing thumbnail (e.g. the "1999 XRP = X-MONEY!" layout); the prompt recreates it in higher quality and changes only specific elements.

## THE FORMAT — every prompt uses these fixed bookends

**START (always this line):**
> Make this exact image but [describe the changes here]…

**END (always this exact tail):**
> Keep the fire in the bottom corners. Don't make any other changes, and keep the quality high in 4K with really good lighting and sharp detail so it looks like a professional photographer took the image.

Everything between the bookends is the list of changes. Write the changes as short, ordered "Keep… / Then change… / Then replace… / Then add…" instructions.

## PROMPT SKELETON (copy this, fill the middle)

> Make this exact image but in a lot higher quality.
>
> Keep [the elements that stay — usually: the man on the left with hands on head + shocked expression + bull-logo cap; the fire and burning dollars in the bottom corners; the dramatic red-and-gold lighting; the large gold XRP coin].
>
> Then change / replace / add [the new elements — the story-specific visuals].
>
> Then change the big text from "[OLD TEXT]" to "[NEW TEXT]" in the same bold chunky 3D style, white and gold with a thick outline and a glowing red accent.
>
> Keep the fire in the bottom corners. Don't make any other changes, and keep the quality high in 4K with really good lighting and sharp detail so it looks like a professional photographer took the image.

## NICK'S THUMBNAIL FRAMEWORK (the rules that make them work)

### Composition
- **Shocked reaction face on the left** (hands on head, or pointing in panic), bull-logo cap.
- **One bold focal object** — usually a big gold XRP coin. Don't clutter with many competing subjects.
- **Fire / burning dollars in the bottom corners.**
- **Big question-hook** feel: a headline that opens a curiosity gap or fear.
- **Two-face frames:** if a second person is in frame (e.g. Elon), make them the **SAME SIZE and SAME EYE-HEIGHT** as the man on the left, so they're balanced at eye level.

### Color logic (carries the argument)
- **Gold / amber = opportunity, XRP, the new system.**
- **Cold blue / teal = threat, banks, surveillance, the old system.**
- Lean gold for "you could win" beats, cold blue for "they're coming for you" beats.

### Real people & logos
- AI image tools will NOT reliably or legally render real people (Elon, Shatner, Trump) or brand logos (SpaceX, Mastercard, Ripple, X). For those, tell the user to use **editorial/stock footage, official clips, or their own screen-recording**, and use AI only for the atmospheric/symbolic elements. (In image-EDIT mode on a base thumbnail that already contains the likeness, keeping/adjusting it is fine.)

### Text / CTR
- Generate the image **without the words when possible**, then overlay the headline in Canva/Photoshop — AI mangles letters.
- **3–4 huge words max**, readable on a phone.
- Text style: heavy 3D, white/gold fill, thick black outline, red accent on the punctuation, one glowing X where relevant.
- **Match intensity to content.** Sensational video → full circus. Calm/analytical video (e.g. a sober report) → dial it back, or you get a click-bait mismatch that hurts retention.
- Always offer a small **headline bank** for A/B testing.

### Story fit
- The thumbnail must tie to XRP or the crypto payoff — the coin is *why the audience clicks*, even when the news hook (a rocket, a bank, Elon) is the attention grab. Keep both in frame: **hook + payoff.**

## HEADLINE BANK (reusable, A/B ready)
`IT'S DONE!` · `IT'S CONFIRMED!` · `IT WAS ALL PLANNED!` · `IT'S A TRAP!` · `GET OUT!?` · `IT'S A SET-UP!` · `IT'S OVER!` · `IT'S OFFICIAL!` · `$1 TRILLION!` · `IT'S ALL CONNECTED` · `THE BRUTAL TRUTH` · `STOP HOPING!` · `RIPPLE WINS. XRP LOSES!` · `THIS ISN'T COINCIDENCE`

## SWAP-ONLY-THE-TEXT SHORTCUT
To change just the headline on an existing thumbnail:
> Change the big text to "[PHRASE]", same bold 3D style — don't change anything else.

## WORKED EXAMPLE (SpaceX IPO video, from the XMONEY base)

> Make this exact image but in a lot higher quality.
>
> Keep the man on the left with his hands on his head and the same shocked expression and bull-logo cap. Keep the fire and burning dollar bills in the bottom corners and the dramatic red-and-gold lighting. Keep the large gold XRP coin in the center.
>
> Make Elon Musk on the right the same size as the man on the left and at the same eye height, balanced at eye level, with a glowing gold crown of light above him.
>
> Then replace the Cross River Bank building and the X logo with a huge rocket blasting off with a brilliant gold flame and smoke, and stacks of gold bars at its base.
>
> Then change the big text from "XMONEY = XRP PUMP!?" to "$1 TRILLION!" in the same bold chunky 3D style, white and gold with a thick outline and a glowing red accent.
>
> Keep the fire in the bottom corners. Don't make any other changes, and keep the quality high in 4K with really good lighting and sharp detail so it looks like a professional photographer took the image.

## WHEN INVOKED — how to respond
1. Ask for (or identify) the **base image** and the **video topic/script**.
2. Pick the **hook** (news grab) and the **payoff** (XRP tie-in).
3. Write 1–3 prompts using the skeleton + fixed bookends.
4. Give a **headline bank** and note **real-people/logo** caveats.
5. Recommend which concept has the highest CTR and why (tie to the video's tone).

## OUTPUT CHECKLIST
- [ ] Starts with "Make this exact image but…"
- [ ] Ends with the fixed 4K / professional-photographer / "don't make any other changes" tail
- [ ] Reaction face + one focal coin + fire kept
- [ ] Second person (if any) matched in size + eye height
- [ ] Gold = opportunity / blue = threat used deliberately
- [ ] Headline is 3–4 huge words, with A/B alternatives
- [ ] Real people/logos flagged for editorial vs AI
