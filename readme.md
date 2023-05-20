## GPT3-HateEval
Code implementation for the paper "Evaluating GPT-3 Generated Explanations for Hateful Content Moderation" (IJCAI'23).


## Getting Started

- The dataset used in this project is [HateXplain](https://huggingface.co/datasets/hatexplain). We performed clustering on the tweets from the HateXplain dataset based on their annotation labels and stored the clustered data in the `data` folder.

- The project's code can be found in the `scripts` folder. The `ExplanationGeneration.ipynb` file is responsible for generating explanations, which are then stored in the `explanations` folder. The `explanations` folder contains two subfolders:

    - The `demonstration_examples` subfolder stores the candidate pool for demonstration examples as well as the selected demonstration examples. These examples are used in few-shots prompting to generate explanations.

    - The `evaluation_explanations` subfolder stores the explanations generated for all evaluation tweets. The tweet and explanation pairs in this folder will be evaluated by human annotators based on the quality of the explanations and the hatefulness of the tweets.

- The `annotation` folder contains all the annotation results collected from the crowd sourcing platform. To preprocess and analyze the human annotations, refer to the `ResultsAnalysis.ipynb` file. The folder `evaluation_table` comprises the table presenting the results of the analysis. A visually enhanced representation of the data is presented in the subsequent section.




## Findings derived from human evaluation.

### The assessment of the quality of explanations.
![Quality Table](image/quality.png)

### The assessment of the persuasive impact of explanations on the perception of hatefulness in the same set of tweets.
![Hatefulness Table](image/hatefulness.png)

### The manifestation of misclassification of tweets influenced by misleading explanations.
The labeling process for each tweet entails initially classifying each annotation as either 'non-hateful' or 'hateful' based on their respective hatefulness scores of 1-2 and 4-5. Each tweet undergoes evaluation by three distinct human evaluators, and the majority vote among them determines the annotated label assigned to the tweet.

![Misclassification Table](image/misclassification.png)

## Acknowledgements

To cite:
```
@inproceedings{gpt3hateeval2023,
    title={Evaluating GPT-3 Generated Explanations for Hateful Content Moderation},
    author={Wang, Han and Hee, Ming Shan and Awal, Md Rabiul and Choo, Kenny Tsu Wei and Lee, Roy Ka-Wei},
    year={2023},
    booktitle = {In Proceedings of the International Joint Conference on Artificial Intelligence (IJCAI)},
}
```

### Correspondence 
Wang Han (han_wang@sutd.edu.sg)
