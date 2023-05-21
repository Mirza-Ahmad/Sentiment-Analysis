
# **Project Title**

## ***Sentiment Analysis*** 

### Sentiment analysis, also known as opinion mining, is a field   of natural language processing that focuses on automatically  determining the sentiment expressed in textual data. Sentiment analysis also plays a vital role in social media monitoring, allowing companies to gauge public sentiment towards their brand and manage online reputation. 

## ***What is spacy in NLP?***
### Spacy is a open-source python library for NLP. Spacy is designed to make it easy ot extract the information from or general purpose natual language preprocessing.

# **Installation of spacy**
### You can install spacy using pip, python package manager. Your run this command to install the spacy in your system.
### **! python -m install spacy**
### After spacy installation in your system. There's one more thing you have to install in your system for difffernt languages.
### **! python -m spacy download en_core_web_sm**
### The en_core_web_sm is a deafult model for the English language. Since the models are quite large, it’s best to install them separately—including all languages in one package would make the download too massive.

# **How the data is look like?**
### data.head()

# ***How big is the data?***
### data.shape

# **What does the load function do?**
### The load() function returns a Language callable object, which is commonly assigned to a variable called nlp.

## **If this type of error occur like A UTF-8 locale is required. Got ANSI_X3.4-1968. Use this command.**
### *import locale*
### *locale.getpreferredencoding = lambda: "UTF-8"*

## **What is Docment Object in NLP?**
###  The text is used to instantiate a Doc object. From there, you can access a whole bunch of information about the processed text. For instance, you iterated over the Doc object with a list comprehension that produces a series of Token objects.

## ***What is Contractions Expansion in NLP?***
### The contractions approach can easily be updated to help correct common spelling mistakes or even change character names in a short story. Like can't to can not, haven't to have not etc.

## ***How to install contractions?***
### ! pip install contractions

## **What is the Regular Expression?** 
###  A Regular string is a specified set of strings that matches it. Regular expressions can be concatenated to form new regular expressions; if A and B are both regular expressions, then AB is also a regular expression. 

## **Quantifers or Repetition Operators**
###  The quantifiers are used to specify the number of occurences to match. Quantifiers (*, +, ?, {m,n}, etc) cannot be directly nested. 

### **Dot character(.)**
### This matches any character except a newline. If the DOTALL flag has been 
### specified, this matches any character including a newline.

### **Caret character(^)**
### Matches the start of the string, and in MULTILINE mode also matches immediately after each newline.

### **Dollar character($)**
### Matches the end of the string or just before the newline at the end of the string, and in MULTILINE mode also matches before a newline. 

### **Multliply character(*)**
### Causes the resulting RE to match 0 or more repetitions of the preceding RE, as many repetitions as are possible. ab* will match ‘a’, ‘ab’, or ‘a’ followed by any number of ‘b’s.

### **Plus character(+)**
### Causes the resulting RE to match 1 or more repetitions of the preceding RE. ab+ will match ‘a’ followed by any non-zero number of ‘b’s; it will not match just ‘a’.

### **QuestionMark(?)**
### Causes the resulting RE to match 0 or 1 repetitions of the preceding RE. ab? will match either ‘a’ or ‘ab’.

### **{m}**
### Specifies that exactly m copies of the previous RE should be matched. Like {6} exactly match six regular expressions.

### **{m,n}**
### Causes the resulting RE to match from m to n repetitions of the preceding RE, attempting to match as many repetitions as possible. For example, a{3,5} will match from 3 to 5 'a' characters. 


### **{m,n}?**
### Causes the resulting RE to match from m to n repetitions of the preceding RE, attempting to match as few repetitions as possible. For example,  while a{3,5}? will only match 3 characters.

### **{m,n}+**
### Causes the resulting RE to match from m to n repetitions of the preceding RE, attempting to match as many repetitions as possible without establishing any backtracking points.  For example, on the 6-character string 'aaaaaa', a{3,5}+aa attempt to match 5 'a' characters, requiring 2 more 'a's, will need more characters than available and thus fail, while a{3,5}aa will match with a{3,5} capturing 5, then 4 'a's by backtracking and then the final 2 'a's are matched by the final aa in the pattern. x{m,n}+ is equivalent to (?>x{m,n}).

