# Udacity Data Scientist Nanodegree Capstone Project
This repository has all the code and report for my Udacity Data Scientist Nanodegree Capstone project.
# Starbucks-Capstone-Challenge

## Blog post on Medium  
https://medium.com/@reemalsaedi6/starbucks-capstone-challenge-b5a91fcc997d

## Install
This project requires Python 3.x and the following Python libraries installed:

- NumPy
- Pandas
- matplotlib
- scikit-learn
## Dataset overview
The program used to make the information mimics how individuals settle on buying choices and how those choices are impacted by limited time offers. 

Every individual in the recreation has some shrouded attributes that impact their buying designs and are related with their detectable characteristics. Individuals produce different occasions, including accepting offers, opening offers, and making buys. 

As a rearrangements, there are no express items to follow. Just the measures of every exchange or offer are recorded. 

There are three sorts of offers that can be sent: get one-get-one (BOGO), rebate, and instructive. In a BOGO offer, a client needs to spend a specific add up to get a prize equivalent to that edge sum. In a rebate, a client increases a prize equivalent to a small amount of the sum spent. In an educational offer, there is no prize, yet nor is there an essential sum that the client is required to spend. Offers can be conveyed by means of various channels. 

The essential undertaking is to utilize the information to distinguish which gatherings of individuals are generally receptive to each sort of offer, and how best to introduce each kind of offer.

## Problem Statement
As expressed over, the issue proclamation I am planning to answer are to (1) Discover client properties and purchasing behaviour , and (2) the amount somebody will spend dependent on socioeconomics and offer sort. 

Utilizing the information gave, I answer the above first inquiry utilizing graphs for (Demographic information for every client) and the subsequent inquiry utilizing 3 order administered AI models, taking care of in the information from three join information (portfolio, profile, Transactional).

## Data 
### profile.json
Rewards program users (17000 users x 5 fields)
- gender: (categorical) M, F, O, or null
- age: (numeric) missing value encoded as 118
- id: (string/hash)
- became_member_on: (date) format YYYYMMDD
- income: (numeric)

### portfolio.json
Offers sent during 30-day test period (10 offers x 6 fields)
- reward: (numeric) money awarded for the amount spent
- channels: (list) web, email, mobile, social
- difficulty: (numeric) money required to be spent to receive reward
- duration: (numeric) time for offer to be open, in days
- offer_type: (string) bogo, discount, informational
- id: (string/hash)
### transcript.json
Event log (306648 events x 4 fields)
- person: (string/hash)
- event: (string) offer received, offer viewed, transaction, offer completed
- value: (dictionary) different values depending on event type
1. offer id: (string/hash) not associated with any "transaction"
2. amount: (numeric) money spent in "transaction"
3. reward: (numeric) money gained from "offer completed"
- time: (numeric) hours after start of test

### Results
My examination recommends that the subsequent irregular timberland model has a preparation information precision of 0.944 and a F-score of 0.939. The test informational collection exactness of 0.929 and F-score of 0.931 recommends that the arbitrary woods model I developed didn't overfit the preparation information.

### Licensing, Authors, Acknowledgements, etc.
Data for coding project was provided by Udacity.
