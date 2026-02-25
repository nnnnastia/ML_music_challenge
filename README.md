# Vodafone Music Challenge
### 📌 Project description

The goal of the project is to build a machine learning model to predict the probability that a mobile operator subscriber will install and pay for the Vodafone Music service within one month after the scoring date.
The model is used to improve the effectiveness of marketing campaigns by targeting the most promising customers.

The task belongs to the binary classification type.
Target variable:

- 1 – the subscriber installed and paid for the first month of using the Vodafone Music service;

- 0 – the subscriber did not install the service within a month after the scoring date.

The model should predict not just the class, but the probability of installing the service, allowing the business to flexibly choose the customer selection threshold for the campaign.

Evaluation metric: **ROC-AUC**

---

### 🎯 Business goal

The model results can be used to:

- optimize advertising costs
- increase conversion rates
- increase subscription revenue

Instead of sending offers to all subscribers, the company can choose, for example, the top 20% of customers with the highest predicted probability of installation.

---

### ⚖️ Business Risk Analysis

**False Positive (FP):** the model predicts installation, but the customer does not install the app.  
_Consequence:_ unnecessary marketing costs.

**False Negative (FN):** the model predicts non-installation, but the customer **would have installed** the app.  
_Consequence:_ loss of potential profit.

In the telecom industry, digital marketing (SMS, push) has a relatively low cost, so minimizing FN is often more critical in terms of long-term revenue.
---

### 📂 Data description

The data contains information about subscribers and their behavior.

Main groups of characteristics:

- Device characteristics
- General characteristics
- User activity features
- All costs
- Recharge statistics
- Voice costs & duration
- Network action stats
- Other Essential Features (including data traffic)
- SMS from Services
- Interests data
- Previous campaigns results — participation in previous campaigns

Aggregates are calculated for:
- m1 — previous month
- m2 — second previous month
- m3 — third month
