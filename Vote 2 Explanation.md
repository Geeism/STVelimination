Whattup. The purpose of making the code public is to allow anyone to see if I fiddled with the data to mess with the outcome.

The counting component of the code is fairly simple. Each vote is a list with candidates listed in order of preference. The code reads down the list, and if the candidate it's looking at is still in the `options` dictionary, then it'll +1 to that candidate and start reading the next vote. Since candidate elimination is simply removal from `options`, the code just skips over preferences that have been eliminated. Nice and simple.

The problem that I needed to solve was that the original code had candidates in the columns (answers) of the multiple choice grid and preferences in the rows (answers). That looks weird, so I wanted to have the candidates as the questions. This changes the layout of the resulting spreadsheet, so the bulk of my code converts the candidate-question data into a candidate-answer format that the counting code can use.

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
