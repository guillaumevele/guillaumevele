# Guillaume Vele

AI product builder. Co-founder and digital director at Nuance Paris.
I ship in constrained, sensitive domains — medical, legal, on-device — and I care
about **verification**, workflow safety and product design as much as the model itself.

- Paris, France · https://www.guillaumevele.fr
- Power-user of the OpenClaw agent stack (not its creator — that is [@steipete](https://github.com/steipete))

## A verified toolchain for Mistral `vibe`

I looked at Codestral's fill-in-the-middle endpoint and saw what the ecosystem
mostly missed: FIM is the only way to make an AI code edit **provably bounded** — you
send the prefix and suffix verbatim, the model writes only the middle, so the rest of
the file comes back as the original bytes *by construction*. I built that into a
primitive and then a coherent toolchain around Mistral's `vibe` agent. All public,
all on PyPI, all CI-green, all honest about their limits.

| Repo | What it is |
| --- | --- |
| [**vibe-fim**](https://github.com/guillaumevele/vibe-fim) | Verified bounded edits via Codestral FIM: byte-identical prefix/suffix **and** an `ast` parse-gate that can actually fail. Plus transactional multi-region edits and **provably-additive** test generation — old tests stay green *by execution* (a real pytest run is the proof). I did not find a prior tool shipping verified bounded edits. |
| [**vibe-orchestra**](https://github.com/guillaumevele/vibe-orchestra) | A Mistral-native router: a Ministral classifier picks the model + specialist + plugin per task; `reason`/`vision`/`quick` reach Magistral/Pixtral/Ministral; a `/goal` autonomous loop decomposes → routes → verifies. Inspired by Sakana Fugu, hand-designed (not learned) — and it says so. |
| [**vibe-ios-kit**](https://github.com/guillaumevele/vibe-ios-kit) | An iOS specialty for `vibe`: a build posture + 38 iOS 26/27 patterns distilled from 67 real projects + a runnable lint, wired to FIM for surgical Swift edits. |
| [**vibe-registry**](https://github.com/guillaumevele/vibe-registry) | `vibe install <name>` — the ecosystem layer `vibe` lacks (no marketplace; [discussion #497](https://github.com/mistralai/mistral-vibe/discussions/497) is unshipped). Community, not official; idempotent and reversible. |

The through-line is verification: each tool separates the invariant that holds by
construction from the checks that can fail, and ships the failing-then-passing tests
to prove it.

## Open-source contribution

[**TrevorS/voxtral-mini-realtime-rs#15**](https://github.com/TrevorS/voxtral-mini-realtime-rs/pull/15)
— open PR adding Q8_0 8-bit GPU quantization to a real-time Voxtral runtime: custom
WGSL compute kernels on both Metal and Vulkan. The base runtime is by
[@TrevorS](https://github.com/TrevorS); this PR proposes the quantization path on top.

## How I work

- **Verification > generation.** "It compiles" is not proof; I ship the test, the
  trace, or the run. The vibe-fim tools refuse to write an edit they cannot prove.
- **Honest limits.** I bound claims — the parse-gate is Python-first, the registry is
  community (not official), the router is hand-designed (not learned) — rather than
  overclaim.
- **Product framing & UX.** Turn a broad capability into a narrow, usable workflow;
  make uncertainty, retries, escalation and failure states clear.

## Products (private, but they ship)

- **Verdict** — iOS skincare/dermatology app; on-device image analysis with a strong
  bias toward scientific honesty (no overclaimed diagnoses, sourced reasoning).
- **Compromis-AI** — real-estate/legal SaaS for French property pre-sale agreements.
- **Nuance Paris** — medical brand and product work as co-founder.
- Medical SEO sites and **Hermes**, a local macOS automation stack.

These stay private by design; the repositories above are the public, inspectable
slice of how I work.

## Also public

[agent-proof-kit](https://github.com/guillaumevele/agent-proof-kit) (deterministic
AI-agent release gates) · [ai-product-lab](https://github.com/guillaumevele/ai-product-lab)
(evaluation harnesses + workflow-safety gates) ·
[voxtral-tts-q8](https://github.com/guillaumevele/voxtral-tts-q8) (Q8_0 / WGSL kernels
around Voxtral TTS).

## Links

- Website — https://www.guillaumevele.fr
- Mistral toolchain — [vibe-fim](https://github.com/guillaumevele/vibe-fim) · [vibe-orchestra](https://github.com/guillaumevele/vibe-orchestra) · [vibe-ios-kit](https://github.com/guillaumevele/vibe-ios-kit) · [vibe-registry](https://github.com/guillaumevele/vibe-registry)
- Voxtral Q8_0 PR — https://github.com/TrevorS/voxtral-mini-realtime-rs/pull/15
