# Guillaume Velé

AI product builder. Co-founder and digital director at Nuance Paris.
I build **evidence-first AI systems**: workflows that preserve canonical inputs,
verify mutations, cite supporting sources, and fail closed when evidence is insufficient.

- Paris, France · https://www.guillaumevele.fr
- Power-user of the OpenClaw agent stack (not its creator — that is [@steipete](https://github.com/steipete))

## Selected public work

| Project | Scope and current evidence |
| --- | --- |
| [**agent-proof-kit**](https://github.com/guillaumevele/agent-proof-kit) | Deterministic release gates for AI-agent runs: policy checks, provenance, SARIF and signed proof bundles. The public suite runs on synthetic fixtures; production use is not claimed. |
| [**vibe-fim**](https://github.com/guillaumevele/vibe-fim) | Uses Codestral fill-in-the-middle to constrain generation between caller-supplied anchors, then verifies that the prefix and suffix remain byte-identical. Its parse gate currently covers Python; other languages require their real toolchain. |
| [**Voxtral Q8_0 contribution**](https://github.com/TrevorS/voxtral-mini-realtime-rs/pull/15) | Open upstream PR adding Q8_0 GPU quantization to a real-time Voxtral runtime, with custom WGSL kernels validated locally on Metal. Vulkan and full-model audio remain unverified; the PR has not yet received maintainer review. |
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
