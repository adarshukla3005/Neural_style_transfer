## Neural Style Transfer

- This repository contains an implementation of Neural Style Transfer using TensorFlow and Keras. Neural Style Transfer is a technique that blends the content of one image with the style of another image to create a new, visually   
  appealing image.
  
- Transfer a content image into the style of a style image.

- A pre-trained VGG19 model is employed as feature extactor of content and style of an image.

- A weighted loss function of content loss, style loss, and total variation loss is used as the optimization objective.

- Visualize the feature maps to choose content and style layers.

## Preview

![g2](https://github.com/adarshukla3005/neural_style_transfer/blob/main/Images/stylizedimg_4.jpg?raw=true)

![g1](https://github.com/adarshukla3005/neural_style_transfer/blob/main/Images/stylizedimg_1.png?raw=true)

![g3](https://github.com/adarshukla3005/neural_style_transfer/blob/main/Images/stylizedimg_5.png?raw=true)

## Usage
Run each cell in the collab file. Upload the required content and style image file.
You can download the files from the repository.
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adarshukla3005/neural_style_transfer/blob/main/Neural_Style_Transfer.ipynb)

1. **Upload Images:**
   The script prompts you to upload a content image and a style image.

2. **Run Style Transfer:**
   To run the style transfer, simply call the `run_style_transfer` function with the appropriate parameters:
    ```python
    best, best_loss, image = run_style_transfer(content_path, style_path, epochs=200)
    ```

3. **Display Results:**
   The script includes functionality to display the content, style, and generated images using Matplotlib.

## Style transfer

Used pretrained VGG19 model.

### Transfer results

![ car](https://github.com/adarshukla3005/neural_style_transfer/blob/main/Images/stylo.png?raw=true)

![ car](https://github.com/adarshukla3005/neural_style_transfer/blob/main/Images/stylo2.png?raw=true)
