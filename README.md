# Naive-Persistence-Model-Simulation-of-Natural-Gas-Daata

This time, I would like to run a test train split simulation and Naive Persistence Model simulation of Natural Gas Data. The data is downloaded from yahoo finance in 5 year range period from June 13, 2016 - June 13, 2021.
[Natural Gas.xlsx](https://github.com/altheanabila/Naive-Persistence-Model-Simulation-of-Natural-Gas-Daata/blob/main/NG.xlsx)

1. First of all, we import the related library, and transform the excel data into panda dataframes


![textimage](https://github.com/altheanabila/Naive-Persistence-Model-Simulation-of-Natural-Gas-Daata/blob/main/pic%201.png)


2.  Run a test train split, we will set 80% of total amount of data for train size

![textimage](https://github.com/altheanabila/Naive-Persistence-Model-Simulation-of-Natural-Gas-Daata/blob/main/pic%202.png)


3. Next, we forecast the data through Naive persistence model simulation.
Define df, and add t columns. Actually, t columns is just the actual data at index 0 + 1. Later we define Adj Close as y variable and t as x variable (predicted values).


![textimage](https://github.com/altheanabila/Naive-Persistence-Model-Simulation-of-Natural-Gas-Daata/blob/main/pic%203.png)


4. Then we set the last 7 data as test data, and the rest as train data, and divide the data into 4 parts


![textimage](https://github.com/altheanabila/Naive-Persistence-Model-Simulation-of-Natural-Gas-Daata/blob/main/pic%204.png)


5. Show the Naive persistence model result


![textimage](https://github.com/altheanabila/Naive-Persistence-Model-Simulation-of-Natural-Gas-Daata/blob/main/pic%205.png)


6. Calculate mean squared error. Mean squared error is actually the sum of squared of subtraction values between y values and predicted values. MSE is needed to evaluate advanced model. If the mse values of the advanced model is greater than mse values from naive persistence model, it means we cant extract any information from that data. And we could categorize the time series data as random walk. 


![textimage](https://github.com/altheanabila/Naive-Persistence-Model-Simulation-of-Natural-Gas-Daata/blob/main/pic%206.png)


7. Visualize the result


![textimage](https://github.com/altheanabila/Naive-Persistence-Model-Simulation-of-Natural-Gas-Daata/blob/main/pic%207.png)
