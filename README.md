# Python 3 code for STV with elimination using Google Forms 
Whattup it's some code by someone who barely knows how to code.

I adapted the code from here: https://gist.github.com/c2huc2hu/a5826b52e838c5845dca.

It was written to count votes for the Marble Showdown Fan Team Contest 2019, a contest run for Jelle's Marble Runs on YouTube. If you're looking for an explanation of how that process for Vote 2 was run (i.e. you want to make sure I didn't tamper with results), please read `Vote 2 explanation.md`. If you're just looking for code that works, just read below.

# Things to keep in mind
First, the question in Google Form is a multiple choice grid *with the candidates on the rows*. This treats each candidate as a question and the associated preference as an answer, so the `X.csv` has candidates as the columns and the associated preference as the data (which is why the code I adapted from needed the alterations).

Second, the code looks for `X_candidates.csv` which has all candidates *in the order that they are on the questions*. That's two spreadsheets - the voting data itself and this candidate sheet.

Third, when looking for preferences the code looks for the string `PX` (P1, P2, P3, etc.) as opposed to Preference 1.

Keeping those three things in mind, any dumbo should be able to run an STV with elimination through Google Forms.

The code outputs `X_outcome.csv` also.
