# Fitness Analytics Dashboard 🏋️‍♂️📊

A **comprehensive fitness analytics dashboard** to track, visualize, and analyze gym members' data for better insights into workouts, calories, and health metrics. Built for professional analytics and interactive reporting.

---

## 🎯 Dataset Overview

The dashboard uses the following columns from the dataset `gym_members_exe`:

| Column Name | Description |
|-------------|-------------|
| Age | Member's age |
| Avg_BPM | Average heart rate during workout |
| BMI | Body Mass Index |
| Calories_Burned | Calories burned during sessions |
| Experience_Level | Beginner, Intermediate, Advanced |
| Fat_Percentage | Body fat percentage |
| Gender | Male / Female |
| Height | Member height in cm |
| Max_BPM | Maximum heart rate recorded |
| Resting_BPM | Resting heart rate |
| Session_Duration | Workout session duration (minutes) |
| Water_Intake | Daily water intake |
| Weight | Member weight in kg |
| Workout_Frequency | Number of workout sessions per week |
| Workout_Type | Type of workout (Cardio, Strength, etc.) |

> This dataset is perfect for building a **fitness analytics dashboard**.

---

## 🚀 STEP 1: Important Measures (DAX)

Create **New Measures** in Power BI under `Modeling → New Measure`:

```DAX
-- Total Calories Burned
TotalCalories = SUM('gym_members_exe'[Calories_Burned])

-- Average BMI
AvgBMI = AVERAGE('gym_members_exe'[BMI])

-- Average Session Duration
AvgSession = AVERAGE('gym_members_exe'[Session_Duration])

-- Average Heart Rate
AvgHeartRate = AVERAGE('gym_members_exe'[Avg_BPM])

-- Total Members
TotalMembers = COUNTROWS('gym_members_exe')

-- High Intensity Members (Optional Advanced Measure)
HighIntensity = 
CALCULATE(
    COUNTROWS('gym_members_exe'),
    'gym_members_exe'[Avg_BPM] > 150
)📊 STEP 2: Dashboard Layout
1️⃣ Top Section: KPI Cards

Add 5 card visuals:

Total Members

Total Calories Burned

Average BMI

Average Session Duration

Average Heart Rate

Use large fonts and bold visuals for a professional appearance.

2️⃣ Middle Section: Charts
Chart	Type	Axis	Values
Calories by Workout Type	Bar Chart	Workout_Type	SUM(Calories_Burned)
Gender Distribution	Pie Chart	Gender	COUNTROWS
Experience Level vs Calories	Column Chart	Experience_Level	SUM(Calories_Burned)
BMI vs Fat Percentage	Scatter Plot	BMI	Fat_Percentage
3️⃣ Bottom Section: Workout Frequency

Chart Type: Column / Histogram

Axis: Workout_Frequency

Values: COUNTROWS

4️⃣ Slicers (Interactive Filters)

Gender

Workout_Type

Experience_Level

Makes the dashboard interactive and dynamic.

🎨 STEP 3: Professional Touch

Add Dashboard Title

Include Gym Logo (demo placeholder)

Show Last Updated Date

Maintain proper alignment and spacing

Use white background with blue + green highlights for a clean, professional look

💡 STEP 4: Advanced Insights (Optional)

Highlight High Intensity Members using Avg_BPM > 150

Apply conditional formatting to key charts

Use tooltips to show additional metrics (Calories/Session, Avg BPM, BMI, Fat Percentage)

Create advanced DAX measures for deeper analytics

⚡ Technologies Used

Power BI – Interactive data visualization

DAX – For calculations and measures

Slicers & Filters – Interactive filtering

Professional Layout & Theme – White background, blue & green highlights

📁 Project Structure
Fitness-Dashboard/
│
├── dataset/
│   └── gym_members_exe.csv
├── README.md
└── PowerBI_Dashboard.pbix
📌 Extra Notes

Ensure your dataset is clean before importing to Power BI

Maintain consistent colors and fonts for a professional appearance

Always include last updated date for clarity

KPI cards should be easy to read and properly aligned at the top

Created with ❤️ for Gym Analytics & Fitness Insights


---

✅ This professional version includes:  
- Dataset details  
- Step-by-step **DAX measures**  
- **Dashboard layout** with KPI cards, charts, and bottom section  
- Interactive **slicers**  
- **Professional touches** (title, logo, theme, spacing)  
- **Advanced analytics insights**  
- Technologies used & project structure  
- Extra notes for maintaining clarity  

---

If you want, I can **also create an enhanced version with demo images, badges, and a GIF of the dashboard** embedded so your GitHub repo looks **super professional and interactive**.  

Do you want me to create that next?
