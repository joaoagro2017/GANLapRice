# GAN-Based Data Augmentation Pipeline for Rice Leaf Diseases Detection 
This repository provides a pytorch pre-trained model inference for generating synthetic images of rice leaf disease using StyleGAN2-ADA and variance of the Laplacian method for filtering out blurry synthetic images.


![Our Method](https://user-images.githubusercontent.com/34354606/194866011-292203a3-df7e-46e3-b618-a2c5c1e86b10.png)

## Generating Synthetic Images of Rice Leaf Disease
python generate.py --outdir=out --trunc=1 --seeds=85,265,297,849 \
      --network=https://

## Filtering blurry Synthetic Images
python laplacian.py 



## Synthetic Datasets of Rice Leaf Disease
This url provides a 50,001 synthetic raw images of rice leaf diseases (Bacterial Blight, Tungro, Brown Spot and Rice Blast)   

##  Experimental Datasets Description
For training, our study used Rice Leaf Disease Image Samples from Mendeley Data https://data.mendeley.com/datasets/fwcj7stb8r/1 ,it’s an open-source dataset with 5,932 images of rice leaf disease. The images are grouped into four rice leaf 
diseases as Bacterial blight (BB), Tungro (TG), Brown Spot (BS), and Rice Blast (RB). The 
category of BB, TG, BS, and RB have 1584, 1308, 1440, and 1600 images respectively. The raw 
images come in different sizes ranging from 150 pixels to 300 pixels.
