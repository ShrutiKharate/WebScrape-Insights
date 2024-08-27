# WebScrape Insights - Data Extraction and Text Analysis from URLs

This project involves extracting articles from a list of URLs, performing detailed text analysis, and merging the results with the original data. The final output provides a comprehensive dataset that combines the original content with various text analysis metrics.

## Workflow Summary

### Extract Articles:

Load URLs from an input Excel file.
Extract and clean the article text.
Save the cleaned articles to text files.

### Analyze Texts:
Load and analyze the text files for various metrics.
Save analysis results to an intermediate Excel file.

### Combine Data:
Merge the original data with analysis results.
Save the combined data to a final Excel file.

### Final Output:
Intermediate Output: Text analysis metrics for each article.
Final Output: Combined original data with analysis metrics, providing a complete view.

## Approach

### Data Extraction and Cleaning

#### Libraries Used:
requests: Fetch web content from the provided URLs.
BeautifulSoup from bs4: Parse and extract article content from HTML.
re: Clean the text using regular expressions.

#### Key Functions:
clean_text(text): Removes unwanted patterns (e.g., URLs, email addresses) to focus on the article's core content.
extract_article(url): Extracts and cleans article text, returning the trimmed content.
save_article(output_folder, url_id, text): Saves cleaned articles as text files using URL IDs as filenames.
Text Analysis

#### Libraries Used:
nltk: Tokenization and syllable counting.
TextBlob: Sentiment analysis.

#### Key Functions:
syllable_count(word): Estimates syllables per word.
analyze_text(text): Computes metrics including sentiment, readability (e.g., FOG index), and additional text metrics.

#### Processing:
process_texts_from_folder(folder_path): Analyzes each text file in the specified folder and saves results to an intermediate Excel file.
Combining Results

#### Combining Data:
combine_and_save(input_file, output_file, final_file): Merges original data with analysis results, saving the comprehensive dataset to a final Excel file.

### Dataset Description
The dataset contains various metrics related to text analysis and readability for a collection of articles or web pages. Each row represents a different article, identified by a unique ID and URL. The metrics provided for each article are:

-URL

-Positive Score

-Negative Score

-Polarity Score

-Subjectivity Score

-Average Sentence Length

-Complex Word Count

-Word Count

-Syllable Per Word

-Personal Pronouns

-Average Word Length

-FOG Index

-Percentage of Complex Words

-Average Number of Words Per Sentence

### Potential Applications
This data is highly versatile and can be used for various purposes, including:

1. Analyzing Readability and Complexity: Assess how easy or difficult it is to read different articles.
2. Sentiment and Subjectivity Analysis: Understand the emotional tone and objectivity of the content.
3. Comparing Writing Styles: Evaluate and compare the writing styles across different articles or authors.
4. Identifying Content Trends: Observe trends in content complexity or sentiment across various topics or time periods.
5. Evaluating Content Effectiveness: Determine how engaging or accessible content is based on readability and sentiment metrics.
