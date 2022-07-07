---
layout: pub
urltitle: "Aragnation"
title: "An AI Generative Art Project by Devi Parikh & Abhishek Das"
categories: Aragnation, Generative Art, AI Art, Devi Parikh, Abhishek Das
favicon: static/img/aragnation.png
permalink: /
---

# Aragnation

By [Devi Parikh][devi] and [Abhishek Das][das]

Aragnation is an anagram of “No-GAN AI Art".

Generative Adversarial Networks (GANs) are a class of deep learning-based methods which try to generate images that look indistinguishable from real images, by jointly training two neural networks against each other in a zero sum game. In a lot of the discourse around AI art, GAN-art has come to become synonymous with AI-art.

But AI art does not have to use GANs! Or even neural networks for that matter. 

Aragnation questions notions of what constitutes AI art. It demonstrates that boundaries are more fluid than commonly assumed. A crisp definition of AI (let alone AI art) can be a lengthy debate. But it is clear that AI is not tied to a set of specific tools. So why should AI art? There are innumerable ways to build models that know something about our world. Correspondingly, there are innumerable ways to use AI for creative expression. 

Aragnation uses two AI models – both designed, implemented, and trained from scratch by the artists for Aragnation. One model focuses on learning the composition of images, and the other on the color gradients in images. 

The first is a probabilistic graphical model that explicitly performs probabilistic reasoning to generate an image. Notably, it is not a GAN or a neural network. It has learned to compose 25 prototype shapes and 17 colors to generate its interpretation of landscapes, flowers, birds, and urban settings. The second is a small neural network (a multilayer perceptron in particular) that has learned to map image (x,y) coordinates to RGB colors. Note that while a neural network, it is still not a GAN or a transformer or a diffusion model – techniques which are commonly used in the recently popularized image generation AI technology.

Roughly half the images the second model has been trained on are photographs taken by one of the artists, Abhishek. The generated pieces thus capture, in broad strokes, [Abhishek’s photography][das-photos] – nature, landscapes and urban settings.

No GPUs were harmed in the making of Aragnation.


<!-- ---

The first is a probabilistic graphical model (not a GAN or a neural network). It has 25 prototype shapes as the core atomic structures. It learns to compose these together to generate images that match the distribution of (its interpretation of) real images. It has been trained on 1000s of images, including landscapes, flowers, birds, and urban settings. The model also learns a mapping of the shapes to a palette of 17 colors. The choice of palette varies across pieces. We designed the model specifically for this project and trained it from scratch, without using existing AI libraries or pre-trained models, unlike what is often done with GAN-based AI art. We then use this model (in p5.js) to generate images.

The generated images are rendered either directly using colors from the palette, or the colors are modified using a second AI model.

This second model is a simple, small multilayer perceptron (MLP) neural network -- still not a GAN, also not a transformer or a diffusion model, or any large or deep neural network for that matter. It learns to map the (x,y) coordinates in an image to RGB color values. It has been trained on over a 100 hand-selected images -- also landscapes, flowers, birds, and urban settings as in the first model. Notably, about half of the images are [photographs taken by Abhishek][das-photos]! The generated pieces thus capture, in broad strokes, the style of Abhishek's photography. This model is also used in p5.js. -->


<!-- Again, the model is used in p5.js to generate images. To enhance variety in generations, the hue of the image is offset across pieces, but the gradients in colors are controlled by the AI model. -->

<!-- The final piece takes a generation from either of the two AI models, and renders it in a consistent style. -->

<!-- We also trained another AI model that classifies the generated image as a landscape, or a flower, or a bird, or an urban scene.  -->

<!-- This classification is also part of the piece, and gives a peek into what the AI model considers to be different image content. The classification is depicted via a symbol at the bottom right of the piece: rectangle = landscape; circle = flower; triangle (e.g., beak) = bird; trapezoid (e.g., perspective) = urban. (Note: This has been completed for the first model, but is work in progress for the second model.) -->

Below are several pieces from the system. You can generate pieces [here][aragnation] (refresh for a new piece).

<div class = 'art'>
  {% for person in site.data.aragnation_1 %}
  <div class = 'aragnationpiece'>
    <a href = '{{ person.link }}'><img src = '{{person.link}}' alt = 'Aragnation'></a>
  </div>
  {% endfor %}
</div>

<div class = 'fullartpiece'>
<a href = './static/img/aragnation_11.jpg'><img src = './static/img/aragnation_11.jpg' alt = 'Aragnation'></a>
</div>

<div class = 'art'>
  {% for person in site.data.aragnation_2 %}
  <div class = 'aragnationpiece'>
    <a href = '{{ person.link }}'><img src = '{{person.link}}' alt = 'Aragnation'></a>
  </div>
  {% endfor %}
</div>

<div class = 'fullartpiece'>
<a href = './static/img/aragnation_22.jpg'><img src = './static/img/aragnation_22.jpg' alt = 'Aragnation'></a>
</div>

<div class = 'art'>
  {% for person in site.data.aragnation_3 %}
  <div class = 'aragnationpiece'>
    <a href = '{{ person.link }}'><img src = '{{person.link}}' alt = 'Aragnation'></a>
  </div>
  {% endfor %}
</div>

<div class = 'fullartpiece'>
<a href = './static/img/aragnation_33.jpg'><img src = './static/img/aragnation_33.jpg' alt = 'Aragnation'></a>
</div>

<div class = 'art'>
  {% for person in site.data.aragnation_4 %}
  <div class = 'aragnationpiece'>
    <a href = '{{ person.link }}'><img src = '{{person.link}}' alt = 'Aragnation'></a>
  </div>
  {% endfor %}
</div>


<!-- Below are examples of how some landscape, bird, flower, and urban images get depicted by the AI model I've trained (using one specific rendering style). Note that the samples shown above are purely generative -- they use a generative model trained on 1000s of images -- they are not based on a 1-1 "translation" or re-rendering of an existing image to generate a sample. These translation examples below are just so you get a sense for how real images would be depicted by this model.


<div class = 'art'>
  {% for person in site.data.aragnation-pairwise %}
  <div class = 'artpiece'>
    <a href = '{{ person.link }}'><img src = '{{person.link}}' alt = 'Aragnation'></a>
  </div>
  {% endfor %}
</div> -->

[das]: https://abhishekdas.com/art/
[devi]: http://stateoftheheart.ai/
[das-photos]: https://www.instagram.com/abhshkdz/
[aragnation]: https://deviparikh.github.io/aragnation/