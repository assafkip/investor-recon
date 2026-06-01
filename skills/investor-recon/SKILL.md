---
name: investor-recon
description: Build a grounded recon brief on a venture fund before a founder meeting. Searches the fund's real public material (site, portfolio, partner writing, recent deals), maps the founder's company against it, predicts questions, finds the fund's likely hesitation, and writes a one-page brief. Every claim about the fund is cited. Refuses to guess. Use before a VC meeting or when researching an investor.
argument-hint: "[fund-name]"
allowed-tools: WebSearch, WebFetch, Write, Read, Glob
---

# Investor Recon

Prep for a VC meeting the way an analyst preps a dossier. Build a picture of the fund from what is public, before the meeting. Ground every claim in a real source. Never invent.

## The one rule that matters

This skill exists because guessing about an investor is worse than knowing nothing. A confident wrong brief walks the founder into the wrong room.

- Every claim about the fund must trace to a source you actually fetched. Cite the URL.
- If you cannot find something, write "Not found." Do not infer the fund's deals, thesis, or check size from the fund name. Do not pattern-match from "funds like this."
- When sources disagree, show both and cite both. Do not pick one and assert it.
- Separate two things clearly: what the fund SAYS (their words, quoted, cited) and what the deals SUGGEST (your read). Label which is which.
- The founder-specific analysis (the hesitation, the counter) is reasoning, not fact. Label it as analysis.

If you break this rule, the tool is worse than useless. It is a liability.

## Step 1: Intake

Ask the user and wait for answers:

1. **Which fund?** Name. (If passed as `$ARGUMENTS`, use it but still confirm.)
2. **Which partner** are they meeting, if known?
3. **Your company.** Name, what you do, stage, the one or two traction facts you would share. This is required. The hesitation and the questions cannot be built without it.
4. **The ask.** What are you raising, roughly, and what round?

## Step 2: Recon (search and fetch the real material)

Do real searches and fetches. Cite every source.

1. `WebSearch` the fund name plus "portfolio", "thesis", "investments". 
2. `WebFetch` the fund's own site: the homepage, the portfolio page, any thesis or "how we invest" page. Pull their words, quoted.
3. `WebSearch` the partner's name plus "essay", "blog", "interview", "thesis". `WebFetch` what you find. Pull what this partner personally cares about, in their words.
4. `WebSearch` for the fund's recent investments. Try the portfolio page first, then sources like Crunchbase, news, fund announcements. List the deals you can actually confirm, each with a source.
5. Note the gaps. If you cannot confirm check size, stage, or recent deals, say "Not found" and move on. Do not fill it in.

**Checkpoint:** Give the user a short summary of what you found and what you could not. Ask if they have material to paste (a deck the partner wrote, a private portfolio list) before you analyze.

## Step 3: Analysis

Build these from the cited material plus the founder's company. Label stated-vs-inferred and fact-vs-analysis throughout.

- **Thesis brief.** What this fund backs, by behavior, not just the homepage line. Stage, sector, check size, the pattern across confirmed deals. Cite each claim. Flag where stated thesis and actual deals diverge.
- **Portfolio map.** Where the founder fits the thesis cleanly. Which portfolio company they collide with (competitive or overlapping). The gap they fill. Name the specific companies, cited.
- **Question set.** The 8-10 questions this partner is most likely to ask, derived from the cited thesis and the founder's stage. For each: the question as the partner would phrase it, what it tests, the shape of a strong answer.
- **The hesitation.** The single biggest reason THIS fund pauses on THIS company. One sentence, the way the partner would say it to their team. This is analysis, label it.
- **The counter.** How the founder surfaces and answers the hesitation before it is raised. The line to say, the evidence, and what not to say.

## Step 4: Report

Write a one-page brief to `output/investor-recon-[fund]-YYYY-MM-DD.md` (create `output/` if needed). Include:

- The thesis the fund is confirming about the founder when they walk in
- The 3 things to land
- The hesitation and the counter, one line each
- The 3 most likely questions with the shape of the answer
- One specific, cited thing about the portfolio or partner to reference naturally
- A **Sources** section listing every URL used
- A **Not found** section listing what could not be confirmed

Tell the user where it saved. Offer to dig deeper on any section.

## Rules recap

- Cite every fund claim. "Not found" beats a guess.
- Stated thesis (quoted, cited) is separate from inferred pattern (your read).
- Source conflicts get shown, not resolved by assertion.
- The founder's company info is required before analysis.
- If a search returns nothing useful, say so. Do not pad.
