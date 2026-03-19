

# What is convexity and why does it matter

Chapter Seven introduces duration as the primary measure of interest rate risk for bonds. It's natural to draw parallels between duration and the Capital Asset Pricing Model's (CAPM) beta, it's important to recognize a key difference: beta is a parameter of an equilibrium model, offering insights beyond mere empirical observation. Duration is less profound; it is a powerful mathematical tool but does not offer predictions about expected bond returns. It is, however, exceedingly useful math.$^{1}$

This chapter builds upon this "useful math" by incorporating the second derivative of the bond's present value formula to define bond convexity, a concept mentioned briefly in Chapter Seven;  we now explore in depth.

### Duration Revisited

As a refresher, a bond's duration is defined as the negative of its first derivative with respect to its yield to maturity ($\text{ytm}$), divided by the bond's value. Duration forms the basis of the first-order Taylor series approximation for changes in bond values due to changes in $\text{ytm}$:

$$\text{Change in Value} \approx -\Delta \text{ytm} \times \text{Modified Duration}$$

In terms of the mathematical components:

$$V(\text{ytm}+\Delta \text{ytm})-V(\text{ytm})\approx -\Delta \text{ytm}\times\sum_{i=1}^{N}t_i\times Cash\ Flow_{t_i} \times e^{-\text{ytm}\times t_i}$$

### Introducing Convexity via Taylor Series Expansion

The general form of a Taylor series expansion is:

$$f(x+\Delta x)\approx \sum\_{i=1}^{N}\frac{d^{i}f(x)}{dx^{i}}\times\frac{1}{i\!}\Delta x^{i}$$

Convexity is defined using the second-order Taylor series expansion:

$$f(x+\Delta x)\thickapprox f(x)+\frac{df(x)}{dx}\times\Delta x+\frac{1}{2}\frac{d^{2}f(x)}{dx^{2}}\times\Delta x^{2}$$

Applying this second-order expansion to the present value formula yields a more accurate estimate of the change in bond value:

\begin{aligned}
V(\text{ytm}+\Delta \text{ytm})-V(\text{ytm})\approx & -\Delta \text{ytm}\times\sum_{i=1}^{N}t_i\times Cash\ Flow_{t_i} \times e^{-\text{ytm}\times t_i} \\ & + \frac{\Delta \text{ytm}^{2}}{2}\times\sum_{i=1}^{N}t_i^{2}\times Cash\ Flow_{t_i} \times e^{-\text{ytm}\times t_i}
\end{aligned}

### The Convexity Formula

Mirroring the definition of duration, convexity is calculated by dividing the bond's second derivative with respect to $\text{ytm}$ by the bond's value:

$$Convexity =\frac{\sum_{i=1}^{N}t_i^{2}\times Cash\ Flow_{t_i} \times e^{-\text{ytm}\times t_i}}{V(\text{ytm})}$$

## Convexity and Duration Predict Bond Price Changes.
The change in bond price ($\Delta V$) can be predicted using a second-order Taylor expansion that incorporates both duration and convexity, as shown below:

<br>

$$\Delta V \approx (Duration \times -\Delta \text{ytm} + \frac{1}{2} \times Convexity \times \Delta \text{ytm}^{2}) \times V(\text{ytm})$$
<br>

The change in yield to maturity ($\Delta \text{ytm}$) can be broken down into its expected value ($E(\Delta \text{ytm})$) and its deviation from that expected value:

<br>

