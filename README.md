# BBC-News-Classification
1)Imported the data and created the data frame called main_data having columns: texts and topic extracted from all the 5 sections.
2)Created the List of all the G20 countries, including possible modifications to the names (e.g. – USA, America and US for the United States). 
3)To mine the information from 2,225 articles from the BBC, I used a NLP technique called Named Entity Recognition (NER), which is used to identify “named entities” in a sentence. Named entities are parts of a sentence such as products, countries, companies, numbers. I am using the spaCy library for this. spaCy recognizes GPE and NORP entities among others. (GPE: Countries, cities, states and NORP: Nationalities or religious or political groups.)
4) Filtered out all the countries common in GPE and the list of G20 Countries and stored in the column g_20_countries.
5) Using g_20_countries I counted the number of articles for each individual country and number of articles for overlapping countries.
Further improvement can be made in identifying a document for a country, if we further process the GPE and NORP found in the process. Also, for documents without a country associated with it, I could have tried a multi output model. The reason I didn’t go forward with this approach is because of the small size of data.
6) I did the pre-processing of texts using Tokenization, Stemming, Lemmatization and removing Stop Words. After that I used two Text vectorization approaches namely TF-IDF and Count Vectorizer to transform text into vectors.
7)Then I used topic modelling to extract the main topics that occur in the given set of articles. I used 3 types of topic modelling namely: Truncated SVD, Randomized SVD and LDA (Latent Dirichlet Allocation). 
8) While all the approaches gave similar results, TF_IDF along with LDA gave the best results providing best segmentation among various topics. I chose 10 topics for modelling, as we wanted to extract all topics being talked about. As we already had 5 topics stated, any number above 5 would’ve been fine. 10 gave the best results.
I used this combination of TF_IDF + LDA for the upcoming tasks.
