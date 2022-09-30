## SenseUA
A Qualitative Survey Response Cleaning Tool

## What it is:
SenseUA is a qualitative survey response cleaning tool that is powered by machine learning. The prototype was created in September 2022 by me (Roshan Edachali) to automate a task I was assigned at work. 

## How it was created:
Working with surveys that contain free form text data can be a chore to clean, and before SenseUA such ‘field cleaning’ of sometimes 1000 respondents at a time was done manually. Whoever was assigned to clean the free form unaided awareness text data would sift through 1000s of rows of 16 responses to questions asking about awareness of financial providers and highlight response IDs that contained null, gibberish, or obscene language.  

<img width="705" alt="Untitled" src="https://user-images.githubusercontent.com/85485511/193170238-bff57109-9fed-4018-834b-dd6e7ee7ef0e.png">

For example, in the above image response IDs corresponding to Roll 1 and 5 would be flagged to be later deleted, whilst the others would be left as is. This process of sifting through responses happened every month and took up to 4 hours to complete. As I reached month two of this field cleaning process, I realized the potential of using the datasets that I had already created to teach a model what and what not to flag. I used Google Colab to create a model that learnt from past month’s field cleaning datasets to predict whether or not future responses would be flagged or not. 

## How it works:
SenseUA works on unsupervised learning of past field cleaning datasets. It is provided with various text responses, and whether or not they were flagged for cleaning. It uses this knowledge to classify inputted text responses with a tested accuracy rate of 94%. Once the classification is complete, I quickly manually check the predictions, and load it into the master dataset for future use. Thus, the model becomes stronger and stronger with use.
