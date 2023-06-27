# Visual-Question-Answering
A linear classifier build using neurel networks that performs text and image encoding using the clip model. The linear classifier model is build basd on a paper named Less Is More: Linear Layers on CLIP Features as Powerful VizWiz Model. The linear classifier performs visual question answering given a question and a image and it returns an approriate answer.

## Table of content
* [Table of Content](#table-of-content)
* [Description](#description)
* [Features](#features)
* [Prerequisites](#prerequisites)
* [Installing](#installing)
* [Executing program](#executing-program)
* [Author](#author)
* [Acknowledgments](#acknowledgments)

## Description
The left handside of the  following architecture is implemented using python.

 ![CLIP architecture](https://github.com/Moustafa-Daebis/Visual-Question-Answering/assets/100102025/d28de275-c2f2-4e46-b04e-97a1c248a5ba)

The CLIP model is used to encode and decode the images and text before concatinating the encoded images and text.The concatinated data is then passed to the linear model where it is passed to a linear layer that performs normalization aswell as dropout. Then it is split into 2 the answer which is simply making a fully connected layer to output the vocab (as in all the answer availiable) and the answermask which is reduing the dimensionalty to 4 before making a fully connected layer to output the vocab size.The answer and answer mask are then multiplied and  argmax if performed on the output before converting it to onehotencoded data to be able perform inverse transform on it to return the predicted answer given that the answers were encoded using onehotencoding.


## Features
Given an image and a question the model will return a suitable answer.

## Getting Started

### Prerequisites 
A suitable editor (perferably kaggle)


### Installing
Import the notebook to a suitable editor


## Author

* [Moustafa Daebis](https://github.com/Moustafa-Daebis)

## Acknowledgments
* [Less Is More: Linear Layers on CLIP Features as Powerful VizWiz Model](https://arxiv.org/pdf/2206.05281v1.pdf)

* [CLIP Model](https://github.com/openai/CLIP)

* [CLIP Model paper](https://arxiv.org/pdf/2103.00020.pdf)
