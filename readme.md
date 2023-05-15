## GPT3-HateEval
Code implementation for the paper "Evaluating GPT-3 Generated Explanations for Hateful Content Moderation" (IJCAI'23).


## Getting Started
- The dataset used in this project is [HateXplain](https://huggingface.co/datasets/hatexplain). We performed clustering on the tweets from the HateXplain dataset based on their annotation labels and stored the clustered data in the `data` folder.

- The project's code can be found in the `scripts` folder. The `ExplanationGeneration.ipynb` file is responsible for generating explanations, which are then stored in the `explanations` folder. The `explanations` folder contains two subfolders:

    - The `demonstration_examples` subfolder stores the candidate pool for demonstration examples as well as the selected demonstration examples. These examples are used in few-shots prompting to generate explanations.

    - The `evaluation_explanations` subfolder stores the explanations generated for all evaluation tweets. The tweet and explanation pairs in this folder will be annotated by human annotators based on the quality of the explanations and the hatefulness of the tweets.

- The `annotation` folder contains all the annotation results collected from the crowd sourcing platform. To analyze and preprocess the human annotations, refer to the `ResultsAnalysis.ipynb` file.




## Evaluation Results Based on Human Annotation

### Explanations Quality Table
![Quality Table](image/quality.png)

### Tweets Hatefulness Table
![Hatefulness Table](image/hatefulness.png)

### Tweets Misclassification Table
![Misclassification Table](image/misclassification.png)


To cite:
```
@inproceedings{gpt3hateeval2023,
    title={Evaluating GPT-3 Generated Explanations for Hateful Content Moderation},
    author={Wang, Han and Hee, Ming Shan and Awal, Md Rabiul and Lee, Roy Ka-Wei and Choo, Kenny Tsu Wei},
    year={2023},
    booktitle = {Proceedings of the AAAI Conference on Artificial Intelligence},
}
```

### Correspondence 
Han Wang (han_wang@sutd.edu.sg)
