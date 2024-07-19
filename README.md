# Hotel Booking Demand : Customer Data Analysis

## Business Problem Understanding
**Context**

In the hospitality industry, efficient management of hotel reservations is necessary to optimize revenue. 
A study conducted by D-Edge Hospitality Solutions found that the cancellation rate across various booking channels in Europe reached almost 40% in 2018 ([Source](https://www.d-edge.com/how-online-hotel-distribution-is-changing-in-europe/)). 
Booking cancellations can potentially disrupt operational schedules and reduce potential revenues. 
Being able to predict booking cancellations is important for implementing strategies to reduce their impact on scheduling and operations.

**Problem Statement**

Booking cancellation can cause potential revenue loss, underutilization of hotel assets, and operational schedule disruption. It is difficult to predict cancellation in advance. Therefore, it is necessary to develop a solution that could predict booking cancellations in advance to minimize potential loss and disruptions.

**Goals**

The goal is to develop a model that could accurately predict booking cancellations before they occur. This model uses historical customer booking data to identify potential cancellations. This could help the hotel in implementing proactive measures to the particular booking such as dynamic pricing or discount offers to discourage cancellation or mitigate potential revenue loss.

**Analytic Approach**

The approach involves gathering historical booking dataset, preprocessing the data by handling missing values, outliers, and data duplicates, analyzing patterns and correlations in the data, encoding categorical and numerical features from the dataset, and training various ML models and its variations to predict the probability of a booking being canceled by assessing its evaluation metrics to ensure it meets the business goals.

**Evaluation Metric**

The performance of the models will be evaluated using metrics such as precision, recall, and F1 score. The primary metric for evaluation will be selected based on its relevance to the business context.

(Positive = Flagged as potentially canceled booking)

* Precision

  The ratio of correctly predicted cancellations to all predicted cancellations (true positives / (true positives + false positives)).

  High precision means that when a booking is predicted to be a cancellation, it is likely correct. This is important to avoid unnecessary actions on bookings that will not cancel.

* Recall

  The ratio of correctly predicted cancellations to all actual cancellations (true positives / (true positives + false negatives)).

  High recall means fewer actual cancellations are missed. This is important if the business wants to ensure that most potential cancellations are identified.

* F1-score

  The harmonic mean of precision and recall (2 * (precision * recall) / (precision + recall)).

  F1-score is used when a balance between catching most cancellations (recall) and ensuring that flagged cancellations are mostly correct (precision) are required. This important if both missing cancellations and misclassifying non-cancellations have comparable business costs.


In this case, if the proactive measure to prevent potential cancellations is to offer discounted pricing (for example, 30%) to discourage cancellations, the effects are as follows:

  **False Negatives:** Loss of 100% of the potential revenue due to the loss of a customer who cancels but was not predicted to cancel.

  **False Positives:** Loss of 30% of the potential maximum revenue because a discount was offered to a customer who would not have canceled and would have paid full price.

Therefore, it is more important to minimize false negatives because their potential loss is higher. As such, the primary evaluation metric for this project will be recall.
