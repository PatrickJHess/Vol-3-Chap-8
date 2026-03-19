# ***Convexity And Interest Rate Risk***

**Key Topics Covered**

* **Convexity measures magnitude of movements**  
    
  * Elaborates the effects of interest rate risk  
  * How duration predictions are modified by the magnitude of changes  
  * Comparing parallel to  realistic changes in the term structure  
  * Simulate the impact of changes in the slope and shape of the term structure  
    

    
* **Python concepts:**  
    
  * SciPy stats module simulates changes in yields to maturity  
  * NumPy arrays  
  * Pandas  
  * Accessing historical par yield data from the U.S.Treasury   
  * Custom modules.  
    * bond\_pay\_data  
    * calc\_duration  
    * calc\_convexity  
    * bond\_pv  
    * one\_y\_axis  
  * calc\_convexity developed in the chapter and added to the custom module

## ***Background***

This chapter's examples and discussions rely on the **Pandas** and **NumPy** libraries.

* **Pandas** is introduced in [*A Quick Introduction to Pandas*](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_Pandas.html#a-quick-introduction-to-pandas).  
* **NumPy** is introduced in [*A Quick Introduction to NumPy*](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/An_Introduction_To_NumPy.html#a-quick-introduction-to-numpy).  
* The bond\_pay\_data function is imported from [Chapter Three](https://patrickjhess.github.io/Imported-Functions/bond_pay_data.html#bond-pay-data-helper-function)  
* The calc\_duration function is imported from [Chapter Seven](https://patrickjhess.github.io/Imported-Functions/calc_duration.html)  
* The bond\_pv function is imported from [Chapter Six](https://patrickjhess.github.io/Imported-Functions/bond_pv.html#bond-pv-helper-function)   
* The one\_y\_axis function is imported from [Chapter One](https://patrickjhess.github.io/Imported-Functions/one_y_axis.html)  
* Additional relevant Python concepts can be found in the introductory volume, [*Background Material: An Introduction to Python for Financial Python*](https://patrickjhess.github.io/Introduction-To-Python-For-Financial-Python/intro.html), that relate to this and other chapters of *Basic Concepts of Fixed Income*.

**The chapter includes Six  sections:**

1. *Convexity measures movement and magnitude but not direction*  
     
   * elaborates on duration  
   * captures volatility of changes in yield to maturity

   

2. The  Jupyter notebook *Convexity and Parallel Shifts in Yields to Maturity*  
   * compares results of duration and convexity with two bonds  
   * calculates gross return from a long convexity zero duration trade

   

3. The jupyter notebook *Volatility and Correlation of Par Yields*  
    * demonstrates that the correlation of par yields are less than perfect  
    * short-term rates are more volatility than long-term and the volatility of all rates vary over time   
    * correlations of changes in par yield vary over time and are related to the respective maturities  
    
4. The jupyter notebook *Convexity and Changes in the Slope and Shape of the Term Structure*  
    * simulates changes in yields to maturity with the SciPy stats module.  
    * simulations document two convexity trades with parallel changes in yields and changes in the slope and shape of yields  
    * three questions are suggested for Gemini to deepen your understanding  
5. *Summarizing the results of calculating and using convexity*  
6. *Functions Imported by Chapter Eight* describes the function imported from DropBox (*module\_basic\_concepts\_fixed\_income*).

