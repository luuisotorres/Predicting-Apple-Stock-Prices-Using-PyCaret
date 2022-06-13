<img src = 'https://miro.medium.com/max/1024/1*Cku5-rqmqSIuhUyFkIAdIA.png'><br>
# Predicting Apple Stock Prices Using PyCaret
--<br><br>
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white) <br>
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)<br>

--

# Introduction

Who wouldn't like to have the hability to predict the future prices of stocks and other financial assets? Such skill would help us to make investment decisions without falling prey to the strong emotions of **doubt**, **fear** and **panic** that takes so many investors and traders into a path of losing money in the long run.<br><br>
With this idea in mind, I decided to develop a **machine learning** model to try to forecast the prices of Apple stocks through <a href = "https://www.ibm.com/topics/linear-regression"><b>linear regression</b> analysis</a>.<br><br>
While I was studying on how to make such predictions, I came across a library called <a href = "https://pycaret.org/">PyCaret</a>, which is an open-source, low-code machine learning library in Python that automates machine learning workflows, ideal for those who are beginners in machine learning, such as myself.<br><br>
Before starting the development of this project, I'd like to make it clear that this is nothing but a study on how to use PyCaret's regression lib to make predictions and I have no intention whatsoever to recommend you to buy or sell any financial asset. There are a lot of factors when it comes to making the market go up or down and no mathematical model will be able to predict with 100% accuracy news, wars, conflicts or any other thing that may trigger the feelings of **fear** or **greed** in investors.

---

# Development

#### Obtaining and Handling Data

The **first step** to start developing this project is **importing all the necessay library** that we need to do all the work.<br>
First, I imported **pandas** to helps us organizing and managing our data, then I imported **pandas_profiling** in order to automatically perform an exploratory analysis of our dataset. Unfortunately, it isn't possible to diplay **Pandas Profiling Reports** on a GitHub notebook, for that reason, I had to save the reports as an *.html* file and upload them to this repository so you can **download** it and have access to all the **rich information** that the **Pandas Profiling Reports** are able to generate with **just one line of code**.<br>
I then imported **Plotly Express** and **Plotly Graph Objects** to create relevant graphics to help with **data visualization**, and  also made all the **necessary* configurations in order to make Plotly charts **visible** on GitHub with **Plotly.io**.<br>
Lastly, I imported the **yfinance** library, which allows us to obtain data from **Yahoo Finance**.<br>
After all libraries were imported, I then proceeded to finally get Apple stocks historic data using **yfinance**, obtaining data from all the **previous 20 years**. I then did an initial exploratory analysis, made all the necessary changes for the dataset and used a **Plotly Candlestick** chart to visualize the period analyzed.

#### Using PyCaret

After separating our dataset into two dataframes, one to create our **regression model** and another one to test it to see how well the model would predict the closing prices of the last **2 years**, I then proceeded to import PyCaret's regression library and set it up for measuring the accuracy metrics among the 20 different regression models.<br>
From all models, the **Bayesian Ridge** presented better metrics for accurary, and after tuning it with PyCaret's *tune_model( )*, I could achieve even better metrics.<br>
I finalized the model, using the tuned **Bayesian Ridge** regression model, and finally tested it, predicting APPL's closing prices from the last 2 years and comparing it to the actual closing prices on a Plotly line plot.

---

# Conclusion
We can conclude that the PyCaret library offers an easy way to explore and test different regression models of **machine learning** and choose which one of them is the best for our dataset.<br>
With this study, it was possible to find a model that adjusted very well to our data and that was capable to predict the closing prices of the last 2 years with high levels of accuracy, sucessfuly indicating the direction of APPL stocks in that period.<br>
Once again, I reinforce that this project has the sole goal of exploring PyCaret's Regression library and I have no intention of recommending the purchase or sale of any financial asset nor I recommend using this strategy blindly to make investment decisions.<br>

----

# Author
**Luís Fernando Torres**
