<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=23&duration=3200&pause=900&color=22C55E&center=true&vCenter=true&width=760&height=64&lines=I+build+AI+systems+that+cite+their+sources;...+and+are+allowed+to+say+%22I+don%27t+know%22;Grounded+RAG+%E2%80%A2+Multi-agent+%E2%80%A2+Evaluation+harnesses" alt="I build AI systems that cite their sources" />

# Hafiz S M Rayyan Alam

**Computer Science @ FAST NUCES**

<a href="https://gov-service-navigator.vercel.app"><img src="https://img.shields.io/badge/Live_Demo-Government_Service_AI-22C55E?style=for-the-badge&logo=vercel&logoColor=white" alt="Live demo"></a>
<a href="https://www.linkedin.com/in/rayyanalam"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:hafizrayyanalam@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>

</div>

---

## 🧭 About

Most AI demos fail the same way: they answer confidently, they answer wrong, and you only find out
afterwards. That is tolerable in a chatbot and unacceptable in a system someone *acts on* — a government
procedure, a credit decision, a bias audit.

So the question I keep circling is the boundary: **which parts of a system are allowed to be a language
model, and which parts must be code you can test.** Most of what I build sits on that line.

- 🔭 Building **[Government Service AI Navigator](https://gov-service-navigator.vercel.app)** — live, deployed, and evaluated against 51 scripted scenarios
- 🧪 I never claim "grounded" without a number attached — there is a harness, and CI fails the build if one unsupported claim gets through
- 🗣️ Ships in **English, Urdu and Roman Urdu**
- 💬 Ask me about grounded RAG, three-valued logic, or why a good fallback beats a confident guess

---

## 🏆 Featured — Government Service AI Navigator

<div align="center">

<a href="https://gov-service-navigator.vercel.app"><img src="https://img.shields.io/badge/%E2%96%B6_Try_it_live-gov--service--navigator.vercel.app-22C55E?style=flat-square" alt="Live"></a>
<a href="https://github.com/RayyanAlam1/gov-service-navigator"><img src="https://img.shields.io/badge/Source-181717?style=flat-square&logo=github&logoColor=white" alt="Source"></a>

</div>

A Pakistani citizen types *"mera CNIC gum hogya hai, Karachi mein hun"* and gets back a personalised,
source-cited action plan: which service, which branch, which documents **they specifically** still need,
which office, what happens next.

It is built around one rule:

> ### 🔒 The language model never supplies a government fact.
>
> Not a fee. Not a deadline. Not a document name. Every such fact traces to a database row or a retrieved
> chunk of an official document, and carries its source to the screen. The model detects intent, phrases
> questions, and translates — nothing else.

The test for whether that boundary actually holds: **swap the model for a template renderer — are the
answers still correct?** They are. `LLM_PROVIDER=mock` runs the whole system that way, and the evaluation
suite still passes.

| | |
|:--|:--|
| 🎯 **Interview** | Asks only questions whose answer can change the outcome — real information gain over the rule set, not a shortened form. Averages **4.5 questions**. |
| 🔍 **Grounding** | An output verifier scans every rendered number, duration, count and URL, and rejects anything not traceable to a fact — including numbers that drift during translation. |
| 📊 **Evaluation** | 51 scripted citizen paths · 3 services · 3 languages · prompt injections included. **100%** service and scenario identification, **100%** document F1, **0 unsupported claims**. |
| 🤲 **Honesty** | Unverified fees ship as `NULL` and render as *"not verified — confirm at the counter."* A plausible invented number is worse than a blank one. |

<div align="center">

![Next.js](https://img.shields.io/badge/-Next.js_15-000000?style=flat-square&logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![pgvector](https://img.shields.io/badge/-pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![CI/CD](https://img.shields.io/badge/-CI%2FCD-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![Vercel](https://img.shields.io/badge/-Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

</div>

---

## 🛠️ Tech Stack

**AI / ML**

![PyTorch](https://img.shields.io/badge/-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Transformers](https://img.shields.io/badge/-Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/-scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

**Languages**

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/-SQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![C++](https://img.shields.io/badge/-C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![C](https://img.shields.io/badge/-C-A8B9CC?style=flat-square&logo=c&logoColor=black)

**Backend & Data**

![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/-Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/-Express-000000?style=flat-square&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Frontend & Tooling**

![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/-Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![Tailwind](https://img.shields.io/badge/-Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/-Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

---

## 📊 By the numbers

<div align="center">

![Eval scenarios](https://img.shields.io/badge/eval_scenarios-51-22C55E?style=for-the-badge)
![Unsupported claims](https://img.shields.io/badge/unsupported_claims-0-22C55E?style=for-the-badge)
![Document F1](https://img.shields.io/badge/document_F1-100%25-22C55E?style=for-the-badge)
![Questions asked](https://img.shields.io/badge/questions_asked-4.5_avg-22C55E?style=for-the-badge)

![Languages](https://img.shields.io/badge/ships_in-English_%C2%B7_Urdu_%C2%B7_Roman_Urdu-1D5B9A?style=for-the-badge)
![Tests](https://img.shields.io/badge/tests-110_passing-1D5B9A?style=for-the-badge)

<sub>Measured by the evaluation harness in <a href="https://github.com/RayyanAlam1/gov-service-navigator">gov-service-navigator</a> — not estimated.</sub>

</div>

---

## 📂 Selected Work

| Project | What it is | Stack |
|:--|:--|:--|
| 🏛️ **[gov-service-navigator](https://github.com/RayyanAlam1/gov-service-navigator)** | Grounded citizen-services decision engine. Live, tested, deployed. | `Next.js` `pgvector` `RAG` |
| 🤖 **[Autonomous-Enterprise-OS](https://github.com/RayyanAlam1/Autonomous-Enterprise-Operating-System)** | Multi-agent orchestration platform for enterprise workflows. | `Python` `FastAPI` `LLM` |
| ⚖️ **[Bias-Detection](https://github.com/RayyanAlam1/Bias-Detection)** | Detecting bias in text — the measurement side of responsible AI. | `PyTorch` `Transformers` |
| 💳 **[Credit_Card_Default](https://github.com/RayyanAlam1/Credit_Card_Default)** | Default prediction on the Taiwan credit dataset. | `scikit-learn` `Jupyter` |
| 📊 **[IBA_Datathon](https://github.com/RayyanAlam1/IBA_Datathon)** | Competition work under time pressure. | `Python` `Pandas` |
| 🔐 **[Escrow](https://github.com/RayyanAlam1/Escrow)** | Escrow payment system on the PERN stack. | `PostgreSQL` `React` |

Coursework lives in **[Compiler-Construction](https://github.com/RayyanAlam1/Compiler-Construction)**,
**[Information-Security](https://github.com/RayyanAlam1/Information-Security)** and
**[DevOps](https://github.com/RayyanAlam1/DevOps)** — kept public because the working is worth more than the grade.

---

## 🤝 Connect

<div align="center">

<a href="https://www.linkedin.com/in/rayyanalam"><img src="https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:hafizrayyanalam@gmail.com"><img src="https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
<a href="https://github.com/RayyanAlam1"><img src="https://img.shields.io/badge/-GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
<a href="https://gov-service-navigator.vercel.app"><img src="https://img.shields.io/badge/-Live_Project-22C55E?style=for-the-badge&logo=vercel&logoColor=white" alt="Live project"></a>

</div>

---

<div align="center">
<sub>Currently working on: retrieval that knows when it has found nothing · evaluation harnesses that fail loudly ·<br>interfaces for people who are anxious, in a hurry, and on a cheap phone.</sub>
</div>
