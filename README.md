# Visual Transformer for Flower Classification

The dataset used in this project is a custom subset of the [Oxford 102 Flowers dataset](https://paperswithcode.com/dataset/oxford-102-flower). It contains 10 classes with 80 images each, a random 60/20/20 split has been applied.

The notebook `flower_classification` first preprocesses and explores the data. A [Visual Transformer](https://arxiv.org/abs/2010.11929) pretrained on ImageNet-21k ([Google's ViT-small](https://github.com/google-research/vision_transformer?tab=readme-ov-file#available-vit-models), 22M parameters) is finetuned on the dataset to achieve an accuracy of 98% on the test dataset. Good hyperparameters were found using Grid Search similar to the method in this [paper](https://openreview.net/pdf?id=4nPswr1KcP).

SGD is used as an optimizer with a momentum of 0.9 and begins with a learning rate of 0.001. The learning rate is then decayed with a cosine schedule incorporating warm starts