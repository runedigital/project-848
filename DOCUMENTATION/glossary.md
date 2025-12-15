# Glossary

*Key terms used in Project 848 documentation*

---

## Core Concepts

### SEED-ANT-PRISM
The three-layer protocol stack for AI memory optimization. SEED compresses context, ANT navigates via trails, PRISM refracts output for specific users.

### Pheromone Dynamics
The biological model for our approach. Ant colonies use pheromone trails that strengthen with use and decay over time. We apply this to AI context management.

### Trail
A weighted connection between two pieces of context. Trails strengthen when used together successfully, decay when unused. The core primitive of ANT protocol.

### Decay Gradient
The rate at which unused context fades. Different contexts decay at different rates (fast for daily updates, slow for foundational knowledge).

### Context Regeneration
The process of expanding a compressed SEED into full context. Like generating a Minecraft world from a seed.

### Refraction
Adapting output for a specific observer. Same knowledge, different presentations based on role, expertise, and context.

---

## Protocol-Specific

### SEED
**S**eed-**E**xtracted **E**ncoding **D**ynamics. The compression layer. Encodes context patterns into compact representations that can regenerate full context on demand.

### ANT
**A**daptive **N**avigation **T**rails. The navigation layer. Follows pheromone-strength trails to find relevant context based on usage patterns.

### PRISM
**P**ersonalized **R**efraction **I**nput **S**haping **M**odule. The output layer. Adapts AI responses based on who's asking and their context.

---

## Technical Terms

### Orchestration Layer
Software that coordinates between user and AI model without modifying the model itself. SEED-ANT-PRISM operates at this layer.

### Context Window
The amount of text an LLM can process at once. GPT-4: 128K tokens. Claude: 200K tokens. SEED-ANT-PRISM extends effective context beyond these limits.

### RAG (Retrieval Augmented Generation)
A technique that retrieves relevant documents and adds them to the prompt. Different from ANT's trail-based navigation.

### Fine-Tuning
Training an AI model on specific data to specialize it. Expensive, slow, requires ML expertise. SEED-ANT-PRISM avoids this.

### Titans
Google's research on memory-augmented transformers. Modifies model architecture. Different layer than our approach.

### Naturalistic Data
AI conversation data collected from real usage, not synthetic benchmarks. Our 27.9GB dataset is naturalistic.

---

## Validation Terms

### Prior Art
Previously published work on the same topic. We found zero prior art for pheromone-inspired LLM memory.

### H-010
Internal hypothesis: timeline prediction accuracy using ANT protocols. Result: 100% accuracy.

### KINGSLAYER
Internal experiment: market signal detection using decay gradients. Result: Detected SVB signals 3 days early.

### Novelty Claim
Assertion that our approach has not been previously published. Verified via 193-paper scan.

---

## Business Terms

### Pre-Seed
Early-stage funding before significant revenue. We're raising $500K pre-seed.

### CMD School
Planned education platform for AI orchestration. Free tier + premium ($9-49/mo).

### IP Licensing
Revenue from licensing SEED-ANT-PRISM protocols to enterprises.

---

## Biological References

### Ant Colony Optimization (ACO)
Established field using ant behavior for routing/scheduling problems. We apply similar principles to memory, not routing.

### Stigmergy
Indirect coordination through environment modification. Ants coordinate via pheromone trails without direct communication.

### Emergent Intelligence
Complex behavior arising from simple rules. No ant knows the big picture, but colonies solve complex problems.

---

## Acronyms

| Acronym | Meaning |
|---------|---------|
| ACO | Ant Colony Optimization |
| API | Application Programming Interface |
| GPU | Graphics Processing Unit |
| LLM | Large Language Model |
| ML | Machine Learning |
| NLP | Natural Language Processing |
| RAG | Retrieval Augmented Generation |
| VC | Venture Capital |

---

## Learn More

- [What is SEED-ANT-PRISM?](../OVERVIEW/what-is-seed-ant-prism.md)
- [Why Pheromones?](../OVERVIEW/why-pheromones.md)
- [FAQ](FAQ.md)
