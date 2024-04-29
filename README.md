# ML_Project24-TextSummarization

### Text Summarization - Extractive Summarization using TextRank
This project implements an extractive text summarization approach using TextRank. It extracts key sentences from a given text document to create a concise summary.

### Extractive Summarization

Extractive summarization identifies and extracts the most important sentences from a document to form a summary. Here, we use TextRank, a graph-based algorithm that analyzes the relationships between sentences to determine their significance.

### Code Workflow

##### Data Loading:
The script loads a CSV file containing the text articles (e.g., tennis.csv).
##### Sentence Tokenization:
NLTK library is used to segment the text into individual sentences.
##### Text Cleaning:
Text cleaning steps are applied to each sentence, including:
1.Removing non-alphanumeric characters.
2.Converting text to lowercase.
3.Removing stop words (common words like "the", "a", "an").
##### Word Embeddings:
A simple word embedding technique (sum of word vectors) is used to represent each sentence numerically.
##### Similarity Matrix Construction:
Cosine similarity is calculated between sentence vectors to measure their semantic similarity. This creates a similarity matrix where higher values indicate more similar sentences.
##### TextRank Algorithm:
The similarity matrix is used to construct a graph where nodes represent sentences and edges represent their similarity. TextRank is applied to this graph to assign a score to each sentence based on its importance and connections to other high-scoring sentences.
##### Summary Generation:
Sentences are ranked based on their TextRank scores. The top-ranked sentences are selected to form the final summary.


### Running the Script
Ensure you have Python 3 and the required libraries installed (numpy, pandas, nltk). You can install them using pip install numpy pandas nltk.

Place the script (text_summarization.py) and the CSV file (e.g., tennis.csv) in the same directory.

Run the script from the command line:
```
Bash
python text_summarization.py
```
This will print summaries for each article in the CSV file.


### Evaluation
Text summarization is a subjective task, and evaluating quality is an ongoing challenge. This code provides a basic extractive summarization approach. You can improve it by:

Trying different sentence ranking algorithms.

Incorporating more advanced features (e.g., named entities, part-of-speech tags).

Evaluating summaries against human-written ones using metrics like ROUGE score.


### Further Exploration

Explore abstractive summarization techniques that generate new text to create summaries.

Apply text summarization to different types of documents (news articles, research papers).

Integrate text summarization into a real-world application (e.g., news aggregator, document analysis tool).
