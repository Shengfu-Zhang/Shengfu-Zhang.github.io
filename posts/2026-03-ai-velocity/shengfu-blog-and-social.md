# Content Package — Shengfu Zhang
*Blog + Social Media Posts | Q1 2026*

---

## 1. BLOG POST (Substack)
*~800 words | English | Personal voice, 2/3 technical*

---

### We Sped Up the Wrong Part: What AI Coding Tools Actually Changed (and What They Didn't)

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

---
---

## 2. LINKEDIN POST
*English | ~200 words | Thought leadership hook*

---

We sped up the wrong part of software delivery.

AI coding agents now generate ~90% of code on most teams. Velocity metrics look great. But ask engineers how it *feels* — almost everyone says the same thing: it doesn't actually feel faster.

Here's why: we sped up generation. We didn't speed up delivery.

Code review became the new bottleneck. PR volume went up. Uncertainty of AI-generated code meant reviewers felt they had to be *more* careful, not less. Revision rounds stayed at 3–5 per PR — same as before AI adoption.

We added a faster engine but forgot the road has a speed limit.

The fix isn't reading more lines. It's building a system you can trust:
→ Steering files that get smarter after every PR
→ Custom lint rules that catch issues before review
→ Tests that prove intent, not just coverage
→ Signals that tell you the factory is healthy without manual inspection

The goal: reduce CR rounds from 3–5 to 1–2. Not by lowering the bar — by raising the floor.

I wrote up the full mental model — pyramid architecture, the transformer analogy, the two feedback loops — on my blog. Link in comments.

What's your team's biggest bottleneck right now — generation or review?

*#AIEngineering #SoftwareEngineering #DeveloperProductivity #AITools*

---
---

## 3. X / TWITTER THREAD
*English | 6 tweets | Punchy, opinionated*

---

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

---
---

## 4. 小红书 POST
*中文 | 轻松、有共鸣、有干货 | ~400字*

---

**标题：用了AI写代码，为什么反而感觉没变快？**

---

最近和很多工程师聊，大家都有同一个感受——

AI现在能写90%的代码了，速度表面上快了很多。但实际交付的时候？感觉还是一样慢。

为什么？

**因为我们加速了错误的环节。**

---

代码生成变快了，但Code Review没有。

PR数量变多了，但每个PR的审查轮数还是3到5轮——和没有AI的时候一样。

我们装了更快的引擎，但忘了路上还有限速。

---

还有一个没人细说的问题：

同样的AI工具、同样的代码库、同样的任务——交给两个不同的工程师，结果差别大得出乎意料。

不是因为谁更聪明，而是因为**谁更会"驾驶"这个AI**。

会的人，给好上下文，一次出结果。
不会的人，来回改十几轮，质量还不如前者。

这不是能力问题，是**系统问题**。系统问题可以用系统来解决。

---

我最近在用一个"金字塔"模型来理解这件事：

软件交付是分层的。越底层，AI越能全权处理。越顶层，越需要人来判断。

现在我们在最底层——代码这一层。

目标是把这一层做成一个**自动运转的工厂**：

✅ 每次PR之后，让AI总结review反馈，更新steering files
✅ 把常见问题做成自定义lint规则，在构建阶段就拦截
✅ 测试用例从用户故事出发，而不只是刷覆盖率
✅ 有监控信号，不用每次手动"检查轮胎"

**底层稳了，信号向上传，再去解决上一层的问题。**

就像训练神经网络一样，一层一层来。

---

现在很多团队的状态是：每天手动检查每条轮胎。

我想做到的是：系统自己报警，我只需要偶尔抽查。

这才是AI时代真正的效率提升——不是生成更快，而是**输出更可信**。

---

我是Shengfu，工程师，在探索AI怎么重塑我们造软件的方式。

有共鸣的欢迎来聊👇你们团队现在卡在哪个环节？

*#AI编程 #工程师成长 #软件开发 #AI工具 #程序员*