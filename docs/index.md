# ReMAP
ReMAP (Remote Monitoring Application in Psychiatry) is an application for Android and iOS developed and used for psychiatric research purposes at the Institute for Translational Psychiatry, University of Münster. 

## Overview
The application provides several questionnaires concerning the user's mental health. Additionally, the app collects location and physical activity data in the background. 
The individual components are: 

#### Active Data - Questionnaires and Tasks
- a digital version of the Beck Depression Inventory (BDI)  
- questionnaires concerning the user's mood and sleep quantity
- a questionnaire enquiring the user's concerns and personal experiences regarding the COVID-19 pandemic
- a voice recording task asking the user to report on their state of health 

#### Passive Data - Background Data Retrieval
- retrieval of current location  
- retrieval of acceleration data provided by the device's sensors 
- retrieval of physical activity data from the user's Google Fit or Apple Health account, such as daily amount of steps and distance covered 
- scan for nearby bluetooth devices (Android only) 

## Libraries used 
#### Android
The application uses components provided by quickbirdstudios' [SurveyKit](https://github.com/quickbirdstudios/SurveyKit).
