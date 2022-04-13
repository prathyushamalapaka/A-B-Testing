# A/B Testing

## Exercise 1: Game Fun: Customer Acquisition through Digital Advertising   

Disclaimer​: “No similarity to actual persons or companies is intended or should be inferred.”  
 
Game Fun is one of the world's top developers of casual mobile games and spends millions of dollars every year on digital advertising. Of particular interest to Game Fun is their efforts on improving their customer acquisition. It is a common belief in the mobile gaming industry that the more paid traffic you have, the better your organic traffic will be. This is known as K-Factor. However, measuring the causal effect of online digital advertising has proven to be an extremely challenging task. Towards this end, Game Fun decided to run an A/B experiment. 

## Display Banners Experiment 
 
Game Fun ran an online display banners advertising campaign with the primary objective of increasing its sales on gaming subscription packages. To attract new users, the display ad advertised their most popular game and offered the user a promotion of $25 signing-up bonus. The credits would appear in the customer’s game account and could be used to purchase any further in-app features. Based on historical data, a new customer subscription brings a revenue of $37.5 on average. This results in a net inflow of $12.5 after the $25 credit for the users acquired through this promotion. 
  
The A/B experiment worked as follows. Before the start of the digital ad campaign, Game Fun chose two different websites (“content publishers”) to run the experiment on. The content publishers have randomly assigned their web users to test and control groups. As users browsed on the two websites, the advertising servers checked whether a given user should be show a Game-Fun ad. If the user qualified for a Game-Fun ad, then the ad server checked whether the user was assigned to the test or the control group. If the user belonged to the test set, a Game-Fun ad was displayed to the user. Otherwise, a completely irrelevant ad was displayed to the user. 
  
However, Game-Fun had to pay the content publishers for these irrelevant ads, as well. This raised a tension between the management and the data scientist teams. The management team had two concerns. First, paying for other companies ads is directly decreasing their marketing budget. Second, they didn’t like the fact that some users who saw an irrelevant ad might have signed up for the Game Fun game in the first place, had they been shown their gaming ad (indirect effect – opportunity cost missed).  For these two reasons, the management team asked their data scientist team to carefully decide on the best proportion of users to assign to the test and control groups, while at the same time maintaining a statistically valid comparison. 
  
The data scientist team ran a statistical power analysis of the experiment, and decided to allocate 70% of users to test group and the rest 30% to the control group (see appendix for an explanation on power analysis). 

## Analysis of the Experiment 
  
After the completion of the experiment, the results came in and you (the data analytics team) is being asked to analyze them. Each row in the 
data belongs to an individual customer. The first column is the anonymized customer id. The second column, “test”, indicates whether the user was part of the treatment group (test =1) or the control group (test=0). There are three demographic variables, “gender” (male =1, female =0), “income” (this is measured in thousands), and “gamer” (gamer = 1, if user is a gaming enthusiast; 0, otherwise). The website that a customer visited is in the variable “site”. The variable “impressions” contains the number of advertising impressions that a customer received. If a customer is in the test group, then all of this customer’s impressions are for the Game-Fun’s ad; if a customer is in the control group, then all of this customer’s impressions are for the irrelevant ad. Last, the column “purchase” is the dependent variable, and it indicates if the customer purchased anything within 30 days after her/his conversation to the game (30 days is the expected customer lifetime duration for a mobile gamer). If a customer purchased, then purchased =1; 0, otherwise.

## Exercise 2: Non-Compliance in Randomized Experiments   
 
Sommer and Ziegler (1991) studied the effect of vitamin A supplements on infant mortality in Indonesia. The vitamin supplements were randomly assigned to villages, but some of the individuals in villages who were assigned to the treatment group failed to receive them. However, none of the individuals who were assigned to the control group received the supplements. This is an example of what we call “One-sided Non-compliance”. 

## Problem Setting 
 
An NGO is interested in purchasing Vitamin A shots for babies in developing countries. Towards this, it consulted four data scientists on how to interpret the results of the Sommer-Zeger experiment. Each data scientist suggested a different way of analysis. Your task is to use the “sommer_deger” dataset and implement their recommendations to decide who is right.  
 
## Data Description  
 
The data contains three variables: instrument (equals one if the mother was offered a vitamin A shot for her baby), treatment (equals one if the baby got the vitamin A shot) and outcome (equals one if the baby did not survive).
