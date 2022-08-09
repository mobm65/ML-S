# ML&S
 
# SCIKIT LEARN

The Scikit Learn Jupyter Notebook opens with a brief outline of the uses of this library for predictive modelling.  There is an image showing the route that a data analyst might take in deciding which of the many scikit learn algorithms may be suitable for the particular dataset being explored.

The dataset I am using is the Palmer Penguins and they are illustrated by an image.  There are three species; Amelie, Gentoo and Chinstrap.  They are measured for a number of traits; bill length and depth, flipper length, sex, habitat (one of three islands), body mass and year.  Using Pandas to read in the dataset the first analysis is to look at the first six instances.  The next method is a basic statistical analysis which gives mean, std, quartile values, minimum and maximum values.  I then dropped any NAN values because they will affect the calculations and I check this has worked.  The first plot is a bar chart which shows the number of each species in the sample.  The next is also a bar chart showing the population of penguins on each island.  A boxplot is useful to see if the bill length and depth are different from one species to the other.  It shows only one outlier on bill length in the Gentoo species and one outlier on bill depth in the Adelie species.  The boxplot illustrating flipper length and species shows only two outliers in the Adelie species.  These plots indicate that bill length, bill depth and flipper length are all likely indicators of species.  The final plot is a barchart showing that males and females are similarly represented in the sample.

### KNeighbours Classifier
The supervised algorithm KNeighbours Classifier which implements learning based on the k nearest neighbors of each instance, where k is an integer value specified by the user.  I imported the necessary libraries and used iloc to isolate the numeric values only.  I then divided the dataset into two arrays, one for testing (20%) and one for training (80%).  To nullify the effects of any outliers and to normalise the data I ran scaler on the data.  I then used a confusion matrix to get the precision, recall and F1 scores.  This checks the reliability of the algorithm.  The scores were mainly at .97 and they were generally above .90, therefore the algorithm is reliable.  I then calculated and plotted the mean error, which is very low between k values of 2 and 50.


### KMeans Clustering
The unsupervised algorithm KMeans Clustering. K-means follows a number of steps. The first step is to randomly select k centroids, where k is equal to the 
number of clusters you choose, I chose three because there are three species of penguins.  I first ran a seaborn scattergraph which illustrates where the penguins are plotted with regard to bill length and depth.  The Kmeans algorithm shows the species as 0 (Amelie), 1 (Gentoo) and 2 (Chinstrap).  To check the prediction value of the algorithm I next randomly selected an array of two instances of penguins.  The answer showed them to be 0 (Amelie) and 1 (Gentoo) which they were.  I used StandardScaler, which subtracts the mean from each features and then scales to the unit variance.  I then used pipeline to train the data, the outputs of the first step become the inputs of the next which allows the clusters to become more identifiable.


### Logistic Regression
To begin this function I dropped one species and the features of the species I was not studying, eg., habitat. 

# Scipy-Stats

This notebook opens with an explaination of the Scipy_stats library including some of its features and functions.  There is also some information on the purpose and process of ANOVA.  ANOVA requires a number of assumptions to be adhered to before you can consider the result of the ANOVA to be reliable.  In the next section I go through the 6 main assumptions. I then read in the crop yield data I have selected and examine the data to plan the study. The values are continuous so this satisfies the 1st assumption.  Next I examine the basic statistical data; mean, sd, quartile values and maximum and minimum values.  I establish one of the independent variables to be fertilizer, which comes in 3 types.  This is a categorical variable satisfying the 2nd assumption.  The dependent variable is crop_yield.  The next two cells show the affect of the density of planting and the part of the field where the crop was planted on the crop yield.  Next is looking at the fertilizer use on crops reiterating assumption 1.  Following this is a statistical analysis of the dependent variable.  The boxplot shows there is only one outlier which satisfies assumption 4.  I then ran a kernel destiny estiimates test which satisfied assumption 5, my samples belong to the normal distribution.  The Shapiro Wilk test confirmed the same.
The Levene tests for homogeneity of variance to satisfy assumption 6.  The result is a p score, anything above .05 is considered non-significant, i.e., that equal variances are assumed.  My dataset satisfies assumption 6.

### ANOVA

The ANOVA is used to find out if there is a statistically significant difference of the means between groups. The p score is below 0.05 so we know at least some of the means are not equal.  We then perform the Tukey test to see if every group has statistically different means from every other group.  The analysis shows that groups one and two may share a mean but groups one and three, and two and three do not.  The Confidence Interval plot illustrates this.
