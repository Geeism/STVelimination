Whattup. The purpose of making the code public is to allow anyone to see if I fiddled with the data to mess with the outcome.

The counting component of the code is fairly simple. Each vote is a list with candidates listed in order of preference. The code reads down the list, and if the candidate it's looking at is still in the `options` dictionary, then it'll +1 to that candidate and start reading the next vote. Since candidates are removed from `options` if they're the lowest, the code just skips over preferences that have been eliminated. Nice and simple.

The problem that I needed to solve was that I wanted to have candidates as rows in the Form multiple choice box question, which resulted in a .csv that wasn't in the 'candidates listed in order of preference' format. The bulk of my code is for converting one format into the other.

#How to check my counting

There are basically four ways that someone could mess with the results.
1. Mess with the raw data
2. Mess the counting process
4. Mess with the presentation of results

## 1. Raw Data
To check that, you'll have to go to the `Fan Team Contest Responses` Sheet and check the History of that document. You should see that the only changes were the addition of new votes by the Form.

## 2. Counting
Maybe I've put things in the code that mess with the results. Looking at the code, it should be apparent that there is nothing of the sort.

## 3. Presentation
The most feasible way to mess with the outcome of the vote would have been to just straight up lie about what the code gave me. It seems unlikely to me that anyone is actually going to go and run the code I've shared, so it'd be a safe bet.

In the end, the two most important things are that the raw data hasn't been altered, and that what I've reported the code output to be from that data is indeed what you get when you run it.
