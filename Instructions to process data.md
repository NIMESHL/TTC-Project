# TTC-Project

The "Toronto Bus Delay" datasets are being retreived from Kaggle. This provides comprehensive information on bus delays experienced in Toronto throughout 2022 and 2023. The data includes multiple fields, such as the duration of the delays, the bus routes involved, the specific locations of delays, the time and date of the incidents, and the reasons for the delays (e.g., mechanical issues, traffic congestion, weather conditions, or accidents). The dataset is valuable for transportation research and can help stakeholders analyze the efficiency of the Toronto Transit Commission (TTC) bus system. By identifying patterns in delay frequency, duration, or causes, the dataset can assist in predicting potential issues and improving the overall service quality. Data scientists and urban planners can use this information to propose solutions to reduce delays, optimize route management, or enhance passenger experience. The dataset also opens up opportunities for predictive modeling, anomaly detection, and trend analysis for public transit operations.

This TTC project is developed to visualize the comparison between delays in TTC Busses based on 3 crieterias using the datasets for 2022 and 2023. Both of these datasets have data from January to June.
Tableau dashboardsa are beaing created to visualize each of these crieterias.

1. TTC Delay by Location.
2. TTC Delay by route.
3. TTC Delay by Time.

Below are the fields available in the datasets:

<strong>Date:</strong> The date when the delay incident occurred.<br>
<strong>Route:</strong> The route number of the bus.<br>
<strong>Time:</strong> The time when the delay incident was reported.<br>
<strong>Day:</strong> The day of the week when the delay incident occurred.<br>
<strong>Location:</strong> The location or station where the delay incident occurred.<br>
<strong>Incident:</strong> The type of incident causing the delay (e.g., Diversion, Security, Cleaning - Unsanitary).<br>
<strong>Min Delay:</strong> The duration of the delay in minutes.<br>
<strong>Min Gap:</strong> The time gap in minutes between buses.<br>
<strong>Direction:</strong> The direction of travel (e.g., Northbound, Southbound). Note: Some entries may have NaN indicating the absence of direction information.<br>
<strong>Vehicle:</strong> The identifier of the bus involved in the delay incident.<br>


 ![Picture1](https://github.com/user-attachments/assets/3065f65a-2699-4479-8d50-6d4ef0ed46e4)<br>
 <!--- ***********************************************   Criteria 1 ************************************************************************************************************* --->
<strong><h2>Criteria 1: Number of delay incidents in each Location(column: Location, Row: count).</h2></strong><br>
![delay by location](https://github.com/user-attachments/assets/f60742cb-b9ac-4912-84f8-355b1bcd1abe)<br>
<strong><ins>Data preparation:</ins></strong><br>
(Since most of the delays were occured in Route no: 32 and Route no:36, we have filtered the other routes data from the data set.)
Steps followed to prepare the data fields.
1.	Right click on field ‘Route’.
2.	Select ‘Convert to Dimension’.<br>
![b1](https://github.com/user-attachments/assets/1874bc84-c3c4-452a-a27e-fa92af4023fe)<br>
3.	Drag the ‘Location’ field into Columns and Count variables(ttc-bus-delay-data-2022.csv) into Rows.<br>
![delay location 2022](https://github.com/user-attachments/assets/8d48bfa7-c8e0-416c-88b7-6fa2d08cd7fb)<br>
4. Since we are using the only the data belong to route 32 and route 36, we need to remove the data that belong to other routes and bad data(ie:'Null' route values). In order to remove these data we must add a filter to the route field. Drag the 'Route' field and drop it into 'Filter' box. Then we get the list of checkboxes for the routes. You need to select only the 32 and 36 routes from the list.<br>![rts](https://github.com/user-attachments/assets/16204d9a-5048-4822-8516-bd3cf5bcf02b)<br>
5. Now we need to visualize the data by coloring the data according to the routes. We add the route field into colors to perform this.<br>![rt](https://github.com/user-attachments/assets/7b979a4a-bbec-4e96-87d4-838d64a7af96)<br>
6.	Next, we need to perform the same steps to the dataset of the year 2023.
7.	When we are processing the dataset for year 2023, drag the ‘Month’ field into ‘Filers box’ and then select ‘Month’. Then select only January to June from the checkbox. Because we have data from Jan to June for 2022.<br>
![x1](https://github.com/user-attachments/assets/b51bd0dc-0706-42db-bb2e-adf333d6a7cb)



 <!--- ************************************************   Criteria 2 ************************************************************************************************************ --->
 <hr width="100%" size="2">
<strong><h2>Criteria 2: Number of delay incidents in each Route (column: Route, Row: count).</h2></strong><br>
![delay vs route](https://github.com/user-attachments/assets/60597cbe-8278-4b29-a35c-f54325a392b2) <br>

<strong><ins>Data preparation:</ins></strong><br>
Steps followed to prepare the data fields.
1.	Right click on field ‘Route’.
2.	Select ‘Convert to Dimension’.<br>
![b1](https://github.com/user-attachments/assets/1874bc84-c3c4-452a-a27e-fa92af4023fe)<br>
3.	Drag the ‘Route’ field into Columns and Count variables(ttc-bus-delay-data-2022.csv) into Rows.<br>![b4](https://github.com/user-attachments/assets/473c2886-e34a-4168-8fe0-a582b69b781a)<br>
4.	When you arrange the data, you can see that there is a ‘Null’ field at the beginning of the list of columns. This occurs because the ‘Route’ was not entered for some records when recording the data. These records are as bad data. Because there is no way that we can identify what are the data that should be entered to the missing ‘Route’ field. Therefore, these records must be removed from the data set, or it would not be useful in the process.<br>![b5](https://github.com/user-attachments/assets/da2ee95c-28d2-467f-b067-294a2a5aa72e)<br>
5.	We can remove the null values, by adding ‘Route’ into Filters box. Then uncheck the ‘Null’. Then the ‘Null’ values will be removed from the data representation.<br> ![b6](https://github.com/user-attachments/assets/8c8fc386-c3c8-4fa1-9df7-48b0d7a83b3e)<br>
6.	Then we will get a fine dataset without NULL values for the Route criteria.<br>
![b7](https://github.com/user-attachments/assets/6ed62899-ba98-4d2a-808b-3dd3e0cf1ddf)<br>
7. Then we need to add colors to the data based on the 'Direction'. Drag the 'Direction' field into color box.
8.	Now we need to perform the same steps to the dataset of the year 2023.
9.	For the year 2023 dataset, drag the ‘Month’ field into ‘Filers box’ and then select ‘Month’. Then select only January to June from the checkbox. Because we have data from Jan to June for 2022.<br>
![x1](https://github.com/user-attachments/assets/b51bd0dc-0706-42db-bb2e-adf333d6a7cb)

<!--- ***********************************************   Criteria 3 ************************************************************************************************************* --->
<strong><h2>Criteria 3: Number of delay incidents according to Time(column: Time, Row: count).</h2></strong><br>
![image](https://github.com/user-attachments/assets/125cb98e-c434-423f-8577-0937502170b1) <br>

<strong><ins>Data preparation:</ins></strong><br>
Steps followed to prepare the data fields.
1.	Right click on field ‘Route’.
2.	Select ‘Convert to Dimension’.<br>
![b1](https://github.com/user-attachments/assets/1874bc84-c3c4-452a-a27e-fa92af4023fe)<br>
3.	Drag the ‘Time’ field into Columns and Count variables(ttc-bus-delay-data-2022.csv) into Rows.<br>
4. Double click on the 'Time' field and write the code as "DATEPART('hour', [Time])" to extract only the hour part from the 'Time'.<br>
5. Drag the 'Route' field into 'Filters' section to remove the records that has 'Null' values and routes other than 32 and 36.<br>
![image](https://github.com/user-attachments/assets/94ec539b-bcde-4074-bed0-72deec92e5b6) <br>
6. Now we need to visualize the data by coloring the data according to the routes. We add the route field into colors to perform this.<br>![rt](https://github.com/user-attachments/assets/7b979a4a-bbec-4e96-87d4-838d64a7af96)<br>
7. Now we need to perform the same steps to the dataset of the year 2023.<br>
8. For the year 2023 dataset, drag the ‘Month’ field into ‘Filers box’ and then select ‘Month’. Then select only January to June from the checkbox. Because we have data from Jan to June for 2022.<br>
![x1](https://github.com/user-attachments/assets/b51bd0dc-0706-42db-bb2e-adf333d6a7cb)
