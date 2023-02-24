# Description

This repository represents a stress tracking project as part of TechLabs in Berlin (ST 2021). 
# Project Summary
https://github.com/TechLabs-Berlin/st21-stress-tracker/blob/main/projectsummary.md

## Ideation Session:
[https://www.notion.so/Ideation-Session-Part-II-14703a952e914db49148e33993b59739](https://www.notion.so/Ideation-Session-Part-II-14703a952e914db49148e33993b59739)
## Questionnaire:
[https://docs.google.com/forms/d/e/1FAIpQLSeJs9v_09XG_vQDJhvS4x-IMReQplxiEyfhgnlYeFJXxKJluA/viewform](https://docs.google.com/forms/d/e/1FAIpQLSeJs9v_09XG_vQDJhvS4x-IMReQplxiEyfhgnlYeFJXxKJluA/viewform)_

The key results from the questionnaire were as follows: 
- 85.3% says that stress has a big impact on their daily lives
- Two key groups: Group A wants to analyze & better understand why they’re stressed; Group B wants to reduce their stress levels
## User personas:
[https://miro.com/app/board/o9J_lBJW7fo=/](https://miro.com/app/board/o9J_lBJW7fo=/)
## User scenario:
[https://miro.com/app/board/o9J_lAADQNw=/](https://miro.com/app/board/o9J_lAADQNw=/) 

## Prototype Figma:
[https://www.figma.com/file/8L3kBzrKBUXWPbGQP37m2B/Stress-Tracker-Wireframes?node-id=121%3A6](https://www.figma.com/file/8L3kBzrKBUXWPbGQP37m2B/Stress-Tracker-Wireframes?node-id=121%3A6)

## Dataset Info
We used SWELL Knowledge Work (SWELL-KW) dataset from kaggle to develop the project.  The original dataset was collected at the Radboud University and featured physiological electrocardiogram (ECG) signals recorded from body sensors. The preprocessed data from kaggle includes most commonly used heart rate variability (HRV) parameters extracted from the raw data.

To collect the data, 25 participants performed typical office work such as writing reports, making presentations, e-mail communication, and searching for information. Then researchers manipulated their working conditions with the stressors: interruptions by incoming emails and time pressure to finish a set of tasks before a deadline. At the end of each experiment condition, each participant was asked to fill in a self-report questionnaire to assess their perceived stress. This ground truth info was used as outcome labels.

We achieved pretty good accuracy (92%) with the Random Forest classifier with eight important features. For the sake of simplicity we used this model in the final app. 
# WebDev / Deployment
The frontend was built using React.js. We utilise some HTTP methods using Axios which impliedly parsed any extracted JSON from the backend or third party API. 

Flask was used on the backend and a couple of files were in action namely a pickled binary file. A POST request was utilised to simulate and track the stress data with the given metrics.
## Deployed version: 
https://limitless-wave-49962.herokuapp.com/

# Requirements
- Python
- Flask
- React.js

We described the whole project cycle and insights in detail in the blog post: 
https://github.com/TechLabs-Berlin/st21-stress-tracker/blob/main/Blogpost.md

# Contributors

- Alex, Data Science track
- Madina, Data Science track
- Marcel, Data Science track
- Mikail, Data Science track

- Alba, UX track
- Priyanka, UX track

- Ikzath, Web Development track
- Suwana, Web Development track

# References
1. K. Nkurikiyeyezu, A. Yokokubo, and G. Lopez "The Effect of Person-Specific Biometrics in Improving Generic Stress Predictive Models". [https://arxiv.org/abs/1910.01770v2]  
2. S. Koldijk, M. A. Neerincx, and W. Kraaij, "Detecting work stress in offices by combining unobtrusive sensors". [https://ieeeexplore.ws/document/7572141]

