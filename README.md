*1.1 Introduction*
------
OriVelt Limited is expanding into new industries so as to diversify its investment portfolio and one of the targeted sectors is aviation, particularly the purchase and operation of aircrafts for both commercial and private enterprices. Aviation is a high-profit, lucrative niche that is highly regulated and very risk intensive where substandard asset selection can result to substantial  financial losses, safety concerns and operational inefficiencies. 

This project aims at performing quantitative risk assessment on three areas; Damage Severity Risk and Geographic Risk. Fatality risk is modeled using reported loss-of-life outcomes to capture human and liability exposure, damage severity risk is assessed through encoded aircraft damage levels as a proxy for financial and asset loss, and geographic risk is analyzed using crash location characteristics that influence accident severity and emergency response effectiveness.

By integrating these risk dimensions, this project aims to identify aircraft types associated with lower overall risk profiles and provide evidence-based guidance to support strategic aircraft acquisition decisions for the company’s new aviation division.

-------
*1.2 Data Understanding*
-----
The dataset consists of historical aircraft crash records containing Date, Aircraft Type, Registration, Operator, Fatalities (fat), Damage Severity (dmg), and Location. These variables support analysis of fatality risk, damage severity risk, and geographic risk by providing outcome-based, operational, temporal, and spatial information.

Several relevant variables are missing, including weather conditions, flight phase, aircraft age, maintenance history, and explicit terrain classification. Financial variables such as acquisition cost and insurance premiums are also unavailable; therefore, damage severity is used as a proxy for financial and asset loss. Location data varies in spatial precision, requiring geocoding and spatial inference for geographic analysis.

----
*1.3 Data Preparation*
-------
Data preparation focuses on cleaning, transforming, and engineering features to support fatality risk, damage severity risk, and geographic risk modeling. Aircraft type and operator fields are standardized to resolve naming inconsistencies and enable reliable grouping. Missing or ambiguous values in fatality counts and damage severity are handled through validation rules and, where appropriate, imputation or exclusion. Damage severity categories are encoded into ordinal numerical values to reflect increasing levels of asset loss.

-------
*1.4	Modeling*
-----
The project focuses on three key dimensions: safety risk, evaluating the severity of human loss across aircraft types and operators; purchase risk, assessing financial exposure through damage severity and asset loss; and geographic risk, examining how location and operating environments influence accident outcomes. The results of these analyses are integrated into an interactive dashboard designed to enable stakeholders to explore risk patterns, compare aircraft options, and support data-driven aircraft acquisition and operational strategies.
------
*1.4.1 Safety Analysis Risk*
------
In this objective, we are not looking at how often accidents happen but rather measuring how bad the outcomes are when they happen.  we are aiming at minimizing loss of life and reputational damage.
Aircraft were grouped into broad operational categories, and fatality severity metrics were used to compare safety risk at the category level, highlighting which categories are associated with more severe human outcomes when accidents occur.
https://public.tableau.com/app/profile/chebet.chelimo3671/viz/SafetyRiskAssessment/Sheet2?publish=yes
-----
*1.4.2 Purchase Risk Analysis (Financial / Asset Risk)*
-------
We cannot change an aircrafts DNA. An aircraft can be safe for people but very expensive to repair or replace. Purchase risk was assessed by analyzing damage severity and total loss rates across aircraft types to estimate the financial exposure associated with aircraft ownership.
Purchase Risk Score =
70% × Average Damage Severity
+ 30% × Total Loss Rate
https://public.tableau.com/app/profile/chebet.chelimo3671/viz/PurchaseRiskAssessment/Sheet3?publish=yes
------
*1.4.3 Geographic Risk Analysis*
-----
Geographic risk focuses on where accidents happen and how location affects outcomes, not on aircraft design or operators. Geographic risk was assessed by evaluating fatality severity and aircraft damage severity across accident locations to identify operationally high-risk regions.

Geographic Risk Score =
50% × Fatality Severity
+ 50% × Damage Severity
https://public.tableau.com/app/profile/chebet.chelimo3671/viz/GeographicRiskAssessment/Sheet4?publish=yes
