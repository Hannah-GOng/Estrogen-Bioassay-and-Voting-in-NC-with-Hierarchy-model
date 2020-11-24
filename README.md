# Estrogen-Bioassay-and-Voting-in-NC

## PART I

### Introduction
The group of hormones known as estrogens are responsible for regulating bones, skin, and organ growth,among other essential bodily functions. Estrogens often serve to disrupt processes within the endocrine system (hormone pathways), which is completely benign when occurring as a natural bodily process. Over the past ten years, however, the increased production of many synthetic and plant products has raised concerns over the potentially adverse impacts these chemicals have on the human body. Chemicals that have estrogenic effects have been labeled environmental estrogens. One method for testing the estrogenic effects of these environmental estrogens is the rat uterotrophic bioassay, which observes the uterus growth response to varying levels of estrogen agonists and antagonists. The expectation is that uterus weight will increase as the amount of prescribed estrogen agonist increases and decreases as the amount of estrogen antagonist increases.

This analysis examines the data from one such uteroptophic bioassay study to determine if the process was successful in identifying both the estrogenic effects of environmental estrogens, and the anti-estrogenic effects of antagonist chemicals. This analysis also examines if and how these effects vary across the laboratories involved in the study and examines how different dosing protocols may have affected the ability to detect the effects of the two chemicals.

### Data Pre-processing
The dataset was accessed via international multilaboratory study on the effect of estrogen agonists and antagonists on the weight of uterus with 2677 non-empty observations. The cleaned data includes three categorical variables – protocol, group and lab – and four numeric variables – uterus weight in mg, the body weight of rats in grams, dose of estrogen agonist (EE) and dose of estrogen antagonist (ZM). The character and numeric values for protocol, group, and lab were factorized. The nature of the data allows us to organize the data with multiple levels. Potential rat groupings to be explored are by lab, protocol, and group.

## PART II

### Introduction
The North Carolina State Board of Elections (NCSBE) is responsible for administering the election process and campaign finance disclosure and compliance. The NCSBE also provides voter registration and turnout data.

The purpose of this analysis is to examine the NCSBE voter data to come to a conclusion on the following questions: 

1. How did demographic subgroups vote in 2016? For example, how did the turnout for males compare to the turnout for females after controlling for other potential predictors?

2. Did the overall probability or odds of voting differ by county in 2016? 3. How did the turnout rates differ between females and males for the different party affiliations?

### Data Pre-processing
The two datasets used in this analysis were the 2016 voter history data and 2016 voter registration data. To prepare for the analysis of voting habits by demographic group the two datasets were grouped by county, age group, ethnicity, race, party, and gender (each row having a unique combination of the variables) and aggregated the number of actual voters or registered voters for the respective dataset. To effectively join the two datasets along all the variable columns we first needed to ensure that the levels for the factor variables for each dataset were consistent. Invalid voter groups levels that did not match, like the age group below 18 years from the voting records dataset were removed. Missing values were also removed from the dataset as any methods to impute the missing values did not seem feasible. Also, the two datasets have a relatively small number of predictor variables compared to a very large number of observations that we were not concerned about the degree of information loss resulting from omitting observations with missing values.

The two cleaned datasets were then merged along all common predictor variable columns. Voter turnout for each row was calculated by dividing the number of actual voters by the number of registered voters. This voter turnout variable was then used as the response variable as we explored relationships in the data.

## Analytical Models: Hierarchical Model, Logistic Regression
