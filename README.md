# Tracing sentiment in the political discourse on homosexuality in the German Reichstag, 1895–1914
## Code repository
### DHNB2026 – Anna Maria Ramm
This repository contains the code for the article 'Tracing sentiment in the political discourse on homosexuality in the German Reichstag, 1895–1914'. Both input data and results can be found in the 'data'-file.

preprocessing.ipnyb: performs standard preprocessing procedures using dataset_speeches.csv, consolidations.csv, spelling.csv and stopwords.csv. The output is prep_dataset_speeches.csv.

surrounding_terms.ipynb: iterates over the preprocessed txt-files to identify the words surrounding the search terms in order to perform a sentiment anaylsis on the context of homosexuality. The output is keyword_contexts.csv.

sentiment_analysis.ipynb: operates with prep_dataset_speeches.csv and keyword_contexts.csv and performs a sentiment analysis using the lexicon sentiment_lexicon.csv. Includes the creation of new columns and an iteration over each word in the speeches that is compared with the lexicon. The output is result_sentiment_speeches.csv and result_sentiment_contexts.csv

most_common_nouns.ipynb: iterates over the preprocessed txt-files to identify nouns in the speeches. The output (most_common_nouns_speeches.csv) contains the extracted nouns with corresponding amounts and ids.

visualizations.ipnyb: creates visualizations found in the article.
- Fig. 01: uses search_terms.csv as input and visualizes the frequency of keywords.
- Fig. 02: creates a bar-plot using search_terms_match_sexu.csv to visualise orthographic and lexical variance of a specific keyword.
- Fig. 03: normalization of calculated sentiment values in sentiment_analysis.ipynb using result_sentiment_speeches.csv and result_sentiment_contexts.csv a new column is created that includes the normalized values. The visualization uses result_sentiment_comparison.csv which includes the normalized sentiment values to compare the results of the sentiment analyses in a line-plot.
- Fig. 04: using heatmap_topics.csv, a heatmap is created that shows the distribution of topics over time.
- Fig. 05: a line-plot (similar to fig. 03) is created that uses topic_count_military.csv, topic_count_law.csv, topic_count_science.csv and topic_count_society.csv to visualize the normalized sentiment values per topic.
- Fig. 6, 7 & 8 reuse result_sentiment_comparison.csv to visualize the sentiment scores of different political orientations in a line-plot. Both Fig. 7 and 8 highlight certain orientations.
