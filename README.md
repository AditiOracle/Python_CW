# Python_CW
**Overview of Election Audit:**

A Colorado Board of Elections employee assigned us the task to audit the result of the Election based on the following attributes:

- Calculate the total number of Votes cast.
- Calculate votes for each county.
- Calculate the percentage votes for each county.
- Determine the winning county.

**Election-Audit Results:**

- Total votes were cast in this congressional election – 369,711
- **County Votes:**

| County | Votes | Percentage |
| --- | --- | --- |
| Jefferson | 38,355 | 10.5% |
| Denver | 306,055 | 82.8% |
| Arapahoe | 24,801 | 6.7% |

- _Denver County has highest number of votes._
- **Candidate Votes:**

| Candidate Name | Votes | Percentage |
| --- | --- | --- |
| Charles Casper Stockham | 85,213 | 23% |
| Diana DeGette | 272,892 | 73.8% |
| Raymond Anthony Doane | 11,606 | 3.1% |

- _Diana DeGette won by 272,892 votes (73.8%)_

![Terminal Output](Terminal Output.PNG)

![Textfile Output](Textfile Output.PNG)

**Election-Audit Summary:**

1. This script can easily be modified for any Municipality elections (for different Wards). A Province (or State) is divided into different wards and each ward has different candidates.

- We will add similar code for Wards as we did for County. Candidate code will remain almost same.
- We would have to add few more Dictionary for the ward and country. Each ward will have the unique number like WARDBRAM\_01,WARDBRAM\_02;WARDMISSI\_01;WARDMISSI\_02 etc…

![Shape1](RackMultipart20220122-4-qx3ewv_html_f77cd82e7600d0b5.gif)
1. CITIES:

Get the cities from the csv file in a LIST and check if the City matches the CSV file THEN -\&gt;only increase the vote

1. WARDS:

Get the wards in the list by checking if the WARD list matches the WARD from the CSV file THEN-\&gt;only increase the VOTE Count

\*we also have to check the IF statement to check the WARD number (each ward number has unique number) belongs to a CITY

We will feed in DICTIONARY3 {WARD:CITY}

1. CANDIDATE, HIS VOTES AND HIS WARD:

Get the candidate names and their wards in the DICTIONARY1

Get Vote counts in the DICTIONARY2

\*\*We will do the calculation similar to the current script in PyPoll\_Challenge.py

1. WIN:

Get the city with HIGHEST votes

Get the WARD with the HIGHEST votes AND Its City

Get the Candidate name with the HIGHEST votes

1. We can also modify this code to check if how many votes were cast using:

- mail
- ballot or
- EVR(Electronic Voting machines).

We have to add a piece of a code where we will check the method of voting from the csv file provided to us using (for loop and If statements)

![Shape2](RackMultipart20220122-4-qx3ewv_html_7f974d9bc7416fa2.gif)

Initialize the methods variable:

EVR=0

MAIL=0

BALLOT=0

#scan through the file

for row in reader:

vote\_method\_name=row[3]

If vote\_method\_name=&quot;EVR&quot;:

EVR=+1

If vote\_method\_name=&quot;MAIL&quot;:

MAIL=+1

If vote\_method\_name=&quot;BALLOT&quot;

BALLOT=+1

VOTE\_METHOD\_SUMMARY=print(

f&quot;EVR:{EVR}\n&quot;

f&quot;MAIL:{MAIL}\n&quot;

f&quot;BALLOT:{BALLOT}\n&quot;}