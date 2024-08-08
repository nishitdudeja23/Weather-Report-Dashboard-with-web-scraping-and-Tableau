## Data Collection Technique
Beautiful Soup:
We employed the Beautiful Soup library, a powerful Python library for web scraping the website: ‘https://ihtiman-meteo.com/wxhistory.php’, to collect weather data for our analysis. Beautiful Soup facilitates the parsing of HTML and XML documents, making it a valuable tool for extracting information from websites. By utilizing Beautiful Soup in conjunction with Python requests, we were able to navigate through the structure of weather websites, locate relevant data, and extract it for further analysis.


## Data Description
The dataset contains 1844 rows and 20 columns covering a wide range of weather-determining factors of the last 5 years of Ihtiman.

1.	Date: The timestamp indicates when the weather data was recorded.

2.	Average Temperature: The mean ambient air temperature over the specified time period, measured in degrees Celsius or Fahrenheit.

3.	Average Humidity: The average percentage of water vapor in the air during the specified time period.

4.	Average Dewpoint: The average temperature to which air must be cooled for saturation, leading to the formation of dew, measured in degrees Celsius or Fahrenheit.

5.	Average Barometer: The mean atmospheric pressure during the specified time period, often measured in inches of mercury (inHg) or hectopascals (hPa).

6.	Average Windspeed: The mean speed of the wind during the specified time period, typically measured in kilometers per hour (km/h) or miles per hour (mph).

7.	Average Gustspeed: The mean speed of wind gusts, which are rapid increases in wind speed during the specified time period.

8.	Average Direction: The average direction from which the wind is blowing, usually expressed in degrees.

9.	Rainfall for Month: The total amount of rainfall during the current month, measured in millimeters or inches.

10.	Rainfall for Year: The cumulative rainfall for the current year up to the recorded date, measured in millimeters or inches.

11.	Maximum Rain per Minute: The highest recorded rate of rainfall within a single minute, measured in millimeters or inches.
 
12.	Maximum Temperature: The highest recorded air temperature during the specified time period, measured in degrees Celsius or Fahrenheit.

13.	Minimum Temperature: The lowest recorded air temperature during the specified time period, measured in degrees Celsius or Fahrenheit.

14.	Maximum Humidity: The highest percentage of water vapor in the air during the specified time period.

15.	Minimum Humidity: The lowest percentage of water vapor in the air during the specified time period.

16.	Maximum Pressure: The highest atmospheric pressure recorded during the specified time period, often measured in inches of mercury (inHg) or hectopascals (hPa).

17.	Minimum Pressure: The lowest atmospheric pressure recorded during the specified time period, often measured in inches of mercury (inHg) or hectopascals (hPa).

18.	Maximum Windspeed: The highest recorded wind speed during the specified time period, typically measured in kilometers per hour (km/h) or miles per hour (mph).

19.	Maximum Gust Speed: The highest recorded wind gust speed during the specified time period.

20.	Maximum Heat Index: The highest calculated heat index, which combines air temperature and humidity to represent the perceived temperature.

## DATASET SCRAPED 

![image](https://github.com/user-attachments/assets/06464d58-7bc5-48a3-b7bb-36669ed12a11)

## PREPROCESSING TECHNIQUES 
PREPROCESSING TECHINQUES DEPLOYED

1.	Date Formatting:
-	Converted the 'Date' column to a datetime format using `pd.to_datetime`.

2.	Numeric Column Conversion:
-	Converted selected columns representing numeric data to numeric format.
-	Used regular expressions (`re`) and `pd.to_numeric` to handle non-numeric characters.

3.	Handling Missing Values:
-	Filled missing values in the DataFrame with the mean of their respective columns using
`fillna`.

4.	Z-Score Filtering:
-	Computed Z-scores for numeric columns using `scipy.stats.zscore`.
 
-	Filtered out rows where the absolute Z-scores for all numeric columns were less than 3, indicating outliers.

5.	Additional Rain Data Processing:
-	Extracted numerical values and time information from the 'Maximum rain per minute' column.
-	Created new columns 'Max Rain Minute' and 'Max Rain Time'.
-	Dropped the original 'Maximum rain per minute' column.

These preprocessing techniques aim to clean and prepare the raw weather data for further analysis by handling date formats, converting data types, addressing missing values, and identifying and filtering out potential outliers. The code demonstrates a comprehensive approach to cleaning and organizing the data for subsequent analysis or modelling.
## PREPROCESSED DATASET
![image](https://github.com/user-attachments/assets/83a1ed37-ee1b-47a9-bace-f3fbc243a5b0)

# TABLEAU DASHBOARD
![image](https://github.com/user-attachments/assets/825fb7c5-fd6b-4208-b56f-b7f1881e31ad)

# FORMS OF DASHBOARD 

![image](https://github.com/user-attachments/assets/c818f4a1-4c1a-46dc-9d92-aacb9553c782)
 
![image](https://github.com/user-attachments/assets/d0c7f820-703d-454d-a9cf-37d925f240c1)


![image](https://github.com/user-attachments/assets/5a05a35a-da19-42d8-957f-c103009ec9b6)

# LINK TO DASHBOARD 
https://public.tableau.com/views/WeatherAnalysis_17231306924690/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link


