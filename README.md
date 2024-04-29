# URL-Bot
Web Data Scraping, Standardization and Automation System for California Construction Projects.

This project automates the process of fetching, extracting,
and standardizing data related to construction and
infrastructure projects in California. It utilizes web scraping
techniques, data parsing, and OpenAI's language model to
generate standardized information.

Libraries Used - 
a) requests: Used for making HTTP requests to fetch web pages.
b) BeautifulSoup: A Python library for parsing HTML and XML documents, used here for web scraping.
c) langchain.llms: Library for interacting with OpenAI's language models (LLMs).
d) langchain openai: Additional library for OpenAI's LLMs. 
e) langchain.prompts: Provides templates for generating prompts for language models.
f) langchain.chains: Module for working with language chains, including LLMChain for OpenAI's LLMs.
g) pandas: A data manipulation and analysis library used here for handling structured data.

Working of the code - 
1. Web Scraping and Data Parsing:
The code starts by fetching the HTML content of a
webpage (a URL related to California construction
projects) using fetchAndSaveToFile.
It then reads the saved HTML file and parses it using
BeautifulSoup (html.parser).
Extracts relevant information (locations) from the
parsed HTML using BeautifulSoup's findAll method
and stores it in p_texts.

3. OpenAI Language Model Interaction:
Initializes an instance of OpenAI's language model
(LLM) using the OpenAI class from langchain.llms.
Defines a prompt template using PromptTemplate
from langchain.prompts, which will be used to
generate standardized data.

3. Generating Standardized Data:
Iterates through the list of locations (p_
texts) and
generates standardized data using the prompt
template.
Appends the generated output to the outputs list.

4. Processing Standardized Data:
Utilizes the initialized OpenAI LLM (llm) to process
each output generated from the prompt template.
Appends the processed text to the output_text list.

5. Data Extraction and Structuring:
Extracts relevant fields (Unique ID, Country Name,
Country Code, Region Name, Region Code, Geo
Location) from each processed text in output_text.
Structures the extracted data into lists (ids,
country_names, country_codes, region_names,
region_codes, geo_locations).

6. Creating a Pandas DataFrame:
Uses pandas (pd) to create a DataFrame from the
structured data.
The DataFrame includes columns for the extracted
fields: ID, Country Name, Country Code, Region Name,
Region Code, Geo Location.

7. Saving Data to Excel:
Specifies the file path for the Excel file
(output_it3.xlsx).
Saves the DataFrame to an Excel file at the specified
path using df.to_excel.

8. Output and Usage:
Prints the message indicating the successful saving of
the output to the Excel file.
The generated Excel file (output_it3.xlsx) contains the
standardized data regarding construction projects in
California, ready for analysis and reporting.
