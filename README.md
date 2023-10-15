# Xtern-AI
This is my repo for submitting to my internship

(25%)  Given the data set, do a quick exploratory data analysis to get a feel for the distributions and biases of the data.  Report any visualizations and findings used and suggest any other impactful business use cases for that data.


First of all, 3 universities account for the most orders are Indiana State University, Ball State University and Butler University with over 1000 orders. With majors, majors over 600 orders are Physics, Chemistry, Biology and Astronomy while sophomores and juniors account over 2250 orders. I suggest that food truck opening hours from 10 AM to 3PM which from 11AM to 2PM are peak hours achieving more than 800 orders. Some of interesting statistics from Ball State University: they are keen on Indiana Corn on the Cob (brushed with garlic butter),Breaded Pork Tenderloin Sandwich ,Indiana Pork, Chili,Sugar Cream Pie ,Ultimate Grilled Cheese Sandwich (with bacon and tomato). Indiana State University liked Hoosier BBQ Pulled Pork Sandwich ,Cornbread Hush Puppies, Sweet Potato Fries ,Fried Catfish Basket ,Indiana Buffalo Chicken Tacos (3 tacos) while Butler doesnt experience significant preferences.


(30%) Consider implications of data collection, storage, and data biases you would consider relevant here considering Data Ethics, Business Outcomes, and Technical Implications


Discuss Ethical implications of these factors
- Privacy and consent: This is alarming since we could not leak the data since it breaches the customer’s privacy.
- Bias: as we could experience in our dataset, it is imbalanced hence we need to pick the best solution to minimize the bias.
- Data Integrity: we need to verify the source of data collection, if the data is not correct, we might lead to false advertising hence harming the business revenues as well as business reputation


Discuss Business outcome implications of these factors:
- Legal and Regulatory Risk: data-mismanagement could lead to penalties for business.\
- Economic Impact: Biases in algorithms, deriving from biased datasets could lead to unfair treatment of underrepresented groups, hence reducing the revenues and lost market target.

Discuss Technical implications of these factors:
- Storage Cost: large dataset require large storage solutions. This can lead to increasing costs, if the data is stored redundantly asnd without data lifecycle management.
- Data security and maintenance: Ensuring the security of data is paramount. This requires securing te data long term ,or regular security audits and detecting the drift in data if it occur.
- Scalability and Version Control: As data grows, ensuring infrastructure can handle the data and having version control to track changes and loss of data.


(35%) Build a model to predict a customers order from their available information.  You will be graded largely on your intent and process when designing the model, performance is secondary. It is strongly suggested that you use SKLearn for this model as to not take too much time.  You may use any kind implementation you would like though, but it must be pickelable and have a “.predict()” method similar to SKLearn


Outline your process for model selection, training and testing. Including data preparation.
Design a function that prepares your data by loading the provided dataset and processes it into an appropriate machine readable format if necessary.
Design a function to train your model and pickle it.
Train and test your model.  Submit any training, testing and model selection visuals or metrics.
Upload your work to GitHub and link the repository, make sure it is public.


First of all, I load the data into a dataframe and analyze the data. Then, I convert all the categorical data into numbers for the machine learning model to fit the x_train and y_train. I use GridSearchCV to choose the best model.


In second.py is where I implement SMOTE which is used to reduce the bias by synthetic samples of the minority class. Also, I tried to find the correlation between columns but it did not turn out any significant covariance. Moreover, I use the PCA method to reduce dimensionality of the data but still keep the correlated data and have an impact on each other. It did not have a significant increase in accuracy.


(10%) Given the work required to bring a solution like this to maturity and its performance, what considerations would you make to determine if this is a suitable course of action?


Most of the problems of machine learning come from imbalanced dataset and the same for this problem. I tried to train it by using SMOTE to upsampling the data but still not increasing the accuracy significantly. In the future, I would suggest trying to collect more data to improve the project benefits for all the food truck intentions. For bigger datasets, we will need storage to keep all the data and secure it. From my standpoint, I need to achieve up to 75% accuracy so that I could let this model predict the orders for the business. For data management, we still need to update the data also detecting the data drift based on the season as well as other factors. These considerations are crucial for maintaining the suitable course of actions

