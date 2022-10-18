## GAN-Based Data Augmentation Pipeline for Rice Leaf Diseases Detection 
This repository provides a pytorch pre-trained model inference for generating synthetic images of rice leaf disease using StyleGAN2-ADA and variance of the Laplacian method for filtering out blurry synthetic images.


![Our Method](https://user-images.githubusercontent.com/34354606/194866011-292203a3-df7e-46e3-b618-a2c5c1e86b10.png)

### Generating Synthetic Images of Rice Leaf Disease
python <a href="https://github.com/NVlabs/stylegan2-ada-pytorch/blob/main/generate.py">
generate.py </a> --outdir=out --trunc=1 --seeds=85,265,297,849 \
      --network=https://drive.google.com/file/d/1K2oPovRjbULI2k6NqqFCWfeXhI0IVdbd/view?usp=sharing
      
### Sample of generated images
<img src="https://user-images.githubusercontent.com/34354606/196154683-7e47a20c-0b55-4d09-b828-4b723f8c6625.png" width=700 height=550>

### Projecting Synthetic Images of Rice Leaf Disease
python <a href="https://github.com/NVlabs/stylegan2-ada-pytorch/blob/main/projector.py">
projector.py </a> --outdir=out --target=~/rice_leaf_disease.png \
      --network=https://drive.google.com/file/d/1K2oPovRjbULI2k6NqqFCWfeXhI0IVdbd/view?usp=sharing

### Filtering blurry Synthetic Images
python
<a href="https://github.com/yunusa2k2/GANLapRice/blob/main/Laplacian.py">Laplacian.py</a>

After generating synthetic images of rice leaf diseases, use the laplacian filter to remove the blurry ones

### Synthetic Datasets of Rice Leaf Disease
This url provides 50,001 synthetically generated raw images of rice leaf diseases (Bacterial Blight, Tungro, Brown Spot and Rice Blast). With a size of 256 * 256. The images are grouped into 5 each containing ~10,000 .png images 

<table>
  <tr>
    <th>#</th>
    <th>Download</th>
    <th>Size</th>
    <th>Quantity</th>
  </tr>
  <tr>
    <td>1</td>
    <td>
<a href="https://drive.google.com/file/d/1bVWQNv68Oh6PB4NDgv9nH7whuBHbquJw/view?usp=sharing">Batch 1</a></td>
    <td>891mb</td>
    <td>10,001</td>
  </tr>
  <tr>
    <td>2</td>
    <td>
<a href="https://drive.google.com/file/d/1sUr_ogXhGUYodmK9QA5fWHRH7F3LDRFf/view?usp=sharing">Batch 2</a></td>
    <td>891mb</td>
        <td>10,000</td>
  </tr>
  <tr>
    <td>3</td>
    <td>
<a href="https://drive.google.com/file/d/1vyWg89Q2pDBRdcj8d9-1k4zeFKKZ9nxz/view?usp=sharing">Batch 3</a></td>
    <td>890mb</td>
        <td>10,000</td>
  </tr>
  <tr>
    <td>4</td>
    <td>
<a href="https://drive.google.com/file/d/1-Qy5YgBxtw1N8mwJqiQ9BRufHqPf0foH/view?usp=sharing">Batch 4</a></td>
    <td>889mb</td>
        <td>10,000</td>
  </tr>
  <tr>
    <td>5</td>
    <td>
<a href="https://drive.google.com/file/d/1R2b7nJG7Pky_XBVZ7GgjnPOXHAhBxOmZ/view?usp=sharing">Batch 5</a></td>
    <td>891mb</td>
        <td>10,000</td>
  </tr>
</table>


### Curated example of an interpolated video
<a href="https://drive.google.com/file/d/1ggt_-SpMIzAZlZtGxvR_NszUazLVpIaK/view?usp=sharing"> Curated Video</a> \
The video shows the curated interpolated video produced using the pre-trained models

###  Experimental Datasets Description
<i>For training the generative model, our study used Rice Leaf Disease Image Samples from Mendeley Data https://data.mendeley.com/datasets/fwcj7stb8r/1 ,it’s an open-source dataset with 5,932 images of rice leaf disease. The images are grouped into four rice leaf 
diseases as Bacterial blight (BB), Tungro (TG), Brown Spot (BS), and Rice Blast (RB). The 
category of BB, TG, BS, and RB have 1584, 1308, 1440, and 1600 images respectively. The raw 
images come in different sizes ranging from 150 pixels to 300 pixels. </i>
