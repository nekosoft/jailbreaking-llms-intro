# Intro to Jailbreaking LLMs and Building Your Own Test Harness

From chatbots to agents: jailbreak techniques, practical experiments, and how to build a test harness to evaluate what actually happened.

By **[Yianna Paris](https://ludahex.nl)**, Offensive Security Engineer at Xebia and Researcher at Luda Hex.

## Download the slides

**[Download the slides (PDF)](ALL-Jailbreaking-Yianna-Paris-2026_v0_6a.pdf)**

The deck, *I Jailbroke a Scam Bot, and So Can You*, is adapted from these talks:

- 26 October 2026: Would you trust an agent to fix prod at 3am? - GoDataFest
- 27 October 2026: One arrow, multiple breaches: What I've learned jailbreaking chatbots - Techorama NL
- 30 October 2026: I jailbroke a scam bot, and so can you - WICCON

## What the slides cover

I merged my slide decks. They target offensive, defensive and software engineering audiences. For those who are "purple teamers" at heart.

- **Jailbreaking basics:** model safety, guardrails, attention, and analysing a target.
- **Attack techniques:** roleplay, code completion, multi-turn attacks and Crescendo, Unicode tags, and chain-of-thought forgery.
- **Chatbots and agents:** prompt leaks, context engineering, RAG, tool use, and the difference between direct model invocation and an agent harness.
- **Building an evaluation suite:** benign baselines, attack families, test runners, judges, human checks, logging, and costs.
- **Experiments and defensive lessons:** AWS agent scenarios, tool-call chains, permissions, and checking actions rather than trusting the model's claims.
- **Code review -> Exploit pipline:** A design rather than something prescriptive.

## Write-ups coming next

This repository will be updated with write-ups that expand on the experiments and examples in the slides.

- [ ] Add experiment write-ups and explain the results.
- [ ] Document the test harness setup and evaluation approach.
- [ ] Expand the AWS agent examples and defensive lessons.

Follow the [write-ups index](./docs/README.md) as these are added, or watch this repository for updates.

## References and further reading

The links below relate to the topics in the slides; the experiments and results presented by Yianna are her own unless otherwise credited.

### Research and explanations

- **Attention and Transformers:** Vaswani et al. (2017), [Attention Is All You Need](https://arxiv.org/abs/1706.03762).
- **Visual explanation of attention:** [Luis Serrano / Serrano Academy](https://www.youtube.com/@SerranoAcademy), credited for the attention and embedding illustrations shown in the slides.
- **Multi-turn escalation:** Russinovich, Salem, and Eldan, [Great, Now Write an Article About That: The Crescendo Multi-Turn LLM Jailbreak Attack](https://www.usenix.org/conference/usenixsecurity25/presentation/russinovich), USENIX Security 2025.
- **Role confusion and CoT forgery:** Charles Ye, Jasmine Cui, and Dylan Hadfield-Menell (2026), [Prompt Injection as Role Confusion](https://arxiv.org/abs/2603.12277). See also the [authors' project page and extended write-up](https://role-confusion.github.io/) and the [LessWrong article linked in the slides](https://www.lesswrong.com/posts/d8xDGzCEYE639qqEv/a-theory-of-prompt-injection-and-why-you-should-study-roles).
- **Invisible prompt injection:** [StegZero: Invisible Prompt Injection](https://stegzero.com/invisible-prompt-injection/), the Unicode-tag resource linked in the slides.
- **Scam-bot prompt-leak example:** [Christel Lim's LinkedIn post](https://www.linkedin.com/feed/update/urn:li:activity:7454688373253885952/), credited in the “Spot the prompt leak” slides.

### Evaluation tools and benchmarks

- **[garak](https://github.com/NVIDIA/garak):** an LLM vulnerability scanner, referenced in the single-turn testing examples.
- **[MT-JailBench](https://github.com/SafetyArena/mt-jailbench):** a modular framework for evaluating multi-turn jailbreaks. [Paper: A Modular Benchmark for Understanding Multi-Turn Jailbreak Attacks](https://arxiv.org/abs/2605.11002).
- **[XSTest](https://github.com/paul-rottger/xstest):** Röttger et al.'s test suite for identifying exaggerated safety behaviours, useful for checking over-refusal alongside harmful-input tests.
- **[MultiBreak](https://proceedings.mlr.press/v306/song26n.html):** Song et al. (2026), *A Scalable and Diverse Multi-turn Jailbreak Benchmark for Evaluating LLM Safety*.

### Agent infrastructure and threat modelling

- **[Strands Agents](https://strandsagents.com/):** the agent toolkit discussed in the AWS experiments.
- **[Amazon Bedrock AgentCore](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/what-is-bedrock-agentcore.html):** documentation for the agent platform discussed in the slides.
- **[The lethal trifecta for AI agents](https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/):** Simon Willison (2025), on the combination of private data, untrusted content, and external communication.
- **[Threat Modeling: What, Why, and How?](https://shostack.org/resources/whitepapers/threat-modeling-what-why-how):** Adam Shostack's explanation of the four-question threat-modelling framework used in the code-review section.

### Hands-on learning

- To be updated
- **[OWASP FinBot CTF](https://genai.owasp.org/resource/finbot-agentic-ai-capture-the-flag-ctf-application/):** hands-on challenges for agentic AI security.

## Licence and attribution

© 2026 Yianna Paris · [ludahex.nl](https://ludahex.nl)

Except where otherwise noted, the slides, diagrams, and written materials in this repository are licensed under **[Creative Commons Attribution–NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/)**. See [LICENSE.md](./LICENSE.md) for the full terms.

You may share and adapt these materials for noncommercial purposes, provided you credit Yianna Paris, link to the licence, and indicate any changes.

Suggested credit:

> Yianna Paris, *I Jailbroke a Scam Bot, and So Can You* (2026), https://ludahex.nl. Licensed under CC BY-NC 4.0: https://creativecommons.org/licenses/by-nc/4.0/. Adapted where indicated.

Third-party materials retain their original rights and are excluded from this licence unless explicitly stated otherwise. Keep their credits when reusing the materials.
