# F0-estimation-Noisy-Periodic-Signal-

The real world applications mostly constitutes of periodic signals, which can be modeled as sum of signals whose frequencies are integral multiples of fundamental frequency. Hence estimating fundamental frequency becomes critical.
Among various estimation methods parameter estimation methods stands out for its accuracy. In this project a parametric estimation algorithm to determine fundamental frequency has been implemented.
The method is based on Non Linear Least Square Estimator and cost function. For the presentation and user interface a GUI has been created in python. The performance is evaluated by test strategy of generating an analog signal and sampling it at a specific sampling frequency, storing the values in an external file and applying the algorithm for the values read from this file.

NLS algorithm for estimation has been implemented successfully and has provided good estimates for all range of frequencies. It has also been tested for different sampling frequencies and this estimator is better compared to autocorrelation method as it doesn’t require any pre-processing. The NLS method is statistically efficient if the noise is modelled as white and Gaussian and much more accurate than the autocorrelation based methods. But a drawback of this algorithm is that it takes time to calculate the cost function matrix as it involves matrix multiplication with an inverse matrix. This method can be made faster if implemented using recursive solver for Toeplitz-plus-Hankel systems for computing NLS cost function.

Model order has been set to 1.
Implementation works for noisy periodic signal having just 1 harmonic.
