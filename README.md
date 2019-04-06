# Orthogonal-Projection
Approximation of orthogonal projection of a point on a convex periodic curve, with period 1. The algorithm uses
a generic combination of *Steepest-descent* method and *Newton-Raphson (secant)* method.

Made as the Course Project 1 for Numerical Analysis and Scientific Computing-1 (MTH308B).

## Description
The problem statement does not emphasize of maximizing the efficiency. Hence, we can relax the restriction on the number
of Newton-Raphson iterations. However, to avoid an infinite loop in case of a malicious input or a badly conditioned
function, we limit the maximum number of iterations to *100000*.

The step value in NR is so chosen as to heavily-optimize the algorithm for the case when ε ≈ exp(-14), hinted as a possible
value by the instructor. Hence, it is reasonable for the algorithm to not be efficient for relatively larger values of ε.
Thus to circumvent the worst case possibility, iteration limit was chosen to be a very large number, i.e 100000 instead of say, 5000.

### Acknowledgement
@shivansh, for providing the implemention of previous version of the project. This project is built on top of that, 
taking into account the modification in the definition of accuracy, and the recommended approach of generalizing the
algorithm for maximum curves, than over-optimizing for a specific curve.
