Whattup. The purpose of making the code public is to allow anyone to see if I fiddled with the data to mess with the outcome.

The counting component of the code is fairly simple. Each vote is a list with candidates listed in order of preference. The code reads down the list, and if the candidate it's looking at is still in the `options` dictionary, then it'll +1 to that candidate and start reading the next 

The original code was really neat, because all that was required was a multiple choice box question with the candidates in the columns (as the answers) and the preferences in rows (as the questions). But I didn't like this, because the team names would fit better into the rows. 

At the time, I also thought that shuffling the questions would only work if the questions were the candidates. The reason for shuffling is so that an auto-clicker script can't be used. But I now realise that the shuffling could still achieve that end if the questions were the preferences rather the candidates. But I still think it's better to have the candidates in the rows, as they can have long names. If you have too many columns, you need a horizontal scroll to fit all of that stuff in so that'd be a bit annoying.

The problem that I needed to solve was to convert the .csv from the candidate-question format to the candidate-answer format, as the candidate-answer format has the list of candidates in order which is what the counter requires. 

#How to check my counting

There are basically three ways that someone could mess with the results.
1. Mess with the raw data
2. Mess with the conversion process
3. Mess with the counting process
4. Mess with the counting output

To check the first one, you'll have go to and look at the history in the `Fan Team Contest Responses` Sheet. The other three you can do yourself with the code.

