# kmeans-review-analysis
This project implements an optimized K-Means clustering solution for analyzing customer review sentences labeled with helpfulness scores. The system processes large JSON datasets efficiently with complete error handling, logging, and visualization capabilities.

Features
Safe JSON Loading: Handles a train JSON datasets with 20,000 lines and test JSON datasets with 2,000 lines with chunked loading and memory management

Text Preprocessing: Cleans and normalizes text data  - lowercasing, punctuation removal, etc.

TF-IDF Vectorization: Converts text to numerical features for clustering

Optimized K-Means: Uses MiniBatchK-Means for efficient clustering of large datasets

Elbow Method: Determines optimal cluster count with sampling for large datasets

Visualization: Generates cluster visualizations and elbow plots

Comprehensive Logging: Detailed logging for debugging and progress tracking

Unit Testing: Complete test coverage for core functionality

Requirements
Python 3.7+

Required packages:

Copy
pandas numpy scikit-learn matplotlib tqdm
Installation
1. Clone this repository
2. Install dependencies:  

Usage
Main Application
Run the clustering pipeline:

bash
Copy
python main.py
This will:

Load and preprocess the review data

Vectorize the text

Determine optimal clusters

Perform final clustering

Generate visualizations

Save results to clustered_results.csv

Configuration
Modify the config dictionary in main() to adjust:

max_samples: Limit records processed (None for all)

elbow_samples: Samples for elbow analysis

viz_samples: Samples for visualization

max_k: Maximum clusters to test

Expected Output Files
clustered_results.csv: Final clustered data

elbow_plot.png: Elbow method visualization

clusters.png: Cluster visualization

clustering.log: Detailed operation log

Testing
Run unit tests:

bash
Copy
python test_main.py
Test coverage includes:

JSON loading under various conditions

Error handling

Chunked loading

Unicode handling

Edge cases (empty files, malformed JSON)

Test results will display in console and successful tests will exit with code 0.

Data Source
The project uses the "Helpful Sentences from Reviews" dataset from AWS Open Data:

License: CDLA-Sharing

Managed By: Amazon

Documentation: AWS Open Data Registry

Contact: gkutiel@amazon.com

How to Cite
Copy
Helpful Sentences from Reviews was accessed on [DATE] from 
https://registry.opendata.aws/helpful-sentences-from-reviews
Project Structure
Copy
project/
│
├── main.py                # Main clustering application
├── test_main.py           # Unit tests
├── clustering.log         # Generated log file
├── clustered_results.csv  # Output data (generated)
├── elbow_plot.png         # Visualization (generated)
├── clusters.png           # Visualization (generated)
└── README.md              # This file
Development Practices
Follows PEP 8 style guidelines

Comprehensive error handling

Memory management for large datasets

Progress tracking with tqdm

Detailed logging

Unit tested components

Conclusion
This project successfully implements an optimized K-Means clustering solution for analyzing customer review sentences labeled with helpfulness scores. By leveraging chunked JSON loading, TF-IDF vectorization, and MiniBatch K-Means, the system efficiently processes large datasets while maintaining robust error handling and performance tracking.

Key Achievements
✅ Efficient Data Handling: The SafeJSONLoader class ensures memory-safe processing of large JSON files.
✅ Text Preprocessing: Automated cleaning (lowercasing, punctuation removal, whitespace normalization) prepares text for analysis.
✅ Optimal Clustering: The elbow method determines the best cluster count, improving model accuracy.
✅ Visualization: Generated plots (elbow_plot.png, clusters.png) provide intuitive insights.
✅ Unit Testing: Comprehensive test cases validate core functionality, ensuring reliability.
