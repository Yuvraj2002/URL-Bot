# URL-Bot
Web Data Scraping, Standardization and Automation System for California Construction Projects.

This project automates the process of fetching, extracting,
and standardizing data related to construction and
infrastructure projects in California. It utilizes web scraping
techniques, data parsing, and OpenAI's language model to
generate standardized information.

1.
requests: Used for making HTTP requests to fetch web
pages.
BeautifulSoup: A Python library for parsing HTML and
XML documents, used here for web scraping.
langchain.llms: Library for interacting with OpenAI's
language models (LLMs).
langchain
_
openai: Additional library for OpenAI's LLMs.
langchain.prompts: Provides templates for generating
prompts for language models.
langchain.chains: Module for working with language
chains, including LLMChain for OpenAI's LLMs.
pandas: A data manipulation and analysis library used
here for handling structured data.
Function fetchAndSaveToFile(url, path):
2.
Takes a URL and a file path as inputs.
Uses requests to fetch the content from the URL and
saves it to the specified file path.
Web Scraping and Data Parsing:
3.
The code starts by fetching the HTML content of a
webpage (a URL related to California construction
projects) using fetchAndSaveToFile.
It then reads the saved HTML file and parses it using
BeautifulSoup (html.parser).
Extracts relevant information (locations) from the
parsed HTML using BeautifulSoup's findAll method
and stores it in p_
texts.
OpenAI Language Model Interaction:
4.
Initializes an instance of OpenAI's language model
(LLM) using the OpenAI class from langchain.llms.
Defines a prompt template using PromptTemplate
from langchain.prompts, which will be used to
generate standardized data.
