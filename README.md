# Guillaume Velé

AI product builder, independent. Founder of [Acuence](https://acuence.app).
I build **evidence-first AI systems**: workflows that preserve canonical inputs,
verify mutations, cite supporting sources, and fail closed when evidence is insufficient.

- Paris, France · https://www.guillaumevele.fr
- Power-user of the OpenClaw agent stack (not its creator — that is [@steipete](https://github.com/steipete))

## Built on Mistral

| Project | Scope and current evidence |
| --- | --- |
| [**ahead-of-time-demo**](https://github.com/guillaumevele/ahead-of-time-demo) | A forecast-then-prescribe loop: Timestral forecasts from ClickHouse on CPU, Mistral Large proposes one action, and a human approval gate with signed receipts blocks execution. Preregistered backtest on two public series against seasonal-naive baselines. One real agent run is traced to Langfuse and read back through its API. |
| [**vibe-fim**](https://github.com/guillaumevele/vibe-fim) · [PyPI](https://pypi.org/project/vibe-fim/) | Uses Codestral fill-in-the-middle to constrain generation between caller-supplied anchors, then verifies that the prefix and suffix remain byte-identical. Its parse gate currently covers Python; other languages require their real toolchain. |
| [**vibe-orchestra**](https://github.com/guillaumevele/vibe-orchestra) · [PyPI](https://pypi.org/project/vibe-orchestra/) | A model-and-specialist router for Mistral Vibe: it classifies a task and routes it to the matching Mistral model, specialist and tool. The routing is hand-written, not learned. |
| [**Voxtral Q8_0 contribution**](https://github.com/TrevorS/voxtral-mini-realtime-rs/pull/15) | Open upstream PR adding Q8_0 GPU quantization to a real-time Voxtral runtime, with custom WGSL kernels validated locally on Metal. Vulkan and full-model audio remain unverified; the PR has not yet received maintainer review. |
| [**vibe-ios-kit**](https://github.com/guillaumevele/vibe-ios-kit) | An iOS posture for Mistral Vibe: an `AGENTS.md` ruleset, an `ios` agent and a lint script for SwiftUI work. The Swift templates are type-checked locally against the iOS SDK; a full app build is not claimed. |

## Other public work

| Project | Scope and current evidence |
| --- | --- |
| [**agent-proof-kit**](https://github.com/guillaumevele/agent-proof-kit) | Deterministic release gates for AI-agent runs: policy checks, provenance, SARIF and signed proof bundles. The public suite runs on synthetic fixtures; production use is not claimed. |
| [**voice-to-vault**](https://github.com/guillaumevele/voice-to-vault) | A small, provider-agnostic router for voice and transcript captures: config-driven routing, atomic writes and idempotence. |
| [**gesture-jellyfish**](https://github.com/guillaumevele/gesture-jellyfish) | An interactive Three.js artwork controlled by webcam gestures, with a mouse fallback and a public static demo. |

## How I work

- **Separate invariants from checks.** Byte preservation can hold by construction;
  syntax, tests and runtime behavior remain checks that can fail.
- **Require evidence for completion.** A build is useful evidence, but not proof of
  runtime behavior, visual quality or production safety.
- **Fail closed when proof is missing.** Surface uncertainty, abstention and human
  approval states instead of converting them into a success claim.

## Product context

My private work spans medical, legal and on-device products. The repositories
above are the deliberately public, inspectable part of that practice; no private
product data is used as public evidence.

## Links

- Website — https://www.guillaumevele.fr
- Voxtral Q8_0 PR — https://github.com/TrevorS/voxtral-mini-realtime-rs/pull/15
