+++
title = "Algebraic Effects: Type-Safe Side Effects for Financial Systems"
description = "Understanding algebraic effects and delimited continuations, and why they're perfect for building robust financial applications."
date = 2025-01-05T09:00:00+00:00
draft = false
template = "blog/page.html"

[taxonomies]
tags = ["algebraic-effects", "functional-programming", "finance", "type-theory"]

[extra]
lead = "Algebraic effects offer a revolutionary approach to handling side effects in programming. Here's why they're a game-changer for financial systems."
math = true
+++

Financial applications are notoriously complex. They need to handle:
- Network failures
- Partial transactions
- Concurrent operations
- Rollback on errors
- Audit logging
- And much more...

Traditional approaches — callbacks, promises, actors — often lead to tangled, hard-to-reason-about code. **Algebraic effects** offer a better way.

## What Are Algebraic Effects?

At their core, algebraic effects let you *declare* what effects your code needs, without *defining* how those effects are handled. The actual implementation is provided separately by **effect handlers**.

Think of it like this:
- **Effects** = "I need to do X" (declare)
- **Handlers** = "Here's how X works" (implement)

This separation is powerful because:
1. The same code can work with different handlers
2. Effects compose naturally
3. The type system tracks which effects are used

## A Financial Example

Consider a pricing function that needs market data:

```scala
def priceOption[S](strike: Double): Price < (Market & Risk & S) =
  for
    spot   <- Market.spot
    vol    <- Market.impliedVol
    risk   <- Risk.assess(spot, vol)
    price  <- Pricing.blackScholes(spot, vol, risk)
  yield price
```

The type `Price < (Market & Risk & S)` tells us:
- Returns a `Price`
- Requires `Market` and `Risk` effects
- May have additional effects `S`

The handler decides how to provide market data — live feed, historical data, or mock data for testing.

## Delimited Continuations: The Magic Behind Effects

Algebraic effects are powered by **delimited continuations**. A continuation represents "the rest of the computation."

$$\kappa: (A \to R) \to R$$

When an effect is performed, the continuation is captured. The handler can then:
- **Resume once**: Normal execution
- **Resume multiple times**: Fan-out for parallel pricing
- **Resume zero times**: Abort/rollback
- **Resume later**: Checkpoint for long-running tasks

### Practical Applications

This enables patterns crucial for finance:

**1. Speculative Execution**
```
Try multiple pricing models in parallel, take the fastest
```

**2. Transactional Rollback**
```
If any leg of a multi-leg trade fails, undo everything
```

**3. Checkpoint/Resume**
```
Long-running optimisation can be paused and resumed
```

**4. Consensus Pricing**
```
Fan-out to multiple sources, aggregate results
```

## Why This Matters for Finance

Financial systems need to be:
- **Correct**: Types prevent entire classes of bugs
- **Auditable**: Effect tracking provides clear execution traces
- **Maintainable**: Separation of concerns reduces complexity
- **Testable**: Swap handlers for deterministic testing

Algebraic effects deliver all of this.

## Kyo: A Modern Effect System

[Kyo](https://github.com/getkyo/kyo), developed at Nubank, is a Scala library that makes algebraic effects practical:

- First-class delimited continuations
- Zero-overhead when no effects are used
- Composable effect handlers
- Full type inference

It's being used in production financial systems today.

## Conclusion

Algebraic effects represent a fundamental shift in how we think about programming with side effects. For financial systems — where correctness is paramount and complexity is unavoidable — they're not just nice-to-have; they're essential.

---

*Want to learn more? Check out my [research](/research/) on algebraic effects in financial systems, or [reach out](/contact/) directly.*
