# investor-recon

A threat-intelligence approach to VC meetings. Built with Claude Code.

I spent 12 years doing threat intelligence. The job was simple to describe. Build a picture of an adversary before they ever know you are looking. Their patterns, their gaps, their next move.

A VC meeting is the same problem.

Most founders prep by rehearsing their pitch. That is backwards. The pitch is not where the decision happens. The fund builds a thesis about you before you walk in. The meeting is where they confirm it.

So stop rehearsing. Run recon.

This is the system I use. Six prompts. About 25 minutes per investor. Drop them into Claude Code, fill the blanks, get a brief.

## What it produces

- **Thesis brief.** What this fund actually backs. Stage, sector, check size, the pattern across their last ten deals. Not what their homepage says. What their behavior says.
- **Portfolio map.** Where you fit. Where you collide with a company they already own. Where the gap is that you fill.
- **Question set.** The questions they will ask, derived from their thesis and your stage. Not generic. Theirs.
- **The hesitation.** The single thing about your company that makes this specific fund pause. Every founder has one. You want to know it before they do.
- **The counter.** How you answer the hesitation before they raise it.
- **The room read.** What they are confirming about you. What to walk in already knowing.

## Quickstart

1. Open Claude Code (or any Claude chat).
2. Open [`SYSTEM.md`](SYSTEM.md).
3. Run the six prompts in order. Paste in the fund's site, the partner's writing, your deck.
4. You get a brief. See [`example-brief.md`](example-brief.md) for what it looks like filled in.

No setup. No API key. No account. Copy, paste, run.

## Why this works

Threat intel taught me one thing. The side that does the homework controls the room. Not the louder side. Not the more polished deck. The side that already knows what the other side is thinking.

A founder who walks in knowing the fund's hesitation is not pitching anymore. They are confirming a thesis they shaped.

## Who built this

I build custom AI systems for founders and small teams. This repo is the free, lighter version of the work I do paid.

If you want the meeting-prep system wired into your actual fundraise, or you have a different operational problem an AI system should be doing for you, that is the consulting. Reach me at assaf@askconsulting.io.

## License

MIT. Use it, fork it, ship it. See [`LICENSE`](LICENSE).
