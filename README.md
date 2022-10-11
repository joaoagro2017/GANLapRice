# GAN-Based Data Augmentation Pipeline for Rice Leaf Diseases Detection 
This repo provides a python source code for generating synthetic images of rice leaf disease using an improved GAN and Laplacian filter. 

For generating the synthetic images of rice leaf diseaese we use the original StyleGAN-ADA repository implementation 

![Our Method](https://user-images.githubusercontent.com/34354606/194866011-292203a3-df7e-46e3-b618-a2c5c1e86b10.png)

# Getting Started
Pre-trained network for generating synthetic images of rice leaf disease are stored as *.pkl files and can be referenced using local filename as or URLs:  

#### Generate
python generate.py --outdir=out --trunc=1 --seeds=
