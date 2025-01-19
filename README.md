# CodeMaster: A DSA Problem Search Engine

## Project Overview
CodeMaster is a powerful search engine specifically designed to process and rank a large collection of DSA problems efficiently. Leveraging cutting-edge text processing techniques such as TF-IDF and BM25, the system ensures precise document ranking and delivers the most relevant results for user queries. It also tackles edge cases to provide accurate and user-friendly search experiences.

![Screenshot 2025-01-19 215821](https://github.com/user-attachments/assets/263513ab-32d0-40be-920b-30b0291769af)
![Screenshot 2025-01-19 215837](https://github.com/user-attachments/assets/649a781a-0d1b-4158-8c20-8be52ca2e694)
![Screenshot 2025-01-19 215856](https://github.com/user-attachments/assets/9626dae9-35b8-451b-9e88-933f502a2460)

## Key Features
- **Efficient Search Mechanism**: Uses TF-IDF and BM25 algorithms to rank documents by relevance to user queries.
- **Advanced Text Processing**: Handles complex cases like spelling corrections, camel casing, lemmatization, and numeric equivalences.
- **Real-Time Ranking**: Scores and ranks documents dynamically, prioritizing trusted sources and showing the top 10 results.

---

## Workflow

### 1. Keyword Generation and Scoring
- **Traditional String Matching**: Provides a basic approach but struggles with scalability.
- **Term Frequency (TF)**: Counts keyword occurrences but tends to favor longer documents.
- **Inverse Document Frequency (IDF)**: Adjusts scores by emphasizing rare terms across documents.
- **TF-IDF**: Combines TF and IDF to determine the importance of keywords effectively.

### 2. Normalization and BM25 Scoring
- **Normalization**: Accounts for document length to remove bias.
- **BM25**: Balances keyword influence to avoid overemphasis on specific terms.

### 3. Text Processing and Query Handling
- **Preprocessing**: Cleans query text by removing stopwords, punctuation, and applying lowercase transformation.
- **Keyword Extraction**: Identifies relevant terms while ignoring unrelated content.
- **Edge Cases**:
  - Spelling corrections.
  - Numeric conversions (e.g., "two" to "2").
  - Splitting camel-cased words (e.g., "twoSum" to "two sum").
  - Lemmatization for accurate word matching.

### 4. Search and Ranking
- **Query Processing**: Extracts and processes query keywords, then computes TF-IDF scores.
- **Cosine Similarity**: Measures the closeness of the query and documents.
- **Title Similarity**: Adds weight to documents with titles that closely match the query.
- **Ranking**: Applies BM25 for ranking and displays the top 10 results.

---

## Edge Cases Handled
- **Stopword Removal**: Eliminates common, irrelevant words (e.g., "is," "the").
- **Punctuation Removal**: Avoids mismatches by stripping punctuation.
- **Spell Checking**: Corrects misspelled query terms.
- **Lemmatization**: Matches words by reducing them to their base forms (e.g., "running" to "run").
- **Number-Word Conversion**: Treats numeric forms and their word equivalents as identical.
- **CamelCase Handling**: Splits camel-cased words for better keyword matching.
- **Title Similarity**: Considers document titles as part of the ranking process.

---

## Performance Optimization
- **RAM-Based Indexing**: Stores TF-IDF values in files and loads them into memory during startup, enabling faster searches and improved response times.

---

## How to Use
1. **Install Dependencies**: Ensure all required packages and libraries are installed.
2. **Start the Application**: Launch the search engine and input your queries to retrieve ranked results.
3. **Explore Results**: View the top 10 most relevant documents based on your search.

---

## Technologies Used
- **Backend**: Node.js
- **Frontend**: ejs template engine
- **Text Processing**: TF-IDF, BM25
- **Storage**: RAM-based indexing for fast access

---

## Future Enhancements
- Add support for more data sources and DSA platforms.
- Optimize the scoring algorithms for even larger datasets.
- Implement a user-friendly interface for better accessibility.

---


