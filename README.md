# investor-recon

A threat-intelligence approach to VC meetings. Runs in Claude Code, searches the fund's real material, and refuses to make things up.

I spent 12 years doing threat intelligence. The job was simple to describe. Build a picture of an adversary before they ever know you are looking. Their patterns, their gaps, their next move.

A VC meeting is the same problem.

Most founders prep by rehearsing their pitch. That is backwards. The pitch is not where the decision happens. The fund builds a thesis about you before you walk in. The meeting is where they confirm it.

So stop rehearsing. Run recon.

## The rule that matters

This searches the real internet for the fund's material and cites every claim. If it cannot find something, it says "Not found." It never guesses the fund's deals, thesis, or check size from the name. A confident wrong brief walks you into the wrong room. That is worse than no brief.

This is why it runs in Claude Code, not a chat box. Claude Code can actually search and fetch. A plain chat guesses, and you cannot tell. The grounding is the product.

## What it produces

- **Thesis brief.** What this fund actually backs, quoted from their own material, with links. Their words separated from your read of their deals.
- **Portfolio map.** Where you fit, which portfolio company you collide with, the gap you fill.
- **Question set.** The questions this partner will ask, from their cited thesis and your stage.
- **The hesitation.** The single thing about your company that makes this specific fund pause.
- **The counter.** How you answer it before they raise it.
- **Sources and gaps.** Every link used, and an honest list of what it could not confirm.

## Use it (two ways)

**Easiest, no install.** Open Claude Code, then copy the block in [`PASTE-THIS.md`](PASTE-THIS.md) and paste it in. It asks you two questions and runs. Full setup steps (including the folder step Claude Code asks for) are in that file.

**As a command.** Install the plugin:

```
/plugin install github:assafkip/investor-recon
```

Then run `/investor-recon` in any Claude Code session.

See [`example-brief.md`](example-brief.md) for what a finished brief looks like.

## Who built this

I build custom AI systems for founders and small teams. This repo is the free, lighter version of the work I do paid. If you want it wired into your actual raise, or a different operational problem an AI system should be handling, reach me at assaf@askconsulting.io.

## License

MIT. See [`LICENSE`](LICENSE).


---

## Built by Assaf

I spent 12 years in threat intelligence watching teams find the same failure and fix it four times. The learning never stuck. I build tools that make it stick.

This is the free version. The paid kits live at [claudedaddy.io](https://claudedaddy.io).

**Want this wired into your team's repo, or a heavier spec-and-review pipeline?** That's the consulting. [Book a call.](https://calendar.app.google/cMFvhvDsfi9iyWYy9)
