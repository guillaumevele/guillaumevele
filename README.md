# Guillaume Vele

AI product builder. Co-founder and digital director at Nuance Paris.
I ship products in constrained, sensitive domains — medical, legal, on-device — and I
care about evaluation, workflow safety and product design as much as the model itself.

- Paris, France
- Website: https://www.guillaumevele.fr
- Power-user of the OpenClaw agent stack (not its creator — that is [@steipete](https://github.com/steipete))

## Open-source contribution

[**TrevorS/voxtral-mini-realtime-rs#15**](https://github.com/TrevorS/voxtral-mini-realtime-rs/pull/15)
— open pull request (in review) adding Q8_0 8-bit GPU quantization to a real-time
Voxtral runtime: custom WGSL compute kernels, run on both Metal and Vulkan.
The base runtime is by [@TrevorS](https://github.com/TrevorS); this PR proposes the
quantization path on top of it.

## Products I work on

Most of my product work is private, but it ships:

- **Verdict** — iOS skincare/dermatology app. On-device image analysis with a strong
  bias toward scientific honesty (no overclaimed diagnoses, sourced reasoning).
- **Compromis-AI** — real-estate/legal SaaS for French property pre-sale agreements.
- **Nuance Paris** — medical brand and product work as co-founder.
- Medical SEO sites and **Hermes**, a local macOS automation stack.

These stay private by design. The repositories below are the public, inspectable
slice of how I work.

## Public repositories

| Repository | What it is |
| --- | --- |
| [voxtral-tts-q8](https://github.com/guillaumevele/voxtral-tts-q8) | Q8_0 quantization and WGSL GPU-kernel work around Mistral Voxtral TTS (Apache-2.0, derived from [@TrevorS](https://github.com/TrevorS)'s runtime). |
| [agent-proof-kit](https://github.com/guillaumevele/agent-proof-kit) | AI-agent release gates: JSON schemas, fail-closed policy checks, JSONL trace normalization, regression diffing and a composite GitHub Action. `npm run verify` runs the full gate set; CI is green. |
| [ai-product-lab](https://github.com/guillaumevele/ai-product-lab) | Runnable evaluation harnesses, repeatability checks and workflow-safety gates, with bounded case studies. |
| [voxtral-mini-realtime-rs](https://github.com/guillaumevele/voxtral-mini-realtime-rs) | Fork tracking the Voxtral PR above. |

## How I work

- **Product framing** — turn a broad model capability into a narrow, usable workflow.
- **UX** — make uncertainty, retries, escalation and failure states feel clear.
- **Evaluation** — define acceptance criteria and release gates, and run them.
- **Implementation** — small prototypes, automation scripts, validation loops.

`agent-proof-kit` and `ai-product-lab` are self-built tooling, designed and tested
against fixtures rather than production traffic. The case studies are bounded so the
method is visible without exposing client or product data.

## Links

- Website — https://www.guillaumevele.fr
- Voxtral Q8_0 PR — https://github.com/TrevorS/voxtral-mini-realtime-rs/pull/15
- agent-proof-kit — https://github.com/guillaumevele/agent-proof-kit/releases/latest
