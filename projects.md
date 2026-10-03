# Projects
This section documents my data science projects, research questions, and data stories I create throughout the semesters.
---
## Project 1
# Poverty and Fertility Rates Across U.S. States (2007-2024) 
## How has the relationship between poverty and fertility rates across U.S. states changed from 2007 to 2024?

# Key Findings
## Chart 1
This chart shows how the relationship between poverty and fertility rates across U.S. states changed from 2007 to 2024. A positive correlation means that states with higher poverty rates also tended to have higher fertility rates, while a correlation closer to zero means the relationship was weaker. The chart shows that this relationship was not consistent throughout the period and became weaker in some years. This instability may partly reflect the fact that poverty and fertility each followed their own separate trends over this time; for instance, poverty rates fluctuated with the economy (e.g., the 2008–2009 recession), while fertility rates were on a longer, steadier decline (USAFacts, 2026). Because these two variables were not always moving for the same reasons, their year-to-year correlation was unlikely to stay constant.

<img width="858" height="546" alt="chart1" src="https://github.com/user-attachments/assets/8fe254bc-4061-4149-a26a-651a7314b6a9" />

## Chart 2
This chart shows how the average fertility rate across U.S. states changed over time. The overall pattern can be compared with broader fertility trends in the United States. USAFacts (2026) reports that fertility rates declined in every state between 2004 and 2024. Similarly, the U.S. Census Bureau reports a long-term decline in the national fertility rate (Hayward et al., 2026). This helps provide context for the changes shown in my visualization and suggests that the state-level patterns in my data are part of a broader change in fertility across the United States.

<img width="842" height="546" alt="chart2" src="https://github.com/user-attachments/assets/c96a679d-74a5-4c14-867f-08daaefe907e" />

## Sources 
My charts use data collected from the Census API. The Census and USAFacts articles are used to support and explain the trends shown in the charts.

Hayward, G. M., Rogers, L. T., & Sabo, S. (2026, June 25). South and Midwest had the highest fertility rates, but even the West and Northeast had pockets of high-fertility counties. U.S. Census Bureau. U.S. Census Bureau article

USAFacts. (2026, May 8). How have US fertility and birth rates changed over time? USAFacts article

U.S. Census Bureau. (2024). American Community Survey 1-year data. U.S. Department of Commerce.

### AI Assistance Disclosure

I used ChatGPT as a tool while working on this project. I used it to help troubleshoot errors in my Python code, understand how to retrieve and clean data from the U.S. Census API, and improve the organization of my visualizations. I reviewed the suggestions, tested the code myself, and edited the written responses to reflect my own understanding of the project and results.
# [Code](https://github.com/nvue4-lgtm/poverty-fertility-analysis/blob/main/ResearchProject.ipynb)

---
## Project 2
# Makeup Shade Inclusivity Classification
## Project Overview
This project explores whether information about a makeup brand's foundation shade lineup can be used to predict whether the brand has a relatively inclusive range of deeper shades.

# Research Question
Can characteristics of a makeup brand's foundation shade lineup help predict whether the brand has an inclusive range of deeper shades?

# Background and Context
Foundation shade inclusivity has become an important topic in the beauty industry. For many years, individuals with deeper skin tones had significantly fewer foundation options compared to those with lighter skin tones. Even when a brand offers a large number of shades, it doesn't always mean that the range is evenly distributed across light, medium, and deep skin tones. Abelman and Dall’Asen (2020) discussed how some makeup brands have expanded their foundation shade ranges to provide more options for a diverse array of skin tones. Similarly, Sinks (2018) explained how drugstores and beauty brands have faced pressure to offer more products specifically tailored for individuals with deeper complexions.

This issue is crucial because foundation is meant to closely match a person’s skin tone, and a limited shade range can make it challenging for some customers to find an appropriate match. As beauty companies continue to expand their shade selections, it is essential to evaluate whether these ranges are genuinely broad and balanced. This project examines foundation shade data across various brands, analyzing factors such as shade lightness, shade count, and other brand-level characteristics to predict whether a brand offers a relatively inclusive range of deeper shades. The goal is to utilize machine learning to explore patterns in foundation shade diversity rather than to establish a final or universal definition of inclusivity.

Sources: 
Abelman, D., & Dall’Asen, N. (2020, June 28). *21 makeup brands that have the most inclusive foundation shade ranges*. Allure. https://www.allure.com/gallery/makeup-brands-wide-foundation-shade-ranges

Sinks, T. (2018, November 10). *What are drugstores doing to factor inclusivity into their makeup aisles?* Allure. https://www.allure.com/story/drugstore-foundation-range-inclusivity-in-the-makeup-aisle

The target variable is:
- 0 = not inclusive
- 1 = inclusive

# Dataset
The dataset comes from the Kaggle Makeup Shades Dataset.

Original dataset source:
https://www.kaggle.com/datasets/shivamb/makeup-shades-dataset?resource=download

# Target and Features
The dataset lacked an official inclusivity label, so I created a proxy for this project. I defined a "deeper shade" as one with a lightness (L) value in the darkest one-third of the dataset and calculated the proportion of deeper shades for each brand. A brand is considered inclusive if its share of deeper shades exceeds the median for all brands. This definition is specific to this project and should not be seen as a universal standard for inclusivity.

The model uses these features:
- Brand group
- Shade count
- Minimum lightness
- Maximum lightness
- Lightness range
- Lightness standard deviation

# Models
I compared three approaches:
1. Baseline model - always predicts the most common class.
2. Logistic Regression - used because the target has two classes and the model is easy to interpret.
3. Random Forest - used because it can learn more complex relationships between the features

# Model Results
Accuracy: 
Baseline - 0.444
Logistic Regression - 1.000
Random Forest - 0.889

F1 Score:
Baseline - 0.615
Logistic Regression - 1.000
Random Forest - 0.889

In a 5-fold cross-validation analysis, Logistic Regression achieved an average F1 score of approximately 0.971, while Random Forest had an average F1 score of around 0.921. Both machine learning models outperformed the baseline, with Logistic Regression yielding the strongest results in this comparison.

# Visualizations

