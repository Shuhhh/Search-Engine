# Search_Engine

A search engine project based on a corpus of 10 million twitts.

Each twitt first goes through a parser (tokenized), which removes all stopwords and irrelevant words or signs, according to some rules.

When the parser ends, the twitt goes through a indexer which creates an inverted index and uploads it to the disk.

The next part is the searcher, the searcher uses LDA model to which separates all the twitts to topics.

When receiving a query, the searcher uses the LDA model to know which topic is more relevant and send all the twitts with the same topic.

Meanwhile, the searcher sends each twitt to the ranker, and rank it by a cossime-similarity formula.

Thus, you will get the most relevant twitts - the 100 twitts with the best score save in a csv file.

#Technology

* Based on python 3.7
* Needs to install all packages in requirements.txt file
