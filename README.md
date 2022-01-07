# RBCModule3-Challenge

## Overview of Election Audit
The purpose of this project is to exemplify basic Python data analytics by importing a csv file of election results, compiling some straighforward analysis and outputting to a txt file. 

## Election-Audit Results
The results, see [here](./analysis/election_analysis.TXT), show that:

1. 369,711 votes were cast in this congressional election.
2. The counties voted as follows:
    - Jefferson: 10.5% (38,855)
    - Denver: 82.8% (306,055)
    - Arapahoe: 6.7% (24,801)
3. Denver county had the largest number of votes. 
4. The voting breakdown is as follows:
    - Charles Casper Stockham: 23.0% (85,213)
    - Diana DeGette: 73.8% (272,892)
    - Raymon Anthony Doane: 3.1% (11,606)
5. Diana DeGette was the winner of the election with the winning vote count of 272,892, 73.8% of the vote. 

## Election-Audit Summary
For future usage, the associated PyPoll script is fairly flexible already, but for other elections, we would suggest two major changes. First, we would suggest that the csv file to be read should not be hard-coded but the user should be asked for input or to navigate to the file through an operating system prompt. Second, for many elections, a voter may be voting on several candidates at once, say for senate, house, and president. Suppose we know each voter will make 3 such choices. To make our script more general, we could loop through several columns of candidate names instead on line 49:

```
    candidate_name = row[2]
```

we could write:
```
    names = []
    for i in range(2:5)
        if (row[i] != ""):
            names.append(row[i])
```

and then we'll add a vote for each name in the list. Obviously we could generalize this further quickly, but further generalization probably isn't necessary for our use case. 