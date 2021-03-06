# **Stress Tracker Web App — How Low Can You Go? (With Your Stress Level)**

![](Images/techlabs_logo.png)

_This project was carried out as part of TechLabs in Berlin (summer term 2021)_


## **Introduction**

_Nowadays stress plays a big part in daily life, with many people struggling to cope with it. Therefore, with Stress Tracker our goal was to develop a web application where anyone can be on top of their stress levels. As we worked to achieve this goal, we developed an app that tracks your stress level and is able to reduce it instantly with personalized exercises. The web app is used in combination with smartwatch of the user in order to track the heart rate and heart rate variability of the user continuously in connection to the user’s stress levels. The web application was created by the three tracks: Data Science, UX, and Web Development._

Since stress is becoming more prominent in everyday life and can bring dangerous health effects with it in the long-run, our aim was to create an app that could track the current stress level of the individual by using the user’s smartwatch data and give the user personalized stress reducing exercises based on that. Before we could further go into the details and web app features, however, we first had to identify the potential target group. 

## **Our project journey**
In order to do so, the UX team initiated a team’s [ideation session](https://www.notion.so/Ideation-Session-Part-II-14703a952e914db49148e33993b59739 ) in which we further brainstormed on the following: 1. User profile; Stress tracking system; and 3. The app’s stress reducing exercises. 

From the ideation session it came clear for the Data Science track that there were a couple of data constraints within the user profile. For example, with the current datasets we realized that we did not have enough data on gender at the moment. That is why we decided to skip that part for the user profile and focus on height, weight, level of fitness, and date of birth instead since these physical aspects can have a direct impact on an individual’s stress level. Furthermore, when it comes to monitoring the user’s stress level, the Data Science track concluded to focus on the heart rate and heart rate variability as the key stress indicators for the web app.

The initial idea for the app was to also include a user evaluation of how stressed he or she is. Due to insufficient data which was binary and that we at this point were unable to track stress live with the user’s smartwatch we decided to skip this option. Instead of that we decided to focus merely on users that want to reduce their stress levels.

Based on the findings from the team’s ideation session, the UX track developed a [questionnaire](https://docs.google.com/forms/d/e/1FAIpQLSeJs9v_09XG_vQDJhvS4x-IMReQplxiEyfhgnlYeFJXxKJluA/viewform) to get a better understanding of the potential target group and their needs. The key results from the questionnaire were as follows: 




* 85.3% say that stress has a big impact on their daily lives
* Two key groups: Group A wants to analyze & better understand why they’re stressed; Group B wants to reduce their stress levels

Based on the results, the UX track further went into creating the [user personas](https://miro.com/app/board/o9J_lBJW7fo=/) and developed a [scenario](https://miro.com/app/board/o9J_lAADQNw=/) to better understand the potential target group.

After we defined our potential target group we further defined the key functionalities of the app. The core functionalities were as follows: 1. Stress monitor that is connected with the user’s smartwatch and shows the level of stress based on the user’s heart rate & heart rate variability; 2. Instant stress reducing exercises that are tailored to the user based on the amount of time the user has (A. 2-3 minutes; B. 20 minutes; C. 1 hour). 

![](Images/main_functions.png)

Now that we had clear insights into the above, we started with the design of the app in terms of look & feel and user interface. Our main aim here was to develop an app that was easy to use and keep the overall design simple and minimalistic in order to keep the main focus on the app’s stress reducing functionality.

Based on this, the UX team created the first sketches of the web app. Together with the Web Development team, the sketches were further optimised to meet the app’s functionalities. 

After several meetings with Web Development, the UX team designed the [prototype in Figma](https://www.figma.com/file/8L3kBzrKBUXWPbGQP37m2B/Stress-Tracker-Wireframes?node-id=121%3A6) that the Web Development team could continue to work on. To further test the app’s functionality, it was tested on potential users. Based on the user feedback, we made a couple of tweaks to the design in terms of user interface. The main feedback that we received from users was regarding the user dashboard after logging in. It was namely not very clear for users yet where to navigate given the multiple options. For the final version of the app, we narrowed the options down so that users only had two options to choose from: 1. To see their current stress levels; and 2. A relax me option to instantly reduce their stress levels. After we revised the design, web development continued working on the app and made the final version. We tested the final version with potential users again and since there was no additional feedback we kept the app with no further changes.

After a profound literature research, our data science team decided to collect the following important parameters of users: 1. Date-of-birth, 2. BMI (height, weight) and 3. Fitness level. These physiological parameters have a direct impact on an individual’s stress level and are therefore important to profile our users. Regarding the key stress parameters, the collection of the heart rate and the heart rate variability play a significant role. 
The initial idea for the app was to also include users' evaluation of how stressed they are. Due to insufficient data which was binary and that we at this point were unable to track stress live with the user’s smartwatch we decided to skip this option. Instead of that we decided to focus merely on users that want to reduce their stress levels.

![](Images/tech-stack.png)

Our Data Science team used Python for developing our project. In order to analyze, clean and understand our data set, we used Numpy, MatPlotlib and Pandas libraries in the first place. After Data cleaning and Data Wrangling we started PEDA (Preliminary Exploratory Data Analysis).
When we completed our statistical analysis, we did our feature selection and got ready for ML model building.
The aim of our notebook and project is to evaluate binary class classification models to predict whether a person is stressed or not-stressed based on Heart Rate Variability (HRV) and other extracted features. Shortly dealing with a type of Supervised Learning Classification problem.
In order to achieve the best result, we build 4 different classification models: 
- Random Forest Classifier
- Support Vector Classifier
- Decision Tree Classifier
- Gradient Boosting Classifier

![](Images/auc_roc.png)

For each model, we estimated the performance via computing the accuracy, precision-recall, F1 score. We performed the hyperparameter optimization for each algorithm via getting the help of Sklearn's model_selection function  GrindSearchCV()
After our evaluation, we saw that all models gave very good results. However, the Random Forest model showed the best "overall" performance for our data set. We obtained the most balanced trade-off between training cost and accuracy. For this reason, we made a decision that Random Forest is the optimal model to measure the HRV feature set and predict stress. On account of this, our StressTracker App will be based on the Random forest model. 

As the frontend was build solely using Resct js the WD team had to utilise some HTTP methods using Axios which impliedly parseed any extracted JSON from the backend or third party API. Flask (Python) was used on the backend and a couple of files were in action namely a pickled binary file, a centralised app file and some configuration files required to run a virtual environment. A POST request was utilised to simulate and track the stress data with the given coordinates. The Node js this transition was abit tricky yet a rewarding experience nevertheless.

![](Images/future-design.jpg)

For now we have built a protoptype web app, but our final vision consists of a fully smart watch and mobile app that is synchronizable and get instant notifications when anyone seems to be over stressed (thus a  almost fully automated mobile app)

**The Team**

A bunch of tech amateurs pooling in our newly learned tech skills to make the world as stress free as possible.

**Alex,** Data Science Track

**Madina,** Data Science Track

**Marcel,** Data Science Track

**Muhammet,** Data Science Track

**Alba,** UX Track

**Priyanka,** UX Track

**Ikzath,** Web Development Track

**Suwana,** Web Development Track
