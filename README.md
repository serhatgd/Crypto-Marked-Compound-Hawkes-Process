# Crypto-Marked-Compound-Hawkes-Process
We build the documentation for the above project/paper.

All data were taken from https://www.kaggle.com/datasets/martinsn/high-frequency-crypto-limit-order-book-data.

Our suggested order for reading the notebooks:
  1) Data visualizations:
    We have plotted the QQ-plot of the interarrival times, 1-minute moving window price changes and an autocorrelation graph for the price increments. These don't have significant implications to the computations of the project.

  2) Empirical Std calculation:

  3) Transition probabilities and asymptotic means:
     First considering a fixed tick, then adjusting it to our data, we get the transition probability matrices and stationary probability distribution vectors for each state. We also derive the asymptotic means to use it in a further analysis.

  4) Estimation of marks and other parameters:
     We first introduce the marks in our marked Hawkes process as the volume in our limit order book. We decide to use the logarithm of the marks, for the sake of numerical stability. We fit a Gaussian to the log-normalised volume data, and estimate its parameters.

     To estimate the parameters (a,b) of the excitation kernel and the background excitation rate ($\lambda_0$), we minimize the negative-log-likelihood function of our marked Hawkes process, taken from [Testing procedures based on maximum likelihood estimation for
Marked Hawkes processes](https://doi.org/10.1007/s00180-025-01664-9). We indeed see that our parameters satisfy the stationarity condition.

  5) Theoretical std calculations:
     Using the parameters we obtained from 4), and other information about the distribution of price changes we obtained from 3), we plot the theoretical standart deviations against the one that we obtained in 2). We do additional MSE and percentage error calculations to quantify our fits.

If you happen to use this code, please cite our paper (here).
     
     



