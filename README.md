# TFM-Evolution-of-Science-Topics-in-Spain


Scientific publishing is growing rapidly in the last years, with the open access publishers contributing heavily to this growth. This study aims to identify the main topics of scientific investigations carried out from 2009 in our country. Also we can see the trend of this and see what fields are the ones with more papers published in this period of time.

The idea is to create a topic modelling based on the abstracts of the papers published from 2009 in Spain, this way we can cluster the documents in the different topics obtained from the abstracts.

### Dataset Creation:

We begin with no dataset for this. For this study I have used the API of Dimensions ( part of Digital Science ) which provides an extensive database containing information about publications, institution, authors, etc. 

Dimensions API provides and intuitive language, named DSL ( Dimensions Query Language )  to interact with their database. From here we will take the paper ids and the year of publication, however the full abstract text is not provided. Using the paper id we will create a web scraper to iterate over this Ids in their API UI. This way we will create our dataset, containing the Publication Id, the ful Publication Abstract and the year of publication of the paper.


### Topic Modelling

First, an important part will be the preprocessing of the abstracts in order to tokenize and lemmatize the abstract content so we can uncover the topics related to the document.

With the abtracts text processed and prepared for our models, we aim to get the topic distribution from the papers abstracts. In order to do this, we will try two of the main algorithms in topic modelling, LDA and LSI. In this algorithms you should entert the number of topics, so we will use the Coherence Model metric to evaluate the 'goodness' of this models and the best number of topics based on the different scores and our purpose. 

We will show the main words in each of the topics identified and from this we will infer the topics. When we have given coherent topic names based on the main words of each topic given in the model output, we will assign a topic to each abstract and create a new column in our dataset with the topic assigned.

### Visualization

In order to visualize the topics identified, we will use Tableau. In here we will create a workbook, showing the total numbers of papers of each topic, so we can easy visualize the main areas of scientific investigation in our country in this period of years. We will also create a timeline so we can see the evolution of these topics accross the years.

