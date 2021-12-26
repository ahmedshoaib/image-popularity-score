## Petfinder Pawpularity Score Prediction

This notebook implements a deep regression model for the competition [Petfinder.my - Pawpularity Contest](https://www.kaggle.com/c/petfinder-pawpularity-score/overview). The problem basically consists of assigning a popularity score to images of pets up for adoption. The given data includes images of pets and their corresponding popularity scores from 0-100. We need design a model that predicts this score. Also given optinally are some binary metadata features about the pets in the images like: blur, occlusion, eye visibility etc. We currently do not use these optional features for our baseline model.
We use timm to get our pre-trained backbones for resnet50 and swin transformers to be used as feature extractors.
A novel method was developed to obtain an end-to-end deep regression model that converts score values to probability distributions and performs training using these prob. distribution labels, in order to get more gradient information backpropogated as compared to backpropogating just one output value.
Detailed documentation in the notebook
