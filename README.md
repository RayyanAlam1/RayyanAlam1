<h1 align="center">Hafiz S M Rayyan Alam</h1>

<p align="center">
  <em>I build AI systems that are allowed to say "I don't know."</em>
</p>

<p align="center">
  Computer Science @ FAST NUCES
</p>

<p align="center">
  <a href="https://gov-service-navigator.vercel.app"><img alt="Live demo" src="https://img.shields.io/badge/live_demo-gov--service--navigator-046C4E?style=flat-square"></a>
</p>

---

Most AI demos fail in the same way: they answer confidently and they answer wrong, and you
only find out afterwards. That failure mode is tolerable in a chatbot and unacceptable in a
system someone acts on — a government procedure, a credit decision, a bias audit.

So the thing I'm actually interested in is the boundary: **which parts of a system are
allowed to be a language model, and which parts must be code you can test.** Most of what I
build sits on that line.

---

## Government Service AI Navigator

**[gov-service-navigator.vercel.app](https://gov-service-navigator.vercel.app)** &nbsp;·&nbsp;
[source](https://github.com/RayyanAlam1/gov-service-navigator)

A Pakistani citizen types *"mera CNIC gum hogya hai, Karachi mein hun"* and gets back a
personalised, source-cited action plan: which service, which branch, which documents *they
specifically* still need, which office, what happens next. English, Urdu and Roman Urdu.

It is built around one rule:

> **The language model never supplies a government fact.**

Not a fee, not a deadline, not a document name. Every such fact traces to a database row or a
retrieved chunk of an official document, and carries its source to the screen. The model
detects intent, phrases questions and translates — nothing else.

The test for whether that boundary holds: *swap the model for a template renderer — are the
answers still correct?* They are. `LLM_PROVIDER=mock` runs the entire system that way, and
the evaluation suite passes in that mode.

| | |
|---|---|
| **Interview** | Asks only questions whose answer can change the outcome — real information gain over the rule set, not a shortened form. Averages 4.5 questions. |
| **Grounding** | An output verifier scans every rendered number, duration, count and URL and rejects anything not traceable to a fact — including numbers that drift during translation. |
| **Evaluation** | 51 scripted citizen paths, 3 services, 3 languages, prompt injections included. 100% service and scenario identification, 100% document F1, **0 unsupported claims**. |
| **Honesty** | Unverified fees ship as `NULL` and render as *"not verified — confirm at the counter."* A plausible invented number is worse than a blank one. |

`Next.js 15` `TypeScript` `PostgreSQL + pgvector` `hybrid RAG` `Docker` `CI/CD`

---

## How I build

**Deterministic where it counts.** Eligibility, document lists and readiness verdicts are
computed by code from database rows, with three-valued logic so *"not yet asked"* is distinct
from *"no"*. Most of the safety properties in that project are downstream of that one
distinction.

**The fallback is a feature.** *"We could not verify this — here is the office that can"* is a
designed output with its own copy and its own tests, not an error path. It earns more trust
than being confidently wrong once.

**Measure the thing you claim.** "Grounded" means nothing without a number attached. So there
is a harness, the targets are absolute, and CI fails the build if a single unsupported claim
gets through.

**Write down what you don't know.** Every unverified fact in that knowledge base is labelled
as unverified, on screen, with the source it still needs checking against.

---

## Selected work

| Project | What it is |
|---|---|
| **[gov-service-navigator](https://github.com/RayyanAlam1/gov-service-navigator)** | Grounded citizen-services decision engine. Live, tested, deployed. |
| **[Autonomous-Enterprise-Operating-System](https://github.com/RayyanAlam1/Autonomous-Enterprise-Operating-System)** | Multi-agent orchestration platform for enterprise workflows. |
| **[Bias-Detection](https://github.com/RayyanAlam1/Bias-Detection)** | Detecting bias in text — the measurement side of responsible AI. |
| **[Credit_Card_Default](https://github.com/RayyanAlam1/Credit_Card_Default)** | Default prediction on the Taiwan credit dataset. |
| **[IBA_Datathon](https://github.com/RayyanAlam1/IBA_Datathon)** | Competition work under time pressure. |
| **[Escrow](https://github.com/RayyanAlam1/Escrow)** | Escrow payment system, PERN stack. |

Coursework lives in [`Compiler-Construction`](https://github.com/RayyanAlam1/Compiler-Construction),
[`Information-Security`](https://github.com/RayyanAlam1/Information-Security) and
[`DevOps`](https://github.com/RayyanAlam1/DevOps) — kept public because the working is worth
more than the grade.

---

## Working on

Retrieval that knows when it has found nothing. Evaluation harnesses that fail loudly.
Interfaces for people who are anxious, in a hurry, and on a cheap phone.

<p align="center">
  <sub>Open to internships and collaboration in applied AI · reach me through GitHub</sub>
</p>
