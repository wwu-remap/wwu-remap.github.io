# ReMAP
ReMAP (Remote Monitoring Application in Psychiatry) is an application for Android and iOS developed and used for psychiatric research purposes at the Institute for Translational Psychiatry, University of Münster. 

## Overview
The application provides several questionnaires concerning the user's mental health. Additionally, the app collects location and physical activity data in the background. 
The individual components are: 

#### Active Data - Questionnaires and Tasks
- Digital version of the Beck Depression Inventory (__BDI__)  
- Questionnaires concerning the user's __mood__ and __sleep__ quantity
- Questionnaire enquiring the user's concerns and personal experiences regarding the __COVID-19__ pandemic
- __Voice recording__ task asking the user to report on their state of health 

#### Passive Data - Background Data Retrieval
- Current __location__ (GPS)
- __Acceleration__ data provided by the device's sensor 
- Physical activity from Google Fit or Apple Health, such as __number of steps__ and __distance walked__
- Scan for nearby __bluetooth__ devices (Android only) 

## Libraries used 
#### Android
The application uses components provided by quickbirdstudios' [SurveyKit](https://github.com/quickbirdstudios/SurveyKit).
