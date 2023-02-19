# Lending Club Case Study
> Lending Club is a finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:

    If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
    If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company


## Table of Contents
* [Problem Statement](#problem-statement)
* [General Info](#general-info)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## Problem Statement
### Business Understanding
When a person applies for a loan, there are two types of decisions that could be taken by the company:

Loan accepted: If the company approves the loan, there are 3 possible scenarios described below:

    Fully paid: Applicant has fully paid the loan (the principal and the interest rate)

    Current: Applicant is in the process of paying the instalments, i.e. the tenure of the loan is not yet completed. These candidates are not labelled as 'defaulted'.

    Charged-off: Applicant has not paid the instalments in due time for a long period of time, i.e. he/she has defaulted on the loan

Loan rejected: The company had rejected the loan (because the candidate does not meet their requirements etc.). Since the loan was rejected, there is no transactional history of those applicants with the company and so this data is not available with the company (and thus in this dataset)

### Business Objectives
This company is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures. Borrowers can easily access lower interest rate loans through a fast online interface.

Like most other lending companies, lending loans to ‘risky’ applicants is the largest source of financial loss (called credit loss). Credit loss is the amount of money lost by the lender when the borrower refuses to pay or runs away with the money owed. In other words, borrowers who default cause the largest amount of loss to the lenders. In this case, the customers labelled as 'charged-off' are the 'defaulters'.

If one is able to identify these risky loan applicants, then such loans can be reduced thereby cutting down the amount of credit loss. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. The company can utilise this knowledge for its portfolio and risk assessment.

To develop your understanding of the domain, you are advised to independently research a little about risk analytics (understanding the types of variables and their significance should be enough).

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## General Info
    Steps for EDA :
        Data Understanding
        Data Cleaning
        Univariate Analysis
        Bivariate Analysis
        Multivariate Analysis
        Conclusion
- Data Set : Loan Lending Club loans

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Conclusions
Factor whether an applicant will be Defaulter:

Continuous Variable:
   1. LOAN_AMOUNT : Loan amount greater than 15000 dollors have higher default rate
   2. FUNDED_AMOUNT : Funded amount greater than 15000 dollors have higher default rate
   3. FUNDED_AMOUNT_INVESTED : Funded amount invested greater than 15000 dollors have higher default rate
   4. INTEREST_RATE : As Interest rate increases the default rate increases steeply
      (5, 10]-> 6.739748%
      (10, 15]-> 14.820089%
      (15, 20]-> 24.826918%
      (20, 25]-> 38.441558%
   5. ANNUAL_INCOME : As the annual income increase the default rate decreases
   6. DTI : As dti increase the default rate increases
   7. MONTHS_SINCE_LAST_DELINQ : Crime committed between 90 to 110 days have higher default percent

Categorical Variable:
   1. TERM : 60 months term have a higher default rate than 36 months term
   2. GRADE : As the Grade decreases (A B C D E F G) default rate increases
   3. SUB_GRADE : As the Sub Grade decreases (A1 A2 B1 B2.....) default rate increases
   4. VERIFICATION STATUS : Percent of loan defaulted is higher for verifed borrowers
   5. PURPOSE : Small business borrowers have high default rate
   6. PUBLIC_BAKRUPTIES_RECORD : One or more pubilc bankruptices have higher default rate
   7. STATE : Percent of loan defaulted is very high for state NE and high for NV and SD

Other suggestions:
    INTEREST RATE AND PUBLIC BANRUPTIES RECORD : Borrowers with lower interest rate and 2 public bankurpties have defaulted
    INSTALLMENT AND PUBLIC BANRUPTIES RECORD : Borrowers with higher installment and 2 public bankurpties have defaulted
    ANNUAL INCONE AND PUBLIC BANRUPTIES RECORD : Borrowers with higher Income and 2 public bankurpties have defaulted

Decisive Factor whether an applicant will be Defaulter:
    FUNDED_AMOUNT_INVESTED
    INTEREST_RATE
    ANNUAL_INCOME
    DTI
    TERM
    GRADE
    SUB_GRADE
    PURPOSE
    PUBLIC_BAKRUPTIES_RECORD   

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
    pandas - 1.3.4
    numpy - 1.20.3
    matplotlib - 3.4.3
    seaborn - 0.11.2

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was group case study for an online advance course.
- https://www.geeksforgeeks.org/
- https://seaborn.pydata.org/
- https://pandas.pydata.org/
- https://learn.upgrad.com/


## Contact
Created by [@vkarkera]


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->