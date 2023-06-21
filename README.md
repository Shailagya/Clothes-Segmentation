# Clothes-Segmentation
The fashion industry is a fast-evolving one where consumers’ choices are always changing. Moreover, there is a rapid increase in the number of competing brands and stores. However, a major problem that the industry faces is how to appropriately and efficiently combine different clothing items worn by people.

This project will help designers instantly analyze a certain style and decide whether they want to move forward with this or not.

Given two images:
 a content image(image containing clothing)
 a style image 
we want to generate an output image in which the clothes of the content image are stylized according to the style image. 

We would like to give the user an option to choose which part of the clothing he wants to have stylized, for example, if an image contains shirt+pant
we first want to separate the two and give the user an option to choose which component he wants stylized.
## Methodology

### Saliency map generation and Cloth Segmentation:
Used a pre-trained U-2-Net model for Cloth Segmentation. 
The model accurately segments cloth components based on upper body cloth, lower body cloth, fully body cloth and background.
The Saliency map generation was also done by the pre-trained U-2-Net model.


![proposed framework](https://github.com/Shailagya/Clothes-Segmentation/assets/137305675/bf97894b-7a44-41d1-be1b-ab0f0b604cb3)

## Experimental Results
![experimental result](https://github.com/Shailagya/Clothes-Segmentation/assets/137305675/9464b71b-4d8a-4a83-bdb1-96ae2822636a)
It can be seen that the cloth is mixed up with the foreground and background, and this leads to the difficulty for identifying the style of cloth easily. But, by using segmentation and saliency maps it is easy to
clearly identify and represent stylized clothing on human subjects. Without the manual segmentation of the object mask, our saliency-based method can simultaneously stylize and highlight the clothing.

![Experimental Results2](https://github.com/Shailagya/Clothes-Segmentation/assets/137305675/ccd47272-a963-4615-8578-55d0bdc5eea4)

The outputs in the above figure, further improve the visual quality of cloth boundaries compared to the pre-saliency blending. It can be seen from the two magnified images that the saliency-based blending helps to smooth the cloth boundary and to blend the stylized segmented cloth and background more naturally, especially when the colours are inconsistent near the cloth boundary.







