# Frequently Asked Questions

---

## General

### What is Project 848?

A research initiative developing pheromone-inspired memory protocols for AI systems. The protocols (SEED-ANT-PRISM) help AI remember, learn, and adapt without retraining.

### Why "848"?

The project started after studying 847 AI startup failures. Project 848 represents the attempt to succeed where others didn't — by solving a fundamental problem (memory) rather than chasing trends.

### Who's behind this?

RUNE Digital, an AI research company based in Adelaide, Australia. Founded by Joel Parkinson.

---

## Technical

### Does this require training a new model?

No. SEED-ANT-PRISM works as an orchestration layer on top of existing models (GPT-4, Claude, Gemini, Llama, etc.). No fine-tuning or retraining required.

### How is this different from RAG?

RAG retrieves documents based on vector similarity. ANT navigates based on usage patterns (trails strengthen with use, decay with neglect). Different approach, often better results.

### How is this different from fine-tuning?

Fine-tuning bakes knowledge into model weights. SEED-ANT-PRISM manages context externally. Faster to update, works across models, doesn't require ML expertise.

### How is this different from Google Titans?

Titans modifies model architecture. SEED-ANT-PRISM is an orchestration layer. We work with any model; Titans requires adopting Google's approach. See [Comparison to Titans](VALIDATION/comparison-to-titans.md).

### What's the context window limit?

There isn't one. SEED compresses context; ANT navigates efficiently. We've tested with months of conversation history compressed into a single session.

---

## Validation

### Has this been peer-reviewed?

Not yet. Academic paper submission planned for Q1 2026. Current validation is documented in [VALIDATION/](VALIDATION/).

### How do you know this is novel?

We scanned 193 academic papers across 11 search queries. Zero prior art matches. See [Novelty Claim](VALIDATION/novelty-claim.md).

### What's the 27.9GB dataset?

Naturalistic AI conversation data collected over 4 weeks. 175,607 conversation files across GPT-4, Claude, Gemini, and Llama. Used for protocol development and validation.

### What's H-010 / KINGSLAYER?

Internal validation experiments. H-010 tested timeline prediction accuracy (100%). KINGSLAYER tested market signal detection. Both demonstrated protocol effectiveness.

---

## Business

### What stage is this?

Pre-revenue, validated research. Raising $500K seed to fund 6-9 month sprint.

### What's the business model?

Three revenue streams:
1. **Research consulting** — Protocol implementation for AI teams
2. **CMD School** — AI orchestration education platform
3. **IP licensing** — Enterprise SEED-ANT-PRISM licenses

### When will this be available?

Research is available now (this repo). Enterprise-ready implementation targeted for Q3 2026.

### Are you looking for investment?

Yes. Pre-seed round open. Contact joel@runedigitalstudio.com.

---

## Using the Protocols

### Can I use this in production?

The concepts are documented here. Production implementations require integration work. Contact us for consulting.

### Is the code open source?

Conceptual documentation is public. Implementation code is in the private investor repo. IP protection until we establish market position.

### Can I contribute?

We're not accepting public contributions at this stage. Academic collaboration inquiries welcome.

---

## Contact

### How do I get in touch?

- **Email:** joel@runedigitalstudio.com
- **Website:** runedigitalstudio.com
- **LinkedIn:** [Joel Parkinson](https://linkedin.com/in/joelparkinson)

### How do I access the private repo?

Investor access granted on request. Email with subject "Investor Repo Access" including your fund/company name.

---

## Quick Links

- [What is SEED-ANT-PRISM?](OVERVIEW/what-is-seed-ant-prism.md)
- [Problem Statement](OVERVIEW/problem-statement.md)
- [Protocol Documentation](PROTOCOLS/)
- [Validation Evidence](VALIDATION/)
- [Pitch Deck](MEDIA/pitch-deck.pdf)
