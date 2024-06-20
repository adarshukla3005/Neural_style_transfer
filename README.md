## Neural Style Transfer
Click on this demo youtube video for complete procedure of the Model.
Click on    [![YouTube](https://img.shields.io/badge/YouTube-Video-red?logo=youtube)](https://www.youtube.com/watch?v=7sgF6nAb32E)

# Neural Style Transfer

This repository contains an implementation of Neural Style Transfer using TensorFlow and Keras. Neural Style Transfer is a technique that blends the content of one image with the style of another image to create a new, visually appealing image.

Transfer a content image into the style of a style image.

A pre-trained VGG19 model is employed as a feature extractor of content and style of an image.

A weighted loss function of content loss, style loss, and total variation loss is used as the optimization objective.

Visualize the feature maps to choose content and style layers.

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

## Model Architecture

The model uses the VGG19 network pretrained on ImageNet. Only the convolutional layers are used, and the fully connected layers are excluded.

- **Content Layer:** `block5_conv2`
- **Style Layers:** `block1_conv1`, `block2_conv1`, `block3_conv1`, `block4_conv1`, `block5_conv1`

## Loss Functions

- **Content Loss:** Measures the difference in content between the generated image and the content image.
    ```python
    def get_content_loss(noise, target):
        loss = tf.reduce_mean(tf.square(noise - target))
        return loss
    ```

- **Style Loss:** Measures the difference in style using Gram matrices.
    ```python
    def get_style_loss(noise, target):
        gram_noise = gram_matrix(noise)
        loss = tf.reduce_mean(tf.square(target - gram_noise))
        return loss
    ```

- **Total Loss:** Weighted sum of content loss and style loss.
    ```python
    def compute_loss(model, loss_weights, image, gram_style_features, content_features):
        ...
        total_loss = content_loss * content_weight + style_loss * style_weight
        return total_loss, style_loss, content_loss
    ```

## References

- [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576) by Leon A. Gatys, Alexander S. Ecker, Matthias Bethge
- [TensorFlow Neural Style Transfer Tutorial](https://www.tensorflow.org/tutorials/generative/style_transfer)

## Style Transfer

Used pretrained VGG19 model.

### Transfer Results

![car](https://github.com/adarshukla3005/neural_style_transfer/blob/main/Images/stylo.png?raw=true)

![car](https://github.com/adarshukla3005/neural_style_transfer/blob/main/Images/stylo2.png?raw=true)
