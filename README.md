# stuod_cyclone

This is my submission for the STUOD hackathon challenge: https://www.imperial.ac.uk/news/219153/stuods-hackathon-winners-announced/ in 2021.
I am thankful for my awesome teammate, and happy to get runner up in this challenge!

Our specific challenge was to determine cyclone trajectories into the future using (~30GB) past time-series-like historical data on attributes of cyclone since 2000. Due to the difficulty in determining exact characteristics of cyclones, most of the data was noisy, and further, of the hundreds of potential attributes a cyclone could have, very few were measured. The characteristics measured also varied between samples.

During this hackathon, we had access to general model methology of competing teams, as well as links to academics with serious weather-forecasting experience.

I believe we were the only team to use a random forest - this inference model was specifically chosen due to the sparsity and noise in the data, giving a clear advantage over neural networks unaccustomed to noise of specific symmetries (ie, non-translational noise in CNNs). The noise gave the opposite effect of pseudo-bagging to decrease model prediction variance, and thus, MSE.

The main caveat in our model was in the type of predictions one would like out of a cyclone. Sometimes this would be speed, or location, or water salinity, or size, with different variability in the time-scale to predict future events by. Due to the unclear nature of model output, an 'autoML'-like function was made, which would give the user the ability to create models and predict any sort of cyclone characteristic at any number of time steps in advance with one line of code.

There was another clear advantage to using random forests - and that was of interprability. Having the ability to make 'partial plots', give 'feature importances', and inspect the decision process over individual trees would give a meteorologist or government great insight into the nature of the cyclone at hand.

A novel method was also used in our model, that was of applying a random forest as a pre-activation to a second random forest. Effectively, one random forest was trained, and extracted were the most useful predictors in the data. A second random forest was then trained exclusively on data containing those predictors of high importance as determined by the prior random forest. This gave a slight improvement to model performance.

---
Post competition, an interesting observation was in the importance water salinity has in cyclone strength - a factor (which I believe) was not considered by the experts at the time to be of major effect.

We are also very greatful for our model's excellent performance, for this characteristic gave us high competition marks.
Thank you for my excellent teammate, Oliver, and the people of the competition.
