# Kalman filtering notes

Regardless of models and optimization processes, it is good to keep in mind
- [Goodhart's Law](https://en.wikipedia.org/wiki/Goodhart%27s_law) in 
mind. Goodhart's law is the idea that "When a measure becomes a target, it ceases to be a good measure." 
One way in which this can occur is individuals trying to anticipate the effect of 
a policy and then taking actions that alter its outcome. 

## Theory

- [Kalman filter on Wikipedia](https://en.wikipedia.org/wiki/Kalman_filter): In statistics
and control theory, Kalman filtering, also known as linear quadratic estimation (LQE), is an 
algorithm that uses a series of measurements observed over time, containing statistical noise 
and other inaccuracies, and produces estimates of unknown variables that tend to be more accurate 
than those based on a single measurement alone, by estimating a joint probability distribution over 
the variables for each time frame. The filter is named after Rudolf E. Kálmán, 
one of the primary developers of its theory.

- [1960 A New Approach to Linear Filtering and Prediction Problems](https://github.com/study-groups/papers-study-group/blob/master/1960-Kalman1960.pdf) by R.E. Kalman. The classical filtering and prediction problem is re-examined using the BodeShannon representation of random processes and the “state transition” method of analysis of dynamic systems. New results are: (1) The formulation and methods of solution of the problem apply without modification to stationary and nonstationary statistics and to growing-memory and infinitememory filters. (2) A nonlinear difference (or differential) equation is derived for the covariance matrix of the optimal estimation error. From the solution of this equation the coefficients of the difference (or differential) equation of the optimal linear filter are obtained without further calculations. (3) The filtering problem is shown to be the dual of the noise-free regulator problem. The new method developed here is applied to two well-known problems, confirming and extending earlier results. The discussion is largely self-contained and proceeds from first principles; basic concepts of the theory of random processes are reviewed in the Appendix.

- [Understanding Kalman Filters, Part 4: Optimal State Estimator Algorithm](https://www.youtube.com/playlist?list=PLn8PRpmsu08pzi6EMiYnR-076Mh-q3tWr):
this is the Kalman filter using the state-space point of view, e.g. A,B,C,D matrices.

- [how-a-kalman-filter-works-in-pictures](https://www.bzarg.com/p/how-a-kalman-filter-works-in-pictures/): Blog post starts slow but good notation for 2 dimensional state variable.

- [A KALMAN FILTERING TUTORIAL FOR UNDERGRADUATE STUDENTS](http://aircconline.com/ijcses/V8N1/8117ijcses01.pdf): Students reading this paper should be able
to understand how to apply Kalman filtering tools to mathematical problems without requiring a deep
theoretical understanding of statistical theory. Table on page 2 is useful, good, readable paper.

-[kalman-filter-a-painless-approach](https://mayitzin.com/2015/06/04/kalman-filter-a-painless-approach/): blog post with explicit algorithm in pseudocode. Beautiful post.

- [A Tool for Kalman Filter Tuning](http://folk.ntnu.no/skoge/prost/proceedings/npc07/DTU/dtu10.pdf): 
by Bernt M. Åkesson, et al. The Kalman filter requires knowledge about the noise statistics. In practical
applications, however, the noise covariances are generally not known. In this
paper, a method for estimating noise covariances from process data has been
investigated. This method yields least-squares estimates of the noise
covariances, which can be used to compute the Kalman filter gain. *Good short paper
to solidify understanding.*

- [how-to-understand-kalman-gain-intuitively](https://dsp.stackexchange.com/questions/2347/how-to-understand-kalman-gain-intuitively): Good stackoverflow highlighting the action of 
K with respect to P and R going to zero.

- [An Introduction to the Kalman Filter](http://www.cs.unc.edu/~welch/media/pdf/kalman_intro.pdf): by 
Greg Welch and Gary Bishop. Great notation and explanations. 
# Octave

- [Octave](https://www.gnu.org/software/octave/), by John Eaton, is the the open source version of Matlab
that runs everywhere and does not require a lot of setup and has been stable for years. The Octave Forge
code base is a great learning resource. Octave allows you to think in vectors and provides a lockdown
reference to code against.

- [Kalman-Filter-for-Beginners](https://github.com/philbooks/Kalman-Filter-for-Beginners): Start with 
chapter 10 (single dimensional 'covariance'), 11 (2 dim covariance), and 12 (4 dim covariance). This 
is my canonical reference -mr.

- [Kalman library function](https://octave.sourceforge.io/control/function/kalman.html). Good for 
seeing use and variable names. The Octave community comes from a Controls background which
is based off of linear algebra and matrix theory. The state-space representation is 
used to model systems. The estimator problem is to mitigate statistical error and 
the Kalman filter uses the state-space model to keep track of observable parameters.
The actual state-space model is not restricted and admits hidden states in a way
the Kalman filter does not- that is, the number of observations need not equal the 
number of states. When H is known, this is not a problem- H maps from observation 
to latent space faithfully.

- [kalman-filter-octave-coding-completed](http://dekalogblog.blogspot.com/2012/03/kalman-filter-octave-coding-completed.html): Octave Kalman filtering code for 
finance.

- [Coursera module on Kalman filtering battery data](https://www.coursera.org/lecture/battery-state-of-charge/3-3-3-introducing-octave-code-to-implement-kf-for-linearized-cell-model-9K8ci)

## Python
Let's use this:
- [Kalman filter guide](http://greg.czerniak.info/guides/kalman1/): by Greg Czerniak. Pretty good
 but requires using classes. Includes self-contained: 
[kalman1.py](http://greg.czerniak.info/guides/kalman1/kalman1.py.txt)


- [Implementation of Kalman Filter with Python Language ](https://arxiv.org/pdf/1204.0375.pdf):
In this paper, we investigate the implementation of a Python code for a Kalman
Filter using the Numpy package. A Kalman Filtering is carried out in two steps:
Prediction and Update. Each step is investigated and coded as a function with matrix
input and output. These different functions are explained and an example of a
Kalman Filter application for the localization of mobile in wireless networks is
given. 


Too big but good reference:
- [Kalman and Bayesian Filters in Python](https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python):
Kalman Filter book using Jupyter Notebook. Focuses on building intuition and experience, not formal proofs. 
Includes Kalman filters,extended Kalman filters, 
unscented Kalman filters, particle filters, and more. All exercises include solutions.

## Related fields

- [Phased Locked Loop](https://en.wikipedia.org/wiki/Phase-locked_loop): A phase-locked loop or phase lock loop (PLL) is a control system that generates an output signal whose phase is related to the phase of an input signal. There are several different types; the simplest is an electronic circuit consisting of a variable frequency oscillator and a phase detector in a feedback loop. The oscillator generates a periodic signal, and the phase detector compares the phase of that signal with the phase of the input periodic signal, adjusting the oscillator to keep the phases matched.

## My notes
Kalman filter's main claim to fame is that it minimizes prediction error based
on the covariance of the components (random variables) of the time varying,
real valued, 
state vector. In other words, Kalman filtering exploits:
1. correlation between multiple state variables to find optimal direction for update gradient
2. comparative differences between measurement (R) and estimation (P) errors

The time-varying K gain matrix keeps track how much of the predicted 
versus how much of the measured/observed value for each state variable
is updated. That is, if measurement error (covariance matrix R)
is greater than predicted error (covariance matrix P) then the state 
update at that time instant k should favor the model estimate y_hat.
Otherwise, one could say the prediction error was greater than the 
the (co)variance in the measurement error so favor the current 
measurement and (partially) ignore the contribution from from the model
prediction H*x_.

The K gain matrix is updated 
so as to favor either the measurement or the estimate. . In the case of no correlation, the 
K matrix is a diagonal with the variance of the individual state variable
along the diagonal and zeros everywhere else (the states are independent).
In this case the greater the variance, the smaller the K.

In the case of stock price estimation,
I don't yet see what the state variables are. I suppose we can have the 
states be the mean and the std-dev of the stock price. But you would need
multiple samples in time to make accurate predictions about the future- but 
not so much history as to loose long term (seasonal) behavior. This suggests 
a financial model which adds two degrees of freedom (mean, sd) for each
step in time. You would need at least two delayed versions to calculate
a second order differential equation. In this line of thinking, could expect
to capture trends on multiple time scales and with various delays. Such 
analysis is in the realm of the Laplace transform.
