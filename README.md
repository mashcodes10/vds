## README: Movie Data Exploration with GraphDB and Azure OpenAI
## Overview
This project utilizes a movie dataset and explores interactions with GraphDB and Azure OpenAI services to build a robust information retrieval and question-answering system. We use this dataset to perform various operations, including loading, cleaning, querying, and building a retrieval-augmented generation (RAG) model for answering queries using LangChain, GraphDB, and Azure OpenAI.

## Dataset
Chosen Dataset: The project uses a movie dataset, potentially containing various features such as titles, genres, release dates, cast, crew, ratings, and other descriptive fields related to movies.
https://raw.githubusercontent.com/tomasonjo/blog-datasets/main/movies/movies_small.csv
## Focus Question and Problem Type
Focus Question: The main focus is to answer complex queries related to movie data by leveraging GraphDB's graph structure for efficient data storage and querying, integrated with Azure OpenAI's capabilities for natural language processing.
Problem Type: This is primarily a retrieval-based problem, focused on question-answering rather than predictive modeling. It leverages information retrieval and natural language processing (NLP) rather than traditional classification or clustering.
## Data Cleaning Plan
General Cleaning Approach:
Ensure consistency in key attributes (e.g., uniform date formats, consistent naming for genres and cast members).
Remove duplicates and null entries where appropriate to maintain database integrity.
Standardize text data to facilitate smoother querying and embedding generation.
Convert categorical information (such as genres) into a format compatible with GraphDB’s indexing and Azure OpenAI embeddings.
# Model Creation Plan
Data Preparation for GraphDB:
Load the cleaned movie dataset into GraphDB.
Organize entities (like movies, actors, genres) and relationships (such as actors starring in movies or movies belonging to genres) to create an efficient graph-based structure.
Building the Retrieval-Augmented Generation (RAG) Model:
Use Azure OpenAI to embed text data, making it easier to perform semantic searches.
Implement LangChain to act as a bridge, allowing us to leverage both GraphDB for structured data and OpenAI for natural language understanding.
## Algorithm Choice
Chosen Algorithm: Retrieval-Augmented Generation (RAG) model
Description: The RAG model combines information retrieval with language generation. GraphDB acts as the retrieval engine, quickly locating relevant data nodes based on structured queries. Azure OpenAI's language model then interprets and generates answers based on retrieved information.
Reasoning: RAG is particularly suited for question-answering tasks that require both factual accuracy (from GraphDB) and natural language generation (from Azure OpenAI).
## Evaluation Metrics
Chosen Metrics:
Precision and Recall for retrieved answers: Measuring the accuracy and completeness of the responses generated.
Response Accuracy: How well the generated answers align with actual data in the database.
Latency: Measuring response times to ensure that the retrieval and generation are efficient.
Why These Metrics Are Useful: Precision and recall provide insight into the model's relevance and coverage, while response accuracy and latency ensure that the model not only retrieves accurate information but does so in a timely manner.
## Model Performance
Metric Scores: [To be added upon completion, e.g., Precision: X%, Recall: Y%, Latency: Z seconds]
Metric Usefulness: The metrics were selected to align with the project’s focus on providing accurate, relevant, and timely information to the user.
## Resources
GraphDB Documentation: https://graphdb.ontotext.com/documentation/
Azure OpenAI Documentation: https://learn.microsoft.com/en-us/azure/cognitive-services/openai/
LangChain for RAG Models: https://python.langchain.com/en/latest/index.html
## Additional Information
Why This Approach is Suited for the Problem: RAG models are ideal for tasks that require structured data retrieval combined with flexible language understanding. This setup takes advantage of GraphDB’s data structure and Azure OpenAI’s powerful language generation, providing a scalable, efficient, and interactive solution to query complex movie-related information.