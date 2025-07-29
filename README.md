# A Remarkable Woman's Sleep Journey

## **The Idea**
How did you sleep last night?  Did you feel rested when you woke up?  Did you ever wonder why?  These questions are the core of this sleep study.  My wife is a wonderful and amazing woman.  Lively, intelligent, and head strong.  Unfortunately, she's one of many who suffers from a myriad of sleep issues.  Often waking up in the middle of the night, having trouble trouble falling asleep, and not feeling rested when she wakes up.  These issues can often result in chronic fatigue, mood swings, and lack of coordination.  We would often bicker about why she was having sleep issues: (whether it was an too early/too late of a bed time, how much she drank during the day, if she napped, etc.)  It was always treateda as a secondary issue or something you just deal with.  This sentiment changed however after she had a particularily close call where she collapsed from fatigue and nearly hit her head on a kitchen counter after a few consecutive nights of poor sleep; we realized something had to be done.  

We started simple at first by doing some basic research, normal doctors visits, etc., but the more we tried different things the more questions arose.  Worst of all, even after all that research and trying different suggestions, she was still having serious sleep issues.  But then I had epiphany... at the time, I was Data Analyst at meat processing and distribution company while working on my Google Data Analyst Certification.  I realized with my skills acquired from my job and the certificate course, I could perform a sleep study and use that data to find out why she was having issues with her sleep. Hence, I present an ongoing study of sleep patterns and behaviors of a remarkable woman.  

## Data:

* The sleep data is collected periodically through Google Forms and from the ZEPP app and stored on Google Sheets. This data is then cleaned, processed, and transformed and linked to a live Looker Studio dashboard.

## Live Dashboard: 
[**👉 A Remarkable Woman's Sleep Journey 👈**](https://lookerstudio.google.com/reporting/5f8bfcfc-974b-4822-8266-00d644420626)

## Live Datasource: 
[**👉 A Remarkable Woman's Sleep Journey - Datasource 👈**](https://docs.google.com/spreadsheets/d/1yWikevLd1LhvP6sW2UZa3YY1vUg9E9ngGVitZTN9lzg/edit?usp=sharing)

* The data itself is split into 2 different sheets/.csv files:
  1. Dashboard Data - The main datasource containing all available data.
  2. Flattened Dashboard Data - A flattened version of the main datasource that allows certain graphics to be created in Looker Studio.

### **Data Types:**
**Dashboard Data**
1. Date - In MM/DD/YYYY format.
2. Day of Week (Numeric)	- Numeric Day of the Week starting at 1 = Sunday.
3. Day of the Week - String day of the week starting on Sunday.
4. Bed Time (Night of Date) - Bed time that corresponds with date of recording in HH:MM:SS AM/PM format.
5. Rise Time (Morning After Date-Night) - Wakeup time of the following night in HH:MM:SS AM/PM format.
6. Sleep Duration	- Duration of sleep in HH:MM:SS format.
7. Sleep Duration (Seconds)	- Duration of sleep in numeric seconds.
8. Stimulants	- Type of stimulant consumed in the morning. (Coffee, Tea, Decaf, None)
9. Amount of Liquid (mL) - Amount of stimulants consumed.	
10. Rested (corrected) - Binary (Yes/No) sleep quality metric.  Collected on wakeup of following day, but recorded on the date of the actual sleep. 
11. Before Sleep Mood (Happy, Sad, Anxious, Agitated, Content, Calm) - Generalized mood before going to sleep.
12. Microsleep (5p-9p) - Binary measure of whether a short sleep occured, but not long enough to count as a nap and in the evening hours.
13. Nap Occured	- Binary (Yes/No) measure of whether a nap occured during the day.
14. Nap Start	- Start time of nap in HH:MM:SS AM/PM format.
15. Nap Wake Up	- End time of nap in HH:MM:SS AM/PM format.
16. Nap Duration	- Duration of nap in HH:MM:SS.
17. Sleep Duration + Nap Duration	- Duration of sleep plus the duration of the nap in HH:MM:SS.
18. Sleep Duration + Nap Duration (Sec)	- Duration of sleep plus the duration of the nap converted to numeric seconds.
19. Did I wake Up? - Binary (Yes/No) measure of whether	a wakeup occured in the middle of a sleep cycle (between Bedtime and Risetime).  Only counted once if there's multiple wakeups.
20. Wakeup Time	- Time wakeup (or longest wakeup if multiple instances) occured in HH:MM:SS AM/PM.
21. Fall Back Asleep Time	- Time when sleep resumed in HH:MM:SS AM/PM format.
22. Wakeup Duration	- Duration of the interruption in sleep in HH:MM:SS.
23. Wakeup Duration (Sec)	- Duration of the interruption in sleep in numeric seconds.
24. Sleep Duration - Wakeup Duration (sec)	- Duration of sleep minus the duration of the wakeup in HH:MM:SS.
25. Steps - Numeric number of steps walked during the day.
26. True Sleep - Duration of sleep plus the duration of the nap minus the wakeup duration in HH:MM:SS.
27. True Sleep (sec) - Duration of sleep plus the duration of the nap minus the wakeup duration in numeric seconds.

**Flattened Data**
1. Date - In MM/DD/YYYY format.
2. Week_Numeric - Numeric Day of the Week starting at 1 = Sunday.
3. Week_String - String day of the week starting on Sunday.
4. Sleep_Metric_Type - Type of sleep metric.  (Sleep Duration, Sleep Duration + Naps, Sleep Duration - Wakeups, True Sleep (Naps - Wakeups))
5. Value_in_Seconds - Duration of sleep metric in seconds.
6. Rested - Binary (Yes/No) metric determining sleep quality. 
                          				
## 🚀 **Future Plans**

**In Progress:**
* (50% Completion) - Feature engineer bedtime variables and link to visualizations on dashboard to compare with rested vs. not rested variables.
* (40% Completion) - Develop and deploy decision tree based machine learning models (MLM) with Python to discover additional insights.

**Planned**
* Transform and feature engineer continuous data into categorical and use Apriori Algorithms via Python to discover insights between different variables.
* Link MLM model results to live dashboard and have it auto update when new data is periodically added.
* Utilize APIs to automatically update static dashboard .csv files.

## 📞 **Contact**
Have questions or want to connect? Feel free to reach out!

* **LinkedIn:** linkedin.com/in/markbingwychock
* **Email:** mark.bing.wychock@gmail.com


