# SuperLife Health Incentive Program

**Aspiring Actuaries**: Jinil Patel, Melissa Renard, Jason Zhang, Ricky Zhang, Yuchi Zhang

Landing page: https://actuarial-control-cycle-t1-2024.github.io/group-page-showcase-aspiring-actuaries/

## Background and program

SuperLife is one of the major life insurance companies of Lumaria. We have been asked to develop a health incentive program that SuperLife can pair with its longer-term life insurance products. SuperLife are looking to improve its policyholders’ expected mortality once the policyholder has purchased an insurance policy. Specifically, SuperLife's primary goals are:
- Incentivise healthy behaviours through participation in the program
- Decrease expected mortality
- Increase product marketability and competitiveness
- Add economic value to SuperLife

We propose a health program that includes a smoking cessation program, a weight management program and cancer prevention initiatives. This proposal and insights have been delivered in a [report](Aspiring-Actuaries-Report.pdf)

## Key insights

 **Program Design**: 
   - Smoking Cessation Program: Implementing a reward-based scheme for smokers to quit, with progressive cash incentives over a 6-month term, aiming to reduce mortality rates attributed to smoking by 25%. Estimated completion rates suggest 33.6%-43.2% of smokers may complete the program, with a 20%-30% probability of long-term cessation.
   - Weight Management Program: Utilizing a dedicated app, offering dietary information and physical activity incentives, with an expected mortality reduction of 5% for non-smokers.
   - Cancer Prevention Initiatives: Providing early detection and prevention initiatives for various cancers, anticipating a 3% reduction in mortality rates.

 **Pricing & Costs**: 
   - Smoking cessation incurs a one-time cost of Č2,177.50 in the first year, with subsequent costs being Č28.75 per year. Weight management costs Č522.50 per program, while cancer prevention initiatives cost Č52.50 per policyholder annually.
   - Despite initial costs, the program is anticipated to significantly increase profitability, particularly evident in the 10-fold increase in profit margin for single-premium whole life insurance policies.

 **Assumptions**: 
   - Mortality reductions are assumed for each program: 25% for smoking cessation, 5% for weight management, and 3% for cancer prevention. These reductions are not considered independent of each other.
   - Pricing is based on age brackets, with consideration for differences between smokers and non-smokers.
   - Sensitivity analyses explore various scenarios, including different mortality decrease rates and withdrawal rates, to understand potential impacts on profits.

 **Risk & Risk Mitigation**:
   - Identified risks include low engagement, adverse selection, increase in risky behavior, data security, equity concerns, regulatory changes, budget overruns, and model risk.
   - Mitigation strategies involve trial phases, personalized services, eligibility criteria, cybersecurity measures, diverse partnerships, proactive regulatory compliance, financial management, and sensitivity analysis.

 **Data and Data Limitations**:
   - Utilized internal datasets from SuperLife but encountered limitations such as missing key policyholder information and unisex mortality rates, requiring assumptions and adjustments in analysis.
   - Information on interventions provided wide ranges of cost and mortality decrease, necessitating additional research and assumptions, with mortality reductions applied universally across policyholders.

Overall, the proposed health incentive program shows promising potential to reduce mortality rates, increase policyholder engagement, and significantly enhance SuperLife's profitability over the long term. However, careful consideration of assumptions, risk mitigation strategies, and data limitations is crucial for effective implementation and monitoring of the program's success.

## Data
The next stage of our project consisted on cleaning and preparing the data provided by SuperLife in preparation for modeling and analysis. We primarily focused on the SuperLife Inforce Dataset in conjunction with the Lumaria mortality table to model mortality. In terms of pricing, we utilised the economic data of Lumaria together with the interventions table and external research on comparable economies and health insurance companies to estimate the mortality improvement and revenue and expenses associated with our health incentive program.

## Data cleaning
**Guide for R code**
- [EDA.Rmd](<R code/EDA.Rmd>): Exploratory data analysis on the inforce dataset.
- [Lapse rates.Rmd](<R code/Lapse rates.Rmd>): Calculations of the lapse rates for each type of policyholder using the inforce dataset, output stored in [Lapse Rates from Data.xlsx](<Data/Lapse Rates from Data.xlsx>). 
- [Mortality.Rmd](<R code/Mortality.Rmd>): Calculations of mortality rates for each type of policyholder using the inforce dataset, output stored in [Mortality Rates from data.xlsx](<Data/Mortality Rates from data.xlsx>). 
- [Policy count.Rmd](<R code/Policy Count.Rmd>): Counts the number of each type of policyholder with each level of benefit in the inforce dataset, output stored in [Policy count.xlsx](<Data/Policy count.xlsx>).

## Model \& pricing

Pricing of SuperLife's insurance products was done by considering the following characteristics of the policyholders:
- Age (10-year age group)
- Smoking status
- Sex (if the policyholder was a non-smoker)

For these differentiated groups of people, mortality and lapse rates were estimated separately using SuperLife's in-force dataset. 

Initial premiums were calculated by ensuring a profit margin of 8\%. Premium prices were not changed after the supposed implementation of our proposed program. 

More details can be seen in the [Model & Pricing Excel worksheet](model_pricing.xlsm).
