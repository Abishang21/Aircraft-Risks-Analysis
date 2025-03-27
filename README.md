**#Aviation Accident Risk Analysis**


**##Project Background**

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


The Python scripts used to inspect and clean the data for this analysis can be found here: [Python Cleaning Scripts]

Targeted Python scripts used to answer specific business questions can be found here:[Python Analysis Scripts]

The interactive Tableau dashboard used to report and explore accident trends can be found here: [Tableau Dashboard]


**#Data Structure & Initial Checks**

The dataset analyzed comes from the NTSB Aviation Accident Database  which contains records of civil aviation accidents and selected incidents within the United States and international waters from 1962 to 2023.The database consists of two tables as follows:

- Aviation Data Table contains 88,889 records with 31 key columns providing detailed information on aircraft accidents.


- US States Abbreviations Table contains 63 records mapping state names to their abbreviations.


The dataset underwent several cleaning and transformation steps using Python (Pandas, Matplotlib, and Seaborn) before being exported to Tableau for visualization.

1. Copied the dataset to preserve the original file.

2. Handled missing values:

    - For numerical columns: If mean > median, filled with median; if median > mean, filled with median; if equal, filled with mean.

    - For categorical columns: Replaced null values with the most frequent value.

3. Checked for duplicates and found none.

4. Converted date columns from string to datetime format.

5. Identified and removed outliers using the IQR method and boxplots.

6. Dropped non-informative columns (e.g., those with only one unique value) to streamline analysis.

6. Standardized text values by converting the Make column to lowercase for consistency.


**#Executive Summary**

**##Overview of Findings**

1.Certain aircraft makes and models have significantly lower accident rates making them safer options for purchase.

2. Human error and weather conditions are major contributing factors to aviation accidents.

3. The number of aviation accidents has decreased over time .


[Snapshot of dashboard]


**#Insights Deep Dive**

**Aircraft Accident Trends**

- Cessna, Piper, and Beech aircraft account for the highest number of accidents 

- Abernathy ,777 and Robert John makes report significantly lower accident rates.

- The most accident-prone aircraft models include Cessna 152 ,172 and 172N.

- There has been reduced number of accidents over the years


[Visualization: Aircraft accident rates by make/model]

[Visualization: Aircraft accident rates by Years]

**#Phase of Flight Risk Analysis**

- Landing (21,470 accidents) and Takeoff (5259 accidents) pose the highest risks.

- Unknown and Others have the lowest accident occurrences.

- Insights suggest a need for more training during Landing and takeoff 


[Visualization: Accidents per phase of flight]


**Weather Condition Impact**

- Aircrafts like Cesna,Piper, Bell and  Beech experience higher accident rates under poor weather conditions.

- VMC((Visual Meteorological Conditions) conditions contribute to more severe accidents compared to IMC(Instrument Meteorological Conditions).


[Visualization: Weather impact on aircraft accidents]


**Passenger Safety & Damage Analysis**

- Cesna and Piper aircraft recorded the highest number of uninjured passengers

- Piper and Bell sustain severe damage has they have the highest accident damage counts.


[Visualization: Passenger safety metrics]

[Visualization: Aircraft accident rates by damagel]


**Recommendations**


Based on the insights above the leadership team should consider the following actions:

1.  Improve pilot training by using simulations to help them handle different weather conditions and reduce human errors. This will increase their awareness and preparedness for any situation.

2.  Encourage adoption of safer aircraft models, such as Abernathy and Robert John, in high-risk operations.

3. Consider investing in aircraft models with lower accident rates and higher safety records, as identified in the bottom 10 list.

4. Prioritize aircraft makes with a high percentage of uninjured passengers in accidents, indicating better safety features.

5. Focus on improving safety measures particularly during the landing phase such as advanced landing assistance systems and pilot training programs.







