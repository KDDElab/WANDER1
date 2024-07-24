
![IF718](https://github.com/user-attachments/assets/b448b7c4-31a1-4684-9a1c-d5b50ead6cd0)
# Weighted-digraph-Guided Multi-Kernelized Learning for Outlier Explanation

Note that this task is also referred to as outlier Interpretation, outlier aspect mining/discovering, outlier property detection, and outlier description.
We make the source code of the six baseline methods publicly available. In addition, since outlier-interpretation-main/model_wander is the core code of the WANDER model, if this paper is fortunate enough to be accepted, we promise to make it publicly available immediately upon acceptance. Thank you for your understanding.

### Seven Outlier Explanation Methods

**This repository contains seven outlier interpretation methods: WANDER[1], ATON [2], COIN[3], SiNNE[4], SHAP[5], LIME[6], and Anchors [7].**

[1] Weighted-digraph-Guided  Multi-Kernelized Learning for Outlier Explanation. 

[2] Beyond Outlier Detection: Outlier Interpretation by Attention-Guided Triplet Deviation Network. In WWW. 2021.

[3] Contextual outlier interpretation. In IJCAI. 2018.

[4] A New Dimensionality-Unbiased Score For Efficient and Effective Outlying Aspect Mining. In Data Science and Engineering. 2022.

[5] A unified approach to interpreting model predictions. In NeuraIPS. 2017

[6] "Why should I trust you?" Explaining the predictions of any classifier. In SIGKDD. 2016.

[7] Anchors: High Precision Model-Agnostic Explanations. In AAAI. 2018.

### Structure
`outlier-interpretation-main/data_od_evaluation`: Ground-truth outlier interpretation annotations of real-world datasets  
`outlier-interpretation-main/data`: real-world datasets in csv format, the last column is label indicating each line is an outlier or a inlier  
`outlier-interpretation-main/model_xx`: folders of WANDER and its contenders  
`outlier-interpretation-main/config.py`: configuration and default hyper-parameters  
`outlier-interpretation-main/main.py` main script to run the experiments

### How to use?
##### 1. For WANDER 
1. modify variant `algorithm_name` in `main.py` to `wander` 
2. use `python main.py --path data/ --w2s_ratio auto --runs 10` to run WANDER  

### Requirements
main packages of this project  
```
torch==1.3.0
numpy==1.15.0
pandas==0.25.2
scikit-learn==0.23.1
pyod==0.8.2
tqdm==4.48.2
prettytable==0.7.2
shap==0.35.0
lime==0.2.0.1
alibi==0.5.5
```
