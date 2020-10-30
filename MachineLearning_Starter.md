# Table of Contents
 - What is ML (Introduction)
 - Types of Machine Learning algorithms
 - Setup development environment
 - Machine Learning work-flow

# What is Machine Learning
```
	Is this email spam (Gmail)
	how can cars drive themselves(Tesla)
	what will people buy(Google search and Amazon)
```

Depending on what inputs you provide
data driven predictions: Data -> modify to be able to used by ML -> this modified data passed to Algorithm -> Data analysis -> creates model that solves data based on data

static program instructions: if else, case, when

# Types of Machine Learning algorithms
	** 1. supervised:**
	Categories: 
		a. Classification: output is category like red or green, disease and no disease 
		b. Regression: real value such as price, weight 

	it consists of 
	outcome -> to be predicted from set of predictors(independent variables) -> we generate a function that maps inputs to desired outputs.
	Above training has to be done until a certain maturity is attained

	**Example:** you provide data (input / independent variables): size, number of bedrooms, year built  (target / outcome variable / dependent variable):  price 
	**Algorithms:** Regression, Decision tree, Random Forest, KNN, Logistic regression

 
	** 2. Unsupervised:**
	Categories: 
		a. Clustering: group customers by purchasing habits
		b. Association: people that buy X also buy Y

	clusters of data. provide voice of different people talking output: identify who is speaking
	**Example:** 
	**Algorithms:** Markov decision process


	** 3. reinforcement learning**
	**Example:**
	**Algorithms:**

**Comparison**

| Supervised     | Unsupervised     |  reinforcement      |
|-----|------|--------|
| value prediction    | identify clusters of like data       |        |
| needs training data containing value being predicted    | data does not contain cluster membership     |        |
| trained model predicts value in new data | model provides access to data by cluster | |

# Setup of development environment
Language: Python 3.5
Easy to learningPowerful, Object Oriented
Elegant syntax, easy to read
standard libraries for most common tasks

python 2.7 and 3.x
	Both used
	
Python 3
	introduced in 2010 and future of python
	few incompatibilities with 2.7
	
Python 2.7
	Last version of Python 2
	static since 2012
	
Different libraries for ML:
numpy - scientific computing 
pandas - data frames
matplotlib - 2D plotting
Scikit-learn 
	Algorithms
	Pre-processing
	Performance evaluation

	(Alternative TensorFlow	)

IDEs: Jupyter environment,  
JetBrains PyCharm community edition
Jupyter
	Formerly Ipython Notebook
	Notebooks contain code and text
	perfect for iterable work like machine learning
	shareable
	support multiple languages (Ruby, R, Haskell, C#, PHP, Scala...)

Installation: Anaconda (https://www.anaconda.com/download/) -> downloaded Anaconda3-5.2.0-Windows-x86_64 which is latest on 08_July_2018
-it takes some time to install
-go to windows -> Anaconda Navigaor -> Jupyter notebook
Shift + enter -> runs code
new -> folder -> untitled folder -> select checkbox left to it -> rename -> notebooks
new -> python 3 -> will open a notebook in new tab
esc + m -> markdown mode
esc + y -> code mode

Conda: package and environment manager


# Machine Learning work-flow
An **orchestrated and repeatable pattern**  
which systematically **transforms and processes information**  
to **create prediction solutions**

   1. Asking the right question
   2. Preparing data( as you will have random data, you need to transform it)
   3. selecting the algorithm 
   4. Training the model 
   5. testing the model (use new data which was not used for training)

### Machine Learning work-flow Guidelines
    Early steps are important (Each step depends on previous step)  
    Expect to go backwards (Later knowledge affects previous steps)  
    Data is never as you need it (Data will have to be altered)
    More data is better ( More data => better results)
    Don't pursue a bad solution (Re-evaluate, fix or quit)

## 1. Asking the right question
Don't we already know the question : 
"Question": "Predict if a person will develop diabetes"
-->need statement to direct and validate the data

Solution statement guidelines
	a. Define scope(including data sources) : 
	b. Define target performance
	c. Define context for usage
	d. Define how solution will be created

a. Define scope(including data sources)
	Understand the feature in data(age, race, gender,..)
	identify critical features()
	focus on at risk population
	select data source (pima Indian diabetes study is a good source of data based on population in Arizona in 1990s, UCI machine learning repository)
	"Question": "Using Pima indian Diabetes data, Predict which people will develop diabetes"

b. Performance targets
	Binary result (true or false)
	but even coin flip has 50% accuracy
	Also, genetic difference are factor
	Hence, 70% accuracy is common target
	"Question": "Using Pima indian Diabetes data, predict with 70% or greater accuracy, which people will develop diabetes"

c. Context for usage
	Disease prediction
	Medical research practices show there is unknown variations between people
	hence, Likelihood is used in healthcare
	"Question": "Using Pima indian Diabetes data, predict with 70% or greater accuracy, which people are likely to develop diabetes"

d. Solution creation
Machine learning workflow
	- process pima indian data
	- Transform data as required
"Question": "Use machine learning workflow to process and transform Pima indian Diabetes data to create a prediction model, This model must predict which people are likely to develop diabetes with 70% or greater accuracy"

## 2. Preparing your data
	find the data we need
	Inspect and clean the data
	Explore the data
	mold the data to tidy data
	
Tidy data:
Tidy datatsets are easy to manipulate, model and visualize, and have a specific structure:
	each `variable` is a `column`
	each `observation` is a `row`
	each type of `observational unit` is a `table`
										- Hadley wickham
Trivia: 50-80% of a ML project is spent on getting, cleaning and organizing data.

## Getting data
	Google(caution: a lot of unvalidated data)
	Government databases
	professional or company data sources
	your company/ your department
	All of the above

Pima Indian diabetes data
Originally from  UCI Machine Learning repository
pima-data.csv - in demo folder , based on UCI data
female patients at least 21 years old
768 patients observation rows
10 columns
	9 feature columns
		number of pregnancies,blood pressure, glucose, insulin level...
	1 class column
		Diabetes - true or false
		
Data rule #1: closer the data is to what you are predicting, the better
Data rule #2: data will never be in the format you need (pandas DataFrames for reformatting)
Data rule #3: Accurately predicting rare events is difficult
Data rule #4: Track how you manipulate data (change tracking)

Loading cleaning and inspecting data

Change Tracking:
Jupyter Notebook
	python interpretor interaction stored via code cells
	documentation stored via markup cells
	still need source code management(Git, TFS, SVN, etc)
	
	Summary:
	use pandas to read in demo data
	identified corelated features
	cleaned data
	molded data
	checked true/false ratio
	discussed data rules

Complete project and modified data for course
http://bit.ly/ml_python


	

	


https://s3-ap-southeast-1.amazonaws.com/mettl-prod/data-science/SMSCollection.txt
https://s3-ap-southeast-1.amazonaws.com/mettl-prod/data-science/train.csv