
##
# Welcome Freshers! 🚀 Level 1 Task: The Super Basic Natural language processing logics

Hello and welcome! As you step into your AI/ML journey, it is essential to understand how computers process human language before diving into complex machine learning models. 

Before, Using automated libraried for processing, Will make a super basic language processor using python basic libraries 

---
## 🧠 Understanding the Problem

When people send messages, they use a lot of filler words like "the", "is", "my", and "to". These words don't help a system in figuring out if a user has any problems.

Your goal is to write a Python script that:
1. **Cleans the text** by removing common stop words so only the main useful keywords remain.
2. **Acts as a Decision Tree** using if-else statements to route the message to the correct department based on those keywords.

---

## 📝 The Official Task

### Objective
Build a Python function that takes a customer message, strips out stop words, and classifies the message into either **"Technical Support"**, **"Billing Support"**, or **"General Inquiry"** using an if-else decision structure.

### Requirements
1. Define a list of common stop words (e.g., `["the", "is", "at", "and", "to", "a", "for", "my", "i"]`).
2. Write a function `clean_tokenize(text)` that converts a sentence to lowercase, splits it into words, and filters out any words present in your stop words list.
3. Write a classification function `classify_message(text)` that passes the filtered keywords through an if-elif-else decision tree:
   * If keywords contain **"crash"**, **"bug"**, **"broken"**, or **"error"** -> Return **"Technical Support"**
   * If keywords contain **"bill"**, **"charged"**, **"payment"**, or **"subscription"** -> Return **"Billing Support"**
   * Otherwise -> Return **"General Inquiry"**
4. Test your script with at least 3 different sentences and print both the filtered keywords and the final classification result.

### Starter Template
You can use this snippet as a starting point to complete the assignment:

```python
# 1. Define common stop words to ignore
STOP_WORDS = ["the", "is", "at", "which", "and", "to", "a", "an", "for", "my", "i"]

def clean_and_tokenize(text):
    # TODO: Convert text to lowercase, split into words, and filter out stop words
    pass

def classify_message(text):
    # TODO: Get filtered keywords and use if-else logic to classify the message
    pass

# Test your code here
print(classify_message("the app crashes every time I open it"))
```
# Learning Resources
To help you complete this task, check out these beginner-friendly guides:

Python Official Tutorial - Control Flow (if-else & loops)

W3Schools Python Lists & Comprehensions Guide

Python Built-in String Methods (lower(), split())

# Resources
Youtube video link :[Video link]( https://www.youtube.com/watch?v=m5n7Gu1unsI)

Documentations : [Documentation](https://www.analyticsvidhya.com/blog/2019/08/how-to-remove-stopwords-text-normalization-nltk-spacy-gensim-python/)