### **[]**
### Used to indicate the set of charcters in a set. Ranges of characters can be indicated by giving two characters and separating them by a '-', for example [a-z] will match any lowercase ASCII letter, [0-5][0-9] will match all the two-digits numbers from 00 to 59. 

## **Functions**

### **Compile Method**
### import re
### syantax
### re.compile(pattern, flags=0)
### Python’s re.compile() method is used to compile a regular expression pattern provided as a string into a regex pattern object (re.Pattern). Later we can use this pattern object to search for a match inside different target strings using regex methods such as a re.match() or re.search().

## **Search Method**
### **syantax**
### re.search(pattern, string, flags=0)
### Scan through string looking for the first location where the regular expression pattern produces a match, and return a corresponding match object. Return None if no position in the string matches the pattern; note that this is different from finding a zero-length match at some point in the string.


### **Match Method**
### If zero or more characters at the beginning of string match the regular expression pattern, return a corresponding match object. Return None if the string does not match the pattern; note that this is different from a zero-length match.

### **Full Match Method**
### If the whole string matches the regular expression pattern, return a corresponding match object. Return None if the string does not match the pattern; note that this is different from a zero-length match.

### **Split Method**
### Split string by the occurrences of pattern. If capturing parentheses are used in pattern, then the text of all groups in the pattern are also returned as part of the resulting list. 

### **For Example**
###  re.split(r'(\W+)', 'Words, words, words.')
### **Output**
### ['Words', ', ', 'words', ', ', 'words', '.', '']

### **Sub method**
### re.sub() function stands for a substring and returns a string with replaced values. Multiple elements can be replaced using a list when we use this function.

### **Lemmetization**
### Lemmetization are used to generate inflected words based on actual language word. It considers the context and convert into meaningful base form called lemmetization. For example convert caring into care, historical into history etc.

### **Removing Rare Words**
### Usually both the most frequent and most rare words are not useful in providing contextual information.Very frequent words are called stop words. As stop-words occur in almost every sentence/document, they do not help in uniquely identifying content in sentences. 

### **Feature Extractor Term Frequency and Inverse Frequency Document (TFIDF)**
### TFIDF works by proportionally increasing the number of times a word appears in the document but is counterbalanced by the number of documents in which it is present. Hence, words like ‘this’, ’are’ etc., that are commonly present in all the documents are not given a very high rank. However, a word that is present too many times in a few of the documents will be given a higher rank as it might be indicative of the context of the document.

### **Cross Validation**
### We used the cross validation to assess the performance and generalization ability of a machine learning model. It involves partitioning the dataset into multiple subsets or "folds" and using these folds for training and evaluation in an iterative manner. The most commonly used type of cross-validation is k-fold cross-validation.

### **Using Logistic Regression**
### Logistic regression is a popular choice for sentiment analysis due to its simplicity, interpretability, and computational the efficiency. By selecting logistic regression as your classification algorithm, you will be able to build a sentiment analysis model that can effectively predict the sentiment or emotion associated with textual data.

### **Model Evaluation**
### This step is an essential step in machine learning to assess the performance and effectiveness of a trained model. It helps determine how well the model generalizes to unseen data and provides insights into its strengths and weaknesses. We calculate Accuracy Score, Precision, Recall, F1-Score.

### **Predictiction on New Data**
### Predictions on new data using trained sentiment analysis model, we Preprocess the new data in the same way you preprocessed the training data. This involves cleaning the text, tokenizing it, removing stop words, and any other necessary transformations or normalizations. Extract the same features from the new data that you used during training. For example, if you used TF-IDF, apply the TF-IDF transformation to the new data to obtain the feature representation. Use trained logistic regression model to predict the sentiment of the new data. Pass the preprocessed and feature-extracted data through the logistic regression model, which will output the predicted sentiment class.


