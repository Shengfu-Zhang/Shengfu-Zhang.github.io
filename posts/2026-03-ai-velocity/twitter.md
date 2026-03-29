**Tweet 1 (hook)**
AI writes 90% of our code now.

So why doesn't delivery feel faster?

We sped up the wrong part. 🧵

---

**Tweet 2**
Code generation got fast.
Code review didn't.

PR volume ↑
Reviewer confidence ↓
Revision rounds: still 3–5 per PR

We added a faster engine but forgot the road has a speed limit.

---

**Tweet 3**
The hidden problem: same agent, same codebase, same task → wildly different outputs depending on who's driving.

It's not a talent gap. It's a systems gap.

Fix the system, compress the variance.

---

**Tweet 4**
Mental model that changed how I think about this:

Software delivery is a pyramid.
- Top floors: abstract, human-heavy, AI can't lead
- Bottom floors: concrete, bounded, AI can own

Floor 0 = code. That's where we are. That's where we fix first.

---

**Tweet 5**
Each floor should be a standalone system. Loosely coupled. No hard dependencies.

Floor above passes an artifact down.
Floor below executes and returns output.
Human sits at the interface — reviewing, sampling, deciding.

When Floor 0 is reliable, you move up. Layer by layer.

---

**Tweet 6 (closer)**
We're checking every tire by hand, every day.

The goal: a system that emits signals. Where review is a sample check, not a manual inspection.

That's the actual productivity unlock. Not faster generation — more trusted output.

Full write-up on my blog 👇
[link]
