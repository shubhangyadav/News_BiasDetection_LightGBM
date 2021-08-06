## Bias Detection in News Articles using LightGBM with Focal Loss
This repository explores the idea of identifying whether or not a news article is biased, and if yes, towards which side.
I have used Microsoft's LightGBM Multi-class Classifier with Focal Loss for this purpose.

### About the Dataset
Hyperpartisan News Detection was a dataset created for PAN @ SemEval 2019 Task 4. Given a news article text, decide whether it follows a hyperpartisan argumentation, i.e., whether it exhibits blind, prejudiced, or unreasoning allegiance to one party, faction, cause, or person.
This particular dataset contains two columns of interest:
1. Hyperpartisan: Indicates whether a news article is biased or not
2. Bias: Indicates the bias level of the article as follows- <br />
If bias value = 0, bias: right <br />
If bias value = 1, bias: right-center <br />
If bias value = 2, bias: least <br />
If bias value = 3, bias: left-center <br />
If bias value = 4, bias: left <br />

Here, we will focus on predicting the bias level of an incoming article.

### Results
| **_Model_**                     | Accuracy | Precision | Recall |
|---------------------------------|:--------:|:---------:|:------:|
| LightGBM                        | 0.8886   | 0.8610    | 0.8610 | 
| LightGBM (with Focal Loss)      | 0.9105   | 0.9166    | 0.8870 | 

### Conclusion
With Focal Loss, the evaluation metrics achieve a higher score and we get a more reliable model for identifying biased news articles.

### References
[[1] Hyperpartisan News Detection Dataset](https://huggingface.co/datasets/hyperpartisan_news_detection) <br />
[[2] Focal Loss for LightGBM](https://maxhalford.github.io/blog/lightgbm-focal-loss/)
