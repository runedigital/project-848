# PRISM Protocol — Output Refraction

*Same knowledge, different views — like light through a prism*

---

## Core Concept

White light contains all colors. A prism separates it into a spectrum based on the observer's angle.

PRISM applies this to AI output.

Same underlying knowledge. Different presentations based on who's asking, what they need, and their current context.

---

## The Problem It Solves

### Current Approach
```
Query: "Explain our API architecture"
Result: Same technical explanation for everyone
```

### PRISM Approach
```
Query: "Explain our API architecture"
To Developer: Code examples, endpoints, authentication flow
To Manager: System diagram, team responsibilities, timeline
To Customer: What it enables, why it matters, no jargon
```

One knowledge base. Multiple refractions.

---

## How It Works

### 1. Observer Profile
PRISM maintains context about who's asking:
- Role (developer, manager, customer)
- Expertise level (beginner, intermediate, expert)
- Current task (debugging, planning, learning)
- Preferences (verbose, concise, visual)

### 2. Refraction Rules
Based on observer profile, apply transformation:
```
Expert Developer → Technical depth, code examples, edge cases
Non-Technical Stakeholder → Analogies, business impact, no jargon
Quick Check → Bullet points, key facts only
Deep Dive → Full context, related topics, history
```

### 3. Output Shaping
Same underlying knowledge, shaped for the observer:
```
Raw Knowledge: "API uses OAuth 2.0 with refresh tokens, rate limited to 100 req/min"

→ Developer: "Auth: OAuth 2.0 + refresh tokens. Rate limit: 100/min. See /auth endpoint."
→ Manager: "Security handled via industry-standard auth. Scales to expected load."
→ Customer: "Your data is protected with bank-level security."
```

---

## Why This Works

### 1. Knowledge Stays Unified
One source of truth. No duplicate documentation for different audiences.

### 2. Reduces Cognitive Load
People get what they need, in the format they can use.

### 3. Enables Personalization
AI that adapts to you, not AI that treats everyone the same.

### 4. Scales Communication
One expert's knowledge, accessible to entire organization at appropriate levels.

---

## Trade-offs

### ✅ Advantages
- Personalized output without duplicate content
- Reduces jargon/complexity barriers
- Enables multi-stakeholder communication
- Learns observer preferences over time

### ⚠️ Limitations
- Requires observer profiling
- Risk of over-simplification for non-experts
- Need to maintain accuracy across refractions

---

## Use Cases

### Documentation
One technical doc, auto-refracted for developers, managers, and new hires.

### Customer Support
Same knowledge base serves different customer sophistication levels.

### Internal Communication
Engineering updates translated appropriately for sales, legal, executive audiences.

### Learning Systems
Adaptive difficulty based on learner progress.

---

## Integration

PRISM is the third layer in the SEED-ANT-PRISM stack.

```
Query → [SEED: regenerate context] → [ANT: navigate trails] → [PRISM: refract output] → Response
```

SEED provides context. ANT navigates to relevant knowledge. PRISM shapes it for this specific request.

---

## Observer Profiles

PRISM maintains lightweight profiles:

```json
{
  "role": "developer",
  "expertise": "senior",
  "preferences": {
    "verbosity": "concise",
    "examples": true,
    "format": "markdown"
  },
  "current_context": "debugging auth flow"
}
```

Profiles update based on interactions. No manual configuration required.

---

## Learn More

- [SEED Protocol](SEED-overview.md) — Context regeneration
- [ANT Protocol](ANT-overview.md) — Trail navigation
- [What is SEED-ANT-PRISM?](../OVERVIEW/what-is-seed-ant-prism.md) — Full overview
