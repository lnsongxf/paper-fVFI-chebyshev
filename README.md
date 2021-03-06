# paper-fVFI-chebyshev
Codes for "Fitted Value Function Iteration with Smolyak-Chebyshev Polynomials: Poor Performance in Practice"
These codes depend on both:
- VFI Toolkit: https://github.com/vfitoolkit/VFIToolkit-matlab
- JMMV2014 Chebyshev-Smolyak implementation: https://au.mathworks.com/matlabcentral/fileexchange/50963-smolyak-anisotropic-grid

WhatGoesWrong.m allows the user to look at the output in detail for a given order of Chebyshev polynomial and experiment for themselves with looking at generating invidual figures and results of the kind reported in the paper.
WhatGoesWrong_Table.m is, roughly speaking, a loop over this that produces the tables and results contained in the paper.

StochasticNeoClassicalGrowthModel_SmolyakChebyshev.m uses fitted Value Function Iteration with Smolyak-Chebyshev polynomials to solve the Stochastic NeoClassical Growth model. Warning: as described in the paper this method fails to converge to the correct solution (converges to incorrect solutions) for 'practical' orders of Chebyshev polynomial.

In principle the codes from the VFI Toolkit used to do the fitted Value Function Iteration with Smolyak-Chebyshev polynomials (as applied to the Stochastic NeoClassical Growth model in StochasticNeoClassicalGrowthModel_SmolyakChebyshev.m) could be used to solve any VFI problem in which all (endogenous and exogenous) state and decision variables are continous; that is, for problems with any number of dimensions. But as emphasised in the paper the required orders of the Chebyshev polynomials are simply impractical.
