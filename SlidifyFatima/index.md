----
title       : Developing Data Products - Course project
subtitle    : shiny application - Mortgage Loan Calculator 
author      : Fatima Mouaki
#hitheme     : tomorrow      # 
#widgets     : []            # {mathjax, quiz, bootstrap}
#mode        : selfcontained # {standalone, draft}
#knit        : slidify::knit2slides
---
  
## Sypnosis
  
  The loan amount, the interest rate, and the term of the mortage loan can have a dramatic effect on the total amount you will eventually pay every month. In this project, Loan payment application has been builed to estimate your monthly payment, and help make decision. 


---
  
## Methodoly
  
  Monthly LOan payment calculator has been builed using Shiny application. the calculation takes three inputs Loan Amount, Interest rate, and Term of the loan.

The formula used for calculating the monthly mortgage amount is as below

Monthly Payment = loan * (1 + i)^ n/((1 + i)^ n - 1)

where

1. loan = loan amount
2. i = interest rate per month (yearly interest rate / 12)
3. n = loan term in number of months
4. ^ = implies power of.


----
  
## Caluclation in R
  The function that calculate the mortage monthly payment is a follow:
  
  
  ```r
  function(AmountIn, MaturityIn, RateIn)
  {
  Amount<-as.numeric(AmountIn)
  Maturity<-as.numeric(MaturityIn)
  YRRate<-as.numeric(RateIn)
  MonthlyRate<-YRRate/12/100
  months<-Maturity*12
  pmt(Amount,months,MonthlyRate)
  }
  ```
  
  ```
  ## function(AmountIn, MaturityIn, RateIn)
  ## {
  ## Amount<-as.numeric(AmountIn)
  ## Maturity<-as.numeric(MaturityIn)
  ## YRRate<-as.numeric(RateIn)
  ## MonthlyRate<-YRRate/12/100
  ## months<-Maturity*12
  ## pmt(Amount,months,MonthlyRate)
  ## }
  ```

where pmt is a function in tvm package that calculates the mothly payment.

----
  
  ## Shiny application
  
  Here is the link to the aplication : 
  
  URL: https://fatimamouaki.shinyapps.io/shiny/
  
  
  
  
  
  
  
  

