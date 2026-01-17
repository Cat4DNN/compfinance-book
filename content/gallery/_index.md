+++
title = "Gallery"
description = "Mathematical visualizations and formulas from the Handbook of Computational Finance."
template = "gallery/section.html"

[extra]
categories = ["Category Theory", "Stochastic Calculus", "Machine Learning", "Risk"]

[[extra.gallery_items]]
title = "Functor Definition"
description = "A functor F maps objects and morphisms between categories"
katex = "F: \\mathcal{C} \\to \\mathcal{D}"
category = "Category Theory"

[[extra.gallery_items]]
title = "Natural Transformation"
description = "A natural transformation between functors F and G"
katex = "\\eta: F \\Rightarrow G"
category = "Category Theory"

[[extra.gallery_items]]
title = "Monad Structure"
description = "The monad triple with unit and multiplication"
katex = "(T, \\eta, \\mu)"
category = "Category Theory"

[[extra.gallery_items]]
title = "Black-Scholes PDE"
description = "The fundamental equation for option pricing"
katex = "\\frac{\\partial V}{\\partial t} + \\frac{1}{2}\\sigma^2 S^2 \\frac{\\partial^2 V}{\\partial S^2} + rS\\frac{\\partial V}{\\partial S} - rV = 0"
category = "Stochastic Calculus"

[[extra.gallery_items]]
title = "Itô's Lemma"
description = "The chain rule for stochastic calculus"
katex = "df = \\frac{\\partial f}{\\partial t}dt + \\frac{\\partial f}{\\partial X}dX + \\frac{1}{2}\\frac{\\partial^2 f}{\\partial X^2}(dX)^2"
category = "Stochastic Calculus"

[[extra.gallery_items]]
title = "Geometric Brownian Motion"
description = "The standard model for stock price dynamics"
katex = "dS_t = \\mu S_t dt + \\sigma S_t dW_t"
category = "Stochastic Calculus"

[[extra.gallery_items]]
title = "Neural Network Layer"
description = "Forward pass through a neural network layer"
katex = "h^{(l)} = \\sigma(W^{(l)} h^{(l-1)} + b^{(l)})"
category = "Machine Learning"

[[extra.gallery_items]]
title = "Attention Mechanism"
description = "Scaled dot-product attention in transformers"
katex = "\\text{Attention}(Q,K,V) = \\text{softmax}\\left(\\frac{QK^T}{\\sqrt{d_k}}\\right)V"
category = "Machine Learning"

[[extra.gallery_items]]
title = "Loss Function"
description = "Cross-entropy loss for classification"
katex = "\\mathcal{L} = -\\sum_{i} y_i \\log(\\hat{y}_i)"
category = "Machine Learning"

[[extra.gallery_items]]
title = "Value at Risk"
description = "The VaR at confidence level α"
katex = "\\text{VaR}_\\alpha = -\\inf\\{x : P(X \\leq x) \\geq \\alpha\\}"
category = "Risk"

[[extra.gallery_items]]
title = "Expected Shortfall"
description = "Conditional expectation beyond VaR"
katex = "\\text{ES}_\\alpha = \\mathbb{E}[X | X \\leq \\text{VaR}_\\alpha]"
category = "Risk"

[[extra.gallery_items]]
title = "Portfolio Variance"
description = "Risk of a portfolio with weight vector w"
katex = "\\sigma_p^2 = w^T \\Sigma w"
category = "Risk"

+++

Explore mathematical formulas and concepts from the handbook. These expressions illustrate key ideas in categorical computational finance.

<div class="alert alert-info mt-4">
<strong>Note:</strong> All formulas are rendered using KaTeX. Hover over cards to see the interactive effects.
</div>
