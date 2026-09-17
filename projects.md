# Projects
This section documents my data science projects, research questions, and data stories I create throughout the semesters.
---
## Project 1
# Poverty and Fertility Rates Across U.S. States (2007-2024) 
## How has the relationship between poverty and fertility rates across U.S. states changed from 2007 to 2024?

# Key Findings
## Chart 1
This chart shows how the relationship between poverty and fertility rates across U.S. states changed from 2007 to 2024. A positive correlation means that states with higher poverty rates also tended to have higher fertility rates, while a correlation closer to zero means the relationship was weaker. The chart shows that this relationship was not consistent throughout the period and became weaker in some years. This instability may partly reflect the fact that poverty and fertility each followed their own separate trends over this time, for instance, poverty rates fluctuated with the economy (e.g., the 2008–2009 recession), while fertility rates were on a longer, steadier decline (USAFacts, 2026). Because these two variables were not always moving for the same reasons, their year-to-year correlation was unlikely to stay constant.

<img width="858" height="546" alt="chart1" src="https://github.com/user-attachments/assets/8fe254bc-4061-4149-a26a-651a7314b6a9" />

## Chart 2
This chart shows how the average fertility rate across U.S. states changed over time. The overall pattern can be compared with broader fertility trends in the United States. USAFacts (2026) reports that fertility rates declined in every state between 2004 and 2024. Similarly, the U.S. Census Bureau reports a long-term decline in the national fertility rate (Hayward et al., 2026). This helps provide context for the changes shown in my visualization and suggests that the state-level patterns in my data are part of a broader change in fertility across the United States.

<img width="842" height="546" alt="chart2" src="https://github.com/user-attachments/assets/c96a679d-74a5-4c14-867f-08daaefe907e" />

## Sources 
My charts use data collected from the Census API. The Census and USAFacts articles are used to support and explain the trends shown in the charts.

Hayward, G. M., Rogers, L. T., & Sabo, S. (2026, June 25). South and Midwest had highest fertility rates, but even West and Northeast had pockets of high-fertility counties. U.S. Census Bureau. U.S. Census Bureau article

USAFacts. (2026, May 8). How have US fertility and birth rates changed over time? USAFacts article

U.S. Census Bureau. (2024). American Community Survey 1-year data. U.S. Department of Commerce.

### AI Assistance Disclosure

I used ChatGPT as a tool while working on this project. I used it to help troubleshoot errors in my Python code, understand how to retrieve and clean data from the U.S. Census API, and improve the organization of my visualizations. I reviewed the suggestions, tested the code myself, and edited the written responses to reflect my own understanding of the project and results.
# [Code](https://github.com/nvue4-lgtm/poverty-fertility-analysis/blob/main/ResearchProject.ipynb)
