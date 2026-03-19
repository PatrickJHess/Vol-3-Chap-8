# Financial Python

## Volume: Basic Concepts of Fixed Income

### Chapter Eight: Convexity And Interest Rate Risk

Chapter Seven introduces duration as the primary measure of interest rate risk for bonds. It's natural to draw parallels between duration and the Capital Asset Pricing Model's (CAPM) beta, it's important to recognize a key difference: beta is a parameter of an equilibrium model, offering insights beyond mere empirical observation. Duration is less profound; it is a powerful mathematical tool but does not offer predictions about expected bond returns. It is, however, exceedingly useful math.$^{1}$

This chapter builds upon this "useful math" by incorporating the second derivative of the bond's present value formula to define bond convexity, a concept mentioned briefly in Chapter Seven. Duration is directional; convexity corrects the directrion of duration.  Duration-bets bet on a direction; convexity-bets bet on movement.


**Parallel Versus Non-Parallel Changes In The Term Structure**

Convexity, a mathematical concept, predicts bond relative price changes when the term structure shifts in a parallel manner. Variations in the slope and shape of the term structure cause actual bond relative prices to diverge from these predictions. Data from the U.S. Treasury documents that the shape and slope of the term structure varies over time.  The chapter presents simulations of convexity trades with changes in the slope and shape of the term structure.   Results that  are perfectly predictable with parallel shifts, demonstrate significant variability with non-parallel changes in the term structure.

### Leapfroggging into the chapter

Like other chapters, there are no required dependencies between this and previous chapters. If you are unfamiliar with the material, you will benefit from reviewing previous chapters but you can begin here. As needed, the previously developed functions used in this chapter are imported from  a custom module. These functions are sufficient for you to benefit from the chapter.


---
$^{1}$Of course beta can be viewed as a useful statistical relation and not a parameter of an equilibrium.  That view is in the spirit of much of total risk or factor investing. Beta and the CAPM are covered in more depth in the *Asset Pricing* volume.

