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

=======
## To do:
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
    
=======
## Personas: (low and income, multicultural - non-white, multigenerational, number of the dependants, presence of 65+ age, 
  - A: likely rejected
  - B: complete opposite of A
  - C: basically the same, good candidate, 1 factor cannot control (race, etc.)  -> get access or no access
  - D: fall short -> give benefit of the doubt 

=======
## Hypothesis:
1) worst persona better off by looking at the financial history using our regression -> we prove our model is better than the credit evaluation traditional model.
2) millions of america are subjected to snap shot of behaviors for lending decision. We believe that looking at one's financial history and behaviors over time is a better indicator and a more comprehensive evaluation of lendabiliy

=======
## Methodology
1. Identify the elements that go into credit score model these days
  - 1.1 Payment History: This is one of the most significant factors in your credit score. It assesses whether you have paid your bills on time and includes information about late payments, accounts in collections, and any public records like bankruptcies or tax liens.
  - 1.2 Credit Utilization: This factor looks at the percentage of your available credit that you are currently using. Keeping your credit card balances low relative to your credit limits can positively impact your score.
  - 1.3 Length of Credit History: This considers the age of your credit accounts, including the average age of your accounts and the age of your oldest and newest accounts. A longer credit history often leads to a higher score.
  - 1.4 Types of Credit: Lenders want to see that you can handle different types of credit responsibly. This factor takes into account credit cards, installment loans, mortgages, and other types of credit accounts.
  - 1.5 New Credit Inquiries: Opening multiple new credit accounts in a short period can negatively affect your score. Each hard inquiry that occurs when you apply for credit can impact your score slightly.
  - 1.6 Public Records: This includes information about bankruptcies, tax liens, and civil judgments. These items can have a significant negative impact on your credit score.
  - 1.7. Total Debt: The total amount of debt you owe, particularly in relation to your credit limits, can influence your score.
  - 1.8 Available Credit: The total amount of credit available to you can affect your score. Having a higher credit limit, while maintaining low balances, is generally favorable.
  - 1.9 Payment Patterns: Some credit scoring models also consider the patterns of your payment history, such as the frequency and consistency of payments.
  - 1.10 Credit Mix: A diverse mix of credit types (credit cards, loans, mortgages) can positively impact your credit score
3. Recreate the credit score model in terms of payability: Regress those credit score to a variable of payability
4. Regress our chosen alternative variables against payability

=======
## Variables
Year: 2009-2021

### FAMILY LEVEL DATA

####  Income and Expenditure 

a) Static Income and Expenditure Profile 
- ER78091  	A31 DOLLARS RENT
- ER78093  	ACCURACY OF RENT
- ER78098  	A33 GOVT PAY PART RENT?
- ER78114  	A42A FUEL EXPENSE PER
- ER78117  	A42C COMBINED GAS/ELECT EXPENSE
- ER78122  	A44 TELEPHONE EXPENSE PER
- ER78125  	A45B TOTAL OTR UTILITIES
- R81914  	TOTAL EXPENDITURE (mortgage & property tax - own a home)
- ER81915  	TOTAL CONSUMPTION WITH RENTAL VALUE (rent value - rent) -> compare with household income 
- ER81775  	TOTAL FAMILY INCOME-2020
- ER81630  	OVERTIME INCOME OF REF PERSON-2020
- ER81631  	ACC OVERTIME INCOME OF RP-2020 -> hustle (extra money)
- ER79460  	G44D WTR ALIMONY INCOME-RP
- ER79508  	G44G WTR ANY OTHER INCOME-RP
- ER72940  	F82 WTR SCHOOL EXPENSES
- ER81354  	M4 WTR DONATED TO ORGANIZATION FOR NEEDY
  

#### Financial Status 

a) Static Financial profile   
- ER81836  	IMP WEALTH W/O EQUITY (WEALTH1) 2021 -> change over year (up and down)
- ER81837  	ACC WEALTH W/O EQUITY (WEALTH1) 2021
- ER78951  	F67 LOAN PMT AMT PER #1
- ER78950  	F67 LOAN PAYMENT AMT #1
- ER80001  	W38A WTR HAVE CREDIT/STORE CARD DEBT
- ER79062  	GCOVID16 HOW MNG FINAN - TAKE OUT A LOAN
- ER77487  	IMP WTR STUDENT LOAN DEBT (W38B1) 2019
- ER77488  	ACC WTR STUDENT LOAN DEBT (W38B1) 2019
- ER77489  	IMP VAL STUDENT LOAN DEBT (W39B1) 2019
- ER77490  	ACC VAL STUDENT LOAN DEBT (W39B1) 2019

b) Financial Behavior 
- ER81354  	M4 WTR DONATED TO ORGANIZATION FOR NEEDY
- ER34995  	H5N7/H50G WTR CHNGE HNDLNG MONEY ISSUE21
- H11E      WTR DIFFICULT MANAGE MONEY-SP
- ER80697  	H11E WTR DIFFICULT MANAGE MONEY-RP
- ER73374  	G44E WTR HELP FROM RELATIVES-RP
- ER73376  	AMOUNT HELP FROM RELATIVES PER-RP
- ER73375  	AMOUNT HELP FROM RELATIVES-RP
- ER73377  	ACCURACY OF HELP FROM RELATIVES-RP
- ER73888  	W38B WTR HAS LOANS FROM RELATIVES
- ER73905  	W39B4 AMOUNT LOANS FROM RELATIVES
- ER72983  	GSD10 WTR PUT OFF PAYING BILLS -> this variable is only specific to 2019 because of 2018 govt shut down


#### Education and Employment 

