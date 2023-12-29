# Exploratory Data Analysis (EDA) - Body Metrics (weight and bioimpedance)
Whatever your purpose in practicing a workout in a base routine, the body metrics such as weight and electric bioimpedance are the most used. In the group of people who have the objective of weight loss. So, those kinds of metric ideas and suggestions to reorganize are very helpful to organize training in terms of intensity and frequency.

Those metrics are also important for people who train for races and or at an advanced level looking at performance, for instance. Typically, athletes combine body metrics with other measurements grabbed during their training, such as HR (heart rate), speed, cadence, power, and others. From that perspective, the training programs are adjusted and well-focused on performance, endurance, and split.

Let's propose the scenario for those with weight loss as the main purpose of tracking their body metrics as soon as they get out of bed every morning. It looks like I used to do it. Naturally, the body weight goes up and down by up to 1kg between daily measurements. It seems to be a sort of reflection about their routine, such as training intensity that typically might swell their legs, or dehydration that occasionally we use to drink water below recommended or even maintain a dietary based on low fat and carbohydrate, but one or other day we could have been eaten something sneaked.
![image](https://github.com/embordin/WorkoutAndBodyMetrics/assets/103783579/d64387ea-a046-4767-8e9a-9e501e17bfdb)

The current exploratory data analysis (EDA) aims to bring insights and ideas to analyze body metrics obtained from a bioimpedance scale. 

Database:
For that purpose, a dataset of almost one year of body bioimpedance (fat, water, muscle, and bone) and weight was tracked in the morning before breakfast. The scale is a Garmin Scale S2
For the execution of EDA: Python (Google Colab); packages: Pandas (data manipulation); Plottly (data visualization) and Statsmodels (correlation and linear regression).

Results:
Body Fat % is usually the most important metric for those who want weight loss. The idea behind this is to decrease body weight by reducing body fat preferentially rather than body skeletal muscle. Based on that, body fat would be more relevant to track than weight loss itself.

The problem is that the electrical bioimpedance scale is typically inaccurate. Sometimes, it gives numbers that would show us as worse than pork bacon in terms of fat content. Specifically, in the case of the Garmin S2 scale, there is a possibility of minimizing such errors by manually adding reference data for body fat and weight. Both measures will make a sort of correction. Graphic 1 below shows when the correction was applied.
![image](https://github.com/embordin/WorkoutAndBodyMetrics/assets/103783579/63b8a88e-8048-4ceb-83a8-80e9c187936e)

Graph 2 also suggests that body fat and water might have a correlation. It applied a filter to the database selection metrics after the fat correction. Graph 3 shows the results below.
![image](https://github.com/embordin/WorkoutAndBodyMetrics/assets/103783579/bd7c3673-3835-4754-b078-2619c7c02078)
![image](https://github.com/embordin/WorkoutAndBodyMetrics/assets/103783579/7b557a7d-acc1-408f-8fff-8defa51dcf6f)



In Graph 1, Body Water (%) seems to mix up with fat. It would be the source of the error that almost all bioimpedance scale algorithms can’t properly sort out what fat and water are. Such an issue is related to the principle of function behind those kinds of measurement scales. In a simple way, bioimpedance analysis measures body composition based on the rate at which an electrical current passes through the body, in which fat tissue causes greater resistance – impedance – than muscles or lean tissue. In that way, the scale estimates the body composition.
