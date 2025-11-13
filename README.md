# Graph Clustering Analysis

A comprehensive analysis of structural patterns across 16 real-world networks from diverse domains using machine learning clustering techniques. This project demonstrates the application of PCA and clustering algorithms to uncover universal principles governing network structures.

## Overview

This project performs exploratory analysis on networks spanning four distinct domains:
- Collaboration Networks
- Retweet Networks
- Email Networks
- Biological Networks

Using advanced dimensionality reduction (PCA) and clustering techniques (K-Means, Hierarchical), the analysis identifies structural patterns that transcend individual network types.

## Key Findings

**Triangle Metrics Dominate Network Structure**
- Triangle-related properties (count, average, maximum) account for 99.67% of variance across all networks
- This suggests triadic closure is the primary structural differentiator between networks

**Three Distinct Network Clusters**
- **Cluster 0**: Majority of networks (14/16) with moderate connectivity across all domains
- **Cluster 1**: Email-dnc network - extreme outlier with exceptional density and clustering coefficient
- **Cluster 2**: CA-HepPh network - high academic collaboration density with robust triangle structure

**Cross-Domain Similarities**
- Networks from different domains (social, biological, communication) often share more structural properties than expected
- Domain type is less predictive of structure than triangle-related metrics

## Methodology

**Data Source**: Stanford Network Analysis Project (SNAP) database

**Analysis Pipeline**:
1. Network property extraction (15+ metrics per network)
2. Robust scaling to handle outliers
3. Principal Component Analysis for dimensionality reduction
4. K-Means clustering (optimal k=3 via Elbow Method)
5. Hierarchical clustering for validation
6. Comparative analysis across domains

**Technologies**: Python, NetworkX, scikit-learn, scipy, pandas, matplotlib, seaborn, community-louvain

## Network Properties Analyzed

**Basic Metrics**
- Nodes, Edges, Density

**Degree Metrics**
- Maximum, Minimum, Average degree

**Clustering Metrics**
- Number of triangles
- Average and maximum triangles
- Clustering coefficient
- Transitivity (fraction of closed triangles)

**Advanced Properties**
- Assortativity
- Maximum k-core
- Lower bound of maximum clique
- Community modularity

## Results

**PCA Analysis**
- First principal component: 99.67% variance explained
- Primary loading: Triangle-related features
- Second component: 0.18% variance (edges, density, clique size)

**Clustering Results**
- Optimal clusters: 3 (determined via Elbow Method)
- Hierarchical clustering confirmed K-Means results
- Email-dnc identified as significant structural outlier

**Key Insights**
- Triadic closure is the dominant structural feature across network types
- Most networks cluster together despite domain differences
- Outlier networks exhibit extreme connectivity patterns useful for specific use cases

## Files

- `Graph_Project-2.ipynb` - Complete analysis notebook with code, visualizations, and results
- `HPGA_Project_Report.pdf` - Detailed project report with methodology and findings

## Applications

This analysis framework can be applied to:
- Social network analysis and community detection
- Biological network modeling (protein interactions, neural networks)
- Communication pattern analysis
- Cybersecurity threat detection
- Infrastructure network optimization

## Authors

- Atharva Karnik - Indiana University Bloomington
- Ayana Holla Pandeshwara - Indiana University Bloomington
- Diksha Adke - Indiana University Bloomington
- VV Hari Chandan - Indiana University Bloomington

## Citation
```bibtex
@article{karnik2024graph,
  title={Unveiling Network Patterns: A Multidomain Network Analysis},
  author={Karnik, Atharva and Pandeshwara, Ayana Holla and Adke, Diksha and Chandan, VV Hari},
  institution={Indiana University Bloomington},
  year={2024}
}
```

## Future Directions

- Temporal network analysis to track structural evolution
- Integration with Graph Neural Networks for predictive modeling
- Application-specific analysis for cybersecurity and bioinformatics
- Extended centrality measures (betweenness, eigenvector centrality)
- Real-time network monitoring and anomaly detection

## License

MIT License
