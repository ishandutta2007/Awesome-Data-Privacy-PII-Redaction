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

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



### Sector Overview & Market Dynamics

The global Data Security Posture Management (DSPM) and data privacy software market is estimated between **$1.1B and $2.5B**, expanding rapidly toward tens of billions at an estimated 25–31% CAGR driven by generative AI adoption and stringent global privacy mandates. The market is **moderately concentrated**: while specialized redaction point solutions create initial fragmentation, enterprise procurement is dominated by a concentrated core of cybersecurity and data governance heavyweights consolidating DSPM, identity security, and privacy vault capabilities.

## SaaS/Hosted Platforms

| Product | Company Size / Valuation | Pricing | Free Tier Limits | Key Capabilities & Best For |
|---|---|---|---|---|
| **CyberArk** | ~$20.6B Market Cap (NASDAQ: CYBR) | From ~$2,400–$4,800/privileged user/yr; Endpoint Privilege Manager from $30/endpoint/yr; secrets manager from $40/workload identity/yr (~$25,000/yr typical minimum contract) | 30-day proof-of-concept / evaluation trial via sales engagement (no permanent free tier) | Enterprise identity security, privileged access management, secret governance, and data boundary protection across hybrid cloud infrastructure. |
| **Varonis** | ~$5.6B Market Cap (NASDAQ: VRNS) | From ~$55–$140/user/yr (typical entry enterprise contracts start around $15,000–$25,000/yr) | 30-day free trial with complimentary automated Data Risk Assessment scan (no permanent free tier) | Automated data security posture management (DSPM), data classification, access governance, and threat detection without charging per GB of data volume. |
| **OneTrust** | ~$4.5B Valuation (Private, $1B+ raised) | From ~$10,000/yr minimum baseline for single-module entry tiers (e.g., CMP or Privacy Automation) | No permanent free tier; time-limited 14-day sales evaluation trial with sandbox access (free standalone tools limited to basic cookie banner generator) | Comprehensive enterprise privacy automation, consent management, data inventory mapping, and AI governance. |
| **Securiti.ai** | $1.725B (Acquired by Veeam Software) | From ~$20,000/yr minimum annual commitment for entry-level modular DSPM / Privacy packages | Customized 14-day guided proof-of-concept (PoC) trial (no permanent free tier; free tier limited to basic cookie consent script) | Unified DataAI Command Platform providing DSPM, contextual sensitive data discovery, access intelligence, and safe AI pipeline redaction. |
| **BigID** | ~$1.2B Valuation (Private, Series E) | From ~$25,000/yr baseline starting contract for BigID Express / sensitive data discovery packages | Customized 14-to-30-day Proof of Concept (PoC) evaluation via sales / AWS Marketplace (no permanent self-serve free tier) | Deep data discovery, classification, and DSPM across unstructured data lakes, structured databases, and AI pipelines. |
| **Immuta** | ~$1.0B Valuation (Private, Series E) | From ~$30,000/yr baseline for enterprise data access control & dynamic masking tiers | Immuta Professional no-cost tier available via AWS Marketplace supporting up to 4 users; 14-day cloud evaluation trial | Cloud data access control, policy-driven dynamic data masking, format-preserving pseudonymization, and audit logging. |
| **Protegrity** | ~$400M Valuation / ~$100M+ Rev | Custom enterprise licensing starting around ~$100,000–$300,000/yr depending on data volume & environments | Custom sales-provisioned sandbox evaluation trial (typically 14–30 days under NDA; no permanent free tier) | Enterprise data-centric protection, format-preserving encryption (FPE), tokenization, and high-performance redaction for large data lakes. |
| **Nightfall AI** | ~$200M Valuation (Series B, $60M raised) | From $4/user/mo for basic SaaS add-ons; Developer API pay-as-you-go from $0.003/scan; enterprise DLP custom quotes | Free Developer Tier forever: 3 GB of uncompressed data scanned per month with API access to core PII/secret detectors; 7-day enterprise Proof of Value (POV) | AI-native DLP with Scan & Workflow APIs, browser extension sanitizing prompts for ChatGPT/Claude/Copilot, and sub-100ms latency. |
| **Skyflow** | ~$150M Valuation (Series B, $100M+ raised) | From ~$195,000/yr average contract value (ACV) on AWS Marketplace / enterprise private offers | Custom sales-led Proof of Concept (PoC) trial with test sandbox credentials (no permanent self-serve free tier) | Patented polymorphic encryption and privacy vault with re-identification Vault Tokens, Detect API for audio/text/images, and Snowflake Native App. |
| **Privacera** | ~$150M Valuation (Series B, $63M+ raised) | From ~$25,000/yr baseline for PrivaceraCloud access governance packages | 30-day free trial of PrivaceraCloud and Trust3 AI evaluation environment | Apache Ranger-based unified data governance, fine-grained access control, and privacy sanitization across multi-cloud environments. |
| **TrustBoost PII** | Seed / Emerging (<$10M Valuation) | From $0.01 USDC per call (`/sanitize/quick`) or 149 USDC for 10,000 sanitizations | Free Forever: 3 free previews per IP; 50 free full sanitizations using `tx_hash="TRIAL"` without credit card or wallet requirement | Agent-native PII sanitization API with multilingual semantic detection (LATAM identifiers), fail-closed security, and Solana on-chain audit proof. |




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
