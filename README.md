# tsd-study-group
Resources for studying time series data.
- [State-space representation](https://en.wikipedia.org/wiki/State-space_representation):  A state-space representation is a mathematical model of a physical system as a set of input, output and state variables related by first-order differential equations or difference equations. State variables are variables whose values evolve through time in a way that depends on the values they have at any given time and also depends on the externally imposed values of input variables. Output variables’ values depend on the values of the state variables.
  - [State-space models’ dirty little secrets: even simple linear Gaussian
models can have estimation problems](https://www.nature.com/articles/srep26677): From Nature magazine. State-space models (SSMs) are increasingly used in ecology to model time-series such as animal
movement paths and population dynamics. This type of hierarchical model is often structured to
account for two levels of variability: biological stochasticity and measurement error. SSMs are
flexible. They can model linear and nonlinear processes using a variety of statistical distributions.
Recent ecological SSMs are often complex, with a large number of parameters to estimate. Through a
simulation study, we show that even simple linear Gaussian SSMs can suffer from parameter- and stateestimation
problems. We demonstrate that these problems occur primarily when measurement error
is larger than biological stochasticity, the condition that often drives ecologists to use SSMs

  - [Gaussian Processes for State Space Models and Change Point Detection](http://mlg.eng.cam.ac.uk/pub/pdf/Tur11.pdf). Great overview  of time-series data through the state-space lens controlled by stochastic sampling. "This thesis details several applications of Gaussian processes (GPs) for
enhanced time series modeling. We first cover different approaches for
using Gaussian processes in time series problems. These are extended
to the state space approach to time series in two different problems.
We also combine Gaussian processes and Bayesian online change point
detection (BOCPD) to increase the generality of the Gaussian process
time series methods. These methodologies are evaluated on predictive
performance on six real world data sets, which include three environmental
data sets, one financial, one biological, and one from industrial
well drilling."

  - See also [bayesian-study-group](https://github.com/study-groups/bayesian-study-group). The bayesian-study-group is geared around the study of [Ben Lambert's Bayesian Statistics](https://www.youtube.com/playlist?list=PLwJRxp3blEvZ8AKMXOy0fc0cqT61GsKCG): This course aims to provide a core understanding of Bayesian statistics  that is grounded in mathematical theory, yet friendly to the less mathematically-minded of persons. It aims to focus on the intuitive results of Bayesian theory rather than dwell on the mathematical minutiae.


- [time-series chapter from Vincent Zoonekynd's Statistics in R](http://zoonek2.free.fr/UNIX/48_R/15.html): After an introduction, motivating the notion of a time series and giving several examples, simulated or real, we shall present the classical models of time series (AR, MA, ARMA, ARIMA, SARIMA), that provide recipes to build time series with desired properties. We shall then present spectral methods, that focus on the discovery of periodic elements in time series. The simplicity of those models makes them amenable, but they cannot describe the properties of some real-world time series: non-linear methods, built upon the classical models (GARCH) are called for. State-Space Models and the Kalman filter follow the same vein: they assume that the data is build from linear algebra, but that we do not observe everything -- there are "hidden" (unobserved, latent) variables.

- [Forecasting: Principles and Practice](https://otexts.org/fpp2/) by Rob J Hyndman and George Athanasopoulos from 
Monash University, Australia. Basic overview of time series analysis from a business economics perspective.

- [Lecture 10: Bayesian modelling of time series](https://www.uio.no/studier/emner/matnat/ibv/BIO4040/h03/undervisningsmateriale/Lectures/lecture10.pdf)
From Introduction to biological time series data by Kyrre Lekve from Department of Biology, University of Oslo.

- [Matlab videos on Kalman Filters](https://www.mathworks.com/videos/understanding-kalman-filters-part-1-why-use-kalman-filters--1485813028675.html) Discover common uses of Kalman filters by walking through some examples. A Kalman filter is an optimal estimation algorithm used to estimate states of a system from indirect and uncertain measurements.


  - [Wikipedia on Kalman Filters](https://en.wikipedia.org/wiki/Kalman_filter) In statistics and control theory, Kalman filtering, also known as linear quadratic estimation (LQE), is an algorithm that uses a series of measurements observed over time, containing statistical noise and other inaccuracies, and produces estimates of unknown variables that tend to be more accurate than those based on a single measurement alone, by estimating a joint probability distribution over the variables for each timeframe. The filter is named after Rudolf E. Kálmán, one of the primary developers of its theory.
  
- [Time sequence prediction using Pytorch](https://github.com/pytorch/examples/tree/master/time_sequence_prediction) This is a toy example for beginners to start with. It is helpful for learning both pytorch and time sequence prediction. Two LSTMCell units are used in this example to learn some sine wave signals starting at different phases. After learning the sine waves, the network tries to predict the signal values in the future.

## Classes being considered for study
- [Stats 270/370 at Stanford,  A Course in Bayesian Statistics](http://statweb.stanford.edu/~sabatti/Stat370/): This class is the first of a two-quarter sequence that will serve as an introduction to the Bayesian approach to inference, its theoretical foundations and its application in diverse areas. **Contains many good references**. No course  

- [Coursera: Bayesian Statistics from Santa Cruz](https://www.coursera.org/learn/bayesian-statistics): This course introduces the Bayesian approach to statistics, starting with the concept of probability and moving to the analysis of data. We will learn about the philosophy of the Bayesian approach as well as how to implement it for common types of data. We will compare the Bayesian approach to the more commonly-taught Frequentist approach, and see some of the benefits of the Bayesian approach. In particular, the Bayesian approach allows for better accounting of uncertainty, results that have more intuitive and interpretable meaning, and more explicit statements of assumptions. 


- [Coursera: Bayesian Statistics from Duke](https://www.coursera.org/learn/bayesian): This course describes Bayesian statistics, in which one's inferences about parameters or hypotheses are updated as evidence accumulates. You will learn to use Bayes’ rule to transform prior probabilities into posterior probabilities, and be introduced to the underlying theory and perspective of the Bayesian paradigm. The course will apply Bayesian methods to several practical problems, to show end-to-end Bayesian analyses that move from framing the question to building models to eliciting prior probabilities to implementing in R (free statistical software) the final posterior distribution. NOT GREAT

- [MIT: 6-041 probabilistic-systems-analysis](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-041-probabilistic-systems-analysis-and-applied-probability-fall-2010/lecture-notes/): Full course with notes and video but not all lectures are necessary.

- [Time Series Analysis | Economics | MIT OpenCourseWare](https://ocw.mit.edu/courses/economics/14-384-time-series-analysis-fall-2013/lecture-notes/)
- [DataCamp: Intro to time series analysis](https://www.datacamp.com/courses/introduction-to-time-series-analysis): Not excited about this one.

- [time-series-forecasting](https://www.udacity.com/course/time-series-forecasting--ud980): Udacity course on time series forecasting. Bit of a softball.


## Projects

- [Predicting Energy-Consumption](https://github.com/khsieh18/Time-Series/blob/master/Energy-Consumption-24.ipynb) by Kunlin Hsieh

## References
- [TDS: Time-series analysis in python](https://towardsdatascience.com/time-series-analysis-in-python-an-introduction-70d5a5b1d52a): One powerful yet simple method for analyzing and predicting periodic data is the additive model. The idea is straightforward: represent a time-series as a combination of patterns at different scales such as daily, weekly, seasonally, and yearly, along with an overall trend. Your energy use might rise in the summer and decrease in the winter, but have an overall decreasing trend as you increase the energy efficiency of your home. An additive model can show us both patterns/trends and make predictions based on these observations.

- [SARIMA](https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/)
- [Grid Search SARIMA](https://machinelearningmastery.com/how-to-grid-search-sarima-model-hyperparameters-for-time-series-forecasting-in-python/) 
- [Multiple Data (Time Series) Streams Clustering](https://petolau.github.io/Multiple-data-streams-clustering-in-r/)
- https://petolau.github.io/Ensemble-of-trees-for-forecasting-time-series/)
