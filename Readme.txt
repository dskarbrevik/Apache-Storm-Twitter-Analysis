David Skarbrevik
MIDS W205 - Section 4
Professor Uri Schonfeld
Fall 2016


READ ME
*****
This application streams words in Twitter and allows some analysis of the resulting stream. Read the Architecture.pdf file for a more detailed explanation of this 
******


Requirements for Execution of Application:
1. Must have a postgres database called “tcount” and associated table called “tweetwordcount”
2. Must have python 2.7 or greater and libraries installed: psycopg2, tweepy
3. Must have library stream parse installed


To Execute the Application:
1. Start a streamparse project by typing [sparse quickstart <project name>]
2. Change directories to “src”->”bolts” and place “parse.py” and “wordcount.py” in this folder
3. Change directories to “src”->”spouts” and place “tweets.py” in this folder
4. Change directories to “topologies” and place “tweetwordcount.clj” in this folder
5. In the main directory for your streamparse project, use command: [parse run] to start streaming tweets
6. In a separate terminal, at any point once stream is running:
   1. Use command: [python finalresults.py <enter a word here>] to view running total for that word.
   2. Use command: [python histogram.py <min num> <max num>] to view all words with total counts between that range of numbers.
7. At any time, stream can be stopped and postgres table will preserve streamed words for later analysis.