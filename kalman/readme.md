# Kalman filtering notes

Regardless of models and optimization processes, it is good to keep in mind
[Goodhart's Law](https://en.wikipedia.org/wiki/Goodhart%27s_law) in 
mind. Goodhart's law is the idea that "When a measure becomes a target, it ceases to be a good measure." 
One way in which this can occur is individuals trying to anticipate the effect of 
a policy and then taking actions that alter its outcome. 

## Theory


- [Kalman filter on Wikipedia](https://en.wikipedia.org/wiki/Kalman_filter): In statistics
and control theory, Kalman filtering, also known as linear quadratic estimation (LQE), is an 
algorithm that uses a series of measurements observed over time, containing statistical noise 
and other inaccuracies, and produces estimates of unknown variables that tend to be more accurate 
than those based on a single measurement alone, by estimating a joint probability distribution over 
the variables for each timeframe. The filter is named after Rudolf E. Kálmán, 
one of the primary developers of its theory.

## My notes
Kalman filter's main claim to fame is that it minimizes prediction error based
on the covariance of the components (random variables) of the time varying,
real valued, 
state vector. In other words, Kalman filtering exploits:
1. correlation between multiple state variables to find optimal direction for update gradient
2. comparative differences between measuremet (R) and estimation (P) errors

The time-varying K gain matrix keeps track how much of the predicted 
versus how much of the measured/observed value for each state variable
is updated. That is, if measurement error (covarriance matrix R)
is greater than predicted error (covariance matrix P) then the state 
update at that time instant k should favor the model estimate y_hat.
Otherwise, one could say the prediction error was greater than the 
the (co)variance in the measurement error so favor the current 
measurement and (partially) ingore the contribution from from the model
prediction H*x_.

The K gain matrix is updated 
so as to favor either the measurement or the estimate. . In the case of no correlation, the 
K matrix is a diagonal with the variance of the individual state variable
along the diagonal and zeros everywhere else (the states are independent).
In this case the greater the variance, the smaller the K.

In the case of stock price estmatation,
I don't yet see what the state variables are. I suppose we can have the 
states be the mean and the std-dev of the stock price. But you would need
multiple samples in time to make accuate predictions about the future- but 
not so much history as to loose longterm (seasonal) behavior. This suggests 
a finanical model which adds two degrees of freedom (mean, sd) for each
step in time. You would need at least two delayed versions to calculate
a second order differential equation. In this line of thinking, could expect
to capture trends on multiple time scales and with vaious delays. Such 
analysis is in the realm of the Laplace transform.


- [Understanding Kalman Filters, Part 4: Optimal State Estimator Algorithm](https://www.youtube.com/playlist?list=PLn8PRpmsu08pzi6EMiYnR-076Mh-q3tWr):
this is the Kalman filter using the state-space point of view, e.g. A,B,C,D matrices.


# Octave
-[Octave](https://www.gnu.org/software/octave/), by John Eaton, is the the open source version of Matlab
that runs everywhere and does not require a lot of setup and has been stable for years. The Octave Forge
code base is a great learning resource. Octave allows you to think in vectors and provides a lockdown
reference to code against.

-[Kalman-Filter-for-Beginners](https://github.com/philbooks/Kalman-Filter-for-Beginners): Start wtih 
chapter 10 (single dimensional 'covariance'), 11 (2 dim covariance), and 12 (4 dim covariance). This 
is my cononical reference -mr.

## Python
Let's use this:


Too big but good reference:
- [Kalman and Bayesian Filters in Python](https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python):
Kalman Filter book using Jupyter Notebook. Focuses on building intuition and experience, not formal proofs. 
Includes Kalman filters,extended Kalman filters, 
unscented Kalman filters, particle filters, and more. All exercises include solutions.