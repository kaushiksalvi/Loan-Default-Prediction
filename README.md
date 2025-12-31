# Loan Default Prediction Using Machine Learning

## Project Overview
This project focuses on predicting whether a loan applicant will default on repayment using machine learning techniques. The objective is to support financial institutions in making data-driven lending decisions by identifying high-risk applicants at an early stage.

---

## Dataset Information
- Dataset contains more than 170,000 loan records
- Final dataset reduced to 22 important features
- Includes borrower details, loan attributes, and repayment history
- Severe class imbalance handled using SMOTE

Dataset Source: Public loan dataset (e.g., Lending Club)

---

## Cloumns Description 

loan_amnt
The total loan amount applied for by the customer, in USD.

term
The duration of the loan. Usually 36 months or 60 months.

int_rate
The interest rate charged on the loan (percentage).

installment
The monthly EMI amount the borrower has to pay.

grade
Overall loan grade given by the lender based on risk (A is best, G is worst).

sub_grade
More detailed version of grade (example: A1, A2, B3). It gives finer risk detail.

emp_length
Number of years the borrower has been employed.

home_ownership
The type of house ownership: RENT, OWN, or MORTGAGE.

annual_inc
Annual income of the borrower in USD.

verification_status
Whether the borrower’s income was verified or not (Verified, Source Verified, Not Verified).

loan_status
Target column. Shows whether the loan is fully paid, charged off, defaulted, etc.

purpose
Reason for taking the loan, like debt consolidation, credit card, medical, car, etc.

dti
Debt-to-Income ratio. It shows how much of the borrower’s income is already used to pay debts.

delinq_2yrs
Number of times the borrower was late on payments in the last 2 years.

inq_last_6mths
Number of credit inquiries made by the borrower in the last 6 months.

open_acc
Number of currently open credit accounts (active loans, credit cards).

pub_rec
Number of public negative records like bankruptcies or legal issues.

revol_bal
Total revolving credit balance (mainly credit card balance) in USD.

revol_util
Percentage of used revolving credit compared to total available credit.

total_acc
Total number of credit accounts the borrower has ever had (open + closed).

initial_list_status
Whether the loan was initially listed as whole loan or fractional loan.

application_type
Whether the loan application was made individually or jointly.

---

## Deleted Columns Description

id – Unique identifier, no predictive value

member_id – Identifier only, not useful for prediction

funded_amnt – Redundant with loan amount

funded_amnt_inv – Duplicate funding information

pymnt_plan – Mostly single value, low information

out_prncp – Post-loan outstanding amount (data leakage)

out_prncp_inv – Investor version of outstanding principal

total_rec_prncp – Post-loan repayment info (leakage)

total_rec_int – Interest received after loan issuance

total_rec_late_fee – Known only after repayment

total_pymnt – Target leakage (depends on loan outcome)

total_pymnt_inv – Investor repayment info

last_pymnt_amnt – Available only after payments start

last_pymnt_d – Post-loan date information

next_pymnt_d – Not available at loan approval time

issue_d – Time-based leakage / not needed

recoveries – Only for defaulted loans (leakage)

collection_recovery_fee – Recovery-related leakage

collections_12_mths_ex_med – Sparse and low impact

policy_code – Constant value column

acc_now_delinq – Almost always zero, low variance

tot_coll_amt – High missing values

tot_cur_bal – Many missing values

open_acc_6m – Incomplete recent account data

open_il_12m – Sparse short-term credit info

open_il_24m – Redundant short-term account data

open_rv_12m – Low contribution recent revolving data

open_rv_24m – Redundant with other credit features

max_bal_bc – High missing values

all_util – Inconsistent utilization data

total_bal_il – Redundant balance information

total_rev_hi_lim – Correlated with other credit limits

inq_fi – Sparse inquiry data

total_cu_tl – Low relevance credit usage feature

title – High cardinality text column

emp_title – Textual, high variance, already captured via emp_length

desc – Free text, noisy, not structured

zip_code – High cardinality, limited predictive value

addr_state – Weak geographical impact

earliest_cr_line – Converted indirectly through credit history

annual_inc_joint – Large missing values (joint loans only)

dti_joint – Only for joint applicants

verification_status_joint – Sparse joint loan feature

mths_since_last_delinq – High missing values

mths_since_last_record – Sparse and inconsistent

mths_since_last_major_derog – Mostly missing

mths_since_rcnt_il – Incomplete installment history

il_util – High missing rate

inq_last_12m – Redundant with inquiry features

---

## Technologies Used
- Programming Language: Python
- Libraries: Pandas, NumPy, Scikit-Learn
- Visualization: Matplotlib, Seaborn
- Techniques: Exploratory Data Analysis, Feature Engineering, SMOTE

---

## Project Workflow
1. Data cleaning and handling missing values
2. Exploratory Data Analysis (EDA)
3. Feature selection and categorical encoding
4. Feature scaling
5. Handling class imbalance using SMOTE
6. Model training and evaluation

---

## Machine Learning Model
- Algorithm used: Random Forest Classifier
- Multiple machine learning models were evaluated during experimentation
- Random Forest was selected due to:
  - High prediction accuracy
  - Robust and stable performance
  - Interpretability through feature importance

---

## Model Performance
- Achieved approximately 90% accuracy
- Demonstrated stable predictions on unseen data

---




