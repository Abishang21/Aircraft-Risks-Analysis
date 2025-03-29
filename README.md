**Aircraft Risk and Safety Analysis**



**Project Background**

Our company is expanding into the aviation industry and plans to purchase aircraft for commercial and private use. To support informed decision-making by the leadership team, this project aims at analyzing aircraft accident data to identify safety risks, vulnerable aircraft makes and models and accident-prone flight phases.


**The key business metrics considered include:**

- Number of accidents per aircraft make and model

- Phases of flight with the highest accident occurrences

- Weather conditions impacting safety

- Passenger injury and aircraft damage statistics


**Insights and recommendations are provided on the following key areas:**

- Aircraft make and model risk assessment

- Common causes of aviation accidents

- Impact of flight conditions on accident rates

- Trends over time in aviation safety


The Python scripts used to inspect and clean the data for this analysis can be found here: [Python Cleaning Scripts](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Aviation_data%20Notebook.ipynb)

Targeted Python scripts used to answer specific business questions can be found here:[Python Analysis Scripts](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Aviation_data%20Notebook.ipynb)

The interactive Tableau dashboard used to report and explore accident trends can be found here: [Tableau Dashboard](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/Dashboard.jpg)




**Data Structure & Initial Checks**

The dataset analyzed is sourced from the NTSB Aviation Accident Database  which documents civil aviation accidents and selected incidents in the United States and international waters from 1962 to 2023. The data consists of two tables and was downloaded from Kaggle.

[Kaggle Link](https://www.kaggle.com/datasets/khsamaha/aviation-accident-database-synopses)

The two tables  are as follows:

- Aviation Data Table contains 88,889 records with 31 key columns providing detailed information on aircraft accidents.Below are some of the columns;

![Aviation Data Table](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/Screenshot%202025-03-27%20153128.jpg)

- US States Abbreviations Table contains 63 records mapping state names to their abbreviations.

![US States Abbreviations Table](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/Screenshot%202025-03-27%20153158.jpg)

The dataset underwent several cleaning and transformation steps using Python (Pandas) before being exported to Tableau for visualization.

1. Copied the dataset to preserve the original file.

2. Handled missing values:

    - For numerical columns: If mean > median, filled with median; if median > mean, filled with median; if equal, filled with mean.

    - For categorical columns: Replaced null values with the most frequent first value.

3. Checked for duplicates and found none.

4. Converted date columns from string to datetime format.

5. Identified and removed outliers using the IQR method and boxplots.

6. Dropped columns that were not needed for my analysis.

6. Standardized text values by converting the Make column to lowercase for consistency.




**Executive Summary**

**Overview of Findings**

1. Some aircraft models are much safer than others, with fewer accidents.

2. Most accidents happen due to human mistakes and bad weather.

3. Aviation accidents have become less common over the years.


![Snapshot of dashboard](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/Dashboard.jpg)




**Insights Deep Dive**

**Aircraft Accident risk assessmentTrends**

- Cessna, Piper, and Beech aircraft makes have the highest number of accidents 

- Abernathy, 777, and Robert John planes have much fewer accidents.

- The most accident-prone aircraft models include  152 ,172 and 172N.



![Visualization: Aircraft accident rates by make](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/1.jpg)
![Visualization: Aircraft accident rates by model](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/2.jpg)


**Aircraft Accident Trends**

- Cessna and Piper aircraft have the highest number of accidents over the years, with Cessna leading significantly

- Accidents peaked between 1980-2000 but have declined due to improved safety regulations even though certain makes still pose risks.

- 67 flying dutchman,a.h gettings,abc, Abernathy,777 and few others have remained to be the safest aircrafts over the years as they have low number of acidents


![Visualization: Accident prone Aircraft rates by Years](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/3.jpg)
![Visualization: safest Aircraft  by Years](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/4.jpg)


**Phase of Flight Risk Analysis**

- Most accidents happen during landing (21,470 accidents) and takeoff (5,259 accidents).

- The least number of accidents occur in the "Unknown" and "Other" flight phases.


![Visualization: Accidents per phase of flight](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/9.jpg)


**Weather Condition Impact**

- Aircrafts like Cesna,Piper, Bell and  Beech experience higher accident rates under poor weather conditions.

- Surprisingly most accidents happen in clear weather (VMC - Visual Meteorological Conditions) rather than bad weather (IMC - Instrument Meteorological Conditions).

![Visualization: Weather impact on aircraft accidents](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/5.jpg)



**Passenger & Damage Analysis**

-Cessna, Piper, and Beech have the most uninjured passengers but also the highest accidents, indicating their widespread use and increased exposure to incidents.

- Despite many accidents Piper, Cessna, and Beech aircraft have many uninjured passengers, showing that their design and safety features help protect people in crashes.

- The bottom 10 aircraft makes have only 1 recorded accident each showing significantly lower exposure or usage.

- Most accidents fall under substantial damage meaning aircraft were significantly damaged but not destroyed entirely.


![Visualization: Passengers metrics](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/7.jpg)

![Visualization: Aircraft accident rates by damagel](https://github.com/Abishang21/Aircraft-Risks-Analysis/blob/master/Images/6.jpg)




**Recommendations**


Based on the uncovered insights above the leadership team should consider the following actions:

1.  Despite some aircraft makes being widely used, choosing safer models like Abernathy, 777, and Robert John can minimize accidents in high-risk operations, reduce maintenance costs and enhance an airline's reputation.

2. Look to invest in aircraft models with lower accident rates as identified in the bottom 10 list to cut operational costs and lower repair expenses.

3. With many accidents happening in good weather, pilot training should emphasize human factors such as decision-making, fatigue management, and situational awareness to reduce preventable errors.

4. Re-evaluate safety checks and operational protocols in clear weather to prevent overconfidence and maintain consistent safety standards.

5. Push for enhanced pilot simulator training to better prepare pilots for handling accidents caused by bad weather hence improving overall flight safety.

6. Continue investing in advanced weather monitoring systems to provide real-time updates to pilots, improving preparedness and reducing weather-related incidents.

7. With landing accidents being a major concern, upgrading landing technology and providing extra pilot training can improve safety and reduce costly damages.

8. Improve takeoff safety by upgrading aircraft systems and providing pilots with additional training to handle takeoff challenges.

















