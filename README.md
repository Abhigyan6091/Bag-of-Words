Objective:
This project explores a set of 9 documents across three domains—politics, science, and sports—using the Bag of Words (BoW) model. We aim to calculate four key distance metrics between these documents: Jaccard Distance, Euclidean Distance, Cosine Distance, and Kullback-Leibler (K-L) Divergence. These metrics are used to assess the similarity between documents, enabling us to visualize patterns and domain-specific relationships.

1. Methodology

1.1 Data Preparation
The dataset consists of nine documents—three from politics, three from science, and three from sports. Each document is processed using Python’s natural language processing libraries. The text data is tokenized, and stop words are removed to focus on meaningful words. The CountVectorizer is then applied to convert these text documents into a numerical format using the Bag of Words (BoW) model.

1.2 Bag of Words Model
The BoW model generates a term-document matrix where:
●	Rows represent the documents.
●	Columns represent unique terms across all documents.
●	Cell values represent the term frequency in each document.
We implemented this using the sklearn library: 
  

3. Distance Matrices
We computed the following matrices for each metric:

2.1 Jaccard Distance Matrix
This matrix captures the Jaccard distance between all document pairs. Documents within the same domain show lower distances, indicating higher similarity in their term sets.
2.2 Euclidean Distance Matrix
The Euclidean distance was calculated using the raw term frequencies from the BoW model. Here too, documents within the same domain showed smaller distances.
2.3 Cosine Distance Matrix
Cosine Distance effectively captured the similarity in the orientation of document vectors, revealing high similarity between documents in the same domain.
2.4 K-L Divergence Matrix
The K-L divergence captured differences in term frequency distributions, revealing greater divergence between documents of different domains compared to those within the same domain.
4. Visualizations
For better understanding, we visualized each distance matrix using heatmaps. These heatmaps provide an intuitive understanding of the relationships between documents. Below is an example of how we visualized the Euclidean Distance Matrix:
 
5. Analysis and Interpretation

4.1 Observations
●	Jaccard Distance: Documents within the same domain (e.g., all politics documents) exhibit smaller Jaccard distances, highlighting the overlap in their term sets.
●	Euclidean Distance: Euclidean distances are smaller between documents in the same domain, showing that these documents share similar term frequency patterns.
●	Cosine Distance: Cosine distance highlighted strong domain-specific clustering. For example, sports documents showed high similarity in vector orientation.
●	K-L Divergence: This metric reinforced domain-based divergence, as the term distributions between documents from different domains (e.g., science and sports) had greater divergences.

4.2 Key Insights
●	The documents within the same domain (politics, science, sports) exhibit higher similarity across all four metrics.
●	Cosine Distance and Jaccard Distance seem particularly useful for identifying domain-specific patterns.
●	K-L Divergence effectively captures the differences in term frequency distributions, offering additional insights beyond simple term overlaps.

6. Code and Documentation
The complete code used in this analysis is attached. It is structured as follows:
●	Data Preparation: Loading and tokenizing the documents.
●	BoW Model: Conversion of text to the term-document matrix.
●	Distance Metrics: Calculation of Jaccard, Euclidean, Cosine, and K-L distances.
●	Visualization: Generating heatmaps for the distance matrices.

Conclusion
This report demonstrated how different distance metrics can be applied to assess document similarity across different domains. By converting the documents into BoW representations and computing various distances, we could easily identify patterns of similarity within each domain.

