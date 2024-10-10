# Generating Text with an Autoregressive Model

We will build a simple model for generating text in the style of a given book. In lecture, we learned about **probabalistic models**, which views the data given as the result of some random process. In this lab, we will be using this probablistic assumption to **generate new data**. Specifically, we will use an autoregressive model, as discussed in Lecture 4. Our model will begin with a list of words, and generate a new word based on the $k$ most recent previous words. $k$ is chosen to be a small fixed constant, which limits the complexity of the model.

Sometimes this type of model is also called a Markov Model. Similar techniques can be used for time-series and really any other data that has some notion of _recency_. For example, our Lab 2 studied an auto-regressive model for time series data. Even fancy modern language models like the GPT family of models are auto-regressive.

We get our input data from [Project Gutenberg](https://www.gutenberg.org/), a free library of public-works books made available online. By default, we include four books in this lab:
- _Alice in Wonderland_ by Lewis Carroll
- _Metamorphosis_ by Franz Kafka
- _The Count of Monte Cristo_ by Alexandre Dumas
- _The Complete Works of William Shakespeare_ by William Shakespeare

