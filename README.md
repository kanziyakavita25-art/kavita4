# **_Bank GoodCredit wants to predict credit score for current credit card customers._**

#  Dataset Overview – Bank GoodCredit Credit Risk Project

## Business Case:

Bank GoodCredit wants to assess the **creditworthiness** of its credit card customers by predicting if a customer is likely to **default** (i.e., become 30+ days past due).
This helps reduce credit risk and improve loan decisions.

**Target Variable:**
`Bad_label`

* `0` → Good credit history
* `1` → Bad credit history (default risk)

---

###  **Dataset Description**

The data is stored in a **MySQL database** with the following three main tables:

---

#### 1. **Cust\_Account**

Customer’s historical account and payment information.

* `customer_no`
* `opened_dt`, `last_paymt_dt`, `closed_dt`
* `cur_balance_amt`, `creditlimit`, `cashlimit`
* `paymenthistory1`, `paymentfrequency`
* `rateofinterest`, `actualpaymentamount`
* ... *(more account-specific fields)*

---

#### 2. **Cust\_Enquiry**

Contains credit enquiry history for each customer.

* `customer_no`
* `enquiry_dt`, `enq_purpose`, `enq_amt`
* Used to evaluate customer's recent credit-seeking behavior.

---

#### 3. **Cust\_Demographics**

Includes demographic and anonymized model features.

* `customer_no`
* `feature_1` to `feature_79`
* `Bad_label` (target variable)

---

### **Project Goal**

Build a classification model using this data to:

* Analyze customer behavior
* Select relevant features
* Predict default risk (Bad\_label)
* Evaluate performance using Gini score and decile ranking
