# Datathon-team-bonkers
**Stepping Through History**

**About the data:** ProQuest Historical Newspapers collection contains machine-readable full text and accompanying metadata for newspapers at the individual article level for 26 historical newspapers. There are 55 million digitized pages covering from the 1800s to 1900s. One feature of newspapers that has a long history is advertisements. In this dataset, each advertisement is labeled so that we are able to analyse them separately.

**Challenge Goals:** What if we were to hold a century’s worth of newspaper advertisements and their features in one dataset? What could we learn about the companies who have advertised and the products they have presented? What do we need to do to obtain information from unmarked text produced by OCR software? The challenge has three goals: to extract elements from historical newspapers, to fix OCR errors in scaled files, and to use NLP in identifying different elements of advertisements.

**Team work:**
There are four steps in our project. 
***Retrieval of data*** Using R code to parse multiple xml files into a single csv file. We created a dataframe to store multiple types of information in the original xml file. The dataframe contains record ID for each newspaper, the publication date of the article, the publisher, the full text of the article and the optional column, abstract.
***Handling OCR errors*** Scanning from the pdf format, the texts in the dataset may contain unreadable characters. Therefore, we need to write algorithms to do the optical character recognition and clean the data so that we could apply following algorithms to analyze. Basically, we remove the 
