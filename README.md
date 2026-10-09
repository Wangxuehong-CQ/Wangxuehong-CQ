# Idemstasis

**磐石架构** — *idem* (the same) + *stasis* (standing).

An open research direction: treating the **continuity of an AI's identity** as
something that can be *measured*, rather than something asserted in a prompt.

---

## Why this direction

Most work filed under "AI memory" is work on **recall**: store text, retrieve
text, put text back into the context window. That is useful, and it is not the
problem I care about.

The problem I care about is narrower and, I think, harder: an assistant whose
identity holds across a long interaction, across new sessions, and across
change that would ordinarily reset it. Whether that is achievable is an open
question. I do not know the answer, and I am not going to claim in a README
that I do.

What I will say is narrower than a thesis: I do not think the difficulty is
where most of the current discussion places it. I am not going to name where I
think it is — that is one of the things the work is supposed to find out.

To show the *shape* of what I mean without giving anything away: a measurement
in this space looks like — put an assistant through a session boundary, ask it
the same identity-relevant question two different ways, record whether the
answers agree in the ways that matter, and compare the gap against an
assistant with nothing but a prompt-level assertion of continuity. That is
not my design; it is the *genre* of artifact this work is supposed to
produce — a number, with a measured zero-ability baseline next to it.

## Principles I hold myself to

1. **A claim I cannot reproduce is not a result.** Everything I publish has to
   be something a stranger can run.
2. **Before trusting a number, I ask what it would be if the ability were
   zero.** A metric that stays high when nothing is there is not evidence of
   anything.
3. **I publish my retractions.** When a result does not survive, it goes in the
   same place as the results that did.

None of the three tells you how to build anything. That is deliberate — they
are about not fooling myself, not about assembling a system.

## What I publish, and what I do not

**I publish:** the direction I am working in and why I believe the problem is
real; my research *method*; and the **by-products** — environment traps,
negative results, retracted claims, and small reusable checklists.

**I do not publish:** the design, or the parts that, written down, would let a
reader assemble the same thing on their own.

I state this boundary openly because a boundary you declare is worth more than
one you keep quiet about. If you are looking for a fully open implementation,
this is not it, and I would rather you knew that in the first paragraph.

## What you can check right now

Two small, self-contained repositories. Both runnable, neither depending on
anything above, and neither one requiring you to trust me:

- **[cpu-torch-segfault-bisect](https://github.com/Idemstasis/cpu-torch-segfault-bisect)**
  — a reproducible environment trap: a loss routed through a large vocabulary
  projection can terminate the process with no traceback. Contains the
  minimal reproduction and the bisection.
- **[experiment-hygiene](https://github.com/Idemstasis/experiment-hygiene)**
  — four checks that catch a metric announcing a capability that is not there,
  with two runnable toys and a retraction procedure. A real, in-place
  correction of one of my own statements lives in the other repository,
  under "Operational note".

These are the "show me one step" I would want if I were reading this page.
They are also the honest answer to "why should I believe there is anything
here": you should not, yet. Run them, or don't.

The fair objection is obvious, so I will make it myself: hygiene is not
evidence of a direction. These two repositories cannot tell you whether this
direction is promising — only what kind of operator you would be working
with. The direction-side evidence does not exist yet, and I would rather say
so than manufacture it.

## Who I am looking for

I am one person, without a team, working on a problem bigger than one person.
I am looking for three kinds of counterpart:

- **a principal partner** who wants to own part of this and work on it as a
  co-founder, not a contributor;
- **academic collaborators** on the measurement side — how to test identity
  continuity honestly, including how to falsify the claims I make;
- **organisations** with a real need for long-horizon continuity, whose
  requirements should shape what gets measured.

If one of those is you: open a thread in **GitHub Discussions under this
organization** — that is the only channel I am opening for now.

## Status

Early, and deliberately so. What exists publicly today is the by-products —
environment traps, negative results, and checklists. The research method
will be the next thing I publish. The architecture is being built and is not
public. I will keep publishing the by-products as I go, including the ones
that do not flatter me.

---

*The name states the question. It does not answer it.*

— maintained by **十二楼** (a pen name; authorship arrangements for academic
collaborators can be settled privately once we start talking)
