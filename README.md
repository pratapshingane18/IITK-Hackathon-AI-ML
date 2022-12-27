# IITK-Hackathon-AI-ML

1 BACKGROUND
Any drug in the US market is prescribed by the HCPs (Health Care Practitioners) to patients thereby making HCPs as the
actual customer for a pharmaceutical company. Companies promotes the drug to HCPs through multiple promotional
channels:
1. Sales Rep Calls: A sales representative visits the HCP, in-person, and details about the drug, its usage, efficacy,
benefits etc.
2. Sample Drops: Free drug samples are shared with the HCP who can then prescribe those drugs to the patients,
and check their benefits and effects
3. Emails: Details of the drug usage, efficacy, safety procedure, side-effects etc are shared with the HCPs through
email campaigns to enable them to know more about the drug
4. Speaker Programs: Pharmaceutical companies organize events and awareness programs related to the drug and
disease area. HCPs are invited to be speakers in such events, thereby initiating a soft promotion for the brand
drug
5. Vouchers Dropped: Coupons and vouchers are shared with the HCPs which they can share subsequently with their
patients along with prescriptions. The vouchers can provide a discount on drug purchase thereby ensuring
popularity with the patients
Pharmaceutical companies therefore want to engage each HCP with the best possible promotional channel and maximize
their brand prescriptions (Brand Rx). The brand drug in question is a skin disease drug in the US market, launched in 2018
and is one of the prominent drugs in the skin disease market.
4 Copyright © 2022 Axtria Inc. All rights reserved.
2 ASK
Based on the datasets shared, project background and promotional constraints, the ask is to identify the best promotional
channel for every HCP for the upcoming week. The best channel should be identified among three channels – sales rep
calls, emails, and sample drops. The best channel should meet promotional constraints shared and should maximize the
brand TRx for the upcoming week for that HCP. Frequency of promotion of the channel should not be considered while
identifying the best promotional channel.
5 Copyright © 2022 Axtria Inc. All rights reserved.
3 DATA
To better understand the problem at hand, the following two datasets have been provided to the candidates:
HCP Data: Details of HCP’s prescriptions and promotions at a week level
• Physician ID: Unique ID of the physician/HCP
• Time Period: Week ending date (spans from Jan’19 to Jan’20)
• Brand Rx: Prescriptions written by the HCP for the brand drug in that week
• Market Rx: Prescriptions written by the HCP for all drugs in Skin Disease market in that week
• Sales Rep Calls: Whether a call was received by the HCP from the sales representative in that week
• Samples Dropped: # Brand drug samples received by the HCP in that week
• Physician Segment: A segment assigned for every HCP based on their value and relevance – High, Medium, Low
• Emails Delivered: # Emails delivered to the HCP through campaigns in that week
• Speaker Programs Attended: # Speaker Program events attended by the HCP in that week
• # Vouchers Dropped: # Brand drug vouchers/coupons received by the HCP in that week
• Specialty: Medical specialty of the HCP – Dermatologist, General Physician or Nurse Practitioner
Patient Data: Details of patient’s visit to HCPs by date
• Patient ID: Unique ID of the patient
• Physician ID: Unique ID of the physician/HCP
• Date of Visit: Date of patient’s visit to the HCP (spans from Jan’19 to Jan’20)
• Year of Birth: Patient’s year of birth
• Gender: Patient’s gender
• Geographical State: Patient’s state of residence in US geography
6 Copyright © 2022 Axtria Inc. All rights reserved.
4 EXPECTED SOLUTION
The model solution should predict the best possible channel for the HCP for the upcoming week (first week of Feb’20)
among three promotional channels – Sales Rep calls, Emails, and Sample Drops by utilizing Brand Rx (prescriptions) as the
maximization criteria.
The candidates must ensure that model predictions are fed through the promotional constraints shared and that the final
channel recommendations meet both the criteria – Brand Rx maximization and promotional constraints.
Promotional Constraints:
• Sales rep calls in last 12 months (including the promotion week to be optimized for) should not be more than:
o 48 calls for High Segment HCPs
o 24 calls for Medium Segment HCPs
o 12 calls for Low Segment HCPs
• Only 25% of the HCPs can be reached out through sample drops in any week
• Overall predicted Brand Rx (across all HCPs) should not deviate more than 10% than the immediate previous week
