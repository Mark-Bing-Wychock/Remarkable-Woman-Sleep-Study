# A Remarkable Woman's Sleep Journey: A Data-Driven Sleep Study

## 💡 Project Inspiration:

This project addresses a profoundly personal challenge: understanding and improving my wife's chronic sleep issues. She often struggles with restless nights, difficulty falling asleep, and persistent fatigue.  After a serious incident in 2024, we realized that we needed to take this issue seriously.

Realizing the potential of deriving insights from personal data, I leveraged my expertise as a Data Analyst to initiate a comprehensive sleep study. This dashboard provides an ongoing, data-driven investigation into the sleep patterns and behaviors of a remarkable woman, seeking to uncover the factors influencing her rest and well-being.

## 📊 Data:

* The sleep data is collected periodically from Google Forms and the ZEPP app and subsequently stored on Google Sheets. This data is then cleaned, processed, transformed, and linked to a live Looker Studio dashboard.

### <ins>Live Dashboard:</ins>
[**👉 A Remarkable Woman's Sleep Journey 👈**](https://lookerstudio.google.com/reporting/5f8bfcfc-974b-4822-8266-00d644420626)

### <ins>Public Datasource:</ins>
[**👉 A Remarkable Woman's Sleep Journey - Datasource 👈**](https://docs.google.com/spreadsheets/d/e/2PACX-1vS6gN98eHvDLC6i1_laAvDrDJ6KsUmXoXPUVnLCZkb_1FTspnAVVESdxZiG6wdFskac5W9ErIy76Kge/pub?output=csv)

The data is organized into two primary tabs/sheets within this public Google Sheet:
* **`Dashboard Data`**: The main dataset containing all available features used in the dashboard.
* **`Flattened Dashboard Data`**: A transformed version of the main data, specifically structured to enable certain advanced visualizations in Looker Studio.

A static snapshot of the raw data used for this project's last major update is also available in this repository: 
* [remarkable_woman_dashboard_data.csv](https://github.com/Mark-Bing-Wychock/Remarkable-Woman-Sleep-Study/blob/main/remarkable_woman_dashboard_data.csv)
* [remarkable_woman_flattened_dashboard_data.csv](https://github.com/Mark-Bing-Wychock/Remarkable-Woman-Sleep-Study/blob/main/remarkable_woman_flattened_dashboard_data.csv)

### **<ins>Data Schema:</ins>**
**Dashboard Data:**
1. `Date` - In MM/DD/YYYY format.
2. `Day of Week (Numeric)` - Numeric day of the week starting at 1 = Sunday.
3. `Day of the Week` - String day of the week.
4. `Bedtime (Night of Date)` - Bedtime that corresponds with the date of recording in HH:MM:SS AM/PM format.
5. `Rise Time (Morning After Date-Night)` - Wake-up time of the following night in HH:MM:SS AM/PM format.
6. `Sleep Duration`	- Duration of sleep in HH:MM:SS format.
7. `Sleep Duration (Seconds)`	- Duration of sleep in numeric seconds.
8. `Stimulants`	- Type of stimulant consumed in the morning (Coffee, Tea, Decaf, None).
9. `Amount of Liquid (mL)` - Amount of stimulants consumed.	
10. `Rested (corrected)` - Binary (Yes/No) sleep quality metric.  Collected on wake-up of the following day, but recorded on the date of the Bedtime. 
11. `Before Sleep Mood (Happy, Sad, Anxious, Agitated, Content, Calm)` - Generalized mood before going to sleep.
12. `Microsleep (5p-9p)` - Binary measure of whether a short sleep occurred, but not long enough to count as a nap and in the evening hours.
13. `Nap Occurred`	- Binary (Yes/No) measure of whether a nap occurred during the day.
14. `Nap Start`	- Start time of nap in HH:MM:SS AM/PM format.
15. `Nap Wake-Up`	- End time of nap in HH:MM:SS AM/PM format.
16. `Nap Duration`	- Duration of nap in HH:MM:SS.
17. `Sleep Duration + Nap Duration`	- Duration of sleep plus the duration of the nap in HH:MM:SS.
18. `Sleep Duration + Nap Duration (Sec)`	- Duration of sleep plus the duration of the nap converted to numeric seconds.
19. `Did I Wake Up?` - Binary (Yes/No) measure of whether	a wake-up occurred in the middle of a sleep cycle (between Bedtime and Rise Time).  Only counted once if there are multiple wake-ups.
20. `Wake-up Time`	- Time wake-up (or longest wake-up if multiple instances) occurred in HH:MM:SS AM/PM.
21. `Fall Back Asleep Time`	- Time when sleep resumed in HH:MM:SS AM/PM format.
22. `Wake-up Duration`	- Duration of the interruption in sleep in HH:MM:SS.
23. `Wake-up Duration (Sec)`	- Duration of the interruption in sleep converted to numeric seconds.
24. `Sleep Duration - Wake-up Duration` - Duration of sleep minus the duration of the wake-up in HH:MM:SS.
25. `Sleep Duration - Wake-up Duration (sec)`	- Duration of sleep minus the duration of the wake-up converted to numeric seconds.
26. `Steps` - Numeric number of steps walked during the day.
27. `True Sleep` - Duration of sleep plus the nap duration minus the wake-up duration in HH:MM:SS.
28. `True Sleep (sec)` - Duration of sleep plus the duration of the nap minus the wake-up duration in numeric seconds.

**Flattened Data:**
1. `Date` - In MM/DD/YYYY format.
2. `Week_Numeric` - Numeric day of the week starting at 1 = Sunday.
3. `Week_String` - String day of the week.
4. `Sleep_Metric_Type` - Type of sleep metric (Sleep Duration, Sleep Duration + Naps, Sleep Duration - Wake-ups, True Sleep (Sleep Duration + Naps - Wake-ups)).
5. `Value_in_Seconds` - Duration of sleep metric in seconds.
6. `Rested` - Binary (Yes/No) metric determining sleep quality. 
                          				
## 🚀 **Future Plans:**

**<ins>In Progress:</ins>**
* (50% Completion) - Feature engineer bedtime variables and create new visualizations for the dashboard to compare with rested vs. not rested variables.
* (40% Completion) - Develop and deploy decision tree-based machine learning models (MLM) with Python to discover additional insights.

**<ins>Planned:</ins>**
* Transform and feature engineer continuous data into categorical and use Apriori Algorithms via Python to discover insights between different variables.
* Link MLM results to the live dashboard and have it auto-update when new data is periodically added.
* Utilize APIs to automatically update static dashboard .csv files.

## 📞 **Contact:**
Have questions or want to connect? Feel free to reach out!

* **LinkedIn:** [linkedin.com/in/markbingwychock](https://www.linkedin.com/in/markbingwychock/)
* **Email:** mark.bing.wychock@gmail.com

