SkimLit: BERT-based Text Summarization Model
SkimLit is a text summarization model based on the BERT (Bidirectional Encoder Representations from Transformers) architecture. It aims to generate concise summaries of scientific articles, enabling users to quickly understand the key points and findings without needing to read the entire document.

Introduction
SkimLit leverages the power of BERT, a state-of-the-art transformer-based model, to perform abstractive text summarization. Unlike extractive summarization, which selects and combines important sentences from the original text, abstractive summarization involves generating new sentences that capture the essence of the document.

Understanding the Dataset
The dataset used for training and evaluation consists of scientific articles and their corresponding summaries. It includes features such as title, abstract, main text, and summary. The goal is to train the model to accurately generate summaries that capture the key information from the main text.

Title: Title of the scientific article Abstract: Summary of the main findings and conclusions Main Text: Full text of the article Summary: Concise summary generated by human annotators or extracted from the article

Model Architecture
SkimLit utilizes a pre-trained BERT model fine-tuned on the task of text summarization. The BERT model is first fine-tuned on a large corpus of text data to learn contextual representations of words. Then, it is further fine-tuned on the specific task of summarization using a supervised learning approach.

![App Screenshot](https://github.com/Ankitb700/Skimlit/blob/main/Images/bert%20model.png)
![App Screenshot](https://github.com/Ankitb700/Skimlit/blob/main/Images/Streamlit.png)
![App Screenshot](https://github.com/Ankitb700/Skimlit/blob/main/Images/app%20output.png)
![App Screenshot](https://github.com/Ankitb700/Skimlit/blob/main/Images/count%20plot.png)
![App Screenshot](https://github.com/Ankitb700/Skimlit/blob/main/Images/f1%20score%20images.png)
![App Screenshot](https://github.com/Ankitb700/Skimlit/blob/main/Images/modeling%20results.png)

Usage
To use SkimLit for text summarization:

Input the scientific article or text document you want to summarize. Pass the input text through the SkimLit model. Receive the generated summary as the output. Model Deployment SkimLit can be deployed as a web application or integrated into other software applications. For deployment:

Set up a web server or cloud hosting platform. Create a user interface for users to input text and view summaries. Deploy the SkimLit model on the server or platform. Connect the user interface to the model for real-time summarization. Example python Copy code from transformers import pipeline

Load pre-trained BERT-based summarization model
summarizer = pipeline("summarization")

Input text to be summarized
text = """ Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. """

Generate summary
summary = summarizer(text, max_length=50, min_length=10, do_sample=False)

print(summary) This example demonstrates how to use SkimLit to generate a summary of input text using the pre-trained BERT-based summarization model.

Screenshots
App Screenshot

Tech Stack
Python: SkimLit is implemented using Python, a versatile programming language widely used in machine learning and natural language processing tasks. Transformers Library: SkimLit utilizes the Transformers library by Hugging Face, which provides pre-trained models for natural language processing tasks, including BERT-based models for text summarization. Streamlit: SkimLit can be deployed as a web application using Streamlit, a Python library for creating interactive web applications. Heroku: SkimLit can be deployed on Heroku, a cloud platform that allows for easy deployment and scaling of web applications. Git: Git version control system is used for managing the source code of the SkimLit project, enabling collaboration and version tracking.
