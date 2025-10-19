# OIL-AND-GAS-WELL-PRODUCTION-DATA-ANALYSIS

## Table of Contents
1. [Abstract](#abstract)  
2. [Dedication](#dedication)  
3. [Problem Statement](#problem-statement)  
4. [Objectives](#objectives)  
5. [Tool Used (Python)](#tool-used-python)  
6. [Methodology](#methodology)  
7. [Limitation](#limitation)  
8. [Insights](#insights)  
9. [Recommendations](#recommendations)  
10. [Conclusion](#conclusion)  

---

## Abstract
This project focuses on the predictive modeling of oil well productivity using both reservoir and operational parameters. It aims to provide a data-driven understanding of Well No. 807’s performance, identify key production influencers, and forecast future oil output trends. Through a combination of exploratory data analysis, statistical investigation, and predictive modeling, the study seeks to deliver actionable insights that support reservoir management and production optimization strategies.

---

## Dedication
This work is dedicated to professionals in the oil and gas industry who strive to enhance production efficiency, embrace data-driven decision-making, and sustain reservoir performance through innovation and technical excellence.

---

## Problem Statement
The oil production from Well No. 807 has exhibited a significant and steady long-term decline, falling from approximately 50 m³/day in 2013 to below 10 m³/day by 2021. This decline in productivity is accompanied by a substantial increase in water cut and a continuous depletion of reservoir pressure. To implement effective reservoir management and production optimization strategies, it is critical to move from simply observing this decline to quantitatively understanding the underlying causes and predicting future performance. Therefore, this project aims to diagnose the key factors driving the production decline and to develop a predictive model for daily oil production to support data-driven decision-making for this well.

---

## Objectives
- To characterize the historical production performance and decline trend of the well.  
- To identify the relationship between fluid production (oil, water, gas) and their impact on well productivity.  
- To evaluate the state of the reservoir energy and its influence on production capability.  
- To determine the key operational and reservoir parameters that correlate most strongly with oil production.  
- To create new, insightful features that capture the well's production behavior and maturity.  
- To visualize the cumulative recovery and forecast the well's future economic lifetime.  

---

## Tool Used (Python)
Python programming language was utilized for the data analysis, and visualization. Key libraries included Pandas for data manipulation, Matplotlib and Seaborn for visualization.

---

## Methodology
1. **Data Acquisition:** Collected daily operational and reservoir data for Well No. 807 including oil, gas, water volumes, water cut, reservoir pressure, and dynamic level.  
2. **Data Cleaning:** Handled missing values, corrected data inconsistencies, and prepared the dataset for analysis.  
3. **Exploratory Data Analysis (EDA):** Conducted statistical and graphical analysis to identify key relationships among parameters.  
4. **Feature Engineering:** Created derived features to enhance model performance and capture production trends.  
5. **Model Development:** Applied regression and machine learning models to predict oil production based on reservoir and operational parameters.  
6. **Model Evaluation:** Assessed model accuracy using R², RMSE, and MAE metrics to determine reliability.  
7. **Visualization:** Generated trend plots and correlation heatmaps for interpretability and insight communication.  

---

## Limitation
The study is limited by the availability and quality of field data. Certain reservoir parameters such as permeability, porosity, and bottom-hole pressure were not available, which may influence the accuracy of the predictive model. Additionally, the analysis focuses on a single well, limiting generalization to field-wide applications.

---

## Insights
1. The oil production trend for Well No. 807 shows a clear long-term decline from approximately 50 m³/day in 2013 to below 10 m³/day by 2021, indicating progressive reservoir depletion and potential increases in water cut or operational inefficiencies. While short-term fluctuations and brief recoveries are visible, likely due to well interventions or equipment adjustments, the overall 7-day moving average trend confirms a steady reduction in productivity. This visualization provides an essential overview of the well’s performance behavior over time, supporting effective monitoring and informed decision-making on production optimization or decline management strategies.

![](https://github.com/isaacquayson/OIL-AND-GAS-WELL-PRODUCTION-DATA-ANALYSIS/blob/main/Screenshot%202025-10-18%20220352.png)

2. The first plot illustrates a gradual decline in daily oil production over time, starting from around 45–50 m³/day and dropping below 10 m³/day by the end of the observed period. This downward trend reflects reservoir pressure depletion and possible production inefficiencies as the well matures. The second plot, showing cumulative oil production, rises steadily but begins to flatten toward the end, indicating slower production rates despite ongoing operation. Together, these graphs effectively visualize production behavior and highlight the well’s transition from a high-yield to a declining phase, supporting timely decision-making for reservoir management and production optimization.

![](https://github.com/isaacquayson/OIL-AND-GAS-WELL-PRODUCTION-DATA-ANALYSIS/blob/main/Screenshot%202025-10-18%20222256.png)

3. The plots show the evolution of water production performance in Well 807 from 2013 to 2021. The top plot reveals a steady rise in water cut from about 30% in 2013 to around 70–80% by 2016, after which it stabilizes with minor fluctuations. This indicates progressive water breakthrough and maturity of the reservoir. The bottom plot shows corresponding spikes in the Water–Oil Ratio (WOR), particularly between 2014 and 2017, reflecting periods of excessive water production. Overall, the sustained high water cut and periodic WOR peaks suggest increasing water encroachment and declining oil efficiency over time, signaling the need for water control or reservoir management interventions.

![](https://github.com/isaacquayson/OIL-AND-GAS-WELL-PRODUCTION-DATA-ANALYSIS/blob/main/Screenshot%202025-10-18%20224225.png)

4. These plots illustrate a consistent decline in reservoir pressure from around 220 atm in 2013 to just above 100 atm by 2021, as shown by both the daily values and the smoothed 30-day moving average. This steady downward trend reflects continuous reservoir depletion, likely due to sustained production without sufficient pressure support from natural drive or secondary recovery methods. The derivative plot below confirms a nearly constant rate of pressure decline throughout the monitoring period, indicating stable but ongoing energy loss within the reservoir system. This suggests that reservoir pressure maintenance or enhanced recovery measures may be needed to sustain production efficiency.

 ![](https://github.com/isaacquayson/OIL-AND-GAS-WELL-PRODUCTION-DATA-ANALYSIS/blob/main/Screenshot%202025-10-18%20225036.png)

5. We can see that from 2013 to around 2018, the dynamic level showed significant variability with frequent dips, which may indicate operational inconsistencies or external influences affecting performance. However, starting in 2018, there’s a clear improvement—the levels rise and then stabilize at a much higher range through 2019 to 2021. This suggests that the changes or interventions made around that time were effective, leading to a more stable and sustained performance in the system.

![](https://github.com/isaacquayson/OIL-AND-GAS-WELL-PRODUCTION-DATA-ANALYSIS/blob/main/Screenshot%202025-10-18%20225535.png)

6. I can see that gas production has shown a clear and steady decline from 2013 to 2021, dropping from around 12,000 m³/day to below 2,000 m³/day. This indicates a consistent reduction in reservoir pressure or resource availability over time. Meanwhile, the Gas-Oil Ratio (GOR) remains relatively stable through most of the period, with some minor fluctuations, but shows a gradual increase and more variability after 2018. This suggests that as gas production decreases, the reservoir may be transitioning, potentially producing proportionally more gas relative to oil toward the later years. Overall, this trend highlights a maturing field that may require optimization strategies or interventions to maintain production efficiency.  

7. This chart shows the monthly average oil production trend from 2013 to 2021. The data clearly indicates a continuous decline in oil output over the years, starting above 40 m³/day in early 2013 and dropping steadily to below 10 m³/day by 2021. While there are short periods of minor recovery or fluctuation, the overall trajectory reflects a consistent depletion in reservoir performance or production capacity. This long-term decline highlights the maturity of the field and suggests the need for enhanced recovery strategies or operational interventions to sustain production levels.  

9. This correlation matrix provides valuable insights into the key factors influencing oil production. Oil volume shows a very strong positive correlation with gas volume (0.98), reservoir pressure (0.84), and cumulative oil (0.89), indicating that higher reservoir pressure and gas production are closely associated with increased oil output. There’s also a strong correlation with volume of liquid (0.75), suggesting that total fluid production impacts oil rates. Conversely, oil volume has a strong negative correlation with water cut (-0.87) and Days_Since_Start (-0.94), meaning that as water production increases and the well matures, oil output declines significantly. Additionally, oil production decreases as dynamic level (-0.45) drops, reinforcing the relationship between reservoir performance and production rates. Overall, maintaining reservoir pressure and managing water production appear to be the most critical factors in sustaining oil production over time.  

10. Water cut % shows a strong negative correlation with the oil production, indicating that as the oil production increases, the water portion or % decreases in the well.  

11. This plot shows a strong correlation between the oil produced vs the reservoir pressure. This shows that, the higher the reservoir pressure, the higher the oil production and vice versa. Thus, the reservoir pressure must be maintained or increased to ensure stable oil production.  

---

## Recommendations
- Implement a Reservoir Pressure Maintenance Program — Initiate water injection to stabilize reservoir pressure.  
- Investigate and Mitigate Water Ingress — Identify and isolate water sources to reduce water production.  
- Optimize the Gas-Oil Ratio (GOR) — Adjust choke settings and wellbore parameters for improved recovery.  
- Plan for Artificial Lift Installation or Optimization — Consider ESP deployment to maintain drawdown.  
- Perform Decline Curve Analysis for Forecasting — Estimate remaining reserves and forecast economic lifetime.  

---

## Conclusion
This study successfully demonstrates how data-driven predictive modeling can enhance understanding of oil well performance. By correlating reservoir pressure, water cut, and other operational parameters with oil output, the project provides a foundation for strategic production optimization. Implementing the recommended actions could significantly improve the economic viability and lifespan of Well No. 807.
