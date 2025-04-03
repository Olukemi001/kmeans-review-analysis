# kmeans-review-analysis
This project implements an optimized K-Means clustering solution for analyzing customer review sentences labeled with helpfulness scores. The system processes large JSON datasets efficiently with complete error handling, logging, and visualization capabilities.


## Features

- **Safe JSON Loading**: Handles test JSON file with 2,000 lines and train JSON file with 20,000 lines with chunked loading and memory management
- **Text Preprocessing**: Cleans and normalizes text data, lowercasing, punctuation removal, etc.
- **TF-IDF Vectorization**: Converts text to numerical features for clustering
- **Optimized K-Means**: Uses MiniBatchK-Means for efficient clustering of large datasets
- **Elbow Method**: Determines optimal cluster count with sampling for large datasets
- **Visualization**: Generates cluster visualizations and elbow plots
- **Comprehensive** Logging: Detailed logging for debugging and progress tracking
- **Unit Testing**: Complete test coverage for core functionality

## Installation

```bash
git clone https://github.com/Olukemi001/kmeans-review-analysisg.git
pip install pandas numpy scikit-learn matplotlib tqdm
```

## Usage

1. Place your `train.json` and `test.json` files in the project root
2. Run the clustering pipeline:

```bash
python main.py
```

### Configuration (in main.py)
```python
config = {
    'max_samples': None,    # None processes all data
    'elbow_samples': 2000,  # Samples for cluster analysis
    'viz_samples': 2000,    # Points for visualization
    'max_k': 6             # Maximum clusters to test
}
```

## Project Structure

```
.
├── main.py                 # Main clustering application
├── test_main.py            # Unit test suite
├── train.json              # Source training data
├── test.json               # Source test data
├── clustered_results.csv   # Output with cluster assignments
├── elbow_plot.png          # Optimal cluster visualization
├── clusters.png            # 2D cluster visualization
├── clustering.log          # Runtime logs
└── test_results.txt        # Test output (generated)
```

## Testing

To run tests and save results:

```bash
python test_main.py > test_results.txt
```

Test coverage includes:
- JSON file loading
- Error handling
- Memory management
- Unicode support
- Edge cases

## Data Source

Dataset: Helpful Sentences from Reviews was accessed on 1st of April 2025 from https://registry.opendata.aws/helpful-sentences-from-reviews 

## Conclusion
This project successfully implements an optimized K-Means clustering solution for analyzing customer review sentences labeled with helpfulness scores. By leveraging chunked JSON loading, TF-IDF vectorization, and MiniBatch K-Means, the system efficiently processes large datasets while maintaining robust error handling and performance tracking.

Key Achievements

✔ **Optimized K-Means** with automated elbow detection  
✔ **Memory-safe processing** of large JSON files  
✔ **Visual analytics** for cluster interpretation  
✔ **Comprehensive testing** with logged results  





