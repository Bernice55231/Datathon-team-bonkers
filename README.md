# Datathon-team-bonkers
**Stepping Through History**

**About the data:** ProQuest Historical Newspapers collection contains machine-readable full text and accompanying metadata for newspapers at the individual article level for 26 historical newspapers. There are 55 million digitized pages covering from the 1800s to 1900s. One feature of newspapers that has a long history is advertisements. In this dataset, each advertisement is labeled so that we are able to analyse them separately.

**Challenge Goals:** What if we were to hold a century’s worth of newspaper advertisements and their features in one dataset? What could we learn about the companies who have advertised and the products they have presented? What do we need to do to obtain information from unmarked text produced by OCR software? The challenge has three goals: to extract elements from historical newspapers, to fix OCR errors in scaled files, and to use NLP in identifying different elements of advertisements.

**Team work:**
There are four steps in our project. 

***Retrieval of data*** Using R code to parse multiple xml files into a single csv file. We created a dataframe to store multiple types of information in the original xml file. The dataframe contains record ID for each newspaper, the publication date of the article, the publisher, the full text of the article and the optional column, abstract.

***Handling OCR errors*** Scanning from the pdf format, the texts in the dataset may contain unreadable characters. Therefore, we need to write algorithms to do the optical character recognition and clean the data so that we could apply following algorithms to analyze. Basically, we remove the rebundant white spaces, replace the html characters with human readable characters, and remove the unnecessary punctuations. Then, we use sym_spell package to fix the misspelled words. We alsi define another function to deal with the stopwords in English since our Natural Language Processing part relies on counting the frequency of words based on their type. Therefore, we need to remove the impact of the stopwords.

***Natural Language Processing*** Importing dataframe from our csv file, we got the originial dataset for these newspapers. We firstly deal with the 'full_text' part, which represents the content of the newspaper. Basically, we do the OCR cleaning, then apply the nltk package to detect the texts and classify them based on their type. Accordingly, we could obtain the words that is most representative or could generalize the content of the newspaper.
