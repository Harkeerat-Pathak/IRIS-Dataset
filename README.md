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

![datatypes_usinginfo](https://user-images.githubusercontent.com/69766918/231433233-7e99fb00-230a-4ec8-9ec5-a14512e48a99.jpg)


![stats_usingdescrib](https://user-images.githubusercontent.com/69766918/231433843-65659706-0293-484f-9110-0601016a4b97.jpg)

#### [SKIP it ,if you already know]

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



