# UiPath Level 3 Project - Assignment 1

# Exercise
In this exercise, you will create a UiPath automation that performs the steps below.
To achieve this, you will use the REFrameWork as the starting template and follow the UiPath development best practices.

1.1 Open the ACME System 1 Web Application.
1.2 Log in to System 1. Required input data: email and password.
1.3 Access the Dashboard - the central location, where the user can pick a specific menu item.
1.4 Access the Work Items listing to view all the available tasks to be performed (Output data: Work Items).
1.5 For each activity of the WI5 type, perform the following steps:
    1.5.A Open the Details page of the selected activity to retrieve the Client Information Details.
    1.5.B Open the SHA1 Online webpage - http://www.sha1-online.com/, and provide the following input: [ClientID]-
    [ClientName]-[ClientCountry]. Replace all the variables with the corresponding values. Use dashes between items,
    as shown above.
    1.5.C Retrieve the Client Security Hash value from the webpage.
    1.5.D Go back to Work Item Details and open Update Work Item.
    1.5.E Set the status to “Completed”. Add a comment with the obtained [SecurityHash].
1.6 Continue with the next WI5 Activity. 
