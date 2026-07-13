# AI Collaboration Operating System ✨

[中文 README](README.md)

An early-stage, lightweight AI collaboration skill experiment that is already ready to try.

This is not a finished product, and it is not a finalized engineering methodology. For now, it is closer to a starting point: a reusable, portable, and intentionally restrained skill that helps small projects, practice projects, startup teams, hackathon work, and early products build basic collaboration habits with AI.

## 🧭 What This Is

The core entrypoint of this repository is still a lightweight skill, but it has grown a small set of supporting materials beyond its original single-file shape:

```txt
skills/
  project-collaboration-operating-system/
    SKILL.md
    references/
    templates/
```

The skill helps a project answer early collaboration questions: what should an AI agent read first, which documents are authoritative, when should engineering scope not expand, what evidence proves a task is done, and how should humans and AI correct course when collaboration drifts.

The specific rules and usage details live in [`SKILL.md`](skills/project-collaboration-operating-system/SKILL.md). `references/` and `templates/` only hold a few cases, pressure checks, and copyable invocation material. This README is not trying to repeat them. It is here to explain why the project exists and how we hope it can grow with contributors.

## 🚀 Quick Start

This skill can create a minimal collaboration starting point for a project that has only scattered ideas, or examine how humans and AI already work together in an existing project. You do not need to understand its four internal modes first. Start from where your project is today.

### 1 - Install the skill

If Node.js is installed locally, run:

```bash
npx skills add yhala2414/ai-collaboration-operating-system --skill project-collaboration-operating-system
```

> This command uses the general-purpose `skills` CLI to read the repository from GitHub, detect the AI agent you use, and install the skill. This project itself is not published as an npm package.

You can also download the repository directly or clone it with Git:

```bash
git clone https://github.com/yhala2414/ai-collaboration-operating-system.git
```

Then copy the **entire directory** below from the repository into your AI tool's skills directory:

```txt
skills/project-collaboration-operating-system/
```

When copying manually, the installed directory should still contain `SKILL.md`, `references/`, and `templates/`. Skills directories vary between tools, so follow the documentation for the tool you use. After installation, reopen your AI tool or start a new session, then ask the agent to use `project-collaboration-operating-system`.

If your tool does not support skills yet, you can still read [`SKILL.md`](skills/project-collaboration-operating-system/SKILL.md) directly and use it as a lightweight collaboration-system checklist.

### 2 - Choose your starting point

#### 🌱 Create a collaboration starting point from scratch

“From scratch” does not have to mean having nothing. You may already have ideas, chat logs, screenshots, drafts, or partial code, but no stable collaboration entrypoint. Give those materials to your agent and copy this prompt:

```txt
Use project-collaboration-operating-system to help me create a minimal,
usable human-AI collaboration starting point for this project.

First inspect the ideas, documents, and code I already have. Separate confirmed
facts, tentative ideas, open questions, and things that are out of scope for now.
Do not create a complete documentation suite by default. Explain what is actually
missing and propose the smallest useful setup. Wait for my approval before editing files.
```

#### 🔍 Check an existing project

If your project already has code, a README, collaboration guidance, or other documentation, but you are not sure whether the current system is clear, begin with a collaboration self-check:

```txt
Use project-collaboration-operating-system to examine how humans and AI
currently collaborate in this project.

I am not sure whether the existing collaboration guidance is clear or what is
most worth improving first. Inspect the code, documentation, and current project
stage, then explain the current collaboration state, the main risks, and the next
step you recommend. Diagnose first and do not edit files.

At the end, generate a copyable follow-up prompt based on what you found.
```

This check is not a project score, and it should not automatically add documentation. The agent will decide whether the project most needs an entrypoint, clearer existing rules, a focused improvement, or a retrospective on a real miss. If the current system is already sufficient, it should say so instead of adding process merely to look complete.

### 3 - Already know the problem? Start directly

You can also skip the broader self-check and describe the problem directly. For example:

```txt
AI agents often start working before reading enough project context. Use
project-collaboration-operating-system to check the project entrypoint, reading order,
and document authority. Diagnose the cause before adding any new documentation.
```

```txt
Project rules are scattered across several documents, and I am not sure which ones
are authoritative. Use project-collaboration-operating-system to find duplicated,
conflicting, stale, or unclear guidance and recommend the smallest cleanup.
```

```txt
A human-AI collaboration miss just happened. Use project-collaboration-operating-system
to review it. First decide whether it was an execution miss or a problem in context,
documentation, or process. Recommend changing collaboration rules only if the problem
is systemic.
```

These are only common starting points. They do not depend on a particular stack, directory structure, or project stage. You can also describe your own situation and let the agent determine the most appropriate next step.

## 🛠️ What It Can Help With Today

Even though the current version is still small, it can already be used as an initializer for a project's collaboration system. It is especially useful for:

- 📚 Organizing documentation collaboration: separating formal rules from drafts, audits, screenshots, and temporary plans.
- 🚪 Creating an AI entrypoint for a project: helping agents find authoritative context instead of editing after reading only the README.
- 🧱 Controlling early engineering scope: reminding teams not to add databases, auth, CI, test frameworks, AI services, or other infrastructure before the project stage calls for them.
- 🔍 Checking user-visible behavior: avoiding UI copy such as "saved", "submitted", or "done" when there is no state, service, API, or persistence path behind it.
- 🔁 Supporting retrospectives and correction loops: when collaboration drifts, classifying whether the issue was an execution miss, documentation ambiguity, context discovery failure, or a missing process.
- 🧷 Preventing documentation drift: when the same rule appears in multiple places, helping the team find the real source of truth before old guidance silently becomes wrong.

