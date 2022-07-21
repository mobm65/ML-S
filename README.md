# ML&S
 
### SCIKIT LEARN

The Scikit Learn Jupyter Notebook opens with a brief outline of the uses of this library for predictive modelling.  There is an image showing the route that a data analyst might take in deciding which of the many scikit learn algorithms may be suitable for the particular dataset being explored.

The dataset I am using is the Palmer Penguins and they are illustrated by an image.  There are three species; Amelie, Gentoo and Chinstrap.  They are measured for a number of traits; bill length and depth, flipper length, sex, habitat (one of three islands), body mass and year.  Using Pandas to read in the dataset the first analysis is to look at the first six instances.  The next method is a basic statistical analysis which gives mean, std, quartile values, minimum and maximum values.  I then dropped any NAN values because they will affect the calculations and I check this has worked.  The first plot is a bar chart which shows the number of each species in the sample.  The next is also a bar chart showing the population of penguins on each island.  A boxplot is useful to see if the bill length and depth are different from one species to the other.  It shows only one outlier on bill length in the Gentoo species and one outlier on bill depth in the Adelie species.  The boxplot illustrating flipper length and species shows only two outliers in the Adelie species.  These plots indicate that bill length, bill depth and flipper length are all likely indicators of species.  The final plot is a barchart showing that males and females are similarly represented in the sample.

### KNeighbours Classifier
The supervised algorithm KNeighbours Classifier which implements learning based on the k nearest neighbors of each instance, where k is an integer value specified by the user.  I imported the necessary libraries and used iloc to isolate the numeric values only.  I then divided the dataset into two arrays, one for testing (20%) and one for training (80%).  To nullify the effects of any outliers and to normalise the data I ran scaler on the data.  I then used a confusion matrix to get the precision, recall and F1 scores.  This checks the reliability of the algorithm.  The scores were mainly at .97 and they were generally above .90, therefore the algorithm is reliable.  I then calculated and plotted the mean error, which is very low between k values of 2 and 50.


### KMeans Clustering
The unsupervised algorithm KMeans Clustering. K-means follows a number of steps. The first step is to randomly select k centroids, where k is equal to the 
number of clusters you choose, I chose three because there are three species of penguins.  I first ran a seaborn scattergraph which illustrates where the penguins are plotted with regard to bill length and depth.  The Kmeans algorithm shows the species as 0 (Amelie), 1 (Gentoo) and 2 (Chinstrap).  To check the prediction value of the algorithm I next randomly selected an array of two instances of penguins.  The answer showed them to be 0 (Amelie) and 1 (Gentoo) which they were.  The 4 integer traits can be entered here and used to check the reliability of the algorithm.

run more centroid
