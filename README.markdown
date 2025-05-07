# Association Rules with Apriori and FPGrowth

Welcome to the **Association Rules with Apriori and FPGrowth** repository! This project demonstrates the implementation and performance comparison of two popular association rule mining algorithms—Apriori and FP-Growth—using a real-world transaction dataset. Leveraging Python and key libraries like `mlxtend`, `pandas`, and `matplotlib`, this work explores frequent itemset mining, rule generation, and scalability analysis, providing valuable insights for recommendation systems and data mining applications.

## Overview

This project analyzes a dataset containing 31,101 transactions with 12,592 unique items to:
- Extract frequent itemsets (pairs and triplets) with a minimum support threshold.
- Generate association rules with confidence metrics.
- Compare the performance of Apriori and FP-Growth algorithms across varying support levels (100, 50, 25).
- Visualize scalability trends and evaluate algorithm efficiency.

Key highlights include:
- Optimized data preprocessing using `TransactionEncoder`.
- Detailed execution time analysis for Pair and Triplet itemsets.
- Comprehensive evaluation of association rule metrics (confidence, lift, conviction).
- Insights into algorithm suitability for different dataset sizes.

## Features

- **Apriori Implementation**: Efficiently mines frequent itemsets with multiple dataset scans.
- **FP-Growth Implementation**: Utilizes FP-tree for reduced scans and improved theoretical scalability.
- **Performance Benchmarking**: Compares execution times and growth rates for both algorithms.
- **Visualization**: Generates plots to illustrate scalability trends.
- **Rule Generation**: Computes confidence for item pair and triplet rules.

## Installation

To run this project locally, follow these steps:

1. **Clone the Repository**
   ```bash
   git clone https://github.com/wajason/association-rules-apriori-fpgrowth.git
   cd association-rules-apriori-fpgrowth
   ```

2. **Set Up a Virtual Environment** (recommended)
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install Dependencies**
   Ensure you have the required libraries installed with the exact versions used:
   ```bash
   pip install matplotlib==3.10.1 mlxtend==0.23.4 nbformat==5.10.4 numpy==2.2.5 pandas==2.2.3
   ```

4. **Prepare the Dataset**
   - Place the transaction dataset file (`browsing.txt`) in the your directory or update the `file_path` variable in the code to match your local path.
   - The dataset should contain one transaction per line, with items separated by spaces.

## Usage

1. **Run the Jupyter Notebook**
   Launch the notebook and execute the cells to reproduce the analysis:
   ```bash
   jupyter notebook Association_Rules_with_Apriori_and_FPGrowth.ipynb
   ```

2. **Key Sections**
   - **Section 1**: Evaluates association rule metrics (confidence, lift, conviction) with theoretical proofs and examples.
   - **Section 2**: Applies Apriori and FP-Growth to find frequent itemsets and generate rules.
   - **Section 3**: Compares algorithm performance with detailed tables, plots, and scalability analysis.

3. **Output**
   - Execution time tables for Pair and Triplet itemsets.
   - Scalability trend plots saved as `fpgrowth_time_trend.png`.
   - Printed results for frequent itemsets and rules.

## Results

### Performance Comparison
- **Apriori**: Average execution time of 27.34 seconds, with a stable growth rate (0.4887), suitable for smaller datasets.
- **FP-Growth**: Average execution time of 984.81 seconds, with a higher growth rate (3.0269), indicating potential for larger datasets with optimization.
- **Scalability Insight**: Apriori scans the dataset 3 times, while FP-Growth scans only 2 times, suggesting better theoretical scalability for FP-Growth in big data scenarios.

### Key Findings
- Apriori outperforms FP-Growth in this 31,101-transaction dataset due to its simpler implementation.
- FP-Growth’s FP-tree approach shows promise for larger datasets or lower support thresholds.
- Frequent itemsets and rules (e.g., confidence up to 1.0) provide actionable insights for recommendation systems.

## Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request with a clear description of your changes.

Please ensure code follows PEP 8 guidelines and includes tests or documentation updates.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the `mlxtend` community for providing robust association rule mining tools.
- Inspired by real-world applications in e-commerce recommendation systems.
- Special thanks to the dataset provider for enabling this analysis.

---

Happy mining! 🚀 Feel free to explore, modify, or extend this project for your own use cases!
