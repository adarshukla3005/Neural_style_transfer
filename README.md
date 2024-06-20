[![GitHub issues](https://img.shields.io/github/issues/jhan15/neural_style_transfer)](https://github.com/jhan15/neural_style_transfer/issues)
![GitHub last commit](https://img.shields.io/github/last-commit/jhan15/neural_style_transfer?color=ff69b4)

# neural_style_transfer

Transfer a content image into the style of a style image.

- A pre-trained VGG19 model is employed as feature extactor of content and style of an image.

- A weighted loss function of content loss, style loss, and total variation loss is used as the optimization objective.

- Visualize the feature maps to choose content and style layers.

- Adam optimizer is used for training.

## Preview

![g2](https://github.com/adarshukla3005/neural_style_transfer/blob/main/content_4.jpg)

![g1](https://github.com/adarshukla3005/neural_style_transfer/blob/main/Images/stylizedimg_1.png?raw=true)

![g3](https://user-images.githubusercontent.com/62132206/120387238-ebad2300-c329-11eb-80b2-74bb83dee39e.gif)

## Usage

Run each cell in the collab file. Upload the required content and style image file. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adarshukla3005/neural_style_transfer/blob/main/Neural_Style_Transfer.ipynb)


## Style transfer

Used pretrained VGG19 model.

### Transfer results

![ car](https://user-images.githubusercontent.com/62132206/120101427-543baa80-c146-11eb-9e55-a0d306473799.png)

### One to many

![one_to_many](https://user-images.githubusercontent.com/62132206/120101446-6a496b00-c146-11eb-8299-a2b190437476.png)

### Many to one

![many_to_one](https://user-images.githubusercontent.com/62132206/120102504-a9c68600-c14b-11eb-90b4-a94c014dae01.png)

### Weight analysis

![weight](https://user-images.githubusercontent.com/62132206/120114778-02644600-c181-11eb-8716-e6fea9a1fb29.png)
