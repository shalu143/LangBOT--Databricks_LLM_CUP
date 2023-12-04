#  सखा- भाषा अब कोई बाधा नहीं है
# Sakha- Language is no more barrier
Databricks LLM CUP: Ready to launch your AI game to new heights? Build, iterate and polish your LLM ideas into shiny, production-ready solutions with this competition.

## Contents
* [Submission or Project Name](#Prakriti)
    * [Contents](#Contents)
    * [Short Description](#Short-description)
         * [What's the Problem?](#what's-the-problem)
         * [The Idea](#the-idea)
    * [Demo Video](#Demo-video)
    * [The Architecture](#the-architecture)
    * [Getting Started](#Getting-started)
    * [Built-with](#Built-with)
    * [Acknowledgments](#Acknowledgments)
 
## Short Description
### What's the Problem
There are many geographical regions in the world, where more than one language is generally spoken. India is one such multilingual country, where a number of languages are spoken, and a mere 10% are English literate. Here, a single common language is adopted in the community for proper communication. But this can cause one language to be dominant over others, and can be a disadvantage to the speakers of other languages. This can also result in the disappearance of a language, its distinctive culture and a way of thinking. For national / international companies here, having their business / marketing content in multiple languages is an expensive option, hence majority of them stick to one language of commerce – English, which could also mean losing opportunity to better connect with local audiences and thus losing potential customers. While there is nothing wrong with using English, those who are not conversant in that language are left out of the mainstream commerce.


### The Idea
Our idea is to bridge this gap. People should be allowed to express themselves, ask their queries in their own language. We propose a solution that Let people ask queries in local language, use LLMs to understand and get information in English and translate this back into local language. We harness the power of Large Language Models for two uses – one to translate from local language to English and vice-versa, find most similar query in our database, if not then to answer his query via base LLM. This solution intends to let people query and get their queries answered in their own local language. This will only be applicable to those languages that are supported by the underlying LLM. This will not only help businesses especially banks reach out wider population but to get benefits of banking reach the common man and help him improve his financial prospects. 

## The Architecture
* The user opens the Gradio app and has options of typing the data in the local language
* Translation: Utilizing given prompt in given local language using LLM (Llama-70b-chat) through mlflow route.
* RAG: The translated prompt is converted to embeddings using Instructor-xl embeddings and searched in the created vector database(chroma) from the local language personalised data.
* The Prompt with the context (most similar embeddings from the semantic search) is passed to the LLM for the result
* Translation: Translation of result in the local language
