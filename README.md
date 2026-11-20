# Bellabeat Case Study: Activity, Sedentary Time & Sleep Patterns

## Project Links & Deliverables
* **Full Analysis Report (Google Doc):** [Bellabeat Case Study - Analysis Report](https://docs.google.com/document/d/1IcYpZHLALhgdnSn3PaQAjSBy5Jkhu1lDwTbtAn85g4A/edit?usp=sharing)
* **Interactive Dashboard (Tableau Public):** [Bellabeat Case Study Dashboard on Tableau Public](https://public.tableau.com:9443/views/BeallabeatXaseStudyActivitySedentaryTimeSleepPatterns/BellabeatCaseStudyActivitySedentaryTimeSleepPatterns?:language=fr-FR&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
* **Kaggle Notebook (`bellabeat-case-study`):** [Bellabeat Case Study Notebook on Kaggle](https://www.kaggle.com/code/roselinee/bellabeat-case-study)
* **Kaggle Writeup:** [Bellabeat Case Study Writeup on Kaggle](https://kaggle.com/writeups/roselinee/bellabeat-case-study-activity-sedentary-time-and-s)

## Overview
This repository presents the **Bellabeat** case study following the six-phase data analysis process (**Ask, Prepare, Process, Analyze, Share, Act**) using public **FitBit Fitness Tracker Data** (`Fitabase Data 4.12.16-5.12.16`, covering 31 days from April 12 to May 12, 2016) under a CC0: Public Domain license[cite: 1, 5]. Insights are focused on the **Bellabeat app** and **Bellabeat membership**[cite: 1, 5].

## Data Preparation & Key Findings
* **Data Cleaning (Python / Pandas & NumPy):** Audited five core CSV tables from the second export (`dailyActivity_merged.csv`, `sleepDay_merged.csv`, `hourlySteps_merged.csv`, `hourlyIntensities_merged.csv`, and `weightLogInfo_merged.csv`), standardized timestamps, removed **3 duplicate rows** from `sleep_day` (`413` to `410` clean rows), documented missingness (`65` missing `Fat` entries out of `67` weight logs and `77` zero-step days in `daily_activity`), engineered helper columns (`DayOfWeek`, `Hour`, `TotalActiveMinutes`, `TotalHoursAsleep`, `SleepEfficiency`), merged hourly steps and intensities into `hourly_activity_clean`, and exported clean CSVs (`hourly_summary_export.csv`, `activity_sleep_merged.csv`, `daily_activity_clean.csv`, `sleep_day_clean.csv`, `user_summary_export.csv`)[cite: 1, 5].
* **Daily Activity & Sedentary Time:** Across `940` daily records (`33` users), average daily steps were **7,637.91** (over `78%` of users averaged below `10,000` steps/day) alongside **991.21 sedentary minutes** (`16.52` hours/day)[cite: 1, 5].
* **Sleep & Sedentary Correlation:** Across `410` clean sleep records (`24` users), average sleep duration was **6.99 hours** (`419.17` minutes) with a strong negative correlation between sedentary minutes and total minutes asleep (`r = -0.601`)[cite: 1, 5].
* **Weekly & Hourly Rhythms:** Daily steps peaked on **Saturday** (`8,152.98`) and **Tuesday** (`8,125.01`), whereas **Sunday** showed the lowest average steps (`6,933.23`) and longest sleep (`452.75` minutes / `7.55` hours)[cite: 1, 5]. Hourly activity peaked between **17:00 and 19:00**, reaching its highest average at **18:00** (`599.17` steps)[cite: 1, 5].
* **Manual Logging Gap:** Only `8` users logged weight (`67` entries), showing low adoption for manual weight entry[cite: 1, 5].

## Core Recommendations (Bellabeat App & Membership)
1. **Late-Afternoon Movement & Evening Wind-Down Nudges:** Prompt movement during the `17:00–19:00` window (peaking around `18:00`) and offer sedentary break reminders linked to sleep duration (`r = -0.601`), paired with guided wind-down routines in the membership[cite: 1, 5].
2. **Weekly Rhythm & Sunday Reset:** Support high-activity days (**Tuesday** and **Saturday**) with realistic milestones while positioning **Sunday** for recovery and weekly planning[cite: 1, 5].
3. **Low-Friction Tracking:** Prioritize automatic sync and quick check-ins over manual logs like weight entry[cite: 1, 5].