$$\Delta \text{ytm} = (\Delta \text{ytm} - E(\Delta \text{ytm}) + E(\Delta \text{ytm})$$

<br>

The squared change in yield to maturity is:

<br>

$$\Delta \text{ytm}^{2} = (\Delta \text{ytm} - E(\Delta \text{ytm})^{2} + E(\Delta \text{ytm})^{2}+2 \times (\Delta \text{ytm} - E(\Delta \text{ytm}) \times E(\Delta \text{ytm})$$

<br>

Consequently, the expected value of the squared change in yield to maturity is:

<br>

$$E(\Delta \text{ytm}^{2}) = \sigma_{\Delta \text{ytm}}^{2}+E(\Delta \text{ytm})^{2}$$

<br>

Substituting the expected values into the Taylor expansion, the expected change in the bond's value is:

<br>

$$E(\Delta V) =(Duration \times -E(\Delta \text{ytm})+ \frac{1}{2} \times Convexity \times (\sigma_{\Delta \text{ytm}}^{2}+E(\Delta \text{ytm})^{2}) \times V(\text{ytm})$$

<br>

The second-order Taylor expansion reveals two primary effects on the expected bond price changes:

<br>


*  $\qquad\textbf{Direction:}\quad   -Duration\times E(\Delta \text{ytm})$
*  $\qquad\textbf{Volatility:}\quad  \frac{1}{2}\times Convexity\times (\sigma^{2}_{\Delta \text{ytm}}+E(\Delta \text{ytm})^2)$

## <font color='green'>Application: Assume that the probability of the increased and decreased YTM is 0.5. Calculate the effect of convexity on the expected bond prices.</font>
<br>

<div>

**Settlement date is January 31$^{st}$ 2026**


|Maturity|Coupon|Initial YTM|Duration|Convexity|Increased YTM|Decreased YTM|Increased YTM|Decreased YTM|
|-------|-------|-----------|------------|--------------|------------|--------------|------------|--------------|
|&nbsp;&nbsp;&nbsp;December 31$^{st}$ 2035|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.0|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5%|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;7.9|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;71.9|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;7%|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3%|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.25%|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.75%|
|&nbsp;&nbsp;&nbsp;December 31$^{st}$ 2055|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.0|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5%|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;15.7|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;357.1|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;7%|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3%|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5.25%|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.75%


<br>


see [Chapter Eight Hints: Calculate the effect of convexity on the expected bond prices](https://colab.research.google.com/drive/1WL30MXvTfn3tTNQaaas2bmHn3G5E3lK4#scrollTo=kfPak5yXNMEq), and check the [expected results here](https://colab.research.google.com/drive/1jULdrPyul6Xs5Zrm4ysXezNNuJG7K6l6#scrollTo=kfPak5yXNMEq).

</div>

## Convexity and Duration: A Portfolio Perspective

The duration of a bond is calculated as the weighted average of the time to each of the bond's payments. The weight for each payment is determined by the present value of that cash flow relative to the total value of the bond.

<br>

$$\text{Duration} = \sum_{i=1}^{N}t_i \times w_{t_i}$$

<br>

$$\text{Where } w_{t_i} = \frac{\text{Cash Flow}_{t_i} \times e^{-\text{ytm} \times t_i}}{V(-\text{ytm})} \quad \text{and} \quad \sum_{i=1}^{N}w_{t_i} = 1$$

<br>

Similarly, the bond's convexity is defined as the weighted average of the squared payment dates, using the identical weights as those used for duration:

<br>

$$\text{Convexity} = \sum_{i=1}^{N}t_i^{2} \times w_{t_i}$$

<br>

The concepts of duration and convexity fundamentally incorporate the arbitrage principle, much like the present value calculation. A bond can be conceptualized as a composite portfolio of zero-coupon bonds, where each component bond represents a single cash flow weighted by its present value. Consequently, a bond's overall duration and convexity are simply the sum of the durations and convexities of these individual cash flows, weighted by their contribution to the total portfolio value. This analogy highlights that duration and convexity of a bond is akin to the convexity of a portfolio and that is simply the weighted average of the duration and convexity of all the cash flows of the portfolio.


---
$^{1}$Of course beta can be viewed as a useful statistical relation and not a parameter of an equilibrium.  That view is in the spirit of much of total risk or factor investing. Beta and the CAPM are covered in more depth in the *Asset Pricing* volume.

