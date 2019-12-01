# Advanced-Training-Project-1
UiPath Level 3 Project - Assignment 1


In this exercise, you will create a UiPath automation that performs the steps below.
To achieve this, you will use the REFrameWork as the starting template and follow the UiPath development best practices.

Here are the steps performed by the Robot in the Dispatcher:
1. Log in to https://www.acme-test.com.
2. On the landing page, Dashboard, click or hover over the Invoices menu item and then click on Search for Invoice. Click on Display All Invoices. 
3. Scrape the data from the whole table displayed.
4. For each row in the datatable, Add a queue item containing the Invoice Number, Vendor Tax ID and Invoice Item.
5. Close ACME System 1.

Steps performed by the Robot in the Performer: 
1. Log in to https://www.acme-test.com.
2. For each Queue Item:
- Click or hover over the Invoices menu item and then click on Search for Invoice;
- Type the Invoice Number retrieved from the queue item into the Invoice Number field field;
- Click on Search;
- Extract the values for the Vendor Tax ID and Invoice Item and compare them with the values from the queue item (check for EXACT match for all fields!);
- If the values are not matching, this should be categorized as a Business Rule Exception, and the queue item should have the status set accordingly;
- If the values match, the transaction is successful.

Note: Navigation can be achieved in multiple ways by the robot - choose whichever you find best.

Constraints to follow in the development, using the REFrameWork:
1. TransactionItem datatype should be a QueueItem. The process should recover and retry 2 times in case of errors in navigation between the Invoice Search and Invoices - Search Results pages. One transaction is the action of navigating to the Invoices Search page, searching for the Invoice Number and scraping the values from the resulting one row table.
2. Create a separate workflow file for the Login to ACME. File input arguments: URL ; Username ; Password .
3. Create a separate workflow file for closing ACME. 
4. Add the ACME_URL and ACME_Credential to the Excel Config file.
5. Populate InitAllApplications.xaml from the Framework folder with Invoking the Login to ACME and navigation to the Work Items.
6. Populate CloseAllApplications.xaml from the Framework folder with Invoking the Close ACME.
7. Populate KillAllProcesses.xaml from the Framework folder with killing the process used.
8. Populate the Process.xaml file with the following actions: Navigation, Searching for Invoice Number, Scraping, Checking if the values match, Handling the Business Rule Exception.

