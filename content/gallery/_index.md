+++
title = "Gallery"
description = "Mathematical visualizations, research diagrams, and key formulas from my work in Category Theory, Deep Learning, and Computational Finance."
template = "gallery/section.html"

[extra]
lead = "Visual representations of key concepts from my research."
categories = ["Category Theory", "Multi-Agent AI", "Deep Learning", "Finance"]

[[extra.gallery_items]]
title = "Functor Definition"
description = "A functor F maps objects and morphisms between categories - the foundation of categorical deep learning"
katex = "F: \\mathcal{C} \\to \\mathcal{D}"
category = "Category Theory"

[[extra.gallery_items]]
title = "Natural Transformation"
description = "Natural transformations relate functors, capturing parameter sharing in neural architectures"
katex = "\\eta: F \\Rightarrow G"
category = "Category Theory"

[[extra.gallery_items]]
title = "Monad Structure"
description = "Monads encode computational effects - essential for functional AI systems"
katex = "(T, \\eta, \\mu) \\text{ where } \\mu: T^2 \\Rightarrow T"
category = "Category Theory"

[[extra.gallery_items]]
title = "Bigraph Composition"
description = "Composition in Milner's Bigraphs, a foundation for Trigraphs"
katex = "G \\circ F: A \\to C"
category = "Category Theory"

[[extra.gallery_items]]
title = "Agent Consensus"
description = "Multi-agent weighted voting for portfolio decisions"
katex = "\\pi^* = \\sum_{i=1}^{n} w_i \\cdot \\pi_i \\text{ s.t. } \\sum w_i = 1"
category = "Multi-Agent AI"

[[extra.gallery_items]]
title = "Sharpe Ratio"
description = "Risk-adjusted performance metric optimised by our multi-agent system"
katex = "S = \\frac{\\mathbb{E}[R_p - R_f]}{\\sigma_p}"
category = "Multi-Agent AI"

[[extra.gallery_items]]
title = "Algebraic Effect"
description = "Effect signature in Kyo's algebraic effect system"
katex = "\\text{op}: A \\to B < E"
category = "Multi-Agent AI"

[[extra.gallery_items]]
title = "Continuation Type"
description = "Delimited continuation for control flow in financial systems"
katex = "\\kappa: (A \\to R) \\to R"
category = "Multi-Agent AI"

[[extra.gallery_items]]
title = "Attention Mechanism"
description = "Scaled dot-product attention, the heart of transformer architectures"
katex = "\\text{Attention}(Q,K,V) = \\text{softmax}\\left(\\frac{QK^T}{\\sqrt{d_k}}\\right)V"
category = "Deep Learning"

[[extra.gallery_items]]
title = "Neural SDE"
description = "Neural stochastic differential equation for financial modelling"
katex = "dX_t = f_\\theta(X_t, t)dt + g_\\phi(X_t, t)dW_t"
category = "Deep Learning"

[[extra.gallery_items]]
title = "Backpropagation"
description = "Gradient computation - viewing backprop as a functor"
katex = "\\frac{\\partial \\mathcal{L}}{\\partial w} = \\frac{\\partial \\mathcal{L}}{\\partial y} \\cdot \\frac{\\partial y}{\\partial w}"
category = "Deep Learning"

[[extra.gallery_items]]
title = "Black-Scholes PDE"
description = "The fundamental equation for European option pricing"
katex = "\\frac{\\partial V}{\\partial t} + \\frac{1}{2}\\sigma^2 S^2 \\frac{\\partial^2 V}{\\partial S^2} + rS\\frac{\\partial V}{\\partial S} - rV = 0"
category = "Finance"

[[extra.gallery_items]]
title = "Risk-Neutral Pricing"
description = "Derivative pricing under the risk-neutral measure"
katex = "V_0 = e^{-rT}\\mathbb{E}^{\\mathbb{Q}}[\\text{Payoff}]"
category = "Finance"

[[extra.gallery_items]]
title = "Portfolio Optimisation"
description = "Mean-variance optimisation objective"
katex = "\\max_w \\left\\{ w^T \\mu - \\frac{\\lambda}{2} w^T \\Sigma w \\right\\}"
category = "Finance"

[[extra.gallery_items]]
title = "Expected Shortfall"
description = "Coherent risk measure used in our multi-agent system"
katex = "\\text{ES}_\\alpha = -\\frac{1}{\\alpha}\\int_0^\\alpha \\text{VaR}_u \\, du"
category = "Finance"

+++

Explore the mathematical foundations underlying my research. These formulas and concepts bridge category theory, AI systems, and computational finance.

<div class="alert alert-info mt-4">
<strong>Interactive Gallery:</strong> All formulas are rendered using KaTeX. These represent key concepts from my publications and ongoing research.
</div>
