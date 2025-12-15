# ANT Protocol — Trail Navigation

*How ant colonies navigate: paths strengthen with use, fade with neglect*

---

## Core Concept

Ant colonies find shortest paths without maps. They use pheromone trails:
- Successful paths get marked with pheromones
- Other ants follow stronger trails
- Trails evaporate over time
- Popular paths strengthen; unused paths disappear

ANT applies this to AI memory navigation.

---

## The Problem It Solves

### Current Approach (RAG)
```
Query: "What did we decide about the API?"
Retrieval: Vector similarity search
Result: 10 potentially-relevant chunks (may miss key context)
```

### ANT Approach
```
Query: "What did we decide about the API?"
Navigation: Follow API → decisions trail
Result: Connected context along well-worn paths
```

Trail-based navigation follows **actual usage patterns**, not just semantic similarity.

---

## How It Works

### 1. Trail Creation
When context A leads to successful use of context B, a trail forms:
```
A ──[trail]──> B
```

### 2. Trail Strengthening
Each successful use strengthens the trail:
```
A ══[strong trail]══> B    (frequently used together)
A ──[weak trail]──> C      (rarely used together)
```

### 3. Trail Decay
Unused trails fade over time:
```
Day 1: A ══════> B (strength: 100)
Day 7: A ════> B   (strength: 70)
Day 30: A ──> B    (strength: 30)
Day 60: (trail gone)
```

### 4. Trail Following
When navigating, prioritize strong trails:
```
Query → Find entry point → Follow strongest trails → Return connected context
```

---

## The Decay Function

ANT uses pheromone-inspired exponential decay:

```
strength(t) = initial_strength × e^(-λt)
```

Where:
- `t` = time since last use
- `λ` = decay rate (configurable per use case)

Fast-moving contexts (daily standups) decay quickly.
Foundational knowledge (company values) decays slowly.

---

## Why This Works

### 1. Reflects Actual Usage
Trails form based on what people actually access together. Not just semantic similarity — real behavioral patterns.

### 2. Self-Organizing
No manual tagging or categorization. The system organizes itself based on use.

### 3. Natural Cleanup
Obsolete context fades away. No manual deletion required.

### 4. Handles Ambiguity
Same term, different contexts? Trails lead to the right interpretation based on current navigation path.

---

## Trade-offs

### ✅ Advantages
- Follows actual usage patterns
- Self-organizing
- Natural decay prevents bloat
- Handles context switches gracefully

### ⚠️ Limitations
- Cold start problem (new contexts have no trails)
- Decay rates need tuning per domain
- May miss rarely-used but important context

---

## Use Cases

### Project Context Switching
Working on Project A? ANT follows trails from "Project A" to related decisions, people, and resources.

### Conversational Memory
Recent topics have strong trails. Old topics fade unless reinforced.

### Knowledge Base Navigation
Organizational knowledge forms natural highways. Key documents get strong trails from everywhere.

---

## Integration

ANT is the second layer in the SEED-ANT-PRISM stack.

```
Query → [SEED: regenerate context] → [ANT: navigate trails] → [PRISM: refract output] → Response
```

SEED provides compressed context. ANT navigates to the right parts. PRISM shapes the output.

---

## Learn More

- [SEED Protocol](SEED-overview.md) — Context regeneration
- [PRISM Protocol](PRISM-overview.md) — Output refraction
- [Why Pheromones?](../OVERVIEW/why-pheromones.md) — The biological inspiration
