# ML Projects

Nethealth Research Project:

In this study, I aim to analyze the self-reported data of first-year college students concerning mental health and related survey data collected in the NetHealth study. The random forest algorithm will be used to predict what survey items are strong predictors for network growth in students. I hypothesized that if mental health and psychological survey data from students was analyzed in correlation to their first semester network growth, then those students with very poor mental health responses will have greater difficulty building network and will thus have fewer social ties and smaller networks. The results of this study will shed insight on the effect of mental and psychological attributes on the growth of social networks in college students.

A random forest algorithm is a set of regression trees which use recursive partitioning to divide the sample into groups with similar values based on a set or calculated response cutoff. Random forests have an advantage to the use of multiple dimension reduction techniques when input variables are factored into reduced sets of variables whereby original variables may have lost importance altogether. The algorithm can process a large number of predictors in multiple trees at the same time and provide separate importance values for predictors. This is essential for determining the most relevant predictor values to reduce the number of dimensions without influence from the order effect and possible interactions that are too complex for parametric regression models. A particular advantage of random forests is the ability to provide feedback of the prediction accuracy on test data. This is done by generating repeated random samples of the training data to track accuracy. (Strobl, Malley, Tutz, 2009).

Using the “caret” package developed by Max Kuhn, a random forest was run with the base R train function. The tuning length was set to 1 with “ntree=10” and “importante=T”. The random forest will use a bootstrap sample to create 100 fixed decision trees simultaneously with a subset of the selected variables. The average of the predictors helps to determine the variable importance. Because the dependent variable being examined was the number of ties, the “tieN” was excluded from the importance calculation used to determine the importance of the remaining variables for the resulting y value. The variable importance is then compared to “rpart” variable importance calculated using the “partykit” package in R developed in R by Hothorn and Zeileis. The importance levels are then compared to determine if there is continuity in the significance of measured variables. Results of the variable importance tests show the improvement in the variable selection among the fixed decision trees accordingly.
