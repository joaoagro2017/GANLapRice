# GAN-Based Data Augmentation Pipeline for Rice Leaf Diseases Detection 
This repository provides a pytorch pre-trained model inference for generating synthetic images of rice leaf disease using StyleGAN2-ADA and variance of the Laplacian method for filtering out blurry synthetic images.


![Our Method](https://user-images.githubusercontent.com/34354606/194866011-292203a3-df7e-46e3-b618-a2c5c1e86b10.png)

# Getting Started
The repo consists of StyleGAN2-ADA and Laplacian Filter, for generating synthetic rice leaf diseases and filtering out the blurry images respectively. 
We used the StyleGAN2-ADA for training datasets of rice leaf diseases which include
Pre-trained network for generating synthetic images of rice leaf disease are stored as *.pkl files and can be referenced using local filename as or URLs:  

#### Generate
python generate.py --outdir=out --trunc=1 --seeds=


##  Experimental Datasets Description
For training, our study used Rice Leaf Disease Image Samples from Mendeley Data https://data.mendeley.com/datasets/fwcj7stb8r/1 ,it’s an open-source dataset with 5,932 images of rice leaf disease. The images are grouped into four rice leaf 
diseases as Bacterial blight (BB), Tungro (TG), Brown Spot (BS), and Rice Blast (RB). The 
category of BB, TG, BS, and RB have 1584, 1308, 1440, and 1600 images respectively. The raw 
images come in different sizes ranging from 150 pixels to 300 pixels.
