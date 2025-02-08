<img width="712" alt="Image" src="https://github.com/user-attachments/assets/57705bb7-be53-449b-bd92-4829e8a17fac" />

<img width="856" alt="Image" src="https://github.com/user-attachments/assets/903e364a-f27b-4600-9c78-85514073a48d" />

<img width="267" alt="Image" src="https://github.com/user-attachments/assets/d3641fbc-ec59-4a42-8fa8-747c9401ee0d" />

**Preprocessing**

When preprocessing, you have to perform the following:

1. Eliminate handles and URLs
2. Tokenize the string into words.
3. Remove stop words like "and, is, a, on, etc."
4. Stemming- or convert every word to its stem. Like dancer, dancing, danced, becomes 'danc'. You can use porter stemmer to take care of this.
5. Convert all your words to lower case.

For example the following tweet "@YMourri and @AndrewYNg are tuning a GREAT AI model at <https://deeplearning.ai>!!!" after preprocessing becomes

\[tun,great,ai,model\]\[_tun_,_great_,_ai_,_model_\]. Hence you can see how we eliminated handles tokenized it into words, removed stop words, performed stemming, and converted everything to lower case.

**The first thing you'll learn about is called stemming and the second thing you will learn about is called stop words, and specifically you will learn how to use stemming and stop words to preprocess your texts.**  
**Description**: This line introduces two key techniques in text preprocessing: stemming and stop words. Stemming reduces words to their base form, while stop words are common words that might not add significant meaning.  
_Example_: In the phrase “running is fun,” stemming reduces “running” to “run,” while “is” would be considered a stop word.

**2\. First, I remove all the words that don't add significant meaning to the tweets, aka stop words and punctuation marks.**  
**Description**: The process begins with eliminating non-essential words and punctuation that do not convey valuable meaning.  
_Example_: In the tweet "The AI model is really great!", the stop words "The," "is," and "really" would be removed.

**3\. In practice, you would have to compare your tweet against two lists. One with stop words in English and another with punctuation.**  
**Description**: Effective preprocessing requires checking the tweet against predefined lists of stop words and punctuation marks.  
_Example_: A stop words list might contain words like "the," "and," "is," while a punctuation list includes ".", ",", "!", etc.

**4\. Every word from the tweet that also appears on the list of stop words should be eliminated.**  
**Description**: Words in the tweet that match entries in the stop words list are removed.  
_Example_: From the tweet "The AI model is really great!", both "The" and "is" are eliminated.

**5\. The tweet without stop words looks like this.**  
**Description**: Illustration of the tweet after removing stop words.  
_Example_: After processing, it reads: "AI model great!"

**6\. Now, let's eliminate every punctuation mark.**  
**Description**: The next step focuses on removing punctuation marks from the tweet.  
_Example_: If the tweet included an exclamation mark, it will be cleaned up in this step.

**7\. In this example, there are only exclamation points.**  
**Description**: Specifies that the punctuation to be removed in this case is limited to exclamation marks.  
_Example_: For "AI is great!", the exclamation mark will be omitted.

**8\. The tweet without stop words and punctuation looks like this.**  
**Description**: This shows the result after removing both stop words and punctuation.  
_Example_: The processed tweet now reads: "AI model great" (without an exclamation mark).

**9\. However, note that in some contexts you won't have to eliminate punctuation.**  
**Description**: Indicates that punctuation might retain meaning in certain contexts, and its removal should be considered carefully.  
_Example_: In "Wow!!! Amazing," the punctuation conveys excitement and should likely be preserved.

**10\. Tweets and other types of texts often have handles and URLs, but these don't add any value for the task of sentiment analysis.**  
**Description**: Handles (like Twitter usernames) and URLs are typically irrelevant for understanding sentiment in text analysis.  
_Example_: From the tweet "Check this out @user [http://link.com](http://link.com/)," both the handle and URL are not necessary for sentiment analysis.

**11\. Let's eliminate these two handles and this URL.**  
**Description**: This directive states that handles and URLs should be removed from the tweet for clarity.  
_Example_: The tweet now becomes just "Check this out."

**12\. At the end of this process, the resulting tweet contains all the important information related to its sentiment.**  
**Description**: After all cleaning steps, the tweet retains essential sentiment information.  
_Example_: The final result, "AI model great," clearly expresses a positive sentiment.

**13\. Tuning GREAT AI model is clearly a positive tweet and a sufficiently good model should be able to classify it.**  
**Description**: This confirms that the processed tweet retains its sentiment and can be easily classified by a model.  
_Example_: A well-trained model would classify "AI model great" as positive sentiment with no ambiguity.

**14\. Now that the tweet from the example has only the necessary information, I will perform stemming for every word.**  
**Description**: The next preprocessing step is stemming, which involves reducing words to their root form.  
_Example_: The word "running" would be transformed into its base form "run."

**15\. Stemming in NLP is simply transforming any word to its base stem, which you could define as the set of characters that are used to construct the word and its derivatives.**  
**Description**: Stemming consolidates different forms of a word into a single representation.  
_Example_: The words "running," "runner," and "ran" will all be reduced to "run."

**16\. Let's take the first word from the example. Its stem is done, because adding the letter e, it forms the word tune.**  
**Description**: This example illustrates how a specific word can have different suffixes added to form new words.  
_Example_: The word "tune" can transform into "tuned" by adding "ed" or "tuning" by adding "ing."

**17\. Adding the suffix ed, forms the word tuned, and adding the suffix ing, it forms the word tuning.**  
**Description**: This emphasizes how the original stem can lead to multiple variations based on added suffixes.  
_Example_: "Tuned" and "tuning" show different usages generated from the same stem.

**18\. After you perform stemming on your corpus, the word tune, tuned, and tuning will be reduced to the stem tun.**  
**Description**: All derived words will consolidate to a single root form, simplifying the vocabulary.  
_Example_: "Tune," "tuned," and "tuning" all become "tun."

**19\. Your vocabulary would be significantly reduced when you perform this process for every word in the corpus.**  
**Description**: Stemming across the dataset leads to a smaller, more manageable vocabulary.  
_Example_: If "running," "runner," and "ran" all point to "run," the vocabulary is simplified, benefiting analysis.

**20\. To reduce your vocabulary even further without losing valuable information, you’d have to lowercase every one of your words.**  
**Description**: Lowercasing words ensures that case variations are treated as identical, further simplifying the vocabulary.  
_Example_: The words "GREAT," "Great," and "great" become one entry: "great."

**21\. This is the final preprocess tweet as a list of words.**  
**Description**: This denotes the end of preprocessing, presenting the cleaned list of words extracted from the tweet.  
_Example_: After processing, the final tweet could appear as the list: \["ai", "model", "great"\].

**22\. Now that you're familiar with stemming and stop words, you know the basics of text processing.**  
**Description**: A summary indicating that the foundational techniques of stemming and removing stop words essential to text processing have been covered.  
_Example_: Understanding these concepts helps in preparing text data for machine learning models.

**23\. In the next video, you can use your processed tweet function to extract a matrix x, which represents all the tweets in your data set.**  
**Description**: The next step building on this lesson involves creating a matrix from the processed tweets for further analysis.  
_Example_: Each processed tweet will be converted into a format suitable for machine learning, such as a matrix where each row represents a tweet.
