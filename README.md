# Visual Transformer for Flower Classification

The dataset used in this project is a custom subset of the [Oxford 102 Flowers dataset](https://paperswithcode.com/dataset/oxford-102-flower). It contains 10 classes with 60 images each, a random 60/20/20 split has been applied.

The notebook `flower_classification` first preprocesses and explores the data. A [Visual Transformer](https://arxiv.org/abs/2010.11929) pretrained on ImageNet-21k ([Google's ViT-small](https://github.com/google-research/vision_transformer?tab=readme-ov-file#available-vit-models), 22M parameters) is finetuned on the dataset to achieve an accuracy of [PLACEHOLDER] on the test dataset. Hyperparameters were tuned based on minimizing validation error.