These capabilities are still early, but they are not just abstract ideas. They come from recurring problems in real projects: AI agents reading the wrong context, collaborators interpreting rules differently, guidance scattered across files, unclear completion standards, and retrospectives that stop at "be more careful next time."

## 🌱 Why We Are Building It

Many mature teams and large companies already have stable AI collaboration flows, documentation systems, and engineering practices. Those practices are valuable and worth learning from.

But they are often tightly coupled to complete projects: code structure, testing systems, PR workflows, platform engineering, organizational memory, internal tools, and collaboration habits that evolved over time. For many small projects, knowing those systems are good is very different from being able to migrate them.

Most early projects also do not need heavy engineering process on day one. Practice projects, course projects, hackathon prototypes, and early startup products often need a lighter starting point: protect against the most common collaboration failures first, then add more formal rules, templates, scripts, and workflows as the project becomes more complex.

So this project is not asking, "How do we create the most complete engineering system from the beginning?" It is asking:

- How can AI collaboration rules grow from light to mature?
- How can documentation help teams act instead of becoming a burden?
- How can a skill be copied across projects instead of being permanently tied to one codebase?
- How can people without deep professional engineering experience participate more easily in building with AI?

## 🧪 Where The First Version Came From

The first version of this skill came from a very concrete collaboration experience. The author previously worked on a hackathon project with many non-technical collaborators, while also needing to align project context across the agents used by different teammates.

The problem was not only "how do we make one AI write code?" It was "how do a group of humans and a group of AI agents keep aligning over time?" Which document is authoritative? Which idea is still only a draft? Which capability should not be built yet? How do we verify locally? How do we review mistakes? How can one collaborator's agent understand the rules already discovered by another collaborator's agent?

To make that project work, the author built an ad hoc documentation collaboration system, retrospective habit, and local testing routine. Later, it became clear that this method should not stay trapped inside one project, and should not have to be explained from scratch every time. This skill is an attempt to turn it into something lighter and more portable.

<table>
  <tr>
    <td>
      <strong>🧩 A tiny sticker from a real project</strong>
      <br><br>
      <a href="https://github.com/yhala2414/tripkin">TripKin</a>
      was one early practice source for this skill, but it is not the template and not the project this skill is tied to.
      The goal is to extract portable methods from concrete projects, then let the skill work independently across contexts.
    </td>
  </tr>
</table>

## 💡 What We Believe

We believe that in the AI era, writing code and building projects should not belong only to professional engineers. Anyone curious about technology should have a lower-cost way to start creating, experimenting, and organizing their ideas.

At the same time, collaborative projects still need some order. Creative freedom does not mean having no boundaries. Lightweight does not mean careless. Early-stage does not mean there is no need to reflect and improve.

Good engineering process should grow gradually: serve collaboration first, then scale; solve real problems first, then add more tools. It should help a team act more clearly, not add ceremony just to look professional.

## 🚧 Current Status

This is a very early concept version. The repository is still intentionally small: one core skill, plus a little reference material and invocation scaffolding, so it stays easy to copy, read, experiment with, and revise.

Future versions may add:

- `references`: more collaboration principles, failure patterns, decision criteria, and real-case pressure checks.
- `scripts`: lightweight checks for documentation drift, repeated rules, or collaboration risks.
- `templates`: more reusable collaboration notes, decision records, stage boundaries, and related project documents.
- `examples`: real small-project usage cases, failure cases, and improvement stories.

None of this is fixed yet. We would rather treat the project as an open experiment than pretend it is already complete.

## 🔭 What We Want To Explore Next

This project could remain "just a lightweight skill." But the more interesting possibility is that it may grow into a shared collaboration language for small teams working with AI.

We want to explore a few directions that are not fully formed yet, but feel worth thinking about together:

- **🤝 Agent-to-agent collaboration**: future projects may not be one person working with one agent, but many people working with their own agents. How should those agents share context, hand off tasks, explain rules, and correct each other? What kind of collaboration protocol would they need?
- **🧳 Portable collaboration memory**: when a project develops a documentation system, retrospective habit, or local verification routine, can those methods move to the next project? How do we migrate the method without copying a pile of files that do not fit the new context?
- **🌈 Entry points for non-technical collaborators**: if someone does not write engineering rules but deeply understands product, content, design, operations, or real users, can they still help improve an AI collaboration system through experience, feedback, examples, and retrospectives?
- **🌿 Progressive engineering for small projects**: we are not against engineering process. We are against process that arrives too early, too heavy, or only to look professional. A healthier path lets rules, scripts, templates, and verification grow as the project needs them.
- **🗂️ A library of real failure cases**: AI agents reading the wrong context, claiming completion without proof, retrospectives with no action, documentation drift, and agents misunderstanding each other are not only incidents. They can become reusable learning material.

These ideas are still sketches, not promises and not a roadmap. They are invitations: if you have run into similar problems, maybe we can turn these blurry experiences into clearer, lighter, and more portable collaboration tools together.

## 🙌 Help Us Improve It

If this direction interests you, contributions are very welcome.

If you are an experienced developer, you can help us judge which collaboration rules are actually useful, which parts are too heavy, which parts are too abstract, and which designs do not transfer well across projects.

If you do not have much engineering experience, your feedback is just as important. Try using AI to start or improve a project. Tell us what was confusing, what felt unusable, what made you more confident, and what still blocked you.

You can also use this skill to initialize or improve your own project documentation system, run experiments, bring back the rough edges from real projects, open issues, add examples, improve the writing, or simply star the project to show that this direction is worth continuing.

## ⭐ Star / Feedback / Contribute

This project is still small and imperfect. What it needs most is not to be treated as a standard answer, but to be tested, questioned, modified, and extended in real projects.

If you believe in this direction, please star it, share it, suggest improvements, or contribute directly. We hope it can slowly become a lighter, more practical, and more portable starting point for AI collaboration.
