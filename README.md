# HGNN: Hierarchical Graph Neural Network for Price-Limit-Hitting Stock Prediction

## Description
Implementation of the HGNN (Hierarchical Graph Neural Network) model for predicting the classification of price-limit-hitting stocks, based on the paper "HGNN: Hierarchical graph neural network for predicting the classification of price-limit-hitting stocks". This implementation uses 1% of the original dataset as a proof of concept.

## Overview
This project implements a hierarchical GNN architecture that predicts whether stocks hitting their daily price limit will close at the same price level. The model considers market states at different hierarchical levels:
- Node view (individual stock patterns)
- Relation view (stock-to-stock relationships)
- Graph view (market-wide patterns)

## Model Architecture
- Hierarchical structure for comprehensive market state analysis
- Stock relation graph construction
- Multi-view information fusion
- Historical sequence pattern integration
- Stock relationship modeling

## Dataset
- Uses 1% of the original dataset from SSE and SZSE markets
- Two years of historical data
- Features price-limit-hitting stocks
- Data preprocessing and sampling methods included

## Requirements
```
torch
torch_geometric
pandas
numpy
scikit-learn
matplotlib
```

## Citation
```bibtex
@article{XU2022783,
title = {HGNN: Hierarchical graph neural network for predicting the classification of price-limit-hitting stocks},
journal = {Information Sciences},
volume = {607},
pages = {783-798},
year = {2022},
issn = {0020-0255},
doi = {https://doi.org/10.1016/j.ins.2022.06.010},
url = {https://www.sciencedirect.com/science/article/pii/S0020025522005928},
author = {Cong Xu and Huiling Huang and Xiaoting Ying and Jianliang Gao and Zhao Li and Peng Zhang and Jie Xiao and Jiarun Zhang and Jiangjian Luo},
keywords = {Hierarchical graph neural network, Stock prediction, Price limit},
abstract = {In some stock markets, stock prices are not allowed to rise above a daily limit to restrain the surge of price (called price limit). When the price limit occurs, investors tend to chase the continuing upward momentum for profit-making. However, For the stocks that hit daily price limit, we observe whether they close at daily price limit will lead to the opposite price trends of the next trading day. Therefore, this work aims to predict whether a stock that hits its daily price limit will also close at the same price level (i.e., Type I or Type II). The occurrence of price limit is driven by different levels of market state. For example, it can result from macro-economic changes of the whole market, or it can be traced to some industry-specific factors. A challenging task is to learn a better stock representation with less uncertainty by comprehensively considering the hierarchical property of market state. Accordingly, we design a novel hierarchical architecture, called Hierarchical Graph Neural Network (HGNN), to investigate the market state at hierarchical view for stock type prediction. In HGNN, we construct the stock relation graph and merge stock information hierarchically extracted from multiple views of market state, including node view, relation view and graph view, which takes both historical sequence pattern and stock relation into consideration. Our key innovation is the introduction of hierarchical structure makes the predictive model able to more comprehensively infer the hierarchical property of market state. Further, it also provides the deeper insight for the actual investment practice. To validate the effectiveness of our method, we conduct back-testing on the two-year historical data of more than 2500 main-board stocks in two China stock markets, SSE and SZSE. To support further study of the stock type prediction task, we have published two long-range stock datasets (Datasets are available at https://drive.google.com/file/d/1TXiAyqt3rHveuzdGT6YtswU1e-tBSFUe/view?usp=sharing). Extensive experiments show that our method outperforms the state-of-the-art solutions including ALSTM, GCN and GAT with the improvements of at least 3.54% on average in accuracy. In addition, the average return ratio of SSE and SZSE has improved by 18.57% and 8.75%, respectively.}
}
```

## Notes
- This implementation uses a reduced dataset (1% of original)
- Modifications made to accommodate smaller dataset size
- Focus on core HGNN architecture and methodology

## Acknowledgments
Based on the research paper "HGNN: Hierarchical graph neural network for predicting the classification of price-limit-hitting stocks"
