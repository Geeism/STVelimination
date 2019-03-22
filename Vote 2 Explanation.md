# How STV with elimination works
In STV, each vote is a single *transferable* vote. A single vote is a list of preferences, and that vote goes to the highest preference that still has a "surviving" candidate. Let's see how that works out with some fruit. 

Let's say we have 4 candidates, Apples, Oranges, Pears and Bananas. You are one of 100 voters, and your vote has bananas first, apples second, pears third, and oranges fourth. Now, let's count all 100 votes. As it turns out, Bananas came last with just 5 votes. Bananas are eliminated, and anyone who preferenced bananas at the top will have their vote moved to a different candidate using the next preference down the list (which is apples for you). The system has *transferred* your vote to your next available preference. This process, of elimination and next-preference distribution, occurs as many times as required until there's a winner. So let's continue with our example: we count up all the votes again and it comes out at 45 for oranges, 45 for pears, and 10 for apples. Apples are last so they get eliminated, and those 10 votes now get distributed out. When the next and final count happens, apples and pears are still drawing from the same 100 votes (assuming everyone filled our their vote from 1-4). And, their numbers will be filled with people who preferenced them first, second, or even third.

The STV system we're using is like doing a single vote poll, but over and over. Each time the last place is removed, giving the people who voted for that eliminated candidate to vote for their next preference. Of course, doing the vote over and over would be annoying so STV takes care of it in a single hit.

It should be noted that this is different to the "normal" STV (such as what's used in Australia), where if a candidate reaches a threshold then they become elected.

# Checking to see if we messed with the coding
### Testing
#### test
## Step 1: preparing the data
Everything's stored on the `Fan Team Contest Responses` Sheet in the `FTC 2019` folder. If you examine the layout of the `Vote 2` sheet, you'll see that there are two columns containing the data that are unrelated to counting, so to neaten things up I made the `Vote 2 export` sheet.

So basically:
- Download the `Vote 2 export` sheet as a .csv
- Download `candidates` sheet as a .csv

### Step 2: running the code
The only thing that you should need to make sure of is that the two downloaded .csvs need to be in the same place as the code. Once you press run, it'll load in the data and do it's counting thing.

### Step 3: checking for discrepancies
Assuming everything went correctly, the code should generate a `FTC19_outcome.csv`.

To really make sure that things haven't been tampered with, you want to go through my code and make sure there's no part 
