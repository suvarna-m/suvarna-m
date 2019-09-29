---
layout: post
title: Survival Analysis
date: 2019-09-28
---

Imagine yourself in a doctor’s office. The doctor tells you that you have esophageal cancer, and explains that the possible treatments are surgery alone, or a combination of surgery and chemoradiotherapy. As a patient, you are likely left wondering which treatment option leads to a better chance of survival. Your physician can use survival analysis to give you a clearer picture. 


Survival analysis is a statistical concept used to analyze the amount of time until a certain event occurs. In this example, our event of interest is death.  To visualize a survival analysis, scientists use Kaplan-Meier survival curves, which, in a health context, can be used to measure the proportion of patients that live for an amount of time after a specific treatment. 


The following graph is an example of a Kaplan-Meier survival curve for patients with esophageal cancer who either underwent surgery alone, or underwent the combination of surgery and chemoradiotherapy (CRT). These data were collected as part of a study that evaluated the 2 different treatments for esophageal cancer (van Hagen et al., 2012). The x-axis shows survival time. In this case, it shows data from 0 to 60 months. The y-axis shows the survival probability, from 0 to 1. <br/>
<img src="KMcurve.PNG" width="500"/><br/>


In our graph, the 0th time point, where x = 0, is the date of surgery. P(survival) when x = 0 is 1, which means that all the patients were alive at the point of surgery.
As time progresses, events, or deaths, occur. As the events occur, the line starts to curve downwards. For example, at the 6-month mark, the probability of survival in both groups is about 0.95, as seen in the graph below. This means that 95% of the patients in both groups are still alive 6 months after their surgery, and 5% of the patients in each group have died. <br/>

<img src="initialKM.PNG" width="500"/><br/>


The median survival is where P(survival) = 0.5. In this example, the median survival is about 50 months for patients who opted for CRT and surgery, and about 25 months for those who opted for surgery alone. <br/>

<img src="medianKM.PNG" width="500"/><br/>


We can also see that, at the end of the study (60 months), only ~35% of surgery-alone patients were still alive, but ~47% of the CRT + surgery patients were still alive.
This means that, to increase your chance of surviving, you would likely go with the CRT + surgery option.<br/>

<img src="finalKM.PNG" width="500"/><br/>

As helpful as survival analysis can be, it has a major flaw, called **censoring**. In our curve, we can see the percent of patients who are still alive at 60 months post-surgery for the 2 groups. However, we do not know what happens after the 60-month period. There also may have been patients who dropped out of the study while it was happening, so we do not have data on them. Censoring is a form of missing data, because the time-to-event data is not observed in these participants. 


Survival analysis and Kaplan-Meier curves are often used in the healthcare industry to show patients their chances and timeline of survival when they get diagnosed with a disease, or to help them choose from various treatments, as shown above. However, there are uses in other industries as well: 
- [Duration modelling in economics](http://www.econ.uiuc.edu/~roger/courses/508/old/2012/L22.pdf)
- [Event history analysis in sociology](https://spia.uga.edu/faculty_pages/rbakker/pols8501/OxfordOneNotes.pdf)

To summarize, despite the issue of censoring, survival analysis and Kaplan-Meier curves continue to be used widely, particularly in the medical community, but also in the fields of economics and sociology. 

##### References:
van Hagen, P., Hulshof, M. C. C. M., Van Lanschot, J. J. B., Steyerberg, E. W., Henegouwen, M. V. B., Wijnhoven, B. P. L., ... & Cuesta, M. A. (2012). Preoperative chemoradiotherapy for esophageal or junctional cancer. New England Journal of Medicine, 366(22), 2074-2084.

*Note: The data and initial graph are from the above study. I added the dashed lines in the 2nd, 3rd, and 4th graphs.*
