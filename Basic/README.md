
# NLTK Concepts (Basics)

### What is Tokenization?
The process of breaking down text into smaller units called tokens. These tokens can be words, characters, subwords, or even sentences, depending on the task at hand. It's a foundational step in NLP because it transforms raw text into a format that machines can understand and analyze.


 | Type                     | Desc                                      | Example                                                                  |
  |:-------------------------|:-----------------------------------------:|-------------------------------------------------------------------------:|
  | Word Tokenization        | Splits text into individual words         | "Maching learning is fun" --> ["Machine", "learning", "is", "fun"]       |
  | Character Tokenization   | Breaks text into individual characters    | "Hi" ----> ["H", "I"]                                                    |
  | Subword Tokenization     | Splits words into smaller meaningful units (useful for rare words)| "unhappiness" --> ["un", "happiness"]                                    |
  | Sentence Tokenization    | Divides text into sentences               | "AI is powerful. NLP is exciting." ----> ["AI is powerful.", "NLP is exciting."] |



Understanding these basic terms is essential for anyone working in Natural Language Processing (NLP). 

| Topic      | Desc                                                                                                                                                  | Example                                                                                                        |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Corpus     | A corpus is a large, organized collection of written, spoken, or digital texts used for training, testing. You can call it as Paragraph               | Collection of 10,000 news articles[1]                                                                          |
| Document   | A document is an individual piece of text within a corpus. It can range from a paragraph, an article, an email, a review, or even a single sentence. | A single news article: "The government announced a new policy today..."[1]                                     |
| Vocabulary | The vocabulary is the set of all unique words (or sometimes tokens) present across the entire corpus. It does not include duplicates; each distinct word only appears once in the vocabulary set. | {"government", "announced", "new", "policy", "today", ...} (all unique words from the entire corpus)[1]      |
| Words      | In NLP, words are the basic units (tokens) obtained from text by splitting it, typically using space and punctuation as delimiters.                   | ["The", "government", "announced", "a", "new", "policy", "today", "..."] (individual tokens in a document)[1] |




#### Different type of Stemmer in NLTK:  
► Stemming (Porter Stemmer): Stemming in Natural Language Processing (NLP) is a text preprocessing technique that reduces words to their root or base form, known as the "stem." The process involves removing suffixes or prefixes from inflected or derived word forms to standardize them into a single morphological base.  
► RegexpStemmer: RegexpStemmer in NLTK is a highly customizable stemming class that uses regular expressions to remove suffixes (or prefixes) from words. Unlike other stemmers that rely on built-in linguistic rules, RegexpStemmer lets you define your own regular expressions, making it suitable for domain-specific stemming tasks or languages with unusual morphology.  
► Snowball Stemmer: The Snowball Stemmer in NLTK is an advanced stemming algorithm, also known as the Porter2 stemmer.  It is more efficient, consistent, and aggressive in its stemming process and is widely used for text normalization in NLP tasks.  
	Compare Porter Stemming and Snowball Stemming:  
	There is still some gap with Snowball Stemming which changes the meaning of word or doest stemm the word fully. Exm:  
		→ snowballsstemmer.stem('goes') -- > goe.  
		→ stemming.stem('goes') --> goe  

► Lancaster Stemmer: The Lancaster Stemmer (also called the Paice-Husk stemmer) in NLTK is an aggressive stemming algorithm designed to reduce words to their root form with high speed and simplicity. It is known for being more aggressive than the Porter and Snowball stemmers, meaning it often shortens words more dramatically and may sometimes produce stems that are not valid English words.  
► These examples show how the Lancaster Stemmer aggressively reduces suffixes and inflections to compact stems, useful for search or classification tasks but sometimes creating non-standard roots.  

Limitations:  
® Over-stemming: Words with different meanings may be reduced to the same stem.  
® Non-dictionary stems: Returned stem can sometimes be a non-word (e.g., 'univers' for both 'university' and 'universe').  
® Best for English: Other languages may not be well-supported.  

► Lemmatizer: A Lemmatizer in NLTK is a tool used in Natural Language Processing (NLP) to reduce words to their base or dictionary form called a lemma. Unlike stemming, which simply chops off prefixes or suffixes and may produce non-words, lemmatization considers the word's meaning and part of speech (POS), ensuring that the base form is a valid word found in the dictionary.
			
► Stopwords: A stopword in NLTK (Natural Language Toolkit) refers to a commonly used word (such as "the", "is", "in") that is often filtered out during text processing because it carries little meaningful information



### Text To Vectoriztion:

#### Vectors and Vectorization Techniques in NLP:
In Natural Language Processing (NLP), vectors play an important role in transforming human language into a format that machines can comprehend and process. These numerical representations enable computers to perform tasks such as sentiment analysis, machine translation and information retrieval with greater accuracy and efficiency.  
	→  Vectors are numerical representations of words, phrases or entire documents. These vectors capture the semantic meaning and syntactic properties of the text, allowing machines to perform mathematical operations on them.  
	→  Vectorization is the process of transforming words, phrases or entire documents into numerical vectors that can be understood and processed by machine learning models. These numerical representations capture the semantic meaning and contextual relationships of the text, allowing algorithms to perform tasks such as classification, clustering and prediction.  

#### What is Sentiment Analysis?
Sentiment analysis in NLP (Natural Language Processing) is the process of automatically identifying and categorizing the emotional tone or sentiment expressed in a piece of text, typically as positive, negative, or neutral.  It is also known as opinion mining or emotion AI and is widely used to analyze opinions, attitudes, and emotions in data such as product reviews, social media posts, surveys, and customer feedback.

### One-Hot Encoding:  https://www.geeksforgeeks.org/machine-learning/ml-one-hot-encoding/

One Hot Encoding is a method for converting categorical variables into a binary format. It creates new columns for each category where 1 means the category is present and 0 means it is not. The primary purpose of One Hot Encoding is to ensure that categorical data can be effectively used in machine learning models.
