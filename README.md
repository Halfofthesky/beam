# BEAM

**B**ackground · **E**xhibit · **A**rgument · **M**ethod

A Claude skill that maps what each source is *doing* in a text, and shows which jobs nobody is doing.

<img width="750" height="409" alt="beam_card_overprint_1600x900" src="https://github.com/user-attachments/assets/7ff55e94-4b51-44da-8273-6baf257b7091" />


## Why

Most source checks ask whether a source is reliable or a claim is true. BEAM asks a different question: what is this source doing here, and is it fit for that job?

A text can cite only accurate, credible sources and still fail because they are in the wrong roles:

- a sharp analysis that joins no debate, so it says only "this is more complicated than it looks";
- a literature review with nothing new to analyse;
- a contested claim cited as settled fact;
- a theory whose vocabulary runs the whole paper but is never acknowledged.

Counting sources won't catch any of this. Looking at their roles will.

## The four roles

Roles are assigned by use, not by type of source. The same article can be Background on one page and an Argument on the next.

| Role | The writer… | Test |
|---|---|---|
| **B**ackground | relies on it | Is its claim treated as settled fact? |
| **E**xhibit | interprets it | Does the text work to establish what this material means? |
| **A**rgument | engages it: affirms, disputes, refines, extends | Is the source's own claim the thing under discussion? |
| **M**ethod | follows it | Does it supply the concepts or procedure the writer works with? |

## What it does

Give Claude a text and say what you want:

- **Audit** your own draft: a role map, a diagnosis of the overall profile, flagged problems with locations, and suggested revision moves. It does not rewrite your text.
- **Read** someone else's text: how it handles its sources, where its stance toward a source shifts, and what that reveals about the argument.
- **Plan** a project: which roles your question and materials already fill, and what to look for next.

**Flags:**
- F1: a contested claim cited as background
- F2: an exhibit quoted but never interpreted
- F3: a debate named but never engaged
- F4: a source used as method in one place and disputed in another, with the tension unaddressed
- F5: an uncited method
- F6: second-hand authority
- F7: an ambiguous role

Ambiguous roles are flagged with both readings, never forced into one.

The core rule of thumb, from Bizup: **if you start from an exhibit, look for arguments to engage; if you start from arguments, look for an exhibit to interpret.**

## Example prompts

```
Run BEAM on my draft. Genre: journal article in sociology.
Use BEAM to read this article: how does it handle its sources?
I have this question and these six sources. BEAM-plan it.
```

It works in any language. Role letters stay B/E/A/M.

## Install

**Claude (web, desktop):** download [`beam.zip`](https://github.com/Halfofthesky/beam/releases/latest/download/beam.zip), then go to **Customize → Skills → + → Create skill → Upload a skill**. Code execution must be on in Settings → Capabilities.

**Claude Code:** copy the `beam/` folder into `~/.claude/skills/`.

**Other tools:** [`beam/SKILL.md`](beam/SKILL.md) is plain Markdown and can be used as a prompt.

The latest [release](https://github.com/Halfofthesky/beam/releases/latest) has `beam.zip`, `beam.skill` (same archive) and `SKILL.md`.

## Source

Joseph Bizup, "BEAM: A Rhetorical Vocabulary for Teaching Research-Based Writing," *Rhetoric Review* 27.1 (2008): 72–86. [doi:10.1080/07350190701738858](https://doi.org/10.1080/07350190701738858)

Roles, profiles and flags F1, F2, F5 and F6 follow Bizup. F3 and F4 are extensions. The skill is not affiliated with the author.

## See also

- [Concept Check](https://github.com/Halfofthesky/concept-check): tests whether a concept earns its place.
- [Evidence Tests](https://github.com/Halfofthesky/evidence-tests): weighs the evidence for causal claims against rival explanations.
- [Stasis](https://github.com/Halfofthesky/stasis): finds where a disagreement sits and whether the text meets it there.
- [Logic & Reasoning Skills](https://github.com/Halfofthesky/logic-reasoning-skills): reconstructs arguments, spots fallacies, solves formal logic.
- [Adversarial Editorial Review](https://github.com/Halfofthesky/adversarial-editorial-review): three reviewers and an editorial synthesis for humanities manuscripts.

## License

MIT
