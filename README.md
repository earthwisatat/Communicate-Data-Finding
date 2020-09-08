# Communicate-Data-Finding: Loan Data from Prosper
## by Wisatat

## Dataset

This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate, current loan status, borrower income, and so on.
For the purpose of this analysis we focused on the following:

-BorrowerAPR - The Borrower's Annual Percentage Rate (APR) for the loan.

-LoanStatus - The current status of the loan: Cancelled,  Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket.
-Occupation - The Occupation selected by the Borrower at the time they created the listing.
-EmploymentStatus - The employment status of the borrower at the time they posted the listing.
-EmploymentStatusDuration - The length in months of the employment status at the time the listing was created.
-ProsperScore - A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score.
-IncomeRange - The income range of the borrower at the time the listing was created.
-DebtToIncomeRatio - The debt to income ratio of the borrower at the time the credit profile was pulled. This value is Null if the debt to income ratio is not available. This value is capped at 10.01 (any debt to income ratio larger than 1000% will be returned as 1001%).
-IncomeVerifiable - The borrower indicated they have the required documentation to support their income.
-Recommendations - Number of recommendations the borrower had at the time the listing was created.
-AvailableBankcardCredit - The total available credit via bank card at the time the credit profile was pulled.



## Summary of Findings
- Normally, people with lower IncomeRange have higher BorrowerAPR at each individual ProsperScore.
- LoanStatus does not affect the BorrowerAPR and LoanOriginalAmount relationship.
- AvailableBankcardCredit and ProsperScore negatively correlated to BorrowerAPR. The high ProsperScore has a low BorrowerAPR and more range of AvailableBankcardCredit. In contrast, the most of low AvailableBankcardCredit has a low BorrowerAPR and BorrowerAPR.
- The Past Due LoanStatus have a higher BorrowAPR than Current, Completed, Chargedoff and Defaulted.
- The employment status of the borrowers are employed.
- The highest of borrowers in ProsperScore is 4.0, then 6.0 and 7.0 respectively


## Key Insights for Presentation

For the presentation, I just focus on features that could affect the BorrowerAPR, which are ProsperScore, IncomeRange and AvailableBankcardCredit. I started by showing the distribution of BorrowerAPR and AvailableBankcardCredit. Then, I showed the relationship between ProsperScore vs. BorrowerAPR with Various IncomeRange. I also investigated the effect of rating on relationship BorrowerAPR and ProsperScore, as well as the effect of rating on relationship between BorrowerAPR and IncomeRange.
