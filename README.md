Spamming is one of the major attacks that accumulate the large number of compromised machines by sending unwanted messages, viruses through emails.

Bayes Theorem:
	P(A|B) = (P(A) P(B|A))  ÷  P(B)
	P(Spam|Free) = P(Spam) P(Free | Spam) ÷ P(Free)
	The numerator is probability of a message being spam and containing the word “free” or any other spam type words.
	The denominator is overall probability of an email containing the word “free” or similar type of words.
	So, together the ratio is the percentage of emails with the word “free” that are spam.
	We construct P(Spam | word) for every word we encounter during training. Then we multiply these together when analyzing a new email to get the probability of it being spam.
	Scikit-learn library is used in this process for calculating the probability.
	from sklearn.naive_bayes import MultinomialNB is the library used.
	Pandas is used to read the files or data of mails.
	We will use a CountVectorizer to split up each message into its list of words, and throw that into a MultinomialNB classifier.
	If more words like “free”, “subscribe” etc. are found then the mail is considered as spam mail.
We will use a CountVectorizer to split up each message into its list of words, and throw that into a MultinomialNB classifier.
