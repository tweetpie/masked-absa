# Masking The Bias : From Echo Chambers to Large Scale Aspect-Based Sentiment Analysis
[https://dx.doi.org/10.1007/978-3-031-78538-2_19](https://dx.doi.org/10.1007/978-3-031-78538-2_19)

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
The study incorporates following datasets : 
### SemEval dataset
SemEval 2014, 2015 and 2016 Stance detection dataset
||Laptop14|Restaurant 14|Restaurant 15|Restaurant16|
|:--------:|:--------:|:--------:|:--------:|:--------:|
|MaskedABSA|86.24|87.65|91.53|94.83|
### US Race Relations Datase
Race and Politics datasets distribution
|Dataset|Positive|Negative|Total|
|:----:|:----:|:----:|:----:|
|Races|Train|885|2115|3000|
|     |Test|309|699|1000|
|Politics|Train|873|2122|2995|
|        |Test|257|751|1008|
* **politic_dataset.zip :** Twitter text data related to the political terms.
* **race_dataset.zip :** Twitter text data related to the races terms.

## Models
The models used in this study are available on Huggingface.

|Dataset|Model|
|:----:|:----:|
|Restaurant14|[masked-absa-rest14](https://huggingface.co/tweetpie/masked-absa-rest14)|
|Laptop14|[masked-absa-rest14](https://huggingface.co/tweetpie/masked-absa-laptop14)|
|Restaurant15|[masked-absa-rest15](https://huggingface.co/tweetpie/masked-absa-rest15)|
|Restaurant16|[masked-absa-rest15](https://huggingface.co/tweetpie/masked-absa-rest16)|
|Race|[masked-absa-race](https://huggingface.co/tweetpie/masked-absa-race)|
|Politics|[masked-absa-politics](https://huggingface.co/tweetpie/masked-absa-politics)|

## Contributions and Feedback
We encourage contributions and feedback to improve this project. If you have suggestions or want to contribute, please open an issue or pull request on our GitHub repository.

## Citation

```bibtex
@inproceedings{maskedabsa2025,
  title={Masking the Bias: From Echo Chambers to Large Scale Aspect-Based Sentiment Analysis},
  author={Lee, Yeonjung and {\c{C}}etinkaya, Yusuf M{\"u}cahit and K{\"u}lah, Emre and Toroslu, {\.I}smail Hakk{\i} and Davulcu, Hasan},
  booktitle="Social Networks Analysis and Mining (ASONAM 2024)",
  year="2025",
  publisher="Springer Nature Switzerland",
  pages="214--225",
  doi="10.1007/978-3-031-78538-2_19"
}
