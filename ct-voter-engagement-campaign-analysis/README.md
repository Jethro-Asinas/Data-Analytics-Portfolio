# Connecticut Young Adult Voter Engagement Analysis

<img width="1920" height="1080" alt="Connecticut Young Adult Voter Engagement Analysis cover" src="https://github.com/user-attachments/assets/4d31a3a2-af5e-40cd-b980-9c7ce2ea48fe" />

## Quick Project Summary

During my UConn Beachball Agency internship, my team partnered with the Connecticut Secretary of the State to encourage municipal voting among young adults. As the team’s sole data analyst, I used 2022 American Community Survey data to profile Connecticut residents ages 18–30. My analysis identified trends of pursuing higher education and employment in lower-wage occupations, helping shape a social media campaign that connected voting with education and workplace issues affecting young adults.


## Project Overview

During my internship with the UConn Beachball Agency, my team worked with the Connecticut Secretary of the State on a social media campaign intended to encourage greater participation in municipal voting. The client wanted to reach a younger audience, so our team was tasked with developing social media graphics that would make municipal voting feel more relevant and approachable.

As the team's sole data analyst, I used 2022 American Community Survey (ACS) data to profile Connecticut residents ages 18–30. I focused on education, occupation, household language, age, gender, school enrollment, and disability status. I shared the findings with the design team to give them a clearer starting point for discussing the campaign's themes, accessibility, and messaging.

## Business Question

**How can demographic data help our team better understand young Connecticut residents before developing a municipal voting campaign?**

## Tools Used

- **Python and pandas:** cleaned and reshaped the ACS tables
- **Excel:** reviewed categories and mapped occupation groups
- **Tableau:** built the interactive demographic dashboards
- **BLS Occupational Employment and Wage Statistics:** added national wage context to the occupation findings

## Data Preparation

The original ACS files contained nested categories and multi-level headers that were not ready for analysis. I cleaned the two source tables separately, removed aggregate rows that would have caused double counting, reshaped the data into a long format, grouped detailed education levels, and mapped occupation titles to their broader occupation groups.

The final demographic dataset represented a weighted population estimate of **621,374 Connecticut residents ages 18–30**. The occupation and demographic tables remained separate because they did not share a valid row-level key.

## Dashboard

[View the interactive Tableau dashboard](https://public.tableau.com/views/ConnecticutYoungAdultDemographics2022ACSPUMS/AdvancedDemographics?:language=en-US&:display_count=n&:origin=viz_share_link)

## Key Findings

### 1. Education changes considerably by life stage

Degree attainment increased from **4% among residents ages 18–21** to **45% among ages 22–25** and **51% among ages 26–30**. Over the same age groups, school enrollment decreased from **73% to 27% to 12%**.

This showed that the campaign's audience included people at very different educational stages. Some were still closely connected to schools and colleges, while many of the older residents had already completed a degree. Education was therefore a reasonable theme for the team to explore, but it could not represent the entire young-adult audience.

### 2. Many residents worked in lower-wage occupation groups

Sales was the largest occupation group, representing **11% of the population**. Office and administrative support and food preparation each represented **9%**, followed by educational instruction and transportation and material moving at **7%** each. Within sales, cashiers accounted for **41%** and retail salespeople accounted for **29%** of the group.

I compared the four leading non-education groups with 2022 national wage estimates from the U.S. Bureau of Labor Statistics. Each had a median hourly wage below the **$22.26 median across all occupations**.

| Occupation group | 2022 national median hourly wage |
|---|---:|
| Sales and related | $16.96 |
| Office and administrative support | $19.67 |
| Food preparation and serving | $14.25 |
| Transportation and material moving | $18.24 |

BLS also identifies cashier and retail salesperson as occupations that typically require no formal educational credential. Together, the ACS and BLS data indicated that lower-wage and customer-facing work was an important part of the audience profile.

### 3. Language and disability were important accessibility considerations

Approximately **58%** of the population lived in households categorized as English only, while **18%** lived in Spanish-speaking households. In addition, **9%** of the population had a recorded disability.

These findings gave the team a reason to discuss bilingual materials, plain-language communication, and accessible visual design as the campaign moved forward.

## Recommendation

Based on the available data, I identified education and employment as two useful themes for the team's early strategy discussions. I recommended exploring posts that connected municipal participation with local education resources and everyday economic concerns while keeping the instructions short, accessible, and easy to understand.

These recommendations were starting points rather than conclusions about why people should vote. The ACS described the audience but did not measure political attitudes, voting barriers, or campaign response. Those questions would require surveys, interviews, voter data, or campaign testing.

## Outcome

The findings were presented to the team and used during development of the social media campaign. The client responded positively to the final project, and the team earned an A for the course. Campaign engagement and voter-turnout results were not available, so client approval should be treated as qualitative feedback rather than proof that the campaign increased participation.

## Limitations

- ACS PUMS provides weighted estimates rather than a complete count of every resident.
- The BLS wage figures are national benchmarks and do not represent the actual earnings of people in the Connecticut ACS dataset.
- Differences between age groups do not track the same people over time.
- Demographic characteristics cannot establish people's political beliefs or reasons for voting.
- The separate demographic and occupation tables could not be combined at the individual level.

## Sources

- [U.S. Census Bureau: American Community Survey](https://www.census.gov/programs-surveys/acs)
- [BLS: May 2022 National Occupational Employment and Wage Estimates](https://www.bls.gov/oes/2022/may/oes_nat.htm)
- [BLS: Sales and Related Occupations](https://www.bls.gov/oes/2022/may/oes410000.htm)
- [BLS: Office and Administrative Support Occupations](https://www.bls.gov/oes/2022/may/oes430000.htm)
- [BLS: Food Preparation and Serving Occupations](https://www.bls.gov/oes/2022/may/oes350000.htm)
- [BLS: Transportation and Material Moving Occupations](https://www.bls.gov/oes/2022/may/oes530000.htm)
- [BLS Occupational Outlook Handbook: Cashiers](https://www.bls.gov/ooh/sales/cashiers.htm)
- [BLS Occupational Outlook Handbook: Retail Sales Workers](https://www.bls.gov/ooh/sales/retail-sales-workers.htm)
- [BLS Occupational Outlook Handbook: Registered Nurses](https://www.bls.gov/ooh/healthcare/registered-nurses.htm)
