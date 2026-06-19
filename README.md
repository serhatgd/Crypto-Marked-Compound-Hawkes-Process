# Crypto-Marked-Compound-Hawkes-Process
We build the documentation for the aforementioned project/paper.

All data was taken from https://www.kaggle.com/datasets/martinsn/high-frequency-crypto-limit-order-book-data.

Our suggested order for reading the notebooks:
  1) Data visualizations:
    We have plotted the QQ-plot of the interarrival times, 1-minute moving window price changes and an autocorrelation graph for the price increments. These don't have significant implications to the theoretical sides of the project.

  2) Transition probabilities and asymptotic means:
     First considering a fixed tick, the adjusting it to the empiric side of our data, we get the transition probability matrices and stationary probability distribution vectors for each state. We also derive the asymptotic means to use it in a further analysis.

  3) Estimation of marks and other parameters:
     We first introduce the marks in our marked hawkes process as the volume in our limit order booklet. We decide to use the logarithm of the marks, for the sake of numerical stability. We fit a gaussian to the log-normalised volume data, and estimate its parameters.

     To estimate the parameters of the excitation kernel(a,b) and the background excitation rate($\lambda_0$), we minimize the negative-log-likelihood function of our marked hawkes process, taken from [Testing procedures based on maximum likelihood estimation for
Marked Hawkes processes](https://doi.org/10.1007/s00180-025-01664-).
     
     



