# Masking The Bias : From Echo Chambers to Large Scale Aspect-Based Sentiment Analysis
Welcome to the **Masked Aspect-Based Sentiment Analysis** repository. This project addresses the challenges of scarcity and high costs associated with manual annotation in Aspect-Based Sentiment Analysis (ABSA) by utilizing weak supervision methods. We have demonstrated the superiority of our model using SemEval datasets and real-world tweet data.

## Masked Aspect Sentiment Classification (MASC)
Aspect-based stance detection identifies the stance towards each aspect term in a sentence. 
<p align="center">
  <img width= 60% src="./images/Masked_Stance_p1.png" alt="sentence">
</p>
In Aspect Term Sentiment Classification, current models often overemphasize the presence of aspect terms and the majority sentiment associated with them, ignoring the broader sentence context. This issue is particularly problematic with real-world datasets that have skewed or missing labels for specific aspects, causing models to memorize and repeatedly predict the same sentiment for certain words. The MaskedABSA method addresses these issues by replacing aspect terms with a placeholder token "[MASK]."
<p align="center">
  <img width= 60% src="./images/Masked_Stance_p3.png" alt="MASC">
</p>

## Weak Supervision Method
<p align="center">
  <img width= 60% src="./images/alm_blm_camp.png" alt="US_races">
</p>
An effective strategy to address the scarcity of ABSA datasets and bias involves using weak supervision with social network structures, like retweet networks. By analyzing retweet patterns, sentiment and aspect orientations within specific groups can be inferred without detailed manual annotation. This approach creates large-scale, weakly labeled datasets that can be refined with machine learning and validated through targeted reviews. A well-defined codebook enhances the efficiency and consistency of labeling by providing guidelines for detecting stances based on community orientations. This method reduces the costs of creating labeled datasets and captures a wide range of aspects and sentiments across diverse groups and sub-communities.

## Datasets

## Contiributions and Feedback
We encourage contributions and feedback to improve this project. If you have suggestions or want to contribute, please open an issue or pull request on our GitHub repository.

## Citation
