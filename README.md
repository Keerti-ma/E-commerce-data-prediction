  
#E-COMMERCE DATA PREDICTION USING LINEAR REGRESSION MODEL IN PYTHON
As an entrepreneur, one should understand that there is a phase where businesses struggle, even those that have been on a very high profit. Over the years, I have come to realize that the major driving force of a business is its customers experience. 
"If you do build a great experience, customers tell each other about that. Word of mouth is very powerful." – Jeff Bezos
 
ABOUT PROJECT
This project is about an E-commerce company that that sells clothing online but they also have in -store style and clothing advice sessions. Customers sometimes order on a mobile app or website for the clothes they want. The company is trying to decide whether to focus their effort on their Mobile App experience or their website. In this project, I created an algorithm using Python which makes prediction to help them solve that problem. 

IMPORTING THE NECESSARY PYTHON LIBRARIES
A library which is a collection of functions that we include in our python code and called as necessary. With libraries, pre-existing functions can be imported which will efficiently expand the code performance. For this project, I will import the following libraries pandas, numpy, matplotlib, seaborn, sklearn e.t.c. Then set %matplotlib inline since I'm using a Jupiter notebook
GETTING DATA
I worked with the Ecommerce Customers csv file from the company[Dataset]. It has Customer info, such as Email, Address, and their colour Avatar. Then it also has numerical value columns: 
Avg. Session Length: Average session of in-store style advice sessions.
Time on App: Average time spent on App in minutes 
Time on Website: Average time spent on Website in minutes
Length of Membership: How many years the customer has been a member. 

PROCEDURES
A lot of procedures was taken, I will be discussing them one after the other. 
 Reading-in-the Ecommerce customers datasets. 

There are several methods to read in files. In this project I used pandas library because it is the most convenient, I have encountered. It allows you to read files with several delimiters.
2.  Checking the head of the dataset.
The head() function is a function in pandas Library. It is used to get the top n-number of rows of the dataframe. It is useful for testing if the object has the right type of data in it.
3. The describe() method 
It returns description of numerical data in the dataframe.
4. The info() method
 It returns the basic information about the Dataframe.

EXPLORATORY DATA ANALYSIS (EDA)
Before I go into creating my Linear model and making the prediction accordingly. I did some exploratory data analysis on the data to further explore the data using visual techniques and check assumptions using graphical representations. I'll only be using the numerical data of the csv file.
Use seaborn to create a jointplot to compare the Time on website and yearly Amount spent columns. To know if the correlation make sense.

2. Also created jointplot to compare the Time on App and Length of membership colums. Here is more correlated than when comparing the Time on website and Yearly Amount spent.
3. There seems to be a good linear fit on the data which means that the longer you stay as a member, the more expenditure you will have.
TRAINING AND TESTING OUR DATASET
After exploring the data, I went further to split the data into training and testing sets. I set a variable X equal to the numerical features of the customers and a variable y which is the predicted variable equal to the "Yearly Amount Spent" column.
At this point, I imported the Sklearn model where I can Use the model_selection.train_test_split from sklearn to split the data into training and testing sets and set test_size=0.3 and random_state =101.

TRAINING THE MODEL
Recall that I made a split on the data into training and testing set, I will now train the model on my training data. I further Imported LinearRegression from sklearn.linear_model and Create an instance of a LinearRegression() model named lm.
I then Train/fit "lm" on the training data.
Now that we have fit our model, let's evaluate its performance by predicting off the test values!
Use lm.predict() to predict off the X_test set of the data Create a scatterplot of the real test values versus the predicted values.
We can see that our model is actually doing well, if it was a perfected straight line thereby having the dots on each other I can then say I have a perfect model. Nevertheless, it still looks good since I'm considering the Y test versus the predicted values.
 
EVALUATING THE MODEL
Let's evaluate our model performance by calculating the residual sum of squares and the explained variance score (R^2).
To calculate the Mean Absolute Error, Mean Squared Error, and the Root Mean Squared Error I will have to import another function called Metrics from sklearn.
The "R^2" is the measurement of how much variance the model explained and we can see that it explained about 99% of the variance which shows that we have a very good fit model.

CONCLUSION
Let us figure out the answer to the original question, do we focus our efforts on mobile app or website development? Or maybe that doesn't even really matter, and Membership Time is what is really important. Let's interpret the coefficients to get an idea.

INTERPRETING THE COEFFICIENTS
  As the size of Avg. Session Length increase by 1 unit the total dollars spent also increase by 25.98 dollars.
As the size of Time on App increase by 1 unit the total dollars spent also increase by 38.59 dollars.
As the size of Time on Website increase by 1 unit the total dollars spent also increase by 0.19 dollars.
As the size of Length of Membership increase by 1 unit the total dollars spent also increase by 61.27 dollars.

From the prediction do you think the company should focus more on their mobile app or on their website?
There are actually two ways to think about this:
  Develop the Website to catch up to the performance of the mobile app
 Develop the app more since that is what is working better.

Thanks for going through my project, your observations and suggestions are highly appreciated, you can leave your inputs in the comment session, email me directly here  or reach me through other of my social media platforms below.
LinkedIn
Twitter 
Dataset
Full code
