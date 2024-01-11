# MAP55614-C-Programming-2021
MAP55614 C++ Programming in 2021, Assignment 1

## Assignment-1
For this assignment you will write some functionality for a class that we will call Gaussian. 
The bones of the class are provided along with a main function in the file assignment1.cc. 
You will write some member function definitions for the class, and also some non-member functions that provide the same functionality. 
The purpose of this is so that you can see both approaches. We will discuss the merits later.

The Gaussian distribution, $N (μ, σ2)$, has probability density function

$$\phi(x) = \frac{1}{\displaystyle \sigma \sqrt{2\pi}} e^{\displaystyle -\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$$

You will write functions which calculate the $φ(x)$ and also which approximate
the Cumulative Distribution Function (CDF), $Φ(x) = \int_{-\infty}^{x} φ(t)dt$, using numerical integration. 
You can compare your answer to a polynomial approximation for same. The code is included for the polynomial approximation and, for reference, is based off the document http://finmod.co.za/Better%20Approximations%20To%20Cumulative%20Normal%20Functions.pdf.

You will also use the identity that

$$\Phi(x) = \frac{1}{2} + \frac{1}{2}\text{erf}\left(\frac{x}{\sqrt{2}}\right)$$

and the inbuilt standard library complimentary error function, std::erfc, as an alternate way to calculate the same thing.
The main function is provided. You can write your own equivalent one, or else comment out bits of this one so that you can check that your code compiles as you are writing the individual functions. But when you submit the assignment, it should ideally be running with the provided main function.

## Note Comments

# Question-1

# Question-2

