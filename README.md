The following code is an alternative to avoid manual hyper-tuning and provide a batch process that can do so automatically.

While performing the different functions, I set up a max number of attempts so we can rule out the possibility of creating an infinite loop.

###############

Key takeaways:

###############

1)Python hyper-opt library will not provide us the optimal minimum of the gradient function but the local minima, which is enough to provide decent hyperparameters.

2)Date diff was the simplest and most efficient transformation approach I used to deal with stationarity. I realize that if I squeeze the p_value of ADF Fuller threshold, I can obtain better predictions.

3)I set up the optimization target for R2_Square but it is even more recommended RSME so you can change the target to follow that approach.

4)I set up the Jupiter workflow in a workflow fashion so the model can easily be retrained if requested.

###############

Should you have any constructive input, please do no hesitate to contact me bpiscoya2020@gmail.com

Best Regards


