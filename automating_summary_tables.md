## DRAFT: Automating Summary Research Tables with ChatGPT and Python

When it comes to conducting research,  ChatGPT can be an incredible force multiplier. 

Just type in a question and ChatGPT returns hundreds of words that you can quickly copy, paste into a word processing tool and tailor to your needs.  

Great. But what about a research effort seeking concise, high-level answers for a long list of items? The type of research that usually is communicated via  summary research tables?

With such research, copy and paste would be incredibly tedious and time consuming.  

Fortunately, you can use a combination of ChatGPT, Python and Excel to automate the process. 

This article walks through a Jupyter notebook showing how a Python program might work on a demo research project.

###  Choosing Between Manual and Automated

This project starts with a list of business and organizational use cases for AI and machine learning algorithms that I have been curating for some time, using  a simple spreadsheet. The list is broken into functional areas (e.g., Marketing, HR, Legal) and industries (e.g., Agriculture, Automotive, High-Tech). 

I could have automated the process, by asking ChatGPT to provide a list of a dozen or so functional areas and industries, and then requesting use cases for each category. But since I already had that information, I simply asked ChatGPT to suggest any changes.  I agreed with some of the edits, and manually made them in the spreadsheet.  

But in addition to identifying use cases, I wanted to expand my table to include examples of which machine learning algorithms (e.g., logistic regression, decision trees) best support each use case.  In particular, with  the emergence of large language models (LLMs), I wanted to ask how they might be applied to each use case. 

The code below automates this process. Note that the code could be modified to automate the first two tasks above (identifying categories and use cases) in a similar way.  The choice of where to draw the line between manual and automated provcesses will depend on your own needs and circumstances.  

### Getting started
First, we install necessary libraries and import them into our environment.

```python
! pip install openai
! pip install requests
```
```python
import os
import openai
import requests
import pandas as pd
```
To use ChatGPT via OpenAI's API, you will need to sign up and request an API key. (OpenAI is the company behind ChatGPT.)

*   Go to OpenAI's Platform website at [platform.openai.com](https://) and select "Sign up" in the top-right corner.
*  Once you have an account, click your profile icon at the top-right corner of the page and select "View API Keys."  
*   Clck "Create New Secret Key" to generate a new API key.
*   Save the API key.


```python
def hello_world():
    print("Hello, world!")
```
```python
def hello_world():
    print("Hello, world!")
```
```python
def hello_world():
    print("Hello, world!")
```
```python
def hello_world():
    print("Hello, world!")
```
