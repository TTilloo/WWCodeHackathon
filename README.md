# WWCodeHackathon
Women Who Code for Social Good Hackathon Project focusing on financial inclusion and behavioral metrics 

## Timeline
Oct 12 - Opening
  - have a list of variables to regress against payability (pred. lending, payday loan, low credit risk) -> have a clear hypothesis

Oct 14-15
  - do expoloratory analysis on our own

Oct 16-20 (work week)
  - block hours 9am-12pm (CST) / 7am-10am (PST)
  - work on code, final product, demo

Oct 21: finalize end product
Oct 22: deadline

<<<<<<< HEAD
## To do:
=======
# To do:
>>>>>>> 44aa8d45300b376d4f63a6846a4647d7e1dd166f
  - Oct 14:
      - decide on end product: visualization of the regression, data exploratory maps and graphs that proves our hypothesis (interactive web app from R, i.e. Shiny App)
  - Oct 15 & 16:
      - dive deep into the data: picking variables regarding payability (Vy & Tanvi)
      - decide on the details of the demographic characteristics of each personas (Tanvi)
  - Oct 17
      - data exploration: different maps and graphs (Vy ?)
  - Oct 18 & 19:
      - run regressions for each personas (Vy & Tanvi, split personas half half)
      - iterate regression -> visualize
      - visualize the code on Shiny app (Tanvi & Vy ?)
  - Oct 20:
      - demo/walkthrough (Tanvi / Vy split ?)

<<<<<<< HEAD
## Personas:
=======

# Personas:
>>>>>>> 44aa8d45300b376d4f63a6846a4647d7e1dd166f
  - A: likely rejected
  - B: complete opposite of A
  - C: basically the same, good candidate, 1 factor cannot control (race, etc.)  -> get access or no access
  - D: fall short -> give benefit of the doubt 

<<<<<<< HEAD
## Hypotheses:
=======
# Hypothesis:
>>>>>>> 44aa8d45300b376d4f63a6846a4647d7e1dd166f
1) worst persona better off by looking at the financial history using our regression -> we prove our model is better than the credit evaluation traditional model.
2) millions of america are subjected to snap shot of behaviors for lending decision. We believe that looking at one's financial history and behaviors over time is a better indicator and a more comprehensive evaluation of lendabiliy

## Methodology
1. Identify the elements that go into credit score model these days
  1.1 Payment History: This is one of the most significant factors in your credit score. It assesses whether you have paid your bills on time and includes information about late payments, accounts in collections, and any public records like bankruptcies or tax liens.
  1.2 Credit Utilization: This factor looks at the percentage of your available credit that you are currently using. Keeping your credit card balances low relative to your credit limits can positively impact your score.
  1.3 Length of Credit History: This considers the age of your credit accounts, including the average age of your accounts and the age of your oldest and newest accounts. A longer credit history often leads to a higher score.
  1.4 Types of Credit: Lenders want to see that you can handle different types of credit responsibly. This factor takes into account credit cards, installment loans, mortgages, and other types of credit accounts.
  1.5 New Credit Inquiries: Opening multiple new credit accounts in a short period can negatively affect your score. Each hard inquiry that occurs when you apply for credit can impact your score slightly.
  1.6 Public Records: This includes information about bankruptcies, tax liens, and civil judgments. These items can have a significant negative impact on your credit score.
  1.7. Total Debt: The total amount of debt you owe, particularly in relation to your credit limits, can influence your score.
  1.8 Available Credit: The total amount of credit available to you can affect your score. Having a higher credit limit, while maintaining low balances, is generally favorable.
  1.9 Payment Patterns: Some credit scoring models also consider the patterns of your payment history, such as the frequency and consistency of payments.
  1.10 Credit Mix: A diverse mix of credit types (credit cards, loans, mortgages) can positively impact your credit score
2. Recreate the credit score model in terms of payability: Regress those credit score to a variable of payability
3. Regress our chosen alternative variables against payability