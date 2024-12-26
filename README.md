# Hackathon Management Platform

This repository contains a comprehensive framework for managing hackathons, offering end-to-end event handling. The project leverages natural language processing (NLP) techniques for summarizing, analyzing, and scoring submissions, along with various tools and utilities to support code evaluation and insights.

## Problem Statement

Build a Hackathon Management platform for end-to-end event handling
Deliverables:
1. Allow participants to register with details
2. Provide a list of hackathon themes or categories.
3. Teams can upload their projects (e.g., code repositories(github links),
documents, and presentations), Store submissions securely with timestamp.
4.Build AI/ML techniques to help judges with insights from the submissions like:
a. Feedback Suggestions:Auto-generate constructive feedback for
submissions to save judges time.
b. Scoring Assistance: LLMs can pre-score submissions by:
i. Summarizing key project features.
ii. Analyzing problem-statement adherence.
iii. Suggesting scores for innovation, feasibility, and impact based on
predefined prompts.

### Libraries/Algorithms Used

## Libraries/Algorithms Used

### Libraries Used
- **[SQLite3](https://www.sqlite.org/index.html)**  
  A module to work with SQLite databases.

- **[Datetime](https://docs.python.org/3/library/datetime.html)**  
  Used for working with dates and times.

- **[re (Regular Expressions)](https://docs.python.org/3/library/re.html)**  
  Regular expression module for pattern matching in strings.

- **[Tabulate](https://pypi.org/project/tabulate/)**  
  For formatting data as plain-text tables.

- **[Requests](https://docs.python-requests.org/en/latest/)**  
  For making HTTP requests.

- **[Argparse](https://docs.python.org/3/library/argparse.html)**  
  A library for parsing command-line arguments.

- **[Base64](https://docs.python.org/3/library/base64.html)**  
  For encoding and decoding binary data in base64.

- **[JSON](https://www.json.org/)**  
  For parsing JSON (JavaScript Object Notation) data.

- **[GitHub API](https://docs.github.com/en/rest)**  
  To interact with GitHub using the API.

- **[Transformers](https://huggingface.co/transformers/)**  
  For using pre-trained models, especially for NLP tasks.

- **[OS](https://docs.python.org/3/library/os.html)**  
  For interacting with the operating system (file operations, etc.).

---

### Algorithms/Models Used
- **[Summarization Model: facebook/bart-large-cnn](https://huggingface.co/facebook/bart-large-cnn)**  
  Hugging Face's pre-trained BART model used for text summarization.

- **[Feedback Generation Model: EleutherAI/gpt-neo-1.3B](https://huggingface.co/EleutherAI/gpt-neo-1.3B)**  
  GPT-Neo (OpenAI GPT-style model) for generating constructive feedback based on provided summaries.

- **[Text Analysis Model: google/flan-t5-base](https://huggingface.co/google/flan-t5-base)**  
  FLAN-T5 (from Google) for code analysis or NLP tasks, a fine-tuned version of T5.

## Key Features

Hackathon Management:

Automates the process of evaluating submissions.

Generates structured analyses of project repositories.

Assigns scores based on predefined criteria, including innovation, feasibility, and impact.

Code Analysis:

Analyzes code files to extract purpose, key functions, and dependencies.

Utilizes Hugging Face models like google/flan-t5-base and facebook/bart-large-cnn for summarization and scoring.

Submission Scoring:

Evaluates combined analyses of all files in a repository.

Assigns scores on a scale of 1 to 10 for aspects like key project features, adherence to problem statements, and innovation.

File and Directory Processing:

Recursively processes all files in a specified directory.

Handles multiple file formats, including .py, .js, .ts, and .json.

Technologies Used

Python: Core programming language for the framework.

Hugging Face Transformers: Pre-trained models for text summarization and generation.

Google Flan-T5 Base: Lightweight model for text-to-text generation tasks.

Facebook BART Large-CNN: High-performance summarization model.

OS Module: For directory traversal and file handling.

Code Overview

summarization_pipeline.py

Summarizes text content using the facebook/bart-large-cnn model.

Handles long text by truncating input to fit the model's maximum token size.

analyze_code.py

Provides detailed analysis of code files.

Key aspects analyzed:

Purpose: Overall objective of the code.

Key Functions: Main methods and their roles.

Dependencies: External libraries or modules used.

Tools and Technologies: Identifies tools utilized in the project.

score_submission.py

Scores a project's analysis based on:

Key Project Features: Relevance and completeness.

Problem-Statement Adherence: Effectiveness in addressing the stated problem.

Innovation: Uniqueness of the approach.

Feasibility: Practicality and implementability.

Impact: Potential significance or usefulness.

Provides justifications for each score.

process_repository_and_score.py

Combines the functionalities of analysis and scoring.

Processes all files in a repository and generates a combined analysis.

Outputs structured scores and insights for the entire project.
