# jepordy-transformer-school-project

In this project, I created a transformer model able to classify the category of a given jepordy question. 

While the accuracy was only 12% on the testing data, when examining the topics guessed by the model, in many cases the topic was a reasonable guess given the question.

More information on this project is included in 


# Jeopardy Question Topic Prediction

## Project Overview

For this project, I decided to go with the Jeopardy questions project.

One thing I needed to decide for this project was how I was going to deal with the amount of data. I narrowed down the data to topics that were repeated more than 15 times and had around 1,500 categories left.

I experimented with different transformer architectures and unembedding methods to find a balance between training time and model accuracy.

## Model Architecture

I decided to go with 4 attention heads and 2 transformer blocks since the timing seemed reasonable and the accuracy seemed higher than other versions.

For the embedding, I decided to go with NLP since I was familiar with it from last project. Since NLP gives 300 entries in the vector by default, that was the dR I went with.

For the unembedding, I tried a few different methods. First, I tried average pooling. After, I used max pooling. When I used max pooling, I reached an accuracy of 30% on the training but only 11% on the testing set. Therefore, I used an attention method and trained it on 20 epochs. This was my final method.

## Results

The model did not do very well on the testing data, not achieving above 12% accuracy on any of my methods. The final model managed training accuracy of around 80%, but the model only had a 9% accuracy on the testing data.

However, when I make up sentences and questions, the topic given seems to be relevant. For example:

- **Input:** "Football and hockey are very popular sports."
  - **Predicted Topic:** BALLET
- **Input:** "I know a song that gets on everybody's nerves."
  - **Predicted Topic:** SONG STANDARDS

## AI Usage

There were some tasks that I used AI with to help me with my code. I used ChatGPT for all of my AI usage. The first thing I used it for was kind of like a diary, where I talked about my ideas for the project and received some feedback, as well as to answer questions and improve my understanding of transformers.

Another thing I used AI for was with the chunking during the word embedding process. I used some help to decide how to chunk the data, though this ended up not being used as I ultimately decided to decrease the amount of data used.

Finally, I had some help from ChatGPT with the unembedding of the transformer.

---

For a more detailed discussion of the project development and experimentation, see the included Word document.
