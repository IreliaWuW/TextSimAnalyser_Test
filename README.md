# TextSimAnalyser: Multi-Stage Text Similarity Analysis Toolkit

**Intelligent Hybrid Approach for Efficient Text Comparison**  
*Combining Traditional Algorithms with Deep Learning for Optimal Performance*

## Key Features
- **Hybrid Computation Architecture**  
  `Jaccard` → `Cosine` → `BERT` staged analysis (saves GPU time vs pure-BERT approach)
- **Multi-Language Support**  
  Chinese/English/Korean (paraphrase-multilingual-MiniLM-L12-v2 model)
- **Production-Ready**  
  Docker/Kubernetes support • REST API • Batch processing • LRU caching
- **Advanced Visualization**  
  Interactive heatmaps • PDF/Excel reports • Threshold analysis charts
  
## Application Scenarios

| Domain               | Use Case                          | Benefit                          |
|----------------------|-----------------------------------|----------------------------------|
| **Academic**         | Paper plagiarism detection        | Accuracy in duplicate text |
| **Customer Service** | FAQ matching optimization         | Faster response         |
| **Legal**            | Contract clause comparison        | Reduction in manual review   |
| **E-commerce**       | Product description similarity    | Improved recommendation relevancy|


## Usage Case

### Basic Analysis
python
from textsimanalyser import TextAnalyzer

analyzer = TextAnalyzer(mode="fast") # fast/standard/deep
result = analyzer.compare(
"Machine learning algorithms",
"Deep neural networks"
)
print(f"Composite Score: {result['composite_score']:.2%}")


### Batch Processing
python
batch_results = analyzer.batch_analyze(
texts=["Text 1", "Text 2", "Text 3"],
output_format="excel", # json/csv/html
visualization=True
)
