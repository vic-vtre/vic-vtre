## Vic V - AI Engineer, LLM Evaluation & Test Automation

Evals, guardrails and RAG for production LLM apps, built on 8 years of test automation. Short demo videos below; the code is private production code.

[LinkedIn](https://www.linkedin.com/in/vic-vtre)

<br>

---

<br>

## AI engineering

### LLM-as-Judge Eval Suite

An AI judge grades my production app's LLM team summaries (private repo) on name coverage, blocker accuracy, mood, and hallucination, and the script exits with code 1 when a case fails. The clip shows three runs: a quick pass over the first 8 of 50 golden cases, the full 50 (trimmed), and a red-team run with deliberately impossible cases to prove the gate fails when it should.

At recording, all 16 hand-written cases passed; the 34 generated ones were still being tuned (mood labels, exact blocker wording). A suite that's green on day one probably isn't testing much. Today all 50 cases run in CI on every prompt change.

`LLM-as-Judge` `Evals` `Prompt Injection` `TypeScript` `Bun`

https://github.com/user-attachments/assets/0f90ba8f-15d8-430f-aceb-7f4d3c00e835

<br>

---

<br>

### LLM Failure Guardrails

What happens when the LLM endpoint accepts the request and never answers (production app, private repo). A rate-limit gate, a timeout, then a plain-text fallback summary flagged is_ai_generated = false, and the daily run still completes. Demo against a local dead endpoint, with the timeout shortened to 5s (20s in production) and the burst traffic pre-filled.

Killed the LLM on purpose. The app shrugged and kept delivering.

`Guardrails` `Fallbacks` `Rate Limiting` `Timeouts` `Graceful Degradation` `TypeScript`

https://github.com/user-attachments/assets/5af5f565-7b43-4045-a248-94d6503810d5

<br>

---

<br>

### Hybrid Semantic Search

Search over check-in history that finds by meaning and by keyword, then merges both into one ranked list (768-d embeddings, pgvector cosine, from my production app, private repo). The clip walks through the semantic pass, the keyword pass, and the merge. This is the retrieval half of RAG, and it now feeds the production AI summaries.

Ctrl+F for people who can't remember the exact words.

`pgvector` `Hybrid Search` `Embeddings` `RAG` `PostgreSQL` `TypeScript`

https://github.com/user-attachments/assets/b92a3f2c-89e8-4aeb-9e1f-0b610db15714

<br>

---

<br>

## Test automation

### AI-Driven Testing (Playwright MCP)

Playwright MCP lets an AI agent drive a real browser. I ask it to plan and debug tests, then record it writing and running them. It does the repetitive execution; I keep the architecture.

`MCP` `AI` `OpenCode` `Playwright` `Agentic Testing` `E2E`

https://github.com/user-attachments/assets/8546ae10-9e58-4017-8d97-2122872b7ed5

<br>

---

<br>

### Playwright Regression Suite

Migrating prod smoke checks into a proper Playwright suite.

Now with 130 tests that are legally speaking "a regression catalog".

Nightly execution - automated reliability while I sleep.

`Playwright` `TypeScript` `SvelteKit` `Regression Testing`

https://github.com/user-attachments/assets/3345ae4e-f2cc-4a65-807f-4ed4ff12145a

<br>

---

<br>

### Playwright (headed)

Cross-browser E2E on Chromium, Firefox, and WebKit, logged in once with a magic link.

Blink and you'll miss the login. I blinked. Nothing happened. That's the magic link working.

`Playwright` `Cross-Browser` `Headed` `E2E` `Magic Link Auth`

https://github.com/user-attachments/assets/dc56444a-5a2f-43e6-96a7-5853ea852373

<br>

---

<br>

### Playwright (trace viewer)

Every click, every request, every pixel - replayed from a trace.

A few years ago with Selenium I'd have assembled this from scratch. Today, Playwright trace viewer handles root-cause analysis out of the box.

`Playwright` `UI-Mode` `Trace-Viewer` `Debugging`

https://github.com/user-attachments/assets/227ef226-e5a6-463b-b091-4a1878f5cab1

<br>

---

<br>

## Earlier Python projects (2021)

### Secure SMTP Automation Module (2021)

A plug-and-play secure networking library. Abstracts complex MIME payload encoding and TLS connections into a portable, easily integrated module.

Useful when you want email automation without becoming an email server engineer.

`Python` `Network Protocols` `TLS Security` `Data Serialization` `API Abstraction`

https://github.com/vic-vtre/easy-smtp

https://github.com/user-attachments/assets/6e827ae8-6531-4273-9f7d-045cd1b768f3

<br>

---

<br>

### Async Audio Playback Library (2021)

A drop-in audio module for Python apps. Handles threaded audio streams, asynchronous UI synchronization, and real-time state binding out of the box.

The goal was simple - press play and hear music. Surprisingly non-trivial.

`Python` `Concurrency` `Async Event Handling` `UI-Backend Sync`

https://github.com/vic-vtre/winamp-from-temu

https://github.com/user-attachments/assets/1ee97382-91b0-43ec-99e0-e660815fb1fb

<br>

---

<br>

### Custom 2D Physics Engine (2021)

A retro passion project built in my free time. A custom 2D engine handling strict render loops, collision math, and sprite state machines from scratch.

Sprites and music belong to Capcom and David Production - I own exactly none of it.

`Python` `State Management` `Render Loops` `Object-Oriented Design`

https://github.com/vic-vtre/dio-runner

https://github.com/user-attachments/assets/577ad9b3-5006-4745-8809-3f98e4209552

<br>
