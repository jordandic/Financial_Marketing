# Financial_Marketing
This project uses ensemble ML algorithms from the Scikit-learn library to classify financial transactions and users based on demographic, financial, and marketing campaign-related data. The goal of this classification is to determine which user transactions are most likely to translate into a subscription to a term deposit product with the goal of sending targeted ads to those users.
Descriptive information for the study and the dataset:
Link: http://archive.ics.uci.edu/ml/datasets/Bank+Marketing 
Study Implications: There are two datasets containing all the instances. bank-full.csv is the chosen one to develop our model since it focuses on information which is less dependent on macro-economic factors. The reasoning behind this is that macro-economic factors will likely dictate how much the bank should scale up or down marketing spend, but it should not be the basis for determining who should be included in the target market. Macro-economic factors are relatively unpredictable and shouldn't necessarily be the basis of developing a target market in any company's overall marketing strategy. Instead, for the purposes of this study, only personal demographic information is used. Furthermore, other demographic information, like 'job' and 'loan,' may be sufficient in reflecting the current implications of the macro-environment on the individual at the micro-level, which is what this study focuses on. In a regression model, the macro-level factors for social and economic context would be included. The ultimate implication of this classification study is to determine which customers are most likely to subscribe to a loan deposit, and therefore how the company ought to select its target market, and how to position its loan products to that cohort. Ultimately, this study will aid the bank in developing it's marketing strategy including decisions related to product, price, place, and promotions. 

Data Description
- Input Variables:
Demographic Variables:
1 - age (numeric)
2 - job : type of job (categorical: 'admin.','blue- collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown') 
3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed) 
4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown') 
5 - default: has credit in default? (categorical: 'no','yes','unknown') 
6 - housing: has housing loan? (categorical: 'no','yes','unknown') 
7 - loan: has personal loan? (categorical: 'no','yes','unknown') 
Last Contact from the Current Campaign Variables:
8 - contact: contact communication type (categorical: 'cellular','telephone')
9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
10 - day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
Other Attribute Variables:
12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact) 
13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted) 
14 - previous: number of contacts performed before this campaign and for this client (numeric)
15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')

Output variable (Target Variable):
16 - y - has the client subscribed to a term deposit? (binary: 'yes','no') 

Omitted Variables:
Social and Economic Context Variables:
- emp.var.rate: employment variation rate - quarterly indicator (numeric) 
- cons.price.idx: consumer price index - monthly indicator (numeric) 
- cons.conf.idx: consumer confidence index - monthly indicator (numeric) 
- euribor3m: euribor 3 month rate - daily indicator (numeric) 
- nr.employed: number of employees - quarterly indicator (numeric) 
