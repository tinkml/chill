[English](./CONCEPT.md) | [Русский](./CONCEPT.ru.md)

# Chill — Project Concept

## Why Chill exists

AI agents are becoming increasingly autonomous. They can work on a task for a long time, explore a codebase, change files, run tests, verify hypotheses, and make local engineering decisions.

Meanwhile, the human's understanding of what is going on can gradually erode.

The problem does not necessarily arise because the agent works poorly. On the contrary, it may be doing the task well — yet the human still stops clearly understanding:

* what has already happened;
* where the task stands right now;
* which decisions were made;
* what remains unknown;
* whether their involvement is needed;
* what will happen next;
* whether the work can be safely stopped.

As a result, technically successful work with AI can subjectively feel like a loss of control.

**Chill exists to reduce this uncertainty and help the human maintain a clear understanding of what is happening when working with AI agents.**

Chill does not make the agent more autonomous.

It makes the agent's autonomous work more understandable to the human.

---

## The Human-Agent State Gap

In ordinary development, a human continuously maintains an internal model of the task.

They roughly understand:

* what has been done;
* what is happening now;
* which approaches have been tried;
* which decisions have been made;
* what remains to be done;
* where the problems and risks are.

When working with an AI agent, this internal model can stop matching the actual state of the task.

An agent can perform far more actions in a short time than a human can absorb.

A gap emerges between:

**the actual state of the agent's work**

and

**the human's understanding of that state.**

Within Chill, this gap is called the **Human-Agent State Gap**.

The larger it grows, the more likely the human is to:

* lose the sense of control;
* start constantly double-checking the agent's actions;
* fear interrupting unfinished work;
* struggle to return to the task later;
* stop understanding the reasons behind changes;
* carry extra cognitive load.

Chill's primary mission is to reduce the Human-Agent State Gap.

---

## How Chill solves the problem

Chill reduces uncertainty not by adding more control over the agent, but by increasing the clarity of the process.

At any important moment, the human should be able to quickly restore a correct understanding of:

* where the task stands;
* what is already complete;
* what is happening now;
* what remains open;
* which decisions were made;
* why they were made;
* where risks or unknowns exist;
* whether human involvement is needed;
* what will happen next.

Chill should help the human maintain an up-to-date mental model of the work without having to watch every single AI action.

The core idea of the project:

> **Calm through clarity.**

---

## Design principles

### The human matters more than the agent's internal state

Information should be presented, first and foremost, in a way that helps the human understand what is happening.

Context that is useful to an AI agent is not necessarily useful to a human.

Chill is designed primarily for human perception.

---

### Clarity instead of reassurance

Chill must not tell the human that everything is fine when that cannot be confirmed.

Instead of:

> Everything is under control.

prefer:

> Tests pass.
> No known blockers.
> One question remains unresolved.

Calm should be a consequence of understanding the facts.

---

### Evidence over confidence

If information can be confirmed — Chill should rely on it.

If something is unknown — the unknown must remain visible.

The statement:

> Tests were not run.

is better than:

> The changes look correct.

Chill must not hide uncertainty behind a confident tone.

---

### Minimally sufficient information

More information does not mean more clarity.

Chill must not become yet another stream of logs, events, and technical details.

The first level of any answer should let the human restore their understanding of the situation in minimal time.

Additional details should appear only when they are actually needed.

---

### Preserving human control

AI autonomy must not mean the loss of human agency.

The user should understand:

* what the agent did on its own;
* which decisions remain with the human;
* where uncertainty exists;
* when the user's involvement is genuinely required.

Chill's goal is not to reduce AI autonomy, but to make it understandable and manageable.

---

### Safe interruption

The human should be able to stop unfinished work without feeling that they will lose the task's context.

Work should never continue merely because the user is afraid of losing the current state.

Any long agentic workflow must allow a safe stopping point.

---

### Continuity for the human

Preserving context for the AI does not automatically solve the problem of human memory.

Resuming work should help the human quickly restore:

* the goal;
* the current state;
* the important decisions;
* the open questions;
* the next action.

Chill should support continuity of work not only for the agent, but for the human.

---

## What Chill is not

### Chill is not a task manager

Chill does not replace Jira, Linear, GitHub Issues, or other task management systems.

A task manager answers the question:

> What tasks exist?

Chill answers a different question:

> What do I need to understand about the current work right now?

---

### Chill is not AI agent memory

Agent memory systems primarily help carry context between agents and sessions.

Chill is aimed at a different task:

> transferring understanding from the ongoing work to the human.

The agent's memory and the human's mental model are different things.

---

### Chill is not an action log

The project's goal is not to display every tool call, command, or file change.

Full observability by itself can increase cognitive load.

Chill should show not everything that happened, but what matters for understanding the state of the work.

---

### Chill is not a micromanagement system

Chill must not require confirmation for every agent action.

Excessive control makes autonomy pointless.

The project must seek a balance:

**the agent can work on its own, while the human never loses their understanding of what is happening.**

---

### Chill is not a psychological or medical product

Chill does not diagnose or treat anxiety.

It works with the characteristics of human-AI interaction:

* cognitive load;
* uncertainty;
* transparency;
* continuity;
* trust;
* the sense of control.

---

## The Chill Test

Every new Chill feature must answer the core question:

> **Does it help the human better understand what is happening and keep a sense of control when working with an AI agent?**

More concretely, it must define:

**Trigger**
At what moment of the interaction does the problem arise?

**Human State**
What exactly does the human stop understanding?

**Missing Information**
What information are they lacking?

**Intervention**
What is the minimal action Chill can take to restore understanding?

**Evidence**
What facts will Chill base its answer on?

If a feature makes the agent faster, smarter, or more autonomous, but does not reduce human uncertainty, it probably lies outside of Chill.

---

## Success criterion

Chill is not successful when the AI does more work.

Chill is successful when the human can let the AI do more work **without a corresponding growth in uncertainty and the feeling of losing control**.

The ideal outcome:

> The human understands where the task stands, what has happened, what remains unknown, and what comes next — and can therefore calmly continue the work or calmly stop it.