a) Employment Behavior 
-   ER78408   	BC8 WTR UNEMPLOYED(RP) -> unemployed during any time in 2020 
-   ER78427     C7 WTR OUT OF LABOR FORCE (RP) -> data exists for every 2 years since '03
-   ER78477   	BC68 CKPT: WTR NOT WRKING/NOT LOOKING
-   ER81189  	  L70 #YRS WRKD SINCE 18-RP
-   ER79561  	  WTR WORK HRS PRO PRACTICE/TRADE-SPOUSE
-   ER79562  	  G18GIGA WTR GIG WORK - SP
-   ER79933  	  W10 WTR OWN BUSINESS/FARM

b) Education 
- ER76916  	L49 GRADE OF SCHOOL FINISHED-RP


  


- R81336  	IMMSTATUS - SP







- ER76690  	H61D2 WTR ANY FU MEMBER HLTH INSURANCE
- ER76692  	H61J PER FU INSURANCE PREMIUMS

- ER72413  	BC62 WTR EVER WORKED
- ER72407  	BC60ACKPT WTR CURRENTLY WORKING
- ER72986  	GSD13 WTR SOLD BELONGINGS
- ER72985  	GSD12 WTR USED MONEY FR RETIREMENT ACCTS -> this variable is only specific to 2019 because of 2018 govt shut down

- ER72968  	F91 COST OF OTR RECREATION LAST YEAR -> this variable is only specific to 2019 because of 2018 govt shut down
- ER72727  	F1H HOW OFTEN INTERACT W/OTHERS-RP
- ER72728  	F1I HOW OFTEN PHYSICAL ACTIVITIES-RP
- ER72729  	F1J HOW OFTEN MENTAL ACTIVITIES-RP
- ER72726  	F1G LEISURE HRS-REF PERSON
- ER72725  	F1F EDUCATIONAL ACTIVITY HRS-REF PERSON
- ER72724  	F1E VOLUNTEERING HRS-REF PERSON
- ER72723  	F1D2 ADULT CARE HRS-REF PERSON
- ER72722  	F1D CHILD CARE HRS-REF PERSON
- ER72721  	F1C SHOPPING HRS-REF PERSON
- ER72720  	F1B PERSONAL CARE HRS-REF PERSON
- ER72794  	F19 WTR FOOD DELIVERED TO HOME -> used food stamp last month
- ER72804  	F23 WTR FOOD DELIVERED TO HOME -> not used food stamp last month
- ER72790  	F17 WTR BUY FOOD TO USE AT HOME
- ER72792  	F18 COST OF FOOD AT HOME PER -> used food stamp last month
- ER72802  	F22 COST OF FOOD AT HOME PER -> not used food stamp last month
- ER72796  	F20 COST OF DELIVERED FOOD PER (time unit) -> used food stamp last month
- ER72806  	F24 COST OF DELIVERED FOOD PER (time unit) -> used food stamp last month
- ER72799  	F21 COST OF FOOD EATEN OUT PER (time unit) -> used food stamp last month
- ER72809  	F25 COST OF FOOD EATEN OUT PER (time unit) -> used food stamp last month
- ER72958  	F89 COST OF CLOTHING LAST YEAR
- ER72963  	F90 COST OF TRIPS, VACATIONS LAST YEAR
- ER72964  	F90 TIME UNIT FOR TRIPS, VACATIONS
- ER72968  	F91 COST OF OTR RECREATION LAST YEAR
- ER72953  	F88 COST OF HHOLD FURNISHINGS LAST YEAR



-   

Demographic:
- ER76960  	L68A RELIGIOUS PREFERENCE-RP
- R76897  	L40 RACE OF REFERENCE PERSON-MENTION 1
- ER76898  	L40 RACE OF REFERENCE PERSON-MENTION 2
- ER76899  	L40 RACE OF REFERENCE PERSON-MENTION 3
- ER76900  	L40 RACE OF REFERENCE PERSON-MENTION 4
- ER76901  	L40A ASIAN ETHNICITY OF REFERENCE PERSON
- ER76902  	L41 ETHNIC GROUP-RP
- ER76906  	YEAR HIGHEST EDUCATION UPDATED-RP
- ER72747  	F6CCKPT WTR FU MEMBER UNDER 16 LAST YR
- ER72745  	F7 CKPT: WTR CHILD 5-18 IN FU LAST YEAR
- ER72767  	F7CCKPT WTR FU MEMBER 60+ LAST YR


Key words:
Loan/lending:
- Mortgage
- Refinance
- foreclosure, bankrupt
  
Living expense
- rent, grocery, insurance, gas
- utilities, utility, eletricity, water, heating, wifi
- house, mortgage, propterty tax,

=======
10/16/23
- Problem: only have variables about repayment loans for car and mortgage, no variables on repayment of other loans, no variables on paying utilities
- Solutions:
    - Look at behavioral of an individual over time! (finish highschool, move out by 18, etc.)
    - Research on Behavioral changes as indicator of trustfulness, trustworthiness, etc. that relate to payability: Character Lab (UPenn) -> child dev -> prediction of child flourish, psychology of money (Book)
    - Taking a multicultural, multigenerationl perspective, justifying the take on behavioral and cultural turn
    - Controlling: first gen (white, hispanic, etc.)
        control for baseline characteristics to make arg tighter, this person have the non-control feature -> always the preferred candidate
      A person's payability depends on family level payability (multicultural and multigenerational household)
      How should financial institution go about looking at the financial data of a family

Credit payment: Ability and willingness to pay to debt (equally determine how they pay for that): 
  - Impatience, impulsiveness (presence bias, discount future, borrow today, harm future by taking on debt today) -> high borrow today = high default in the future
  Risk tolerance and trustworthiness
  - self eval fin health -> strong presence bias -> more risky
  Variables:
  - borrow for post secondary education
  - laid off
  - 
