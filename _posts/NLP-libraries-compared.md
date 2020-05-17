---
title: NLP Comparison
author: Allan
layout: post
icon: fa-lightbulb
icon-style: regular
---

NLP is becoming increasingly important for more business objectives. Common use cases include question answering, paraphrasing or summarizing text, sentiment analysis, natural language BI, disambiguation, etc. Accurately extracting contextual information from text is critical for increasingly commonplace applications like chatbots, evaluating customer service or sales calls.
There are many options for NLP tools as a result of this popularity. Below are a selection of the most popular libraries with pros and cons for different use cases.

## SpaCy

SpaCy is a popular library for NLP for several key reasons. It is one of the fastest of the libraries compared here, in large part due to the fact that it was written in Cython from the ground up. It has an easy to learn interface, prioritizing one single tool with an object-oriented approach that can be highly optimized over offering a variety of tools for each application. With one line of code you can tokenize, lemmatize, label parts-of-speech and named entities, and embed your text with vectors from pre-trained models, among other options. Spacy comes with built in visualizers that can be incredibly useful in EDA. That usability comes at the expense of flexibility to some degree, when compared to NLTK. I find SpaCy to be my go-to tool for fast NLP pipelines and vectorization.

## NLTK

NLTK (short for Natural Language ToolKit) is essentially a string processing library, and although this seems straightforward, you may find yourself having to comb through the documentation to discover all of the functionality. It has many third-party extensions and plenty of approaches to each NLP task. NLTK tends to be more popular in scholarly research and with teams that want to build a solution from the ground up. I find NLTK most useful for quick tokenization or single element of a pipeline, for instance most common words in a corpus.

<span class="image left"><img src="{{ 'assets/images/nlp_pros_cons.png' | relative_url }}" alt="" /></span>

## Gensim

Gensim is an open-source library designed to handle large text collections through streaming data. This differentiates it from other libraries that target in-memory processing. Gensim includes several popular NLP Algorithms such as word2vec, latent semantic analysis, and non-negative matrix factorization, among others. However, it was primarily designed for unsupervised text modeling. Although the algorithms are powerful, it lacks the tools to provide a full NLP pipeline, and thus must be used alongside other libraries such as SpaCy or NLTK. I find Gensim to be very useful in unsupervised models like topic clustering.

## SparkNLP

SparkNLP unsurprisingly is designed to work within the Apache Spark ML framework. This has several advantages to other libraries mentioned here: Spark allows vectorization of in-memory columnar data, and optimizing for TensorFlow, which it uses behind the scenes, and allows the model to scale on any Spark cluster. This means that Spark NLP is able to optimize the entire execution (data load, NLP, feature engineering, model training, hyper-parameter optimization, and measurement) together at once.

If you are jealous of the speed and functionality, but aren’t comfortable moving your project to Spark, fear not, the API provides full Java, Scala, and Python functionality. Spark NLP, like SpaCy, supports a full NLP pipeline, and includes several additional features, like spell checking and sentiment analysis. SparkNLP includes production-ready implementation of BERT embeddings among other pre-trained models. I have found SparkNLP to be the best option for production models which require fast execution and scalability.

<span class="image left"><img src="{{ 'assets/images/NLP_table.png' | relative_url }}" alt="" /></span>

To summarize, both SpaCy and SparkNLP are powerful NLP tools for full NLP pipeline and fast processing. NLTK is powerful and can be used for simple NLP processes, or as an NLP pipeline but tends to have a steeper learning curve. Gensim is great for unsupervised NLP clustering and vectorization.

I would love to hear what your favorite NLP libraries are and how are you using them in the comments.
