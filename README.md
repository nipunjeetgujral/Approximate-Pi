## Defining Problem

The famously irrational number pi in a number than can be conceptuialized by humans and used regularly in computations by simpily using symbology as means of representing all the copmlexity imbune with $\pi$. But for a computer, such an irrational number can provide to be difficult due to limitation in memory and the utlization of the Base-2 (binary) number system. We as humans have therefore devised methods of approximating pi using computational method dependent on iterative estimations that provide a closer approximation to true pi. The following code will use various methods to approximate pi and include analysis on which method provides that most accruate and speedy approximatation of pi. 

Regarding the methods used to estimate pi, I chose to use the Talor Series Expansion (TSE) method and two variations of Monte Carlo Simulation (MCS) methods to test which method more accurately and rapidly approximates pi as listed below:

### Approximating $\pi$ via the Taylor Series Expansion:

$$\pi = 4 \sum_{i=1}^{n} \frac{(-1)^{n}}{2n-1}$$

$$ \pi = 4 \left( 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \frac{1}{9} ... \frac{1}{n} \right) = 3.1415926...$$

### Aproximating $\pi$ via Monte Carlo Simulation:


![MC_Simulation](./Monte_Carlo_Approximation.gif)


However two variations of MCS are used; one method involving the traditional _Numpy_ library from which so much of Python is based on, and the other involves the use of **IBM's Quantum Computing** simulator via the _Qiskit_ library. Implicitly the MCS method of approximting $\pi$ relies on the utilization of random numbers and is therefore best suited for the application of a Quantum Computer, as such machines are fickle to say the least. The errant and unreliable nature of the current iterations of quantum computers provides a degree of randomness that would be best suited in this application as it might accelerate the approximation of $\pi$ by using fewer iterations to produces a reasonable answer.


### Test and Evaluation:

Testing and evaluating the aforementioned algorithms require the use of large populations within whihc iterative computations can take-place. This below code uses test populations of $10^{2}, 10^{3}, 10^{4}, 10^{5}, 10^{6}, 10^{7}$ and $10^{8}$ to test the accuracy and speed of the algorithms at large scale and to illustrate any asymptotic behaviors.
