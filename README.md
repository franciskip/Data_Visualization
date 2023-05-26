# (Dataset Exploration Title)
## by Francis


## Dataset

This databset utilized in this project is prosperLoan Data which was obtained from https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv . This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.
The dataset contains some missing values and also not all the the features are essential, some variables which can answer research questions would be selected for analysis. Quite a number of variables which were redundant and thus were ignored. Only few variables about 16 were selected since they were features of interest (could answer research questions). Also, some observations (rows) with missing values were dropped.

## Summary of Findings
**The main features of interest from the prosper dataset are**
- factors that affect a loan's outcome status,
- factors that affects the borrower's APR or interest rate,
- ascertaining if there are differences between loans depending on how large the original loan amount was?

The BorrowerAPR distribution is a multimodal since it has atleast three peaks, the first smaller peak is observed between 0.0 & 0.1, then large peak at 0.2 and very high peak between 0.35 & 0.36, but above 0.4 BorrowerAPR the peak decreases. Thus BorrowerAPR is high between 0.35 & 0.36 and at around 0.2.

The  Stated Monthly income in the original data has a right long-tailed distribution 'right skewed'.There is high level of skewness and the far outliers are also observed when Stated Monthly Income  is above 100,000 so, thus it would be significant to transform or perform log scaling to this feature and check if there is improvement or outliers. After performing log-scaling on Stated Monthly income variable some outliers were observed above than 20K.

The distribution of original loan amount is a multimodal with various peak variations. Moreover, outliers were above 25000 are observed,this depicts that few individuals were granted huge amount of loans as compared to those who were given lower especeially those who granted loan amount in range of 15000 and below.
The current status of the loan has largest proportion of loan status followed by those who have completed there are few cases loan defaulters.
Most of the individuals who took loan prefer 36 months plan but few borrowers opted for 12 months term
There is high multicollinearity between LenderYield, BorrowerAPR and BorrowerRate.
It was observed that some factors that affect borrower's APR or interest rate are LoanOriginalAmount followed by MonthlyLoanPayment, DelinquenciesLast7Years, StatedMonthlyIncome,IsBorrowerHomeowner,ListingCategory

The correlation matrix heatmap and scatter plot, showed that a negative correlation exists between the BorrowerAPR and the LoanOriginalAmount and also the Borrower Interest Rate vs Loan Original Amount. Loan original amounts greater than $20,000 are much more prone to have lower Borrower APR and Borrower Interest Rate compared to lesser amount of $10,000 and below which are more likely to have higher Borrower APR and Borrower Interest Rate. Thus, there is clearly a negative correlation albeit a weak one.

The barplot and box plot shows Term have effect on Borrower Interest. A closer assessment of Term on Borrower APR, showed that average Borrower APR rates for borrowers who takes 12 month Term is lower than borrowers who take 36 and 60 months plans. The Borrower Rate, a 36 and 60 month Term would have a higher BorrowerRate than a loan of a 12 month Term.

The high income earners such as those who earn above `$100,000` got access to larger sizes of loans followed by those who earn between `$75,000-99,999`. On other hand low income earners such as those earning between `$1-$25,000` had access to the smallest size of loans. It seems the size of income is directly proportional to amount of loan that one can access the the higher the income the higher the loan that one can access, the lower the income the lower the loan that one can access.

There is is quite relatationship between employement status  and loan amount. Those who are employed have access to higher sizes of loans, followed by those who are self-employed. Also full time borrowers could access higher loan than part-time borrowers. Persons who are not employed could access the smallest sizes of loans.

Employement status has no significant  effect on term of loan since most of the borrowers prefer 36 months plan irrespective of employment status. Most of the employed indivuals prefer 36 months term and some 60 months plan. Most of borrowers who take 36 months plan are those who are employed followed by full time and others.

The borrower rate seems to be negatively correlated with monthly loan payment. Borrowers who chose 12 months plan are making higher monthly loan payments and their rate of borrowing (The Borrower's interest rate for the loan) is also low (between 0.05 and 0.18). On other hand borrowes who take 36 months and 60 months term make lower monthly loan payments and their Borrower's interest rate for the loan is high. 

Self-employed borrowers who took 60 months plan have highest average Borrower's Annual Percentage Rate (APR) compared to average borrower rate of employed, part-time, retired etc of the same plan.Part-time borrowers have the highest 12 months term average borrower rate ompared to average Borrower's Annual Percentage Rate (APR) of employed, part-time, retired etc of the same plan. Also the mean Borrower rate Self-employed borrowers who take 36 months term is the lowest compared average Borrower's Annual Percentage Rate (APR) of employed, part-time, retired etc of the same plan.

After excluding outliers it is clear Loan Status has some effect on relationship  between Stated Monthly Income and borrower rates. Since excecpt for loan status where 'Past Due (>120 days)' which exhibit moderate positive correlation between tated Monthly Income and borrower rates , most of the loan status such as Completed', 'Current', 'Past Due (1-15 days)', 'Defaulted','Chargedoff', 'Past Due (16-30 days)', 'Past Due (61-90 days)', 'Past Due (31-60 days)', 'Past Due (91-120 days)', 'FinalPaymentInProgress' which show oderate negative correlation between tated Monthly Income and borrower rates.

The borrowers who earn income range of $1-24999 have the highest average Borrower's Annual Percentage Rate (APR) for all terms (12, 36 and 60 months plans). On other hand borrowers who earn income of atleast $100,000 have the lowest average Borrower's Annual Percentage Rate (APR) especially those taking 12, and 60 months term.

There is positive correlation between Monthly Loan Payment and Loan Original Amount. Borrowers who took 12 months term loan pay more loan every month than those who took 36 and 60 months plan.

IsBorrowerHomeowner variable affect the relationship between loan status and Borrower's Annual Percentage Rate (APR). It seems borrowers who have competed loan and the current have lower  Borrower's Annual Percentage Rate (APR) as compared to those who have defaulted. Homeowners borrowers who have completed,current and those who have defaulted their loans have lower borrower's annual percentage rate (APR) than those who are not homeowners.|

The employment status has impact on the correlation between the original loan amount and The Borrower's Annual Percentage Rate (APR) for the loan. There is strong negative correlation between the original loan amount and the Borrower's Annual Percentage Rate (APR) for employed, full-time borrowers while the others can be characterized as moderately negative. However borrowes who are not employed exhibit no correlation or weak positive correlation.

## Key Insights for Presentation

We can see that there is high multicollinearity between LenderYield, BorrowerAPR and BorrowerRate and so LenderYield may be removed since it is redundant. Factors that affect borrower's APR or interest rate are mainly LoanOriginalAmount followed by MonthlyLoanPayment, DelinquenciesLast7Years, StatedMonthlyIncome,IsBorrowerHomeowner,ListingCategory

The high income earners such as those who earn above $100,000 got access to larger sizes of loans followed by those who earn between $75,000-99,999. On other hand low income earners such as those earning between $1-$25,000 had access to the smallest size of loans. It seems the size of income is directly proportional to amount of loan that one can access the the higher the income the higher the loan that one can access, the lower the income the lower the loan that one can access.

Employement status has no significant effect on term of loan since most of the borrowers prefer 36 months plan irrespective of employment status. Most of the employed indivuals prefer 36 months term and some 60 months plan. Most of borrowers who take 36 months plan are those who are employed followed by full time and others.
