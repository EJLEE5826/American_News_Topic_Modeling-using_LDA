# American_News_Topic_Modeling-using_LDA  

Analysis the Difference in Usual Vocabulary between American Press with Different Political Tendencies  
- liberal (Atlantic, Buzzfeed News, Vox)  
- conservative (Breitbart, New York Post, National Review, Fox News)  

Download Dataset: https://www.kaggle.com/snapcrack/all-the-news

<br>

## Development environment

- Language: Anaconda Python 3.6  
- IDE: Jupyter Notebook  

<br>

## How to Process  

1. Preprocessing  
   - Divide article based on political orientation  
   - Text operation  
   - Delete nonsense words-journalist, journalist name, and SNS account information  
   - Remove redundant words from both sides  
   
   Result of preprocessing: `saved_conserv.txt` `saved_liberal.txt`  

<br>

2. Topic Modeling - using LDA  
   - Make Bag of Words
   - TF-IDF vectorization
   - Trainign LDA model

    We use Gensim for LDA.  
    Result of Topic Modeling: `final_LDAmodel/*`  
    
    reference:  
    https://towardsdatascience.com/topic-modeling-and-latent-dirichlet-allocation-in-python-9bf156893c24  
    https://datascienceplus.com/evaluation-of-topic-modeling-topic-coherence/  

<br>

3. Evaluate  

    We make LDA models with topic num 10, 15, 20, 25.  
    We compared the results of each model and chose the model that best represents the difference between "liberal" and "conservative".  
    
    As Topic N becomes larger, the words that form Topic are revealed in detail.  
    However, the same word occurs in multiple topics.  
    
    You can see here an analysis of our model results.  
    `final report-American_News_Topic_Modeling-using_LDA.docx`  

<br>

## Manual  

  Run in your terminal (for conda environments):  

    $ conda install -c conda-forge gensim  
    $ conda install nltk  
    $ conda install -c anaconda matplotlib

- `Preprocessing.ipynb` Preprocess articles(with `Preprocessing/`)  
- `LDA.ipynb` make LDA models  
