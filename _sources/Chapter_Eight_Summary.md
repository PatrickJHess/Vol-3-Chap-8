# ***Summarizing Convexity and Interest Rate Risk***

Duration is derived from the first derivative of the present value function with respect to the yield to maturity and is only accurate for small changes in interest rates. Convexity is derived from the second derivative of the present value function with respect to the yield to maturity and attenuates the predicted losses of duration and amplifies the predicted gains (curvature of a convex function versus the linear approximation).

It's correct to relate volatility of interest rates to convexity.  The chapter explores  trades expressing views on volatility but are agnostic on directional changes of interest rates.  The risk of  convexity trades, but not their expected gain, depends upon how changes in interest rates affect the term structure.  The results for parallel shifts in interest rates are never less than zero; changes in the slope and shape of the term structure produces more volatility results often returning negative payoffs.  
   
The following table summarizes the results from simulating parallel and non-parallel changes in interest rates.  Expected payoffs are positively related to convexity; volatility depends upon how interest rates change are expressed.

|  | Long Thirty Short Twenty |  | Long Thirty Short Ten |  |
| :---- | ----- | ----- | ----- | ----- |
| **Duration** | 0 |  | 0 |  |
| **Convexity** | 98.07 |  | 219.12 |  |
| **Simulation Type** | Parallel | Non-Parallel | Parallel | Non-Parallel |
| **Mean** | 0.165 | 0.173 | 0.368 | 0.39 |
| **Standard Deviation** | 0.151 | 3.326 | 0.334 | 3.327 |
| **Minimum Value** | 0 | \-9.117 | 0 | \-8.236 |
| **25%  Percentile** | 0.031 | \-2.164 | 0.068 | \-1.981 |
| **50% Percentile** | 0.122 | 0.180 | 0.273 | 0.380 |
| **75% Percentile** | 0.273 | 2.506 | 0.613 | 2.752 |
| **Maximum Value** | 0.577 | 10.213 | 1.243 | 10.526 |

