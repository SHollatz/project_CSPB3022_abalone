# project_CSPB3022_abalone

### Predicting the Age of Abalone by Body Measurements
#### Sabine Hollatz

### The Problem
Abalone are marine snails with a single shell that feed on kelp and live on rocks along the coastlines around the world. Their meat is considered to be a delicacy and their shells are used for producing jewelery and other decorative objects. The global population has declined by more than 50% according to the FAO. In California is the harvest of natural populations strongly restricted. Demands are met by farms such as the Monterey Abalone Company that grow abalone in cage cultures underneath the warf. The age can only be determined from the inside of the shell, counting growth rings under the microscope. This is time-consuming and kills the animal. Predicting the age range from body measurments that can be assessed from the outside would improve the research as well as farming evaluations.

### Personal Interest
Even though the data is collected in Tasmania, Australia, from a population of blacklip abalone that do not exist in California, certain characteristics such as the process of growth is the same among species. As the abalone grows it adds new shell to the outer rim causing the shell to increase in diameter and showing the rings that can be counted to determine the age. I am very interested in California's environment.

In California exist 7 species that are closed for commercial fishery since 1997. Poaching is an issue, since a single animal sells for up to $100. The decrease in kelp forests is a major concern, also because many abalone starve to death and their empty shells are washed ashore. Abalone will be highly effected by climate change.


Interesting facts about these animals are that they have blue-green blood, produce pearls, and that they can twist their shell and run off when they are touched by a predatory sea star.
I say abalones are keepers. Let's help environmental science and research to study and protect these fabulous animals.

### The Data
The dataset is collected by the Sea Fisheries Division in Tasmania 1994 and publicly available at kaggle.com: <br>
https://www.kaggle.com/hurshd0/abalone-uci#abalone_original.csv

8 body charateristics of 4177 abalone are taken, including sex (male, female, infant), length, diameter, height, number of rings, and weights of different body parts. Whole-weight includes all parts, shucked-weight is just the meat without the shell, viscera-weight is the gut weight after bleeding, and shell is the weight of the shell after drying. The units are in millimiters or grams. The age is traditionally determined by the number of rings plus 1.5. The only categorical attribute is 'sex'. All other features are continuous. <br>

### Proposed Types of Analysis
The first steps are to clean and preprocess the data for the analysis. This includes adjusting variable names and data types if needed, checking for missing or zero values and filling them in, and detecting outliers and measurment errors and removing them if possible. Missing values in the numerical variables will be replaced by the variable mean and missing data in the categorical variable will be replaced by the mode. Outliers are detected using the interquartile range. Min/Max normalization will be applied to compare distributions from different variables and to perform multilinear regression during the main analysis. Visualization techniques such as boxplots, scatterplots and histograms will help with further error identification and potential imbalances in the data. However, missing values and outliers in the response variable 'number of rings' will be filled in with 'nan' instead of a central measure of tendency. Potential outliers in the response will not be removed since they are the values that need to be predicted. 

The second step is the exploratory data analysis where statistical calculations and tests will provide insight into the distribution of each predictor and response variable and potential correlations. Correlations between body measurements and age are expected and will be determind by calculating the correlation coefficients pairwise.

The third step is the main regression analysis. Single linear regression, multilinear regression and polynomial regression will be performed, evaluated and compared. Fluctuations in length and other body measurements related to age are expected. Californian red abalone do not grow continously. They take 12 years on average to reach a length of 7 inches, 5 more years to grow from 7 to 8 inches, and another 13 years to grow from 8 to 9 insches. This will be kept in mind, when analysing the Australian blacklip abalone data set.

A brief outlook will be given into the potential of more flexible models on the example of decision tree classification.

Difficulties are anticipated in the limitations of the dataset due to the small number of attributes and the usually large variance in biological systems. 


