# IRIS-dataset

Python is a high level,dynamic language and open-source language used for general-purpose programming.

Pandas is a powerful, fast, flexible open-source library used for data analysis and manipulations of data frames/datasets. Pandas can be used to read and write data in a dataset of different formats like CSV(comma separated values), txt, xls(Microsoft Excel) etc.

#### Iris dataset is the Hello World for the Data Science. A career in Data Science and Machine Learning will definitely be practicing basic ML algorithms on this famous dataset.


## What is the Iris dataset?

The iris data consisted of 150 samples of three species of Iris (The data set contains 3 classes of 50 instances each, where each class refers to a type of iris plant). The picture of the Iris species is given below:

![iris species](https://user-images.githubusercontent.com/69766918/231418457-fd1dcd96-b3d9-4686-a38c-4c1d798f07bc.jpg)

What do I mean with  length and width of petal and sepal respectively:

![length breadthof petal sepal](https://user-images.githubusercontent.com/69766918/231420487-dbcc469d-ee29-4398-ac66-224cd3323fa7.jpg)


In fact, three of these iris species look similar, but the difference in measurements can be used to classify them. This data set is a classic example of supervised learning. The input variables are sepal length and width and petal length and width; each row represents an instance or observation. The output variable is Iris-setosa, Iris-versicolor, or Iris-virginica; each column represents a class label.


#### Attribute Information:-

   1. sepal length in cm
   2. sepal width in cm
   3. petal length in cm
   4. petal width in cm
   5. species
      (a) Iris Setosa
      (b) Iris Versicolour
      (c) Iris Virginica

I'm going to use sci-kit-learn to classify these instances according to their species of Iris, which will be distinguished based on their measurements.

## Pyhton Code for Exploring the Iris Dataset

#### STEP 1: Importing libraries

  ![loading libraries](https://user-images.githubusercontent.com/69766918/231424716-28ab6abd-c864-407b-aa7a-7502364632b1.jpg)
  


   *  pandas - used to perform data manipulation and analysis
   *  numpy - used to perform a wide variety of mathematical operations on arrays
   *  matplotlib - used for data visualization and graphical plotting
   *  seaborn - built on top of matplotlib with similar functionalities
   *  warnings - to manipulate warnings details

filterwarnings('ignore') is to ignore the warnings thrown by the modules (gives clean results)

#### STEP 2: Loading the dataset

![loading-dstaset](https://user-images.githubusercontent.com/69766918/231426956-9a0c209c-dfd0-4d05-bcb2-86619f8cade4.jpg)

#### STEP 3: Datatypes and statistical information

To know only column names:
![columns-names](https://user-images.githubusercontent.com/69766918/231712244-bb97f2a5-58b7-4f36-8025-b4e2aa09ccd2.jpg)

To print column names with datatypes: 

![datatypes_usinginfo](https://user-images.githubusercontent.com/69766918/231433233-7e99fb00-230a-4ec8-9ec5-a14512e48a99.jpg)



![stats_usingdescrib](https://user-images.githubusercontent.com/69766918/231433843-65659706-0293-484f-9110-0601016a4b97.jpg)

#### **************************************[SKIP ,if you already know]

The describe() method returns description of the data in the DataFrame.

If the DataFrame contains numerical data, the description contains these information for each column:

* count - The number of not-empty values.
* mean - The average (mean) value.
* std - The standard deviation.
* min - the minimum value.
* 25% - The 25% percentile*.
* 50% - The 50% percentile*.
* 75% - The 75% percentile*.
* max - the maximum value.

**Percentile**  meaning: Percentiles are used in statistics to give you a number that describes the value that a given percent of the values are lower than.

**For Example** :If 75 percentile of SepalLengthCm column is 6.4, meaning that 75% of the sepal lenght (in cm) are of length 6.4 or lower to it.

**The mean** is the sum of all the entries divided by the number of entries

**Standard deviation** is a measure of the amount of variation or dispersion of a set of values. **The square root of the variance is the standard deviation**. We first need to calculate the mean of the values, then calculate the variance, and finally the standard deviation.

Steps to Calculate Standard Deviation

   1. The mean of [1, 2, 3, 4, 5] is 3.
   2. Calculate variance for each entry by subtracting the mean from the value of the entry. So variance will be [-2, -1, 0, 1, 2].
   3. Then square each of those resulting values and sum the results. For the above example, it will become 4+1+0+1+4=10.
   4. Then divide the result by the number of data points minus one. This will give the variance. So variance will be 10/(5-1) = 2.5
   5. So **standard deviation** will be **sqrt(2.5)** = 1.5811388300841898.

#### ***************************************************************[Back to the Python code for dataset]


#### STEP 4: Count of unique values

![value_count](https://user-images.githubusercontent.com/69766918/231443083-6e222e83-b1fe-4973-8c68-79e0b7cf2e93.jpg)

    * value_counts() creates a dictionary of counts for each unique value.

    * We have 50 samples in each output class
    
## Preprocessing the Dataset

Before exploratory data analysis, make sure it is clean.
Since this is a relatively simple data set there is not much cleaning that needs to be done.
    
#### Check for Missing Values

![findingmissingvalue](https://user-images.githubusercontent.com/69766918/231449109-528fcc65-ac16-447b-ab7d-fcd125af789b.jpg)

* There are no NULL values present in the dataset. 

* If any NULL values are present, we have to fill all the NULL values before proceeding to model training.

This data set is not missing(and having no NUll) values. While this makes modeling much easier, this is not usually the case.

## Model Training and Testing

![train-test-split](https://user-images.githubusercontent.com/69766918/231648580-8c55b72d-fe29-4d4b-ab66-830eaf365190.jpg)

   * X - contains input attributes
   * Y - contains the output attribute
   * train_test_split() - splits the data for training and testing (here we are splitting 70% data for training and 30% for testing)
    

(For more details:https://machinelearningmastery.com/train-test-split-for-evaluating-machine-learning-algorithms/)
    
    
## Import some models and train


### Steps to apply Algorithm

    1. Split the dataset into training and testing dataset. The testing dataset is generally smaller than training one as it will help in training the model better.
   2.  Select any algorithm based on the problem (classification or regression) whatever you feel may be good. we are going to use Logistic Regression Algorithm.
   3.  Then pass the training dataset to the algorithm to train it. We use the .fit() method
   4.  Then pass the testing data to the trained algorithm to predict the outcome. We use the .predict() method.
   5.  We then check the accuracy by passing the predicted outcome and the actual output to the model.
   


### 1. Logistic Regression

 Logistic Regression is  used when the dependent variable(target in our case Y) is categorical. Logistic regression is a useful analysis method for classification problems. 
 
 (Read in Detail: https://towardsdatascience.com/logistic-regression-detailed-overview-46c4da4303bc)

![logistic-regression](https://user-images.githubusercontent.com/69766918/231647848-0a113cd2-e9e8-4af1-9f6a-2aef93fc9912.jpg)

* fit() - used for training the model with the data
* model.score() - gives the accuracy for the test data

#### (Note: Are you getting different results for your machine learning algorithm? https://machinelearningmastery.com/different-results-each-time-in-machine-learning/)

### 2. k-nearest neighbors (KNN)

The k-nearest neighbors algorithm, also known as KNN or k-NN, is a non-parametric, supervised learning classifier, which uses proximity to make classifications or predictions about the grouping of an individual data point.The KNN algorithm assumes that similar things exist in close proximity. In other words, similar things are near to each other.

#### (Read: https://towardsdatascience.com/machine-learning-basics-with-the-k-nearest-neighbors-algorithm-6a6e71d01761)

![k-nearsetneighbor](https://user-images.githubusercontent.com/69766918/231651975-ed4fd82d-a44c-4936-82c4-bc1c21673dc3.jpg)

### 3. Decision Tree

A decision tree is a non-parametric supervised learning algorithm, which is utilized for both classification and regression tasks.  It is one way to display an algorithm that only contains conditional control statements.

#### (Read: https://towardsdatascience.com/decision-trees-in-machine-learning-641b9c4e8052)
![decision-tree](https://user-images.githubusercontent.com/69766918/231719050-80ea6ecf-fa2f-4177-8a7d-48e6e311213d.jpg)



