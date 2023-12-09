# more-of-the-same-thing
Repositiory for USC CSCI 567 ML project on 
## INVESTIGATING VARIABILITY IN DATASETS AND IT’S IMPACT ON MODEL ROBUSTNESS

by Abhishek Anand, Muyuan He

The project contains 2 phases:
1. Calculate the explained variance curve for each dataset by sampling subsets.
2. Train a model for each subset and check their test set accuracy for in-distribution performance and accuracy on other dataset test sets for out-of-distribution performance/model robustness.


All the experiments were carried out on Google Colab and Kaggle using H100, P100 and T4 GPUs.

## Datasets

### Training datasets

Dataset variablility analysis was performed on the following datasets 
#### Sentiment Analysis
1. IMDB [Link](https://huggingface.co/datasets/imdb)
2. SST2 [Link](https://huggingface.co/datasets/sst2)
3. Tweet Eval [Link](https://huggingface.co/datasets/tweet_eval)

#### Natural Language Inference
1. SNLI [Link](https://huggingface.co/datasets/snli)
2. MNLI [Link](https://huggingface.co/datasets/SetFit/mnli)
3. ANLI R3 [Link](https://huggingface.co/datasets/anli)

### Eval datasets'

Additional eval dataset for both the tasks were used to get a representative sample for testing model robustness.

#### Sentiment Analysis
1. Rotten Tomatoes [Link](https://huggingface.co/datasets/rotten_tomatoes)
2. Yelp Reviews [Link](https://huggingface.co/datasets/yelp_polarity)
3. Amazon Kindle Reviews [Link](https://www.kaggle.com/datasets/meetnagadia/amazon-kindle-book-review-for-sentiment-analysis)
4. Twitter [Link](https://www.kaggle.com/datasets/cosmos98/twitter-and-reddit-sentimental-analysis-dataset)
5. Reddit [Link](https://www.kaggle.com/datasets/cosmos98/twitter-and-reddit-sentimental-analysis-dataset)
6. Finance Sentiment [Link](https://www.kaggle.com/datasets/sbhatti/financial-sentiment-analysis)


#### Natural Language Inference
1. SICK [Link](https://huggingface.co/datasets/sick)
2. ANLI R1 [Link](https://huggingface.co/datasets/anli)
3. ANLI R2 [Link](https://huggingface.co/datasets/anli)
4. SemEval 2014 Task 1 [Link](https://huggingface.co/datasets/sem_eval_2014_task_1)


## Execution
* All code is in the notebooks folder separated between the 2 tasks. There is one notebook for each dataset and a separate notebook for generalization evaluation.

* Each notebook saves the results in the local directory which would have to be created according to the path mentioned in the code.

* Final results are processed using notebooks in post-processing folders where we each dataset result-[dataset-name].ipynb processes dataset specific results and agg-*.ipynb aggregates the dataset specific results and processes the results for a task to generate metrics and plots which are saved in each task's analysis_results folder.