+++
title = "Research"
description = "Explore Serge Youmbi's research areas: Category Theory, Deep Learning, Multi-Agent AI Systems, and Computational Finance."
sort_by = "weight"
weight = 1
template = "research/section.html"

[extra]
lead = "Undertaking research at the intersection of abstract mathematics and practical AI applications."
+++

My research program explores how **category-theoretic abstractions** can inform the design of **robust AI systems** for **computational finance**. This interdisciplinary work spans pure mathematics, theoretical computer science, and quantitative finance.

---

## Core Research Areas

### 1. Category Theory & Deep Learning

Category theory provides a powerful language for understanding the compositional structure of neural networks. My work explores:

- **Functorial Neural Networks** — Viewing layers as functors between categories of representations
- **Natural Transformations** — Understanding parameter sharing and architectural symmetries
- **Monoidal Categories** — Formalising tensor operations and attention mechanisms
- **Backpropagation as a Functor** — Categorical semantics for automatic differentiation

$$F: \mathcal{C} \to \mathcal{D}$$

Where $F$ preserves the compositional structure: $F(g \circ f) = F(g) \circ F(f)$

---

### 2. Multi-Agent AI Systems for Finance

Modern financial markets demand intelligent systems that can process diverse information streams and make coordinated decisions. My research develops:

- **LLM Agent Orchestration** — Coordinating specialised agents for fundamental, technical, and sentiment analysis
- **Consensus Mechanisms** — Aggregating agent opinions for robust decision-making
- **Risk-Aware Trading** — Agents with heterogeneous risk profiles collaborating on portfolio construction
- **Systematic Deliberation** — Structured reasoning protocols for financial strategy formulation

---

### 3. Algebraic Effects in Financial Systems

Financial applications require sophisticated control flow: speculative execution, transactional semantics, and checkpoint/resume for long-running optimisations. Using **Kyo's algebraic effect system**, I explore:

- **Delimited Continuations** — First-class continuations for flexible control flow
- **Effect Handlers** — Type-safe management of side effects in trading systems
- **Transactional Rollback** — Atomicity for multi-leg trades
- **Formal Reasoning** — Mathematical proofs for regulatory compliance

```scala
// Type-safe effect tracking in Kyo
def pricingEngine[S]: Price < (Market & Risk & S) =
  for
    spot   <- Market.spot
    vol    <- Market.impliedVol
    risk   <- Risk.assess(spot, vol)
    price  <- Pricing.blackScholes(spot, vol, risk)
  yield price
```

---

### 4. Generalisations of Bigraphs

Robin Milner's **Bigraphs** provide a mathematical framework for modelling systems with both spatial structure (place graphs) and connectivity (link graphs). My work extends this to **Trigraphs**:

- **Third Structural Component** — Exploring temporal, computational, or informational dimensions
- **Symmetric Partial Monoidal Categories** — Extending categorical operations
- **Applications to Distributed Systems** — Modelling complex multi-agent interactions

---

### 5. Supply Chain Optimisation

Applying AI to supply chain management, focusing on:

- **Multi-LLM Orchestration** — Dynamic model selection based on task characteristics
- **Operations Research Integration** — Combining classical optimisation with modern AI
- **Resilience & Efficiency** — Balancing competing objectives in uncertain environments

---

## Research Impact

My research aims to:

1. **Advance Theory** — Develop new mathematical frameworks for understanding AI systems
2. **Enable Practice** — Create tools and architectures deployable in production
3. **Ensure Safety** — Provide formal guarantees for AI systems in high-stakes domains
4. **Foster Collaboration** — Bridge communities across mathematics, CS, and finance

---

## Current Projects

| Project | Status | Collaborators |
|---------|--------|---------------|
| Multi-Agent Portfolio Management | Active | University of Derby |
| Algebraic Effects for Trading Systems | Active | — |
| Trigraphs: Generalising Bigraphs | Active | — |
| Category-Theoretic Deep Learning | Ongoing | — |

---

<div class="text-center mt-5">
  <a href="https://derby.academia.edu/SergeYoumbi" class="btn btn-primary btn-lg" target="_blank">View Publications</a>
  <a href="https://cat4dnn.github.io/sergeyoumbi/contact/" class="btn btn-outline-primary btn-lg ms-3">Collaborate With Me</a>
</div>
