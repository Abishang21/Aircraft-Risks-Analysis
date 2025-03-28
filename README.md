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


The Python scripts used to inspect and clean the data for this analysis can be found here: [Python Cleaning Scripts](https://github.com/Abishang21/Projects/blob/master/Aviation_data%20Notebook.ipynb)

Targeted Python scripts used to answer specific business questions can be found here:[Python Analysis Scripts](https://github.com/Abishang21/Projects/blob/master/Aviation_data%20Notebook.ipynb)

The interactive Tableau dashboard used to report and explore accident trends can be found here: [Tableau Dashboard](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-a69909ee5a0494881b51f8eb86ec9b623c0ea89f4087b15ad66b17d65e35faa6)




**Data Structure & Initial Checks**

The dataset analyzed comes from the NTSB Aviation Accident Database  which contains records of civil aviation accidents and selected incidents within the United States and international waters from 1962 to 2023.The database consists of two tables as follows:

- Aviation Data Table contains 88,889 records with 31 key columns providing detailed information on aircraft accidents.


- US States Abbreviations Table contains 63 records mapping state names to their abbreviations.


The dataset underwent several cleaning and transformation steps using Python (Pandas, Matplotlib, and Seaborn) before being exported to Tableau for visualization.

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


![Snapshot of dashboard](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-a69909ee5a0494881b51f8eb86ec9b623c0ea89f4087b15ad66b17d65e35faa6)




**Insights Deep Dive**

**Aircraft Accident risk assessmentTrends**

- Cessna, Piper, and Beech aircraft have the highest number of accidents 

- Abernathy, 777, and Robert John planes have much fewer accidents.

- The most accident-prone aircraft models include Cessna 152 ,172 and 172N.




![Visualization: Aircraft accident rates by make](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-129e085644279f2f7bb1ef8edf17ab60a8291a86f1bfd1953d162b30e008641f)
![Visualization: Aircraft accident rates by model](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-20dc9543a5d3d0eac5433200946342929c9e084f6fb00e24609c30a79d600ee6)

**Aircraft Accident Trends**

- Cessna and Piper aircraft have the highest number of accidents over the years, with Cessna leading significantly

- The number of accidents has gone down over the years.

- 67 flying dutchman,a.h gettings,abc, Abernathy,777 and few others have remained to be the safest aircrafts over the years.


![Visualization: Accident prone Aircraft rates by Years](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-063c4710878b775a229ffc40912a4b8cd13c7ac9859567d7a857c9e46ba5071a)
![Visualization: safest Aircraft  by Years](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-676bd2c6c128633c7c2431bbf370bd70b6674fd13c9b634436caa498d1bac4e1)


**Phase of Flight Risk Analysis**

- Most accidents happen during landing (21,470 accidents) and takeoff (5,259 accidents).

- The least number of accidents occur in the "Unknown" and "Other" flight phases.


![Visualization: Accidents per phase of flight](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-b5766027b604f63bdb4798c0afaed7c31f2478e6787f2c6bc9c758f24ad239ac)



**Weather Condition Impact**

- Aircrafts like Cesna,Piper, Bell and  Beech experience higher accident rates under poor weather conditions.

- Most accidents happen in clear weather (VMC - Visual Meteorological Conditions) rather than bad weather (IMC - Instrument Meteorological Conditions).


![Visualization: Weather impact on aircraft accidents](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-6c4b4343d02ee01034d34bd809f6d2569b5d48fc2bcf5931851730aabbaecc0c)



**Passenger & Damage Analysis**

- Cesna and Piper aircraft recorded the highest number of uninjured passengers after accidents.

- Piper and Bell aircraft sustain the most damage in crashes.

- Cessna has the highest number of accidents but also a strong safety record.

- Boeing has a moderate number of accidents with a good number of uninjured passengers.


![Visualization: Passengers metrics](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-05d3f5ce7f60aacda0f49bc80be9ac5b2fff910611da25e480ed405300224f3a)

![Visualization: Aircraft accident rates by damagel](https://github.com/Abishang21/Projects/commit/ca8babeebdf3e09778374750a5882b2b0ed05b33#diff-6d649eada555cfc55af8b2e9ccb3c2098d3512b359adc80b626b24e1886e3cb2)





**Recommendations**


Based on the insights above the leadership team should consider the following actions:

1.  Train pilots better by using flight simulators to help them practice flying in different weather conditions and avoid mistakes.

2.  Choose safer planes by using aircraft models with fewer accidents, like Abernathy and Robert John for high risk operations.

3. Consider investing in aircraft models with lower accident rates and higher safety records  as identified in the bottom 10 list.

4. Pick planes with good safety features by using aircraft that protect passengers better in case of an accident.

5. Improve landing  safety by adding better landing technology and giving pilots extra training to prevent landing accidents.

6. Improve takeoff safety by upgrading aircraft systems and providing pilots with additional training to handle takeoff challenges.






