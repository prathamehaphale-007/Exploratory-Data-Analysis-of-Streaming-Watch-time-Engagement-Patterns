Streaming and Watchtime Engagement Analysis

This repository contains an exploratory data analysis (EDA) of a streaming and watchtime dataset. The goal of this project is to analyze user viewing patterns, content preferences, and platform-specific behaviors to uncover insights into how, where, and when users consume digital content.

This analysis is designed to move beyond high-level averages and identify granular patterns that can inform content strategy, user experience improvements, and marketing decisions.

Project Goals and Key Questions
This analysis seeks to answer several key questions about user engagement:

How does engagement (measured by watch_time_minutes and completion_rate) vary across different streaming platforms, devices, and global locations?

What is the typical user's viewing behavior? Are they binge-watching, or consuming content in shorter sessions?

Which content genres are the most popular, and how does this differ across platforms or regions?

Are there specific high-performance user segments (e.g., specific country/device combinations) that show exceptionally high engagement?

How does total user engagement fluctuate over time on a monthly basis?

What is the relationship between different features like device, location, and genre? Are they independent, or do they influence each other?

The Dataset
The analysis is based on a clean dataset of 5,000 streaming records with no missing values or duplicates.

Platforms: 6 unique (Zee5, Prime Video, Netflix, Hotstar, SonyLiv, YouTube)

Genres: 19 unique (e.g., Horror, Animation, Sci-Fi, Romance)

Devices: 6 unique (Smart TV, Gaming Console, Set-top Box, Mobile, Desktop, Tablet)

Locations: 15 unique (e.g., UK, Brazil, Germany, Australia)

Key Columns: user_id, platform, watch_time_minutes, genre, date, device, location, completion_rate, watch_category (Binge, Long, Medium, Short)

Analytical Steps
Data Cleaning & Preparation: Loaded the dataset, confirmed data integrity (no nulls or duplicates), and converted the date column to datetime objects for time-series analysis.

Descriptive Statistics: Ran a high-level df.describe() to understand the central tendencies and ranges of all features.

Univariate & Bivariate Analysis:

Plotted the distribution of individual features (e.g., watch_time_minutes histogram, platform frequency bar chart).

Analyzed the relationship between completion_rate and watch_time_minutes using a scatter plot.

Multivariate & Segment Analysis:

Used groupby operations to segment users by platform, device, location, and genre, aggregating key metrics (mean, min, max) for both watch_time_minutes and completion_rate.

Visualized market share and engagement share using pie charts for genre, location, and device.

Generated boxplots to compare the distribution of engagement metrics across all platforms.

Correlation & Time Series:

Plotted the total watch time trend by month to identify seasonality.

Created a feature correlation heatmap to check for (and confirm the lack of) multicollinearity between categorical features.

Tools and Libraries
Python

Pandas for data manipulation and aggregation.

Matplotlib & Seaborn for data visualization (bar charts, pie charts, boxplots, histograms, scatter plots, and heatmaps).

Key Findings & Insights
This analysis revealed a platform with exceptionally broad, stable, and consistent user engagement.

A Remarkably Balanced Ecosystem: The analysis showed a fascinating and well-balanced content ecosystem. Total watch time is almost perfectly distributed across all 19 genres, 15 locations, and 6 device types, indicating a broad appeal with no over-reliance on a single category or market.

Highly Sustained & Sticky Engagement: The watch_time_minutes distribution is highly uniform, showing that users are just as likely to engage in short sessions as they are in long, 300-minute binge-watches. This suggests a very "sticky" platform that successfully caters to all viewing intents.

Universal Platform Appeal: All streaming platforms (Netflix, Zee5, etc.) show nearly identical high-engagement profiles, with a high median watch time of ~150 minutes and a strong median completion rate of ~60%. This indicates a healthy, competitive market where all services have cultivated a deeply committed audience.

Feature Independence is a Strength: A key finding is the near-zero correlation between features like device, genre, and location. This is a strategic strength, proving that users are willing to watch any content on any device, maximizing the value of the entire content library.

Clear Engagement Lifecycle: The monthly trend showed a strong launch period for the first quarter, followed by a healthy stabilization to a consistent baseline. This indicates a mature and predictable user base.

Future Scope
This EDA provides a strong foundation for more advanced analysis. Possible next steps include:

Predictive Modeling: Build a model to predict a user's completion_rate based on genre, device, and initial watch time.

Deeper Segmentation: Analyze the watch_category (Binge, Long) to build a specific profile of "binge-watchers."

Content Strategy: Drill into completion_rate by genre to identify which content types are not just watched, but finished and most compelling.

Conclusion
This analysis demonstrates a platform with broad, stable, and highly consistent user engagement across all segments. The key takeaway is the universal appeal of the content and the flexibility of the user base, presenting a strong foundation for any future data-driven strategies.
