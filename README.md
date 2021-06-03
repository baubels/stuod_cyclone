# stuod_cyclone

This is my submission for the STUOD hackathon challenge: https://www.imperial.ac.uk/news/219153/stuods-hackathon-winners-announced/. 
I am thankful for my awesome teammate, and happy to get runner up in this challenge!

The point of our model was to predict properties about tropical cyclones in advance using data-driven methods. Models were compared against other models used
with input from industry knowledge, and mathematical ones using mathematical modelling techniques. The data itself was quite sparse, so a decision tree was used.

The model is different from most, in the sense that it has autoML characteristics in it - with one function (super_rf), we can predict any interesting property
about tropical cyclones some time steps in advance, using user-specified amount of data in the past, and save them into fully working, highly accurate models.
Each model can then be analysed using some tools such as partial dependence and feature importance, or individual decision trees can even be plotted.

To visualise my NN graph topology, use the following tool: https://github.com/szagoruyko/pytorchviz.
