# We Sped Up the Wrong Part: What AI Coding Tools Actually Changed (and What They Didn't)

*By Shengfu Zhang*

---

I've been thinking about a paradox that's been living in my head for the past year.

AI coding agents now generate roughly 90% of the code on my team. Ticket velocity is up. Features ship faster. If you look at a dashboard, things look great.

But when I talk to engineers — really talk to them — almost everyone says the same thing: *it doesn't actually feel faster.*

Here's why: we sped up generation. We didn't speed up delivery. And those are not the same thing.

---

**The bottleneck moved, but we didn't notice**

Before AI, the constraint was writing code. That's where time went — thinking through implementation, typing it out, debugging.

AI mostly solved that. But it created a new constraint nobody talked about enough: **code review**.

The volume of PRs went up. The uncertainty of AI-generated code meant reviewers felt they had to be *more* careful, not less. So review rounds stayed at 3 to 5 per PR — exactly where they were before AI adoption.

We added a faster engine but forgot the road has a speed limit.

---

**The variance problem nobody is talking about**

Here's something I found genuinely surprising. Give the same agent, the same codebase, and the same task to two different engineers. You'll get surprisingly different results.

Not because one is smarter. But because one knows how to *steer* an agent.

A skilled prompter provides rich context upfront, decomposes the problem cleanly, and gets a near-correct result in one pass. Someone less experienced iterates 15 times, loses context mid-loop, and ends up with lower-quality output — despite more effort.

This is not a talent gap. It is a **systems gap**. And systems gaps can be closed.

If the scaffolding around an agent is tight enough — good steering files, clear conventions, well-scoped tasks — the starting point for every engineer is roughly the same. The variance compresses. The output becomes more predictable.

That's the actual problem worth solving. Not "how do we get AI to write better code" — but "how do we build a system where the quality of AI-generated code is consistent regardless of who's driving."

---

**Think of it as a pyramid, not a pipeline**

I've started thinking about software delivery as a pyramid. At the top: company goals, roadmaps, product decisions — abstract, human-heavy, hard for AI to touch. At the bottom: code, tests, review — concrete, bounded, increasingly AI-owned.

The lower you go, the more AI can help. The higher you go, the more human judgment is irreplaceable.

Most teams are focused on the bottom floor right now — and that's right. But the insight I keep coming back to is that **each floor should be a standalone system**, loosely coupled to the ones above and below it. No hard dependencies. A floor above passes down an artifact — a spec, a contract, a task. The floor below executes it and returns an output. A human sits at the interface, reviewing the output and deciding whether to pass the signal upward.

When you build it this way, something interesting happens. The bottom floor can become autonomous. It runs like a factory. You don't live in it anymore — you observe it, monitor its health signals, and occasionally sample-check it. Then you move up to the next floor, which becomes the new frontier.

Layer by layer. Bottom up.

---

**The transformer analogy that won't leave my head**

I'm an engineer, so I can't help mapping this onto something technical: this is exactly how you train a neural network.

Each floor of the pyramid maps to a layer of a transformer. The feedback from code review is backpropagation. You stabilize the bottom layer, let the signal propagate upward, then tackle the next layer. You don't skip layers. You don't rush to the top. You earn trust at each level before moving up.

We're not just using AI to write code. We're building the training loop for our entire engineering organization.

---

**What I think needs to happen next**

Two things, running in parallel:

First, every engineer needs to treat steering files as a living artifact. After every PR, ask the agent: *what did you learn from the review feedback? What should we update in our steering files?* Small habit, compounding return.

Second, senior engineers need to spend real time — not 10%, maybe 30–40% — building the harness. Custom lint rules with agent-readable error messages. Test conventions tied to user stories, not branch coverage. Guardrails that catch issues at build time, before anyone has to review them.

The goal is to get to a state where the system emits signals. Where you can look at a dashboard and trust that Floor 0 is healthy. Where review becomes a sample check, not a manual inspection of every tire.

Right now, we're checking every tire by hand, every day. That's where I'm trying not to stay.

---

*I'm Shengfu Zhang — an engineer thinking about how AI is reshaping the way we build software. If this resonated, I'd love to hear how your team is navigating the same tension. Follow along for more.*
