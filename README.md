The following code is an alternative to avoid manual hyper tuning and provide a batch process that can do so automatically.

While performing the different functions, I set up a max numbers of attemps so we can rule out the possibility to create an infinite loop.

###############

Key takeaways:

###############

1)Python hyperopt library will not provide us the optimal minimal of the graduate function but the local minimal, which is enough to provide a decent hyperparameters.

2)Date diff was the simplest and most efficient transformation approach I used to deal with stationarity. I realize that if I squeze the p_value of ADF Fuller threshold, I can obtain better preditions.

3)I set up the optimization target for R2_Square but it is even more recommended RSME so you can change the target to follow that approach.

4)I set up the jupiter workflow in a workflow fashion so the model can easily be retrained if requested.

###############

Should you have any constructive input, please do no hesitate to contact me bpiscoya2020@gmail.com

Best Regards


