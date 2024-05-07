# WebScrape-NLP-Analyzer

## Data Extraction and NLP

This project is designed to extract textual data articles from given URLs and conduct text analysis to compute variables. The code is implemented in Jupyter Notebook, chosen for its flexibility in experimentation and documentation.

### Approach

The project follows these steps:

1. **Input Data**: Reads input data from input.xlsx using pandas.

2. **Web Scraping**: Utilizes the requests module to retrieve the raw HTML content from the URLs specified in the input file. Web scraping is facilitated using the BeautifulSoup module.

3. **Text Extraction**: 
   - Identifies the article title using the <h1> tag and extracts the content using appropriate <div> tag and class name selectors.
   - Employs try-except blocks to handle exceptions due to potential variations in class selectors across different articles.

4. **Text Analysis**:
   - Utilizes the NLTK library for text analysis.
   - Segments the text into sentences using the Punkt tokenizer via sent_tokenize function.
   - Removes stop words (common words like 'the', 'and', 'I', etc.) using the NLTK stopwords module.
   - Tokenizes the text into words using the word_tokenize function.
   - Estimates the number of syllables in words using a simple syllable estimator.

5. **Variable Computation**:
   - Computes the required variables by iterating through multiple URLs and performing various calculations.

6. **Results Storage**:
   - Stores the computed variables in lists and organizes them into a dictionary with the specified column names.

7. **Exporting Results**:
   - Exports the results to Output Data Structure.xlsx for further analysis.

### Output

The output file "Output Data Structure.xlsx" contains the computed variables for each article, providing valuable insights into the characteristics of the text data extracted from the URLs.
