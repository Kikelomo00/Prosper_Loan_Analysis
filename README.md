# Prosper Loan Data Exploration
## by (Abdurrahman Kareemat)


## Dataset

The dataset is a loan dataset of a lending company Prosper. It consists of 113,066 rows and 17 columns
Variables description link https://rstudio-pubs-static.s3.amazonaws.com/86324_ab1e2e2fa210452f80a1c6a1476d7a2a.html .
The original dataset consists of 113,937 rows and 81 columns. I chose columns based on my variables of interest and created a new dataframe consisting of 17 columns and 113,937 rows before I went on to wrangle. I changed columns to their appropriate data types and created appropriate functions.  There were duplicate loan keys(i.e the id) but no duplicate record, this was due to some records having 2 prosper score but all other columns had the same thing. I dropped the column prosper score, which led to the presence of duplicate records and then dropped duplicate rows. I dropped prosper score because I was working with prosper rating. I also created a new column LoanStatusReviewed to compress the column Loan Status which had multiple Past Due with days into a single 'Past Due'. 

## Summary of Findings

My main variables of interest were the loan status and ratings. The ratings was introduced into the Prosper system in 2009 and we could see that the probablity of low ratings defaulting payments is higher than higher ratings. While about 83% of loans were either completed, current or had their final payment in progress. 17% of the loans were charged off or defaulted. The most common ratings of Borrowers was the average i.e 'C'. There is a bit of a relationship between my two main variables,I saw that low ratings had more charged off and defaulted loans. Prosper gives loans on 3 different terms, i.e. 12,36 and 60 months. Most of the loans were given on 36 months terms with less than half the number of 36 as 60 months and very few on 12 months term. Each term had a large amount of outliers in their relationships to the loan amount. 60 month loans have higher loan amounts, followed by 36 and then 12 months. Higher loan amounts have a longer.
period of payment. 36 month terms have  higher interest rates. 
Loans were mostly given to employed people and people with an income of 25,000 dollars and above.
There is no strong relationship between loan amount and borrower's rate. Most Borrower's took loan out for Debt Consolidation, other frequent reasons people took out loan include others, home improvement and business. 
Most  Borrowers had low debt to income ratio of mostly between 0 and 1.

## Key Insights for Presentation

Relating my 2 main variables of interest, we could see a higher number of people defaulted and had their loans charged off compared to other ratings.

The prosper rating enabled prosper determine its rate and loan amount. Low risk ratings could loan a higher amount with lower rates while high risk ratings could not necessarily do the same. High rated Borrowers that borrow a high amount have high income range. Poor ratings were as a result of high debt to income ratio. People with good ratings majorly had low debt to income ratio and majority are current on their loan or have completed it. 

Most people took out loans for debt consolidation, they also took out loans for home improvement and business. People who took out loans for business purpose charged off and defaulted the most. 

Looking at the effect of the introduction of the rating system in prosper, we can see a lesser proportion of charged and defaulted loan in comparison to the years before. Also the introduction led us to see that good  ratings had lower rates and higher loan amounts. With this introduction, it is seen that years before have had exceedingly high interest rates like 50%.