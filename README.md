# Intro to Jailbreaking LLMs and Building Your Own Test Harness

From chatbots to agents: jailbreak techniques, practical experiments, and how to build a test harness to evaluate what actually happened.

By **[Yianna Paris](https://ludahex.nl)**, Offensive Security Engineer at Xebia and Researcher at Luda Hex.

## Download the slides

**[Download the slides (PDF)](WICCON-Conference-Script-Kitty-Style_v0_6a.pdf)**

The deck, *I Jailbroke a Scam Bot, and So Can You*, is adapted from these talks:

- 26 October 2026: GoDataFest
- 27 October 2026: Techorama NL
- 30 October 2026: WICCON

## What the slides cover

- **Jailbreaking basics:** model safety, guardrails, attention, and analysing a target.
- **Attack techniques:** roleplay, code completion, multi-turn attacks and Crescendo, Unicode tags, and chain-of-thought forgery.
- **Chatbots and agents:** prompt leaks, context engineering, RAG, tool use, and the difference between direct model invocation and an agent harness.
- **Building an evaluation suite:** benign baselines, attack families, test runners, judges, human checks, logging, and costs.
- **Experiments and defensive lessons:** AWS agent scenarios, tool-call chains, permissions, and checking actions rather than trusting the model's claims.

## Write-ups coming next

This repository will be updated with write-ups that expand on the experiments and examples in the slides.

- [ ] Add experiment write-ups and explain the results.
- [ ] Document the test harness setup and evaluation approach.
- [ ] Expand the AWS agent examples and defensive lessons.

Follow the [write-ups index](./docs/README.md) as these are added, or watch this repository for updates.

## Relevant links

### Testing and research

- [garak](https://github.com/NVIDIA/garak): an LLM vulnerability scanner.
- [XSTest](https://github.com/paul-rottger/xstest): a test suite for identifying exaggerated safety behaviours and over-refusal.
- [The Crescendo Multi-Turn LLM Jailbreak Attack](https://www.usenix.org/conference/usenixsecurity25/presentation/russinovich): the research behind gradual escalation across a conversation.
- [Attention Is All You Need](https://arxiv.org/abs/1706.03762): the Transformer paper referenced in the attention section.

### Agent infrastructure

- [Strands Agents](https://strandsagents.com/): the agent toolkit used in the AWS examples.
- [Amazon Bedrock AgentCore](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/what-is-bedrock-agentcore.html): documentation for the agent platform discussed in the slides.

## Licence and attribution

© 2026 Yianna Paris · [ludahex.nl](https://ludahex.nl)

Except where otherwise noted, the slides, diagrams, and written materials in this repository are licensed under **[Creative Commons Attribution–NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/)**. See [LICENSE.md](./LICENSE.md) for the full terms.

You may share and adapt these materials for noncommercial purposes, provided you credit Yianna Paris, link to the licence, and indicate any changes.

Suggested credit:

> Yianna Paris, *I Jailbroke a Scam Bot, and So Can You* (2026), https://ludahex.nl. Licensed under CC BY-NC 4.0: https://creativecommons.org/licenses/by-nc/4.0/. Adapted where indicated.

Third-party materials retain their original rights and are excluded from this licence unless explicitly stated otherwise. Keep their credits when reusing the materials.
