# Awesome-Data-Privacy-PII-Redaction

## Top Data Privacy & PII Redaction Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on LLM Prompt Sanitization, Reversible Tokenization & Audit Trails*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Privacy & PII Redaction**. These tools enable organizations to detect and remove personally identifiable information before text reaches an LLM or external API—from privacy vaults that tokenize data at rest to lightweight libraries that mask prompts in-flight with zero dependencies.



**Examples** include Skyflow, BigID, Privacera, Immuta, Securiti.ai, OneTrust, Protegrity, CyberArk, Varonis, and Nightfall AI (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for local-first redaction, reversible masking, and open PII detection—ideal for privacy engineers, AI developers, and organizations seeking transparent, vendor-independent data sanitization.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **Skyflow**  

  **Data privacy vault built for isolating, protecting, and governing sensitive data** . Features **patented polymorphic encryption and tokenization**—data is encrypted using multiple schemes, allowing **aggregation and comparison on encrypted data without decryption** . **Detect API** analyzes **text, audio, and images** for PII, PHI, and PCI with **dedicated file-type endpoints** (PDFs with density/resolution optimization, audio with bleep frequency control, images with privacy transformations) . **Fine-grained token types**: **Vault Tokens** for re-identification (inference apps) vs. **Entity-Only Tokens** for one-way anonymization (model training) . **Data residency** compliance for GDPR, DPDP, PIPL . **Snowflake Native App** available in the Snowflake Marketplace for quick deployment . **Best for**: organizations needing a governed privacy vault with **re-identification capabilities** for production AI applications.



- **Nightfall AI**  

  **AI-native data loss prevention (DLP)** with **Scan and Workflow APIs** for developers . **Detects PII, PHI, PCI, banking information, API keys, passwords, and network information** across **text, documents, spreadsheets, logs, zips, and images** . **Precision and recall rates of 95%+**, handles **over 1K requests per second**, and **latency under 100 ms** . **Customizable redaction** per entity type, with **minimum confidence thresholds** and **context/exclusion rules** to reduce false positives . **Browser extension** monitors and redacts sensitive data before submission to **ChatGPT, DeepSeek, Copilot, Gemini, Grok, Perplexity, Claude** . **Best for**: teams wanting **API-first DLP** with high throughput and browser-level protection.



- **BigID, Privacera, Immuta, Securiti.ai, OneTrust, Protegrity, CyberArk, Varonis**  

  Enterprise data security and governance platforms with **data discovery, classification, access control, and compliance** capabilities. These tools provide **broader data security posture management (DSPM)** beyond prompt-level redaction—covering data at rest, in motion, and across cloud environments. **Best for**: large enterprises needing **comprehensive data governance** rather than just LLM prompt sanitization.



## Open-Source GitHub Projects



- **Presidio (Microsoft)**  

  **Open-source framework for detecting, redacting, masking, and anonymizing sensitive data** (MIT) . **11,000+ GitHub stars** and **OpenSSF Scorecard 8.4/10** with **CII-Best-Practices 10/10** . **Supports text, images, and structured data** with **NLP, pattern matching, and customizable pipelines** . **The most mature and widely adopted open-source PII detection framework**—often used as the detection engine inside other tools (DataShield, Redactify) . **Best for**: teams wanting a battle-tested PII detection foundation they can extend.



- **pii-masker-ai**  

  **Ultra-fast, zero-dependency PII masking and reversible unmasking for AI prompts, LLM agents, and vector databases** (MIT) . **The most practical reversible masking tool for LLM workflows**—**100% pure Python standard library**, zero attack surface . **Bi-directional reversible masking** with sequential placeholders (`<EMAIL_1>`, `<PHONE_1>`) so the LLM retains conversational context, then restores original data on return . **Comprehensive pattern suite**: credit cards with **Luhn validation**, IBAN, IPv4/IPv6, MAC addresses, JWT tokens, PEM private keys, **OpenAI/Anthropic/GitHub/AWS/Slack/Stripe API keys**, SSN, international phones, Vietnam Citizen ID . **CLI scanner** for CI/CD pre-commit checks (`pii-masker scan ./data/ --strict` returns exit code 1 on leaks) . **Best for**: Python teams wanting **reversible masking with zero dependencies** and CI integration.



- **Bogu**  

  **Local-first Python toolkit for detecting and redacting private information before text or documents are sent to an LLM** (open-source) . **The most explicit transmission-boundary design**—**`create_preview()` performs no network operation**, returns redacted text and categories for approval, then you explicitly send only `preview.redacted_text` . **`BoguClient` wraps OpenAI clients** with **`preview()` and `send()` as separate calls**—the first network call happens only when you call `send()` . **Custom policies from examples**—teach the detector private vocabulary (`Project Cedar`, `CUSTOMER-42`) without writing regex . **Irreversible types** become `[TYPE_REDACTED]` and are never added to the restoration map . **Optional OpenAI Privacy Filter** integration (opt-in, requires separate install) . **Best for**: teams wanting **explicit human approval before transmission** with custom private vocabulary.



- **Securedact MCP**  

  **MCP server for PII redaction with policy engine and residual validation** (Apache-2.0) . **The most security-focused MCP-native redaction tool**—**deterministic + contextual detectors** feed a **policy engine** that outputs **minimal, review, debug, or restore_capable** responses . **Minimal responses contain no original text, raw entity values, mapping, or restoration handle** unless explicitly requested . **Residual validator** checks output for missed PII before approval . **In-memory restoration sessions** use **cryptographic random handles, bounded capacity, expiration, and single-use consumption**; process exit destroys all sessions . **`prepare_for_external_ai`** is the recommended complete safe workflow . **Best for**: teams using **MCP hosts (Claude Code, Gemini CLI)** who want **policy-enforced redaction with audit-grade response modes**.



- **TrustBoost PII Sanitizer**  

  **API-based PII sanitizer built for autonomous agent pipelines** (MIT) . **The most agent-native API design**—**`POST /sanitize`** returns sanitized text with `[REDACTED]` replacing PII . **Semantic PII detection** (well above regex-only accuracy) with **multilingual support** (EN, ES-LATAM, PT-BR, DE, JA, FR, IT, KO) and **LATAM identifiers** (RFC, CPF, CUIT, RUT) that regex cannot cover . **Fail-closed**: on any API error it returns `[REDACTED]`, **never raw PII** . **On-chain proof of sanitization anchored on Solana**—verifiable audit trail . **MCP compatible** (`api.trustboost.dev/mcp`) . **50 free sanitizations** with `tx_hash=TRIAL` . **EU AI Act compliant** (Articles 12, 13, 26) . **Best for**: agent pipelines needing **multilingual semantic detection** and **cryptographic audit proofs**.



- **Privaro SDK**  

  **Privacy infrastructure for enterprise AI with blockchain-certified audit trails** (open-source SDK) . **`privaro.protect()`** tokenizes PII before LLM calls with **consistent tokens across conversation turns** via `conversation_id` . **`relay()` and `relay_stream()`** handle the full cycle—protect, call LLM, de-tokenize response—with **streaming support for OpenAI, Azure, Anthropic** . **`protect_output()`** scans LLM responses for **PII that leaked via RAG, tool results, or model memorization** . **`AgentRun`** context manager for **LangChain and CrewAI** integration . **Every interaction is tokenized, audited, and blockchain-certified** . **Best for**: teams wanting **full-cycle relay with streaming** and **blockchain audit trails**.



- **RedactKit**  

  **CLI and local proxy for PII redaction with tiered detection** (open-source) . **The most deployment-flexible redaction toolkit**—**Tier 1 (regex + Luhn) is default and zero-dependency**; **Tier 2 (local NER via transformers.js)** detects names, locations, orgs; **Tier 3 (local LLM via Ollama)** handles hardest semantic cases . **Local proxy** redacts everything sent to **Claude Code** (`ANTHROPIC_BASE_URL`), **Codex CLI** (`OPENAI_BASE_URL`), and **Cursor** (custom endpoint) . **Image sanitization** via OCR + face detection + blur . **Compression** reduces tokens without changing meaning . **Best for**: developers wanting **proxy-based redaction for coding agents** with tiered local detection.



- **DataShield**  

  **Privacy-preserving data sanitization for AI training** (open-source) . **The most compliance-focused dataset sanitizer**—**PII detection, secret scanning, sensitive classification** (medical, financial, legal), **anonymization, redaction, data minimization, transformation** . **Differential privacy** (Laplace/Gaussian noise with configurable epsilon) and **k-anonymity** . **GDPR and HIPAA compliance checks** (Art. 5, 9, 17, 25, 32, 35; Privacy Rule, Security Rule, Minimum Necessary) . **MCPGuard policy generation** and **mcp-taxonomy adapter** . **Multi-format input** (JSON, JSONL, CSV) . **Best for**: teams preparing **training datasets** with **regulatory compliance verification**.



- **Redactify**  

  **Efficient data redaction tool combining transformer-based NER, regex, and Presidio analysis** (open-source) . **Full redaction or partial masking**—ensuring compliance while **preserving data utility** . **Best for**: teams wanting **partial masking** that keeps analytical value.



### Additional Strong Open-Source Options



- **PII Sanitization Agent (500-AI-Agents)** — Thin client for TrustBoost API (MIT) . **Agent-native fail-closed design**—on any error returns `[REDACTED]`, never raw PII . **Context modes** (general, financial, legal, medical, code) . **No raw PII stored by the agent**; optional on-chain proof . **Best for**: autonomous pipelines needing **fail-closed behavior** with minimal code.

- **pii-masker-ai CLI** — CI/CD scanner for PII leaks (MIT) . **`pii-masker scan ./data/ --strict`** returns exit code 1 on leaks—**the pre-commit gate for PII** .

- Community **n8n** workflows for PII detection alerting and redaction pipeline automation.



**Frameworks for building custom systems**: Combine **Presidio** for battle-tested PII detection with **pii-masker-ai** for reversible LLM prompt masking, **Bogu** for explicit human approval before transmission, **Securedact MCP** for policy-enforced MCP redaction, and **DataShield** for compliance-verified dataset sanitization—creating a comprehensive data privacy stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- PII redaction tools handling sensitive data must comply with data protection regulations (GDPR, CCPA, HIPAA, etc.) and implement appropriate access controls and audit logging.

- **Open-source PII redaction is mature for text masking but varies in semantic coverage.** **pii-masker-ai** provides **reversible masking with zero dependencies** and comprehensive pattern coverage . **Presidio** offers **NLP-based detection** with OpenSSF Scorecard 8.4/10 . **But semantic PII detection (names, addresses, contextual identifiers) is fundamentally harder than regex**—**TrustBoost and Nightfall claim semantic detection with multilingual support**, while most open-source tools rely on regex + optional NER . **Test against your actual data** before trusting any tool with production PII .

- **Reversible vs. irreversible masking is a security trade-off.** **Reversible masking** (pii-masker-ai, Privaro, Bogu) preserves conversational context by restoring original data—**but creates a mapping table that must be protected** . **Irreversible redaction** (DataShield, Securedact's irreversible types) eliminates the mapping risk but **breaks continuity** if the LLM needs to reference the same entity across turns . **Bogu's `irreversible_types`** lets you mix both per entity type .

- **The transmission boundary is the critical design decision.** **Bogu** makes it explicit: `preview()` performs **no network operation**; `send()` is the **first network call** . **Securedact MCP** has **no provider clients**—it's purely a redaction layer . **TrustBoost** is an **API**—it receives the text to sanitize, which **recreates the data-egress problem** if the sanitizer itself is untrusted (a concern raised in the DeerFlow issue thread) . **For data-residency-constrained deployments, local-first tools (Bogu, pii-masker-ai, Presidio) are the safer choice.**

- **On-chain proof is an emerging differentiator.** **TrustBoost** anchors proof of sanitization on **Solana** . **Privaro** generates **blockchain-certified audit trails per interaction** . **This provides cryptographic evidence that sanitization occurred**—valuable for regulated industries and compliance audits. **But on-chain proofs don't guarantee detection accuracy**—they prove the sanitizer ran, not that it caught everything .

- **Fail-closed behavior is non-negotiable for autonomous pipelines.** **TrustBoost's agent** returns `[REDACTED]` on **any API/transport error**—**never raw PII** . **Securedact MCP** blocks on residual PII detection . **If your redaction layer can fail open, it will fail open**—design for the failure case first.

- Self-hosted open-source solutions require proper model management (for NER/LLM tiers), dependency updates, and ongoing maintenance. **PII detection is probabilistic, not perfect**—no tool catches everything. **Defense in depth with multiple detection engines and human review for high-risk workflows is essential.**



---



**Made for privacy engineers, AI developers, and organizations building transparent data privacy solutions.**  

Let's make Data Privacy & PII Redaction more open, data-driven, and fail-closed.
