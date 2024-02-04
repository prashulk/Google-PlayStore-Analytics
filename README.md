# Google-PlayStore-Analytics

### Purpose:
The purpose of our project is to create a web application that leverages Google App Store data to deliver key insights on app performance, user engagement, and retention. This application will serve as a valuable tool for developers, providing them with detailed analytics to understand the drivers behind an app's popularity and success. It will also cater to consumers by offering an easy-to-navigate interface to discover and evaluate top-rated apps across various categories, based on user reviews and ratings. By integrating features for analyzing app trends and enabling user review submissions, the project aims to facilitate informed decision-making for both app creators and users, ultimately enhancing the app selection and development process.

### Technical Description
In our project, first we utilized a python script to remove bad quality data from the Kaggle source we used as input. The python script mainly removed ‘NA’ values and converting non integer to integer values (like removing ‘,’ in prices and app installs) and also removing duplicate values. We then employed MySQL for data normalization and cleansing. The process involved pre-normalization, normalization, and post-normalization stages to ensure the integrity and quality of the Google App Store data. This approach was essential for obtaining clean and well-structured app data and user review data. For Pre-normalization using the SQL queries we prepared the raw Google App Store data for normalization. This step was crucial for setting a clean baseline. Next, we then proceeded to structure the data effectively. This process ensured that the data adhered to database normalization principles, optimizing it for efficient querying and analysis. 
This finally resulted in 4 tables i.e. – apps_dim, app_ratings, app_categories_genres, app_reviews and app_price. 


### Data Model - 
<img width="490" alt="image" src="https://github.com/prashulk/Google-PlayStore-Analytics/assets/67316162/122d7df8-d60e-4870-811c-a8a7feaddb74">


### User Functionalities -
The web application provides different functionalities to manage app reviews and add and manage app data as well.

-	Manage Apps:

  	Helps to add a new app by entering the app name. 
  	Different fields namely size of the app, number of installs, last update, current version, app price is required to enter while entering a new app in the database.
  	Updating app price is also available. If the app price is set to 0 it shows that the app is free and not paid anymore.
  	Deleting an app data is also available by selecting the name of the app, the app information can be deleted from the database.

-	Manage reviews:
  
  	By selecting the name of the app, you can write the review and add a new review about the app.
  	Deleting a review can also be done by selecting the name of the app and selecting which review is to be deleted from the available reviews of the app.

-	App information:

  	We can get to know the app information by entering the application name in the text box and it will display the results pertaining to that app.
  	The application also displays the top expensive apps based on user input, top rated apps whether free/paid depending on the user input, then visualization showing the app by creation year and size, top app by installs in each category as per user      input and finally we also provide functionality to view reviews for the app queried by the user.


