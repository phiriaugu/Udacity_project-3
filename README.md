# Prosper Loan Dataset Exploration Report
## by Augustine Phiri


## Dataset

> In downloaded Prosper Loan Dataset from the link provided by udacity in the classroom. The data set contained 113,937 loans with 81 variables on each loan. The dataset included loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.
> After after downloading `ProsperLoanDataset.csv` file, I saved in the project two folder and then loaded it in the project notebook. After assess data, I found out that `LoanOriginationDate` had a wrong data type, and therefore I converted the its data type from string into datetime stamp. Some columns names were not in the standard form, so I Rename Columns into standard form (`loan_clean.rename(columns = {"ListingCategory (numeric)":"ListingCategory", "BorrowerAPR": "BorrowerApr"}, inplace = True)`.Lastly, I removed all columns that I was not interested to use in my analysis.


## Summary of Findings

> After visual exploration of  main variables of interest, which included `Loan Status`. The results showed that there was highest concentration of income between 25,000 and 49,999 USD($). looking at the distribution of `Borrower`s interest Rate (BorrowerRate)`, the distribution of `borrower interest rates` was right skewed, and most of the `borrowers` fell within the `higher interest rate` loans.
> After plotting bar graph for Loan Status, I combined all past Due in the `Loan Status` column to make my visualization simple and very clear, then, looking at the graph, the majority of loans were either in current or completed status.

> Coming up with percentages of loans in each status, it was observed that about 50% of all `Prosper loans` are in `current state` and being paid by `Prosper's borrowers`, 34 percent are `completed`, about 11% of Prosper's loans were `charged off`, 4 % were `defaulted` and about 0% percent of loans are `past due`.

> Plotting `Loan Original Amount` bar standard plot, the Loan orginal amount had a long-tailed distribution with a lot of loans on the low original amount end, and few on the high original amount end. When I tried to visulize on a log-scale, the `Loan original amount` distribution looked roughly `bimodal` with peaks on `10000`, `20000`, `22000`, `32000`, `34000` and `35000`.


## Key Insights for Presentation

> The project was focused much on answering the following questions:

- What factors affect a loan’s outcome status?
- What affects the borrower’s APR or interest rate?
- Are there differences between loans depending on how large the original loan amount was?

> So in summary, the factors that most seemed to affect a loan's outcome was the amount of money borrowed and the interest rate of the loan. The Higher the interest rate, and high loan values are likely to be past due. The employment statues had an enfluence of borrowers Apr. This was seen as the Employed individuals had the highest spread in the data, meaning that most of them were in current loan status. The higher the original loan amount the higher the loan appers to be.

> The factors that most affected the borrower's interest rate were investigated further down by the correlation heat matrix. None of the features had a strong correlation but the highest was the credit score. As the borrower's credit score increases, the interest rate decreases.

> Despite that there is no much interesting difference between the categories of Loan Status and the borrower interest rate, charged off and defaulted loans are higher than the rest of loan status. looking at the correlation between loan status to the original loan amounts, it actually appears as though the larger the loan amount, the more chance of being in current loan status